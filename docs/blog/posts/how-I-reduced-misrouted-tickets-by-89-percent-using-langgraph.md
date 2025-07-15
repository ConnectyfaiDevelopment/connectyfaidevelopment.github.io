---
date: 2025-07-15
authors:
  - rokpopovledinski
categories:
  - AI Implementation
  - Customer Support
  - LangGraph
  - Instructor
description: How I built a structured ticket classification system that reduced misrouted tickets by 89% using LangGraph, Instructor, and Pydantic. No chatbots, just solid engineering.
---

# How I Reduced Misrouted Tickets by 89% Using LangGraph

If you've ever watched a customer support ticket bounce between three different agents… or had a customer rage-quit after explaining their problem for the third time - this is why:

**Your tickets aren't getting to the right people.**

27% of support tickets land on the wrong desk. That means 1 in 4 customers gets transferred, re-explains their problem, and waits longer for help.

Misrouted tickets slow down support, kill customer trust, burn team time, and spike churn. Trying to patch it with a chatbot only makes it worse.

So instead of building another chatbot, I built them a system to fix the root cause. And the misroutes were cut by 89% in a couple of weeks.

<!-- more -->

<div style="text-align: center; margin: 3rem 0;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/C3ttvbTn43o" title="How I Reduced Misrouted Tickets by 89% Using LangGraph" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="max-width: 100%; border-radius: 8px;"></iframe>
  <p style="margin-top: 1rem; font-style: italic; color: #666;">Watch: The complete technical breakdown of how I built structured ticket classification using LangGraph</p>
</div>

I've built AI systems at enterprise scale and inside messy startup ops. After years watching these projects fall apart for the same reasons, I started helping businesses build AI that actually sticks.

In my last article, I walked you through the 6-step system behind every AI support project I build. Today we're zooming in on Step 1, and how one structured layer cut misrouted tickets by 89%, without ever touching a chatbot.

## The Real Problem Isn't Conversations

Here's what this company was dealing with:

- **27% of tickets were going to the wrong person**
- **Agents were spending 20–40% of their time** just figuring out what the ticket was about
- **Founders assumed this was a problem a chatbot could solve** — it wasn't

The real issue? No structure. Just raw ticket text flowing in, overwhelming everyone.

Most teams make the mistake of trying to patch it with chatbots. But chatbots don't fix chaos. They amplify it.

You don't need a crystal ball at this point. You need structure, clean, predictable, composable outputs you can build on.

So instead of trying to make chatbots smarter, we made the problem simpler.

## The Strategic Design Philosophy

The key question wasn't "How do we make AI smarter?" It was: **"How can we force every incoming ticket to fit into a structure we can work with?"**

What does that mean? We have a ticket coming in and the ONLY thing we are interested in is the category. We don't need additional descriptions, explanations, nothing. We just need to know plainly, whether it is A, B, C, or D.

The answer wasn't prompt engineering. It was enforced structure with Pydantic and Instructor, wrapped in a LangGraph node we could expand on top of later.

## The Tech Stack That Actually Works

Now, if some of those names sound unfamiliar, let me give you the 10 second overview:

- **LangGraph** — a framework for building AI workflows with clean separation between each step
- **Instructor** — a tool that makes sure the AI gives us structured outputs instead of loose text  
- **Pydantic** — a validator that catches errors before they cause issues downstream
- **Streamlit** — a lightweight UI library for building throwaway dashboards fast

You don't need to remember the tool names, just this: Instead of AI that "kind of works," we built AI with guardrails.

## System Architecture: Simple but Scalable

Here's the thing about most AI systems - they're built like houses of cards. One thing breaks, everything falls down.

I wanted something different. Something that could grow without breaking what already works.

The flow is dead simple:

1. **Upload CSV** → Streamlit handles the file upload
2. **Validate data** → Make sure we have what we need  
3. **LangGraph processes** → One node for now, but ready to expand
4. **Instructor + GPT** → Structured outputs, no free-form text
5. **Pydantic validates** → Catch errors before they spread
6. **Clean categories** → Exactly what the support team needs
7. **Download results** → CSV they can actually use

The beauty is in the constraints. Every output is validated. Every category comes from a predefined enum. If the model fails? We catch it, log it, and keep going.

No hallucinations. No surprises. No "the AI said something weird" moments.

This isn't just a demo that works once - it's architecture that can handle real business chaos.

## The Code: Where Structure Meets AI

Let me walk you through the actual implementation:

### 1. Models: Real Categories, Not Generic Ones

We start with real business categories, not generic ones like 'positive sentiment'. These are actual buckets the support team cares about:

```python
class TicketCategory(str, Enum):
    SHIPPING_TRACKING = "Shipping & Tracking"
    ORDER_ISSUE = "Order Issue (Missing, Damaged, Wrong Item)" 
    PRODUCT_QUESTION_ONLINE = "Product Question - Bought Online"
    PRODUCT_QUESTION_STORE = "Product Question - Bought In Store"
    WHOLESALE_INQUIRY = "Wholesale Inquiry"
    COLLAB_SPONSORSHIP = "Collab or Sponsorship"
    WEBSITE_TECH_ISSUE = "Website or Tech Issue"
    SOMETHING_ELSE = "Something Else"

class TicketClassification(BaseModel):
    category: TicketCategory
    
    model_config = ConfigDict(use_enum_values=True)
```

These categories aren't just labels, they're constraints. We're forcing the large language model to fit every ticket into clear buckets your team can act on.

No "maybe it's this, maybe it's that" answers. Very clean structure; so routing, analytics, and even replies later on all run on solid ground.

In code, these are called enums - which just means: "Only these values are allowed. Nothing else."

Why does that matter? Because when the AI is limited to your actual categories, you get consistency, not creativity. And that means fewer errors, faster decisions, and way less cleanup later.

### 2. The Classifier: Structure Over Prompts

Now this is the piece that actually talks to the AI, but not in the way most teams do.

Instead of crafting a clever prompt and hoping the AI follows instructions, we use Instructor to say: "Here's the format. Fill it out. No deviations."

```python
import instructor
from openai import OpenAI
from .models import TicketClassification

class TicketClassifier:
    """Structured ticket classification using Instructor + Pydantic."""
    
    def __init__(self, api_key: str, model_name: str = "gpt-4o-mini", temperature: float = 0.1) -> None:
        self.client = instructor.from_openai(
            OpenAI(api_key=api_key),
            mode=instructor.Mode.TOOLS
        )
        self.model_name = model_name
        self.temperature = temperature
        
    def classify(self, ticket_message: str) -> TicketClassification:
        """Classify a single support ticket."""
        return self.client.chat.completions.create(
            model=self.model_name,
            response_model=TicketClassification,
            messages=[
                {"role": "system", "content": "Classify this customer support ticket into the most appropriate category."},
                {"role": "user", "content": f"Classify this customer support ticket:\n\n{ticket_message}"}
            ],
            temperature=self.temperature,
        )
```

It's like giving the AI a form to complete, not a blank canvas to paint on.

We define that structure using a `TicketClassification` model, and Instructor forces the LLM to return exactly that, or it fails fast.

So instead of your team being blindsided by misclassifications later, we catch bad outputs right here, before they pollute the rest of the system.

### 3. LangGraph: One Node Today, Five Tomorrow

This is where the real design payoff happens.

Right now, this LangGraph has only one node, just the classifier. But here's why that matters:

```python
from typing import TypedDict
from langgraph.graph import StateGraph, START, END
from .classifier import TicketClassifier

class TicketState(TypedDict):
    message: str
    category: str | None
    error: str | None
    api_key: str | None
    model_name: str
    temperature: float

def classify_node(state: TicketState) -> TicketState:
    """Core classification logic."""
    try:
        api_key = state.get("api_key") or os.getenv("OPENAI_API_KEY")
        classifier = TicketClassifier(
            api_key=api_key,
            model_name=state.get("model_name", "gpt-4o-mini"),
            temperature=state.get("temperature", 0.1)
        )
        result = classifier.classify(state["message"])
        
        return {
            **state,
            "category": result.category,
            "error": None
        }
    except Exception as e:
        return {
            **state,
            "category": None,
            "error": str(e)
        }

def build_classification_graph():
    """Build the LangGraph workflow."""
    graph = StateGraph(TicketState)
    graph.add_node("classify", classify_node)
    graph.add_edge(START, "classify")
    graph.add_edge("classify", END)
    return graph.compile()
```

We're not using LangGraph just because it's fancy. We're using it for control, and for future growth.

Every team has had that moment where you try to add one more feature to a script... and the whole thing breaks. Routing logic bleeds into classification. Summarization overrides state. Everything becomes fragile.

LangGraph fixes that. It gives us clear separation of steps. So classification stays clean. Routing is its own node. Summarization? Another.

One node today means five nodes tomorrow; without rewriting everything.

### 4. Streamlit UI: Throwaway Code That Saves Projects

Let's talk about the UI, and why we built it.

```python
import streamlit as st
import pandas as pd
import plotly.express as px
import streamlit_ui.utils as utils

st.set_page_config(
    page_title="Support Ticket Classifier",
    page_icon="🎫",
    layout="centered"
)

def main():
    st.title("🎫 Support Ticket Classifier")

    st.markdown("""
    Upload a CSV file with customer support tickets and get them automatically classified 
    using **LangGraph + Instructor + Pydantic**.

    **Required columns:** `date`, `from_email`, `first_name`, `message`
    """)

    uploaded_file = st.file_uploader("Choose a CSV file", type="csv")

    if uploaded_file is not None:
        df = pd.read_csv(uploaded_file)
        is_valid, error_message = utils.validate_csv(df)

        if not is_valid:
            st.error(f"❌ {error_message}")
            return

        st.success(f"✅ Loaded {len(df)} tickets successfully!")

        if st.button("🚀 Classify Tickets", type="primary"):
            progress_bar = st.progress(0)
            
            def update_progress(progress):
                progress_bar.progress(progress)
            
            df_classified = utils.classify_tickets_streamlit(df, update_progress)
            st.session_state.classified_df = df_classified

    # Show results if we have them
    if 'classified_df' in st.session_state:
        df_classified = st.session_state.classified_df
        
        stats_df = utils.get_classification_stats(df_classified)
        st.dataframe(stats_df, use_container_width=True)
        
        # Download results
        csv_data = utils.prepare_download_data(df_classified)
        st.download_button(
            label="📥 Download Full Results",
            data=csv_data,
            file_name="classified_tickets.csv",
            mime="text/csv"
        )
```

This is throwaway code. It's not meant for production. It's not branded. It's not beautiful.

But it solves one of the biggest problems in AI implementation: keeping domain experts close to the dev process while the foundation is still being laid.

The people who actually handle the tickets; agents, support leads; could:
- Upload a CSV of real tickets
- See the classification results live
- Spot problems in the categories
- Download and share feedback instantly

This is how we made sure the foundation was solid, before building anything on top of it.

Most failed projects don't collapse because the AI is bad. They collapse because bad assumptions go untested until it's too late.

### 5. Utils: The Boring Stuff That Makes It Work

```python
import pandas as pd
from typing import Tuple
from app.graph import classify_ticket

def validate_csv(df: pd.DataFrame) -> Tuple[bool, str]:
    """Validate uploaded CSV has required columns."""
    required_columns = ['date', 'from_email', 'first_name', 'message']
    
    if df.empty:
        return False, "CSV file is empty"
    
    missing_columns = [col for col in required_columns if col not in df.columns]
    
    if missing_columns:
        return False, f"Missing required columns: {', '.join(missing_columns)}"
    
    if df['message'].isna().any():
        return False, "Some message fields are empty"
    
    return True, ""

def classify_tickets_streamlit(df: pd.DataFrame, progress_callback=None) -> pd.DataFrame:
    """Classify tickets using LangGraph workflow."""
    tickets = df['message'].tolist()
    total_tickets = len(tickets)
    
    categories = []
    for i, ticket in enumerate(tickets):
        try:
            result = classify_ticket(ticket)
            categories.append(result)
        except Exception as e:
            categories.append("Classification Error")
        
        if progress_callback:
            progress = (i + 1) / total_tickets
            progress_callback(progress)
    
    df_classified = df.copy()
    df_classified['category'] = categories
    
    return df_classified

def get_classification_stats(df: pd.DataFrame) -> pd.DataFrame:
    """Get classification statistics."""
    counts = df['category'].value_counts()
    total = counts.sum()
    
    stats_df = pd.DataFrame({
        'Category': counts.index,
        'Count': counts.values,
        'Percentage': (counts.values / total * 100).round(1)
    })
    
    return stats_df

def prepare_download_data(df: pd.DataFrame) -> bytes:
    """Prepare classified data for download."""
    return df.to_csv(index=False).encode('utf-8')
```

This isn't glamorous code, but it's what makes the system actually usable. CSV validation, progress tracking, data preparation - all the stuff that turns a cool demo into something people can actually use.

## Testing: Trust Through Validation

Before we wrap, I want to show you something that helps you trust the system.

Because when you're rolling out AI in your support flow, the #1 question your team will ask is: "How do we know this actually works?"

Proper evaluation for LLMs is a big topic, and it can take weeks to build custom eval pipelines. But you don't need all that complexity to start validating today.

Instead, we add simple assertion-based LLM tests, not to check syntax, but to catch real-world reasoning failures:

```python
def test_classification_examples():
    tests = [
        ("Where is my package? It was supposed to arrive last week.", "Shipping & Tracking"),
        ("My item arrived broken and missing the manual", "Order Issue (Missing, Damaged, Wrong Item)"),
        ("I bought this online but I'm not sure how to use it properly", "Product Question - Bought Online"),
        ("Hello, I was wanting to inquire about any wholesale opportunities", "Wholesale Inquiry"),
        ("The checkout button isn't working and I can't complete my order", "Website or Tech Issue"),
        ("I'm a content creator and would love to collaborate with your brand", "Collab or Sponsorship"),
    ]
    
    for message, expected in tests:
        result = classify_ticket(message)
        assert result == expected, f"Expected {expected}, got {result}"
```

These are the kinds of cases that can break any prompt-based system. The same goes for:
- Late shipments vs damaged items
- Wholesale inquiries vs product questions  
- Website bugs vs user errors

**Why this matters:** This isn't overengineering. It's the smallest possible step toward building trust with your team.

If your support lead asks "Can we trust this classifier?" — now you can run these tests and show them the results.

That's how we avoid surprises in production. And that's how we make AI feel safe to adopt, and not risky to deploy.

## The Results: What Actually Happened

So what did this actually give the business?

Not just clean categories. Not just "some AI working in the background."

This gave them:

✅ **89% fewer misrouted tickets** — instantly saving agent hours  
✅ **Actionable data from Week 1** — for routing, staffing, automation  
✅ **A structure that won't break** the second something changes  
✅ **Confidence that what's working today** won't blow up tomorrow  
✅ **And most importantly** — a system they can actually trust and grow with

And yeah, this is just Step 1. But it's what unlocks everything else.

Classification might feel basic, but if this part isn't right, nothing downstream works.

Because we used LangGraph, this isn't a one-off prototype. It's something you can build on without breaking what's already working.

- Want to add routing later? Easy.
- Summarization? That's just another node.
- Enrich with customer context? Plug it in and keep going.

The whole thing is built to evolve safely, and fast.

## The Takeaway: Structure First, Features Second

You don't need a massive system, you just something your team can trust, extend, and actually use.

<div style="text-align: center; margin: 3rem 0;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/C3ttvbTn43o" title="LangGraph Ticket Classification Implementation" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="max-width: 100%; border-radius: 8px;"></iframe>
  <p style="margin-top: 1rem; font-style: italic; color: #666;">Ready to implement this system? This video shows you exactly how to build it step by step.</p>
</div>

**Want to follow along with the code?** The complete implementation is available on [GitHub:] 
(https://github.com/RokPopov/ai-garage/tree/main/customer_support_ai)

You can clone it, run it, and tweak the categories for your business in under an hour.

And this is just the beginning. In the next articles, we'll keep building - adding automatic ticket routing, summarization, and enrichment to this exact workflow.

While your competitors are burning cash on chatbots that frustrate customers, you could be getting real results from week one.

The choice is yours: Start with the foundation, or start over in 6 months.

