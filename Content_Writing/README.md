# ✍️ Content Writing & Copywriting Prompts

A curated collection of prompts designed for technical bloggers, marketers, copywriters, and content creators to generate SEO blog structures, write engaging newsletters, script videos, and convert long articles into social media threads.

## Table of Contents
* [1. SEO Blog Post Outline](#1-seo-blog-post-outline)
* [2. Copywriting Framework Adapter](#2-copywriting-framework-adapter)
* [3. Engaging Newsletter Writer](#3-engaging-newsletter-writer)
* [4. YouTube/Video Script Outline](#4-youtubevideo-script-outline)
* [5. Step-by-Step Tech Tutorial Writer](#5-step-by-step-tech-tutorial-writer)
* [6. Click-Worthy Headline Generator](#6-click-worthy-headline-generator)
* [7. Article-to-Thread Converter](#7-article-to-thread-converter)
* [8. Meta Description & SEO Snippet Writer](#8-meta-description--seo-snippet-writer)
* [9. Hero's Journey Story Outline](#9-heros-journey-story-outline)
* [10. SaaS Product Copywriter](#10-saas-product-copywriter)

---

### 1. SEO Blog Post Outline

*   **Purpose**: Create highly structured, SEO-optimized blog outlines targeting specific search keywords and user intent.
*   **Prompt**:
    ```text
    You are an SEO Content Strategist. Design a comprehensive outline for a blog post based on the target topic and focus keywords.

    Target Topic: [TOPIC] (e.g., "Introduction to Kubernetes for frontend developers")
    Primary Keyword: [PRIMARY_KEYWORD]
    Secondary Keywords: [SECONDARY_KEYWORDS_LIST]
    Target Audience: [AUDIENCE] (e.g., beginner developers, enterprise buyers)

    Please produce:
    1. **Recommended SEO Metadata**:
       - Title Tag (<70 characters, keyword-frontloaded).
       - Meta Description (<155 characters, including Call to Action).
    2. **Structured Heading Outline**: Include H1, H2, and H3 headings. For each heading section, provide:
       - Core message/point to explain.
       - Keyword integration instructions.
       - User search intent to satisfy (Informational, Transactional, Navigational).
    3. **Internal/External Linking Strategy**: Recommendations on what types of resources to link to.
    ```
*   **Tips for Better Results**:
    *   State the specific search volume or competition tier of the keywords if known, so the model can adjust the density of secondary keywords.
*   **Example Use Case**:
    *   **Input**: "Best practices for React state management in 2026." Primary keyword: "React state management".
    *   **Output**: Outlines H1, H2 sections covering Redux, Context API, Zustand, Meta tags, and lists internal link ideas.

---

### 2. Copywriting Framework Adapter

*   **Purpose**: Rewrite features/product specifications into high-conversion copy using standard frameworks like AIDA, PAS, or BAB.
*   **Prompt**:
    ```text
    You are a conversion-focused Copywriter. Translate raw product features into persuasive marketing copy using a specific copywriting framework.

    Target Copywriting Framework: [AIDA / PAS / BAB]
    - **AIDA**: Attention, Interest, Desire, Action
    - **PAS**: Problem, Agitation, Solution
    - **BAB**: Before, After, Bridge
    Raw Product Features/Details:
    [INSERT_PRODUCT_DETAILS]

    Target Audience: [AUDIENCE]

    Please output:
    1. **Framework Analysis**: Briefly explain why this framework fits the product type.
    2. **Formatted Copy**: Provide the written copy structured section-by-section according to the selected framework.
    3. **Call to Action (CTA)**: 3 high-impact variations of buttons/CTAs.
    ```
*   **Tips for Better Results**:
    *   Use PAS (Problem, Agitation, Solution) for B2B/SaaS software tools, and AIDA (Attention, Interest, Desire, Action) for consumer apps/marketing landing pages.
*   **Example Use Case**:
    *   **Input**: A tool that automatically tests APIs for security flaws. Framework: PAS.
    *   **Output**: 
        *   Problem: APIs are leaking credentials in production.
        *   Agitation: A single leak can result in $100k data breach fines and ruin customer trust.
        *   Solution: Security Scanner automatically audits endpoints in CI/CD before deploy.

---

### 3. Engaging Newsletter Writer

*   **Purpose**: Write engaging, personal, and high-click-rate email newsletters using a conversational tone.
*   **Prompt**:
    ```text
    You are a professional newsletter writer and email marketer.
    Write an engaging, conversational newsletter based on the provided core message.

    Core Message / Theme: [THEME] (e.g., "Why microservices are overrated for small startups")
    Value Proposition / Link to share: [URL_OR_RESOURCE]
    Target Reader: [TARGET_READER] (e.g., tech founders, design students)

    Guidelines:
    1. Generate 3 click-worthy Subject Line options (incorporating curiosity or urgency, under 60 chars).
    2. Provide a single line of Preview Text.
    3. Write the newsletter body (250-400 words) using a conversational, storytelling tone. Use short paragraphs (<3 sentences) and bullet points for readability.
    4. Include a clear call-to-action (CTA) button/link anchor.
    5. Conclude with a memorable sign-off.
    ```
*   **Tips for Better Results**:
    *   Incorporate a personal anecdote or a recent industry event in the email start to establish trust.
*   **Example Use Case**:
    *   **Input**: Retiring dynamic typing in teams; links to TypeScript migration guides.
    *   **Output**: Subjects like "Why we deleted 5,000 lines of JavaScript". Body detailing runtime crashes, migration speedups, and links to the guide.

---

### 4. YouTube/Video Script Outline

*   **Purpose**: Structure engaging video script outlines including visual cues, spoken dialogue drafts, and pacing rules.
*   **Prompt**:
    ```text
    You are a YouTube Creator and Video Producer.
    Design a video script outline designed to maximize viewer retention and click-through rates.

    Video Title / Topic: [VIDEO_TOPIC]
    Target Video Length: [DURATION] (e.g., 5 minutes, 10 minutes)
    Key takeaways for the viewer: [TAKEAWAYS]

    Your script structure must outline:
    1. **The Hook (First 30 seconds)**: Visual cues and spoken script to stop users from clicking away, stating the value promise.
    2. **The Story/Core Content Section**: Timed blocks detailing:
       - Spoken Dialogue summary.
       - B-Roll/Visual overlay directions (e.g., showing terminal, graphics).
       - Engagement triggers (asking questions, calls to subscribe).
    3. **The Outro (Last 30 seconds)**: Clean transition to card link/call to action without lowering energy.
    ```
*   **Tips for Better Results**:
    *   Specify if you want the visual cue style to be fast-paced (TikTok/Shorts format) or educational (long-form tutorial).
*   **Example Use Case**:
    *   **Input**: "How I learned Git in 4 hours." 8-minute runtime.
    *   **Output**: Hook comparing git merges to scary movie scenes, timed blocks explaining commits, branching, and resolve conflicts visually.

---

### 5. Step-by-Step Tech Tutorial Writer

*   **Purpose**: Write high-quality, step-by-step developer tutorials that are easy to follow and technically accurate.
*   **Prompt**:
    ```text
    You are a technical writer and developer advocate.
    Write a detailed, step-by-step tutorial explaining how to build or configure the target technology.

    Tutorial Subject: [SUBJECT] (e.g., "Setting up a Redis Cache in Go")
    Prerequisites: [PREREQS] (e.g., Go installed, Docker installed)
    Source Code / Logic:
    [INSERT_CODE_OR_STEPS]

    Tutorial Requirements:
    1. **Introduction**: What the reader will build and *why* this technology stack is used.
    2. **Prerequisites Checklist**: Clear setup requirements.
    3. **Step-by-Step Sections**: Numbered steps. Each step must contain:
       - Code block with comments.
       - Detailed explanation of what the code lines do.
       - Expected output or verification test (e.g., console log or server status).
    4. **Troubleshooting Guide**: 2 common configuration errors and how to solve them.
    5. **Next Steps**: Suggestions for extension exercises.
    ```
*   **Tips for Better Results**:
    *   Ask the model to include standard terminal command blocks (`mkdir`, `cd`) so beginners don't get lost in folders setup.
*   **Example Use Case**:
    *   **Input**: Setting up PostgreSQL in Docker.
    *   **Output**: Step 1: docker-compose configuration. Step 2: running containers. Step 3: connecting via `pgcli` tool, with clear commands and troubleshooting tips.

---

### 6. Click-Worthy Headline Generator

*   **Purpose**: Generate multiple clickable, non-clickbait titles and headlines for articles, blogs, or newsletters.
*   **Prompt**:
    ```text
    You are a digital editor. Generate 10 distinct, click-worthy headlines for the following article draft.
    Your headlines must avoid generic "clickbait" formatting but maximize curiosity, interest, and search click rates.

    Article Draft / Summary:
    [INSERT_SUMMARY_OR_TEXT]

    Categorize the 10 suggestions into these buckets:
    1. **SEO-Focused (2 suggestions)**: Target keyword included, standard format.
    2. **Curiosity Gap (2 suggestions)**: Creates questions in readers' minds.
    3. **How-To / Value-Driven (2 suggestions)**: Promising a specific skill or time saving.
    4. **Social Proof / Authority (2 suggestions)**: (e.g., "What Senior Engineers get wrong about...")
    5. **Contrarian/Bold (2 suggestions)**: Challenges standard assumptions.
    ```
*   **Tips for Better Results**:
    *   Provide the target primary keyword so the SEO-focused titles optimize it.
*   **Example Use Case**:
    *   **Input**: Article about refactoring nested loops to use map filters.
    *   **Output**: Suggestions like "Stop using nested loops in JavaScript (Contrarian)" and "How to refactor O(N^2) complexity code in 3 steps (How-To)".

---

### 7. Article-to-Thread Converter

*   **Purpose**: Condense long articles or technical blogs into engaging Twitter/X threads.
*   **Prompt**:
    ```text
    You are a social media manager specializing in tech content.
    Convert the following long-form article or technical document into an engaging, multi-tweet thread.

    Article Content:
    [INSERT_ARTICLE_TEXT]

    Target Platform: Twitter/X (280 character limit per post)

    Requirements:
    1. **Tweet 1 (The Hook)**: Highlight the most shocking result, metric, or question to get retweets.
    2. **Structured Thread**: 5 to 8 tweets total. Number each tweet (e.g., 1/, 2/).
    3. **Formatting**: Use bullet points and spacing to make it readable.
    4. **Visual suggestions**: For each tweet, suggest if a code snippet, diagram, or chart should be attached.
    5. **Final Tweet**: Conclude with a call to action linking to the full article.
    ```
*   **Tips for Better Results**:
    *   Ask the model to summarize code blocks into short descriptions rather than pasting wide syntax lines that break the 280-char limit.
*   **Example Use Case**:
    *   **Input**: Article about optimizing Python performance by compile to Cython.
    *   **Output**: 6-tweet thread outlining Python bottlenecks, introducing Cython, showing speedup comparisons (10x metrics), and links to the full post.

---

### 8. Meta Description & SEO Snippet Writer

*   **Purpose**: Write search-engine-optimized meta titles and descriptions to boost Google Search organic CTR.
*   **Prompt**:
    ```text
    You are an Search Engine Optimizer (SEO). Write search-engine snippets for the provided web page content.

    Page Title/Header: [HEADER]
    Focus Keyword: [KEYWORD]
    Page Summary: [SUMMARY]

    Generate 3 distinct metadata options:
    - **Option 1: Value-Driven**: Emphasizes what the searcher will learn or get.
    - **Option 2: Direct & Informational**: Focuses on raw facts.
    - **Option 3: Urgency / CTA-heavy**: Focuses on immediate action.

    Ensure every option respects the strict character bounds:
    - Title Tag: Between 50 and 60 characters.
    - Meta Description: Between 120 and 150 characters.
    - Include the focus keyword naturally near the beginning.
    ```
*   **Tips for Better Results**:
    *   Use character-count checks inside the model loop to prevent it from outputting strings that get truncated on Google Search results pages.
*   **Example Use Case**:
    *   **Input**: Title: "Database migration guide". Keyword: "database migration". Summary: guide on migrating from MySQL to PostgreSQL.
    *   **Output**: "Database Migration: A Step-by-Step Guide (51 chars)" / "Learn how to migrate from MySQL to PostgreSQL safely. This database migration guide covers schemas, data sync, and minimizing downtime. (142 chars)".

---

### 9. Hero's Journey Story Outline

*   **Purpose**: Structure business, career, or product stories using the Hero's Journey narrative framework to build deep audience connection.
*   **Prompt**:
    ```text
    You are a narrative designer and copywriter.
    Structure my raw experience or company journey into the classic "Hero's Journey" narrative framework.

    Raw Experience / Story:
    [INSERT_RAW_STORY] (e.g., "How we started our software consultancy with no clients")

    Target Audience: [e.g., LinkedIn feed, website 'About Us' page]

    Map the story to these phases:
    1. **The Status Quo (Ordinary World)**: The initial state and background.
    2. **The Call to Adventure & Obstacle**: The problem encountered or decision to start.
    3. **The Abyss (Lowest Point)**: A critical struggle (e.g., server failure, losing a client).
    4. **The Revelation / Solution (Meeting the Mentor/Tool)**: What changed, key realization.
    5. **The Return (Polished State)**: The current successful status, lessons, and values you share now.
    ```
*   **Tips for Better Results**:
    *   Highlight your actual "abyss" moment (e.g., "having only $50 left in the bank") to make the narrative arc feel authentic.
*   **Example Use Case**:
    *   **Input**: Starting an open-source library that initially failed but succeeded after refactoring.
    *   **Output**: Outlines ordinary developer world, call (frustration with tools), abyss (0 downloads for weeks), revelation (user feedback), and return (1k stars).

---

### 10. SaaS Product Copywriter

*   **Purpose**: Write feature headlines, benefit bullet points, and pricing tiers copy for SaaS web landing pages.
*   **Prompt**:
    ```text
    You are a landing page copywriter. Design copy sections for a Software-as-a-Service (SaaS) homepage.

    Product Name: [NAME]
    Core Value Proposition: [VALUE_PROP] (e.g., "Instantly generates beautiful reports from raw data")
    Key Features: [FEATURES_LIST]
    Target Buyer: [BUYER] (e.g., Freelance Designers, CTOs)

    Please output copy for:
    1. **Hero Section**:
       - Primary Header (Hook, max 10 words).
       - Sub-headline (Value explanation, max 20 words).
       - Primary Call to Action button.
    2. **Features vs. Benefits Grid**: A 3-column grid mapping:
       - Feature Name (What it is).
       - Benefit Copy (Why they should care - time/money saved).
    3. **Pricing Tier Copy**: Short taglines for "Starter", "Pro", and "Enterprise" plans explaining value shifts.
    ```
*   **Tips for Better Results**:
    *   Specify the exact aesthetic tone of your SaaS (e.g., "minimalist and professional" vs "fun and playful") so the vocabulary aligns.
*   **Example Use Case**:
    *   **Input**: Report generator for freelancers.
    *   **Output**: Headline: "Send client reports in 60 seconds." Benefits: "Saves hours of design work." Pricing tiers detailing features matching size of freelance clients.
