---
title: Home - Legal AI Solutions
description: Save 20-40 hours monthly on repetitive legal ops with AI systems that integrate with your existing workflow
keywords: legal AI automation, law firm efficiency, legal operations, AI for lawyers
author: Rok Popov Ledinski
canonical_url: https://www.rokpopovledinski.com/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,400;1,600&display=swap');

body, * {
  font-family: 'Open Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif !important;
}

/* Hide sidebar only on larger screens, but keep it functional on mobile */
@media screen and (min-width: 76.25em) {
  .md-sidebar--primary {
    display: none !important;
  }
  
  .md-main {
    grid-template-columns: [content-start] 1fr [content-end] 12rem [toc-end] !important;
  }
}

/* On smaller screens, keep the sidebar functional for mobile menu */
@media screen and (max-width: 76.24em) {
  .md-main {
    grid-template-columns: 1fr !important;
  }
  
  /* Don't hide the sidebar on mobile - let it work normally */
  .md-sidebar--primary {
    display: block;
  }
}

/* Base styles */
.landing-page {
  min-height: 100vh;
  background: #ffffff;
}

/* Header */
.header {
  border-bottom: 1px solid #e2e8f0;
  background: white;
  padding: 1rem 0;
}

.header-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.25rem;
  font-weight: 700;
  color: #1e293b;
}

.support-email {
  font-size: 0.875rem;
  color: #64748b;
}

/* Rating Badge Section */
.rating-section {
  background: white;
  padding: 1rem;
  text-align: center;
}

.rating-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: #1e293b;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 9999px;
  font-size: 0.875rem;
}

.stars {
  display: flex;
  gap: 2px;
}

.star {
  width: 1rem;
  height: 1rem;
  color: #10b981;
  fill: #10b981;
}

/* Badge component */
.badge {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #f0fdf4;
  color: #16a34a;
  border-radius: 0.375rem;
  font-size: 0.875rem;
  font-weight: 600 !important;
  text-transform: uppercase;
  letter-spacing: 0.025em;
  margin-bottom: 0.5rem !important;  /* reduced from 1.5rem */
}

/* Hero Section */
.hero-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.hero-content {
  max-width: 1100px; /* wider so lines don’t wrap too early */
}

.hero-title {
  font-size: 3.5rem !important;
  font-weight: 800 !important;
  color: #1e293b !important;
  margin-bottom: 0.75rem !important;  /* reduced from 1.5rem to bring subtitle closer */
  line-height: 1.1;
  letter-spacing: -0.02em;
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 800 !important;  /* Extra Bold */
}

.hero-subtitle {
  font-size: 1.5rem !important;  /* bigger */
  color: #1e293b !important;
  font-weight: 500 !important;
  margin-bottom: 2rem;
  margin-top: 0 !important;  /* no extra top margin */
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 400 !important;  /* Regular */
}

.cta-button {
  display: inline-block;
  background: #10b981 !important;  /* your exact green */
  color: white !important;         /* white text, not light green */
  padding: 1.5rem 2rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: 600 !important;
  font-size: 1.125rem;
  transition: all 0.2s;
  margin-bottom: 0.5rem;
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 600 !important;  /* Semibold */
}

.cta-button:hover {
  background: #059669 !important;  /* darker green on hover */
  color: white !important;         /* keep white text on hover */
  text-decoration: none;
}

.cta-subtext {
  font-size: 1.5rem !important;  /* increased from 0.875rem */
  color: #64748b;
  margin-bottom: 2rem;
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 400 !important;  /* Regular */
}

/* Testimonial Card */
.testimonial-card {
  max-width: 24rem;
  margin: 0 auto;
  background: #1e293b;
  color: white;
  border-radius: 0.5rem;
  padding: 1.5rem;
}

.testimonial-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 0.5rem;
}

.testimonial-avatar {
  width: 3rem;
  height: 3rem;
  background: #f97316;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.875rem;
  font-weight: 700;
}

.testimonial-quote {
  font-weight: 700;
  color: #10b981;
  font-size: 1.125rem;
}

.testimonial-text {
  font-size: 0.875rem;
  color: #cbd5e1;
}

/* Problem Section */
.problem-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.problem-content {
  max-width: 1024px;
  margin: 0 auto;
  text-align: center;  /* ensure everything is centered */
}

.section-title {
  font-size: 2.8rem !important;
  font-weight: 800 !important;   
  color: #1e293b !important;     /* dark blue */
  margin-bottom: 2rem;
  line-height: 1.1 !important;
  max-width: 900px !important;
  margin-left: auto !important;
  margin-right: auto !important;
  text-align: center !important;
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 800 !important;  /* Extra Bold */
}

.section-subtitle {
  font-size: 1.3rem !important;
  color: #1e293b !important;     /* dark blue, not gray */
  margin-bottom: 2rem;
  font-family: 'Open Sans', sans-serif !important;
  font-weight: 400 !important;  /* Regular */
}

.problem-list {
  background: #f8fafc;  /* subtle gray background */
  border-radius: 12px;
  padding: 2rem;
  max-width: 800px;
  margin: 2rem auto;
  text-align: left;  /* keep bullets left-aligned within the container */
}

.problem-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.problem-item:last-child {
  margin-bottom: 0;  /* remove bottom margin from last item */
}

.problem-item span {
  font-size: 1.2rem;
  line-height: 1.4;
  color: #1e293b !important;
}

.problem-bullet {
  width: 0.5rem;
  height: 0.5rem;
  background: #ef4444;
  border-radius: 50%;
  margin-top: 0.75rem;
  flex-shrink: 0;
}

.solution-text {
  font-size: 1.125rem;
  font-weight: 600;
  color: #1e293b !important;     /* dark blue */
  margin-bottom: 2rem;
}

/* Also fix the final subtitle */
.problem-content .section-subtitle:last-of-type {
  color: #1e293b !important;     /* dark blue */
}

/* Clients Section */
.clients-section {
  /* background: #f8fafc; */
  padding: 1rem;  /* reduced padding */
  text-align: center;
}

.clients-label {
  font-size: 1.5rem;
  font-weight: 600;
  color: #1e293b;  /* changed from #94a3b8 to match your dark blue text */
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 1rem;
}

.clients-grid {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2.5rem;  
  max-width: 400px;  
  margin: 0 auto;
}

.client-logo-img {
  max-height: 50px;
  max-width: 180px;  
  object-fit: contain;
  opacity: 0.6;
  transition: opacity 0.2s;
}

/* Datalumina needs dark background for white text */
.client-logo-img[alt="Datalumina"] {
  background-color: #1e293b;
  padding: 8px 12px;
  border-radius: 4px;
}

/* Hoorntje Legal is fine as-is */
.client-logo-img[alt="Hoorntje Legal"] {
  background-color: transparent;
}

.client-logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: #10b981;
  display: none;  /* hide placeholder logos for now */
}

/* Solution Section - aligned with other sections */
.solution-section {
  background: #f8fafc;
  padding: 4rem 1rem;
  text-align: center;
}

.solution-content {
  max-width: 1024px;
  margin: 0 auto;
}

.solution-section .section-title {
  font-size: 2.8rem !important;
  font-weight: 800 !important;   
  color: #1e293b !important;     
  margin-bottom: 2rem;
  line-height: 1.1 !important;
  max-width: 900px !important;
  margin-left: auto !important;
  margin-right: auto !important;
  text-align: center !important;
  margin-top: 0 !important;  /* no extra top margin */
}

.stat-highlight {
  background: #1e293b;
  color: white;
  padding: 2rem;
  border-radius: 12px;
  font-size: 1.5rem;
  font-weight: 600;
  margin: 2rem auto;
  max-width: 800px;
  line-height: 1.4;
}

.solution-text {
  text-align: left;
  max-width: 800px;
  margin: 2rem auto;
}

.solution-text p {
  font-size: 1.3rem !important;
  color: #1e293b !important;
  font-weight: 400 !important;  /* NORMAL weight, not bold */
  line-height: 1.6;
  margin-bottom: 2rem !important;
}

.highlight-text {
  font-weight: 600 !important;  /* only the highlight text should be bold */
  font-style: italic;
  color: #1e293b !important;
}

.solution-section .badge {
  margin-bottom: 0.75rem !important;  /* same as problem section */
}

.cta-container {
  margin-top: 3rem;
}

/* Responsive tuning */
@media (min-width: 1280px) {
  .hero-title { font-size: 5rem; }
}

@media (max-width: 1024px) {
  .hero-title { font-size: 3.5rem; }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem !important;
  }
  .hero-subtitle {
    font-size: 1.1rem !important;
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem !important;
  }
}

/* Responsive */
@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .problem-list {
    text-align: left;
  }
}

/* Container utility */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.problem-section .badge {
  margin-bottom: 0.75rem !important;  /* much smaller gap */
}

.problem-section .section-title {
  margin-top: 0 !important;  /* remove any top margin */
}

.center-text {
  text-align: center !important;
  font-size: 1.3rem !important;
  color: #1e293b !important;
  font-weight: 600 !important;
  margin: 2rem auto !important;
  max-width: 800px;
}

/* R.A.P.I.D. System Section - Fixed Layout */
.rapid-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.rapid-content {
  max-width: 1400px;
  margin: 0 auto;
}

/* Fix spacing between badge and title in R.A.P.I.D. section */
.rapid-section .badge {
  margin-bottom: 0.25rem !important;
}

.rapid-section .section-title {
  margin-top: 0 !important;
  margin-bottom: 2rem;
}

/* R.A.P.I.D. System Section - 2 Row Layout */
.steps-container {
  margin: 3rem 0;
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

.steps-row {
  display: flex;
  justify-content: center;
  gap: 3rem;
  margin-bottom: 3rem;
}

.steps-row:last-child {
  margin-bottom: 0;
}

.steps-row.first-row {
  justify-content: space-between;
}

.steps-row.second-row {
  justify-content: center;
  gap: 6rem;
}

.step {
  flex: 1;
  text-align: center;
  max-width: 280px;
}

.step-icon {
  margin-bottom: 1.5rem;
  display: flex;
  justify-content: center;
}

.step-title {
  font-size: 1.3rem;
  font-weight: 800 !important;  /* Bold */
  color: #1e293b;
  margin-bottom: 0.5rem;
}

.step-subtitle {
  font-size: 1.2rem;
  font-weight: 600;
  color: #10b981;
  margin-bottom: 1rem;
}

.step-description {
  font-size: 1rem;
  color: #1e293b;
  line-height: 1.5;
}

.rapid-cta {
  margin-top: 3rem;
  text-align: center !important;
}

.rapid-cta .cta-headline {
  font-size: 1.3rem !important;  /* smaller, matching the reference */
  font-weight: 400 !important;   /* normal weight, not bold */
  color: #1e293b !important;
  margin-bottom: 2rem !important;
  text-align: center !important;
  display: block !important;
  width: 100% !important;
}

.guarantee {
  font-size: 0.9rem;
  color: #64748b;
  margin-top: 1rem;
}

/* Before/After Section - Match index.md styling */
.before-after-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.before-after-content {
  max-width: 1024px;
  margin: 0 auto;
}

.comparison-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  margin-top: 40px;
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

.before-column, .after-column {
  background: white;
  padding: 32px;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

.column-title {
  font-size: 24px;
  font-weight: 800 !important;  /* Make BEFORE and AFTER bold */
  text-align: center;
  margin-bottom: 24px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.before-title {
  color: #ef4444; /* red */
}

.after-title {
  color: #10b981; /* your green */
}

.comparison-list {
  display: flex;
  flex-direction: column;
  gap: 16px;
  list-style: none;
  padding: 0;
}

.comparison-list li {
  padding: 8px 0 8px 30px;  /* padding for the icon */
  font-size: 20px;
  font-weight: 500;
  text-align: left;
  line-height: 1.4;
  color: #00112c;
  position: relative;
  /* Remove any bullet points */
  list-style: none;
}

.before-list li:before {
  content: "✗";  /* Red X */
  position: absolute;
  left: 0;
  color: #ef4444;
  font-weight: bold;
  font-size: 20px;
}

.after-list li:before {
  content: "✓";  /* Green checkmark */
  position: absolute;
  left: 0;
  color: #10b981;
  font-weight: bold;
  font-size: 20px;
}

/* CTA Button below comparison */
.before-after-cta {
  margin-top: 3rem;
}

.before-after-cta .cta-button {
  display: inline-block;
  background: #10b981;
  color: white;
  padding: 16px 32px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.2s;
}

.before-after-cta .cta-button:hover {
  background: #059669;
  color: white;
  text-decoration: none;
  transform: translateY(-1px);
}

@media (max-width: 768px) {
  .comparison-container {
    grid-template-columns: 1fr;
    gap: 24px;
  }
}

.offer-box {
  background: white;
  border-radius: 12px;
  padding: 2.5rem;
  margin: 2rem auto 3rem auto;
  max-width: 600px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border: 1px solid #e2e8f0;
  text-align: center; /* Center everything in the box */
}

.offer-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 2rem;
  text-align: center; /* Center the title too */
}

.offer-list {
  list-style: none !important; /* Remove bullet points */
  padding: 0;
  text-align: center;
  margin: 0 auto;
}

.offer-list li {
  padding: 12px 0;
  font-size: 1.2rem;
  color: #1e293b;
  position: relative;
  text-align: center; /* Center the text */
  padding-left: 0; /* Remove left padding */
  margin: 0 auto;
  display: block;
}

.offer-list li:before {
  content: "✓ "; /* Green checkmark with space */
  color: #10b981;
  font-weight: bold;
  font-size: 1.3rem;
  margin-right: 8px; /* Space between checkmark and text */
}

.offer-section .offer-list {
  list-style: none !important;
  padding: 0 !important;
  margin: 0 auto !important;
  display: inline-block; /* Center the entire list */
  text-align: left; /* But keep items left-aligned within it */
}

.offer-section .offer-list li {
  padding: 12px 0 12px 30px !important; /* Space for the checkmark */
  font-size: 1.2rem !important;
  color: #1e293b !important;
  position: relative !important;
  text-align: left !important;
  list-style: none !important;
}

.offer-section .offer-list li:before {
  content: "✓" !important;
  position: absolute !important;
  left: 0 !important;
  color: #10b981 !important;
  font-weight: bold !important;
  font-size: 1.3rem !important;
}

.offer-section .offer-box {
  background: white !important;
  border-radius: 12px !important;
  padding: 2.5rem !important;
  margin: 2rem auto 3rem auto !important;
  max-width: 600px !important;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1) !important;
  border: 1px solid #e2e8f0 !important;
  text-align: center !important;
  min-height: auto !important; /* Remove any height restrictions */
  height: auto !important; /* Allow natural height */
  overflow: visible !important; /* Make sure content isn't cut off */
}

.offer-section .offer-title {
  font-size: 1.5rem !important;
  font-weight: 700 !important;
  color: #1e293b !important;
  margin-bottom: 2rem !important;
  text-align: center !important;
}

.offer-section .offer-list {
  list-style: none !important;
  padding: 0 !important;
  margin: 0 auto !important;
  display: inline-block !important;
  text-align: left !important;
  width: 100% !important;
  max-width: 100% !important;
}

/* Fix the description text above the box */
.offer-section .offer-description {
  font-size: 1.3rem !important;
  color: #1e293b !important;
  font-weight: 400 !important;
  margin-bottom: 2rem !important;
  text-align: center !important;
  max-width: 900px !important;
  margin-left: auto !important;
  margin-right: auto !important;
}

.offer-section .pilot-slots {
  font-size: 1.2rem !important;
  color: #1e293b !important;
  font-weight: 400 !important;
  margin-bottom: 3rem !important;
  text-align: center !important;
}

/* Fix the CTA button centering */
.offer-section .offer-cta {
  text-align: center !important;
  margin-top: 3rem !important;
}

/* Video Section */
.video-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.video-content {
  max-width: 1200px;
  margin: 0 auto;
}

.video-description {
  font-size: 1.3rem;
  color: #1e293b;
  font-weight: 400;
  margin-bottom: 2rem;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

.video-subtitle {
  font-size: 1.2rem;
  color: #1e293b;
  font-weight: 400;
  margin-bottom: 3rem;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

.videos-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin: 3rem 0;
  max-width: 1200px; /* increased from 1000px */
  margin-left: auto;
  margin-right: auto;
}

.video-item {
  background: #000;
  border-radius: 8px;
  overflow: hidden;
  aspect-ratio: 16/9;
}

.video-item iframe {
  width: 100%;
  height: 250px; /* increased from 200px */
  border: none;
  border-radius: 8px;
}

.video-footer {
  font-size: 1.2rem;
  color: #1e293b;
  font-weight: 400;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .videos-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}

@media (max-width: 1024px) and (min-width: 769px) {
  .videos-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Social Buttons */
.social-buttons {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-top: 3rem;
}

.social-button {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.2s;
  border: 2px solid #e2e8f0;
  background: white;
  color: #1e293b; /* your blue for normal state */
}

.social-button:hover {
  text-decoration: none;
  transform: translateY(-1px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.youtube-button:hover {
  border-color: #cc0000;
  color: #cc0000; /* Same red as border */
}

.linkedin-button:hover {
  border-color: #0077b5;
  color: #0077b5; /* Same blue as border */
}

.button-icon {
  font-size: 1.1rem;
}

@media (max-width: 768px) {
  .social-buttons {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
}

.video-section .social-button {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.2s;
  border: 2px solid #e2e8f0;
  background: white;
  color: #1e293b !important; /* Force your blue */
}

.video-section .youtube-button:hover {
  border-color: #cc0000 !important;
  color: #cc0000 !important; /* Force red */
}

.video-section .linkedin-button:hover {
  border-color: #0077b5 !important;
  color: #0077b5 !important; /* Force LinkedIn blue */
}

/* FAQ Section */
.faq-section {
  background: #f8fafc;
  padding: 4rem 1rem;
  text-align: center;
}

.faq-content {
  max-width: 1024px;
  margin: 0 auto;
}

.faq-list {
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.faq-item {
  background: white;
  border-radius: 12px;
  padding: 2rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border: 1px solid #e2e8f0;
  text-align: left;
}

.faq-question {
  font-size: 1.5rem !important;
  font-weight: 800 !important;
  color: #1e293b !important;
  margin-bottom: 1rem !important;
  line-height: 1.3 !important;
}

.faq-answer {
  font-size: 1.1rem !important;
  color: #1e293b !important;
  line-height: 1.6 !important;
  margin: 0 !important;
  font-weight: 400 !important;
}

/* Final CTA Section */
.final-cta-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.cta-content {
  max-width: 800px;
  margin: 0 auto;
}

.final-cta-section h2 {
  font-size: 2.8rem;
  font-weight: 800;
  color: #1e293b;
  margin-bottom: 2rem;
  line-height: 1.1;
}

.final-cta-section p {
  font-size: 1.3rem;
  color: #1e293b;
  font-weight: 400;
  margin-bottom: 2rem;
}

.cta-button.primary.large {
  background: #10b981;
  color: white;
  padding: 20px 40px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.2rem;
  transition: all 0.2s;
  display: inline-block;
  margin-bottom: 1rem;
}

.cta-button.primary.large:hover {
  background: #059669;
  color: white;
  text-decoration: none;
  transform: translateY(-1px);
}

.final-cta-section .cta-subtext {
  font-size: 1rem;
  color: #64748b;
  font-style: italic;
  margin: 0;
}

/* Testimonial Section */
.testimonial-section {
  background: white;
  padding: 2rem 1rem;
  text-align: center;
}

.testimonial-content {
  max-width: 1024px;
  margin: 0 auto;
}

.testimonial-author {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 20px;
  align-items: stretch;
  max-width: 1600px;
  margin-left: auto;
  margin-right: auto;
}

.testimonial-card-left {
  background: white;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.testimonial-card-right {
  background: white;
  padding: 50px;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.testimonial-photo {
  width: 220px;
  height: 220px;
  border-radius: 12px;
  object-fit: cover;
  margin-bottom: 24px;
  flex-shrink: 0;
}

.testimonial-info {
  text-align: center;
  margin: 0;
  font-size: 18px;
  color: #374151;
  font-weight: 500;
  line-height: 1.4;
}

.testimonial-content blockquote {
  font-size: 18px !important;
  font-style: italic;
  color: #374151;
  margin: 0;
  line-height: 1.6;
  text-align: left;
}

@media (max-width: 768px) {
  .testimonial-author {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}

.testimonial-section {
  background: white;
  padding: 4rem 1rem;
  text-align: center;
}

.testimonial-box {
  background: white;
  border-radius: 12px;
  padding: 2rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border: 1px solid #e2e8f0;
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 2rem;
  align-items: center;
  max-width: 800px;
  margin: auto;
}

.testimonial-left {
  text-align: center;
}

.testimonial-photo {
  width: 150px;
  height: 150px;
  border-radius: 12px;
  object-fit: cover;
  margin-bottom: 1rem;
}

.testimonial-info {
  font-size: 14px;
  color: #374151;
  font-weight: 500;
}

.testimonial-right blockquote {
  font-size: 16px;
  font-style: italic;
  color: #374151;
  margin: 0;
  line-height: 1.6;
  text-align: left;
}

@media (max-width: 768px) {
  .testimonial-box {
    grid-template-columns: 1fr;
    text-align: center;
  }
}

/* Fix spacing between badge and title in Before/After section */
.before-after-section .badge {
  margin-bottom: 0.25rem !important;
}

.before-after-section .section-title {
  margin-top: 0 !important;
  margin-bottom: 2rem;
}

/* Email Opt-in Styling */
.email-optin-box {
  padding: 2rem;
  margin: 2rem auto;
  max-width: 600px;
  text-align: center;
}

.email-optin-box h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 1rem;
}

.email-optin-box p {
  font-size: 1.1rem;
  color: #374151;
  margin-bottom: 1.5rem;
}

.email-form {
  display: flex;
  gap: 0;  /* Remove the gap */
  max-width: 400px;
  margin: 0 auto 1rem auto;
}

.email-form input[type="email"] {
  flex: 1;
  padding: 12px 16px;
  border: 1px solid #d1d5db;
  border-right: none;  /* Remove right border */
  border-radius: 8px 0 0 8px;  /* Only round left corners */
  font-size: 0.7rem;  /* Reduced from 1rem */
  background: white;
}

.email-form button {
  background: #10b981;
  color: white;
  border: 1px solid #10b981;
  padding: 12px 24px;
  border-radius: 0 8px 8px 0;
  font-size: 0.9rem;
  font-weight: 600;
  cursor: pointer;
  white-space: nowrap;
}

.email-form button:hover {
  background: #059669;
}

.privacy {
  font-size: 0.875rem;
  color: #6b7280;
  margin: 0;
}

/* Header email opt-in - match your other forms */
.header-email-optin {
  display: flex;
  gap: 0;
  align-items: center;
  margin-top: 10px;
}

.header-email-optin input[type="email"] {
  flex: 1;
  padding: 8px 12px;
  border: 1px solid #d1d5db;
  border-right: none;
  border-radius: 6px 0 0 6px;
  font-size: 0.8rem;
  background: white;
  width: 180px;
  font-family: 'Open Sans', sans-serif;
}

.header-email-optin button {
  background: #10b981;
  color: white;
  border: 1px solid #10b981;
  padding: 8px 16px;
  border-radius: 0 6px 6px 0;
  font-size: 0.85rem;
  font-weight: 600;
  cursor: pointer;
  white-space: nowrap;
  font-family: 'Open Sans', sans-serif;
}

.header-email-optin button:hover {
  background: #059669;
}

/* Make sure it's positioned properly in the header */
.md-header__option {
  display: flex;
  align-items: center;
  margin-left: auto;
}
</style>

<div class="landing-page">

<!-- Header -->
<header class="header">
  <!-- <div class="header-content">
    <div class="logo">AI Legal Automation</div>
    <div class="support-email">support@yourlegalai.com</div>
  </div> -->
</header>

<!-- Hero Section -->
<section class="hero-section">
  <div class="hero-content">
    <div class="badge">
      FREE R.A.P.I.D. WORKFLOW AUDIT FOR SMALL LAW FIRMS
    </div>
    
    <h1 class="hero-title">
      Stop Losing €5-15k/Month on<br>
      Non-Billable Legal Work
    </h1>
    
    <p class="hero-subtitle">
      Without New Tools, Hiring Engineers, or Workflow Disruption
    </p>
    
    <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">
      Book A Free R.A.P.I.D. Process Audit
    </a>
    
    <p class="cta-subtext">
      2 pilot engagements left
    </p>

    <!-- Hero Testimonial Card
    <div class="testimonial-card">
      <div class="testimonial-header">
        <div class="testimonial-avatar">DE</div>
        <div>
          <div class="testimonial-quote">"I Finally Got My Time Back"</div>
          <div class="testimonial-text">"This system reclaimed 20+ hours/month of billable time." - Dave E.</div>
        </div>
      </div>
    </div> -->
  </div>
</section>

<!-- Testimonial Section -->
<section class="testimonial-section">
  <div class="testimonial-content">
    <h2 class="section-title">Don't Take My Word For It…</h2>
    <div class="testimonial-box">
      <div class="testimonial-left">
        <img src="/assets/daveebbelaar.jpg" alt="Dave Ebbelaar" class="testimonial-photo">
        <div class="testimonial-info">
          <strong>Dave Ebbelaar</strong><br>
          CEO & Founder @ Datalumina
        </div>
      </div>
      <div class="testimonial-right">
        <blockquote>
          "Over the past two years, I've worked with dozens of developers and AI engineers. It's rare to find someone like Rok who really gets AI engineering on a deep level. Not just from the software side, but also when it comes to LLMs and prompt design. Building AI products that actually make it to production requires both, and Rok nails that balance. He's helped us on several internal projects, often taking the lead and full ownership. He doesn't need a lot of input, he's super organized, and he just gets it done."
        </blockquote>
      </div>
    </div>
  </div>
</section>

<!-- Clients Section -->
<section class="clients-section">
  <div class="container">
    <p class="clients-label">CLIENTS INCLUDE</p>
    <div class="clients-grid">
      <img src="/assets/hoorntje_legal_logo.png" alt="Hoorntje Legal" class="client-logo-img">
      <img src="/assets/Datalumina_Logo.png" alt="Datalumina" class="client-logo-img">
    </div>
  </div>
</section>

<!-- Problem Section -->
<section class="problem-section">
  <div class="problem-content">
    <div class="badge">
      MOST SMALL LAW FIRMS ARE STRUGGLING WITH INEFFICIENCY
    </div>
    
    <h2 class="section-title">
      No More Lost Revenue and Dealing with Administrative Chaos
    </h2>
    
    <p class="section-subtitle">I get it, I've been in your shoes and know what it feels like to:</p>
    
    <div class="problem-list">
      <div class="problem-item">
        <div class="problem-bullet"></div>
        <span>Struggle with manual client intake and scattered communications...</span>
      </div>
      <div class="problem-item">
        <div class="problem-bullet"></div>
        <span>The fear of losing billable hours to administrative work...</span>
      </div>
      <div class="problem-item">
        <div class="problem-bullet"></div>
        <span>And not having a clear path forward to automate repetitive tasks...</span>
      </div>
    </div>
    
    <p class="center-text">But don't worry, I got great news for you!</p>
    <p class="section-subtitle">All this can be fixed faster than you ever thought possible with our method and process, so keep reading and I'll explain...</p>
    
    <!-- Email Opt-in #1 - After Problem Section -->
    <div class="email-optin-box">
      <form class="email-form">
        <input type="email" placeholder="Enter your email address" required>
        <button type="submit">Get Tips</button>
      </form>
    </div>
  </div>
</section>

<!-- Solution Section -->
<section class="solution-section">
  <div class="solution-content">
    <div class="badge">
      FINALLY A PROCESS THAT WORKS
    </div>
    
    <h2 class="section-title">
      There's a Better Way to Reclaim Your Billable Hours
    </h2>

    <p class="section-subtitle">And it's not doing more of what you've already tried...</p>
    
    <div class="stat-highlight">
      Small law firms lose <strong>€5K-€15K every month</strong> to repeatable administrative work that should be automated
    </div>
    
    <div class="solution-text">
      <p>The old way is trying random AI tools and hoping they stick, and it doesn't work because it's only causing you more wasted money and frustrated teams who revert back to email...</p>
      
      <p>Instead, you need a new way to identify high ROI automation opportunities, so that you can finally reclaim those 32 - 48 hours of lost time every month.</p>
      
      <p>The <strong>R.A.P.I.D. AI Audit System</strong> will get you clarity on exactly what to automate way faster and easier than anything you've tried in the past...</p>
      
      <p>And the best part?</p>
      
      <div class="highlight-text">
        You'll know exactly where to invest your automation budget <em>before</em> building anything, saving you from the €10K-€50K mistakes most firms make.
      </div>
    </div>
    
    <div class="cta-container">
      <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">
        Book A Free R.A.P.I.D. Process Audit
      </a>
      <p class="cta-subtext">Get your AI readiness check - no pressure, instant value</p>
    </div>
  </div>
</section>
<!-- R.A.P.I.D. System Section -->
<section class="rapid-section">
  <div class="rapid-content">
    <div class="badge">
      HERE'S HOW IT WORKS
    </div>
    
    <h2 class="section-title">
      The R.A.P.I.D. System to Reclaiming Your Billable Hours
    </h2>
    
    <p class="section-subtitle">Once you start using our system, you'll never go back. Here's why:</p>
    
    <div class="steps-container">
      <!-- First Row - 3 Steps -->
      <div class="steps-row first-row">
        <div class="step">
          <div class="step-icon">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2">
              <circle cx="11" cy="11" r="8"/>
              <path d="M21 21l-4.35-4.35"/>
            </svg>
          </div>
          <h2 class="step-title">R.</h2>
          <h4 class="step-subtitle">Reality Check</h4>
          <p class="step-description">We map your current workflows and identify the biggest time drains costing you billable hours.</p>
        </div>
        
        <div class="step">
          <div class="step-icon">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2">
              <path d="M9 11H1l6-6 6 6"/>
              <path d="M9 17l3 3 3-3"/>
              <path d="M22 18.5V2l-3 3-3-3v16.5"/>
            </svg>
          </div>
          <h2 class="step-title">A.</h2>
          <h4 class="step-subtitle">Analyze</h4>
          <p class="step-description">You get a clear picture of what's broken, what's compliant, and where the quick wins are hiding.</p>
        </div>
        
        <div class="step">
          <div class="step-icon">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2">
              <path d="M9 12l2 2 4-4"/>
              <path d="M21 12c0 4.97-4.03 9-9 9s-9-4.03-9-9 4.03-9 9-9 9 4.03 9 9z"/>
            </svg>
          </div>
          <h2 class="step-title">P.</h2>
          <h4 class="step-subtitle">Prioritize</h4>
          <p class="step-description">You know exactly which automation will save the most hours with the least disruption to your team.</p>
        </div>
      </div>
      
      <!-- Second Row - 2 Steps -->
      <div class="steps-row second-row">
        <div class="step">
          <div class="step-icon">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2">
              <circle cx="12" cy="12" r="3"/>
              <path d="M12 1v6m0 6v6"/>
              <path d="m9 9 3 3 3-3"/>
            </svg>
          </div>
          <h2 class="step-title">I.</h2>
          <h4 class="step-subtitle">Implement</h4>
          <p class="step-description">Your processes get streamlined and automated without disrupting how your team already works.</p>
        </div>
        
        <div class="step">
          <div class="step-icon">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2">
              <path d="M4.5 16.5c-1.5 1.26-2 5-2 5s3.74-.5 5-2c.71-.84.7-2.13-.09-2.91a2.18 2.18 0 0 0-2.91-.09z"/>
              <path d="m12 15-3-3a22 22 0 0 1 2-3.95A12.88 12.88 0 0 1 22 2c0 2.72-.78 7.5-6 11a22.35 22.35 0 0 1-4 2z"/>
            </svg>
          </div>
          <h2 class="step-title">D.</h2>
          <h4 class="step-subtitle">Deploy</h4>
          <p class="step-description">You reclaim 20+ hours monthly while your team actually uses the system instead of reverting to email.</p>
        </div>
      </div>
    </div>
    
    <div class="rapid-cta">
      <h3 class="cta-headline">Experience it yourself and say goodbye to administrative chaos</h3>
      <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">Book A Free R.A.P.I.D. Process Audit</a>
      <p class="guarantee">14 Day No-Questions Money Back Guarantee</p>
    </div>
  </div>
</section>

<!-- Before/After Section -->
<section class="before-after-section">
  <div class="before-after-content">
    <div class="badge">
      WHY WE'RE DIFFERENT
    </div>
    
    <h2 class="section-title">
      Ready to Work With Us & See Real Results?
    </h2>
    
    <div class="comparison-container">
      <div class="before-column">
        <h3 class="column-title before-title">BEFORE</h3>
        <ul class="comparison-list before-list">
          <li>Manual Client Intake</li>
          <li>Unbillable Admin Hours</li>
          <li>Scattered Client Communications</li>
          <li>Repetitive Contract Drafting</li>
          <li>Time Tracking Nightmares</li>
          <li>Learning Complex AI Tools</li>
          <li>€5-15k Monthly Revenue Loss</li>
        </ul>
      </div>
      
      <div class="after-column">
        <h3 class="column-title after-title">AFTER</h3>
        <ul class="comparison-list after-list">
          <li>Automated Client Intake</li>
          <li>20+ Billable Hours Reclaimed</li>
          <li>Centralized Client Management</li>
          <li>AI-Powered Contract Drafts</li>
          <li>Automatic Time Capture</li>
          <li>Works with Your Current Tools</li>
          <li>€5-15k Additional Monthly Revenue</li>
        </ul>
      </div>
    </div>
    
    <div class="before-after-cta">
      <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">Book A Free R.A.P.I.D. Process Audit</a>
    </div>
  </div>
</section>

<!-- What You'll Get Section -->
<section class="offer-section">
  <div class="offer-content">
    <h2 class="section-title">
      What You'll Get in FREE AI Audit
    </h2>
    
    <p class="offer-description">
      This system has already helped small firms reclaim 20 - 40 hours/month and reduce repetitive admin by up to 60%.
    </p>
    
    <p class="pilot-slots">
      I'm opening 2 final pilot slots before transitioning to fully paid engagements.
    </p>
    
    <div class="offer-box">
      <h3 class="offer-title">You'll get:</h3>
      <ul class="offer-list">
        <li>A free AI workflow audit</li>
        <li>A tailored roadmap to save your team hours</li>
        <li>Option to move into delivery only if it's a clear fit</li>
      </ul>
    </div>
    
    <div class="offer-cta">
      <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">Book A Free R.A.P.I.D. Process Audit</a>
    </div>
  </div>
</section>

<!-- Video Section -->
<section class="video-section">
  <div class="video-content">
    <h2 class="section-title">
      See How I Work - Before We Even Talk
    </h2>
    
    <p class="video-description">
      Want to understand how I think through automation, what real AI systems look like, and why most don't work?
    </p>
    
    <p class="video-subtitle">
      I publish breakdowns every week on YouTube and LinkedIn, showing the exact frameworks, failures, and lessons I use to help teams like yours eliminate repetitive legal work.
    </p>
    
    <div class="videos-grid">
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/yI0vlfbyfeA" title="Video 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/dlrGJ7y-6fg" title="Video 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/qo6M3kTePkA" title="Video 3" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/ndJKK3dE1sg" title="Video 4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/H_l_ktyH53A" title="Video 5" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <div class="video-item">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/zNT8OH5lfvo" title="Video 6" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
    </div>
    
    <p class="video-footer">
      If you're considering automation but need to see behind the curtain first, that's where to start.
    </p>
    
    <div class="social-buttons">
      <a href="https://www.youtube.com/@RokPopov?sub_confirmation=1" target="_blank" class="social-button youtube-button">
        <span class="button-icon">▶</span>
        YouTube Channel
      </a>
      <a href="https://www.linkedin.com/in/rok-popov-ledinski/" target="_blank" class="social-button linkedin-button">
        LinkedIn Profile
      </a>
    </div>
    
    <!-- Email Opt-in #2 - After Video Section -->
    <div class="email-optin-box">
      <form class="email-form">
        <input type="email" placeholder="Enter your email address" required>
        <button type="submit">Subscribe</button>
      </form>
    </div>
  </div>
</section>

<!-- FAQ Section -->
<section class="faq-section">
  <div class="faq-content">
    <h2 class="section-title">
      Frequently Asked Questions
    </h2>
    
    <div class="faq-list">
      <div class="faq-item">
        <h3 class="faq-question">Do I need to understand AI?</h3>
        <p class="faq-answer">No, you don't need any technical background. Our system is designed to work with your existing processes and we handle all the technical implementation.</p>
      </div>
      
      <div class="faq-item">
        <h3 class="faq-question">What if our systems are messy or outdated?</h3>
        <p class="faq-answer">That's exactly why we start with an audit. We work with your current setup and gradually introduce improvements that fit your workflow.</p>
      </div>
      
      <div class="faq-item">
        <h3 class="faq-question">Will we need to buy new software?</h3>
        <p class="faq-answer">In most cases, no. We focus on automating your existing tools and processes. Any new tools we recommend are carefully selected for maximum ROI.</p>
      </div>
    </div>
  </div>
</section>

<!-- Email Opt-in #3 - After FAQ Section -->
<section class="email-optin-section">
  <div class="email-optin-box">
    <form class="email-form">
      <input type="email" placeholder="Enter your email address" required>
      <button type="submit">Stay Updated</button>
    </form>
  </div>
</section>

<!-- Final CTA Section -->
<section class="final-cta-section">
  <div class="cta-content">
    <h2>Let's Get Started</h2>
    <p>Ready to see exactly where you're losing hours? Let's start with your free audit.</p>
    <a href="https://cal.com/rok-popov-ledinski/free-ai-audit" class="cta-button">Book A Free R.A.P.I.D. Process Audit</a>
    <p class="cta-subtext">(Just 2 pilot spots left)</p>
  </div>
</section>

</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const emailForms = document.querySelectorAll('.email-form');
  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbwOD_hKonRr-ITVwKC8_KO_8rk9hpbHpTy98jeVDM1GauYv1-sbk3DL9PtXKz9AP1TWUw/exec';
  
  emailForms.forEach((form, index) => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      
      const emailInput = this.querySelector('input[type="email"]');
      const email = emailInput.value;
      const button = this.querySelector('button');
      
      if (email) {
        // Show loading state
        const originalText = button.textContent;
        button.textContent = 'Submitting...';
        button.disabled = true;
        
        console.log('Submitting to:', SCRIPT_URL);
        console.log('Email:', email);
        
        // Submit to Google Sheets
        fetch(SCRIPT_URL, {
          method: 'POST',
          mode: 'no-cors', // Add this to handle CORS
          headers: {
            'Content-Type': 'application/json',
          },
          body: JSON.stringify({
            email: email
          })
        })
        .then(response => {
          console.log('Response received:', response);
          // With no-cors mode, we can't read the response, so assume success
          showThankYouPopup();
          emailInput.value = '';
        })
        .catch(error => {
          console.error('Fetch error:', error);
          alert('Something went wrong: ' + error.message);
        })
        .finally(() => {
          // Reset button
          button.textContent = originalText;
          button.disabled = false;
        });
      }
    });
  });
});

function showThankYouPopup() {
  // Create popup overlay
  const overlay = document.createElement('div');
  overlay.style.cssText = `
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
  `;
  
  // Create popup content
  const popup = document.createElement('div');
  popup.style.cssText = `
    background: white;
    padding: 3rem;
    border-radius: 12px;
    text-align: center;
    max-width: 500px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    font-family: 'Open Sans', sans-serif;
  `;
  
  popup.innerHTML = `
    <h3 style="color: #10b981; margin-bottom: 1.5rem; font-size: 2rem; font-weight: 700; font-family: 'Open Sans', sans-serif;">Thank You!</h3>
    <p style="color: #1e293b; margin-bottom: 2rem; font-size: 1.2rem; line-height: 1.6; font-family: 'Open Sans', sans-serif;">You're now subscribed to our legal automation updates.</p>
    <button onclick="this.closest('.popup-overlay').remove()" style="background: #10b981; color: white; border: none; padding: 16px 32px; border-radius: 8px; cursor: pointer; font-weight: 600; font-size: 1.1rem; font-family: 'Open Sans', sans-serif;">Close</button>
  `;
  
  overlay.className = 'popup-overlay';
  overlay.appendChild(popup);
  document.body.appendChild(overlay);
  
  // Auto-close after 3 seconds
  setTimeout(() => {
    if (overlay.parentNode) {
      overlay.remove();
    }
  }, 3000);
}
</script>

