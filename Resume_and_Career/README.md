# 💼 Resume & Career Prompts

A curated collection of career-advancement prompts designed to help software engineers and AI/ML professionals craft impactful resumes, build outstanding LinkedIn headlines, practice technical interviews, and optimize salary negotiations.

## Table of Contents
* [1. Google XYZ Resume Bullet Writer](#1-google-xyz-resume-bullet-writer)
* [2. LinkedIn Profile Headline Planner](#2-linkedin-profile-headline-planner)
* [3. Cover Letter Tailoring Guide](#3-cover-letter-tailoring-guide)
* [4. Mock Interview Simulator](#4-mock-interview-simulator)
* [5. Salary Negotiation Coach](#5-salary-negotiation-coach)
* [6. Career Transition Roadmap](#6-career-transition-roadmap)
* [7. Portfolio Project Planner](#7-portfolio-project-planner)
* [8. Cold Outreach Email Draft](#8-cold-outreach-email-draft)
* [9. Resume-to-Job Fit Gap Analyzer](#9-resume-to-job-fit-gap-analyzer)
* [10. STAR Interview Response Writer](#10-star-interview-response-writer)

---

### 1. Google XYZ Resume Bullet Writer

*   **Purpose**: Rewrite weak, task-based resume bullet points into high-impact accomplishment statements using Google's XYZ formula: *Accomplished [X], as measured by [Y], by doing [Z]*.
*   **Prompt**:
    ```text
    You are an expert technical resume writer and career coach.
    Your task is to rewrite raw resume bullet points into highly impactful accomplishments using the Google XYZ formula:
    "Accomplished [X], as measured by [Y], by doing [Z]"

    Raw Bullet Points:
    [INSERT_RAW_BULLETS]

    Target Role: [TARGET_ROLE] (e.g., ML Engineer, Full Stack Developer, DevOps Engineer)

    For each bullet point, provide:
    1. **Analyzed Weakness**: Why the original bullet is weak (e.g., lacks metrics, too task-focused, passive verbs).
    2. **XYZ Rewritten Bullet**: The polished, metric-driven version.
    3. **Key Action Verbs Used**: List of strong technical verbs introduced.
    4. **Suggested Metrics (If missing)**: If the user didn't provide metrics, suggest 3 plausible KPI metrics (e.g., % latency reduction, % test coverage, $ cost savings) they can research and insert.
    ```
*   **Tips for Better Results**:
    *   If you don't know the exact metrics, approximate them and let the model know (e.g., "sped up database significantly"). The model will help translate that into a formal performance metric structure.
*   **Example Use Case**:
    *   **Input**: "Helped design and code a FastAPI backend database pipeline."
    *   **Output**: 
        *   XYZ: "Optimized backend database latency by 42% (X) as measured by Prometheus API telemetry (Y) through refactoring FastAPI SQLAlchemy queries and implementing Redis query caching (Z)."

---

### 2. LinkedIn Profile Headline Planner

*   **Purpose**: Create highly searchable, professional, and attention-grabbing headlines for LinkedIn targeting recruiters and hiring managers.
*   **Prompt**:
    ```text
    You are a personal branding consultant specializing in tech careers.
    Create 5 distinct LinkedIn headlines tailored to my profile and target roles.

    My Core Tech Stack / Experience:
    [INSERT_TECH_STACK_AND_EXPERIENCE]

    Target Roles:
    [INSERT_TARGET_ROLES] (e.g., Senior Data Scientist, Graduate AI Engineer)

    Unique Value Proposition (UVP) / Project: [e.g., "Built an open-source vector DB wrapper with 1k stars"]

    Provide headlines matching these templates:
    1. **Formula 1: Role | Core Stack | Specific Impact** (Professional & Standard)
    2. **Formula 2: Role | Passion/Focus | Tech Keywords** (Keyword-Rich for SEO)
    3. **Formula 3: Value-First ("Helping [target] do [action]")** (Solution-Oriented)
    4. **Formula 4: Short, Punchy & Credential-Focused** (High Status)
    5. **Formula 5: Project/Achievement Centric** (Portfolio Builder)
    ```
*   **Tips for Better Results**:
    *   Incorporate key terms directly from active job postings to score higher in LinkedIn recruiter search algorithms.
*   **Example Use Case**:
    *   **Input**: Graduate student in ML, knows PyTorch/FastAPI, built an automated medical imaging classification app.
    *   **Output**: "AI/ML Engineering Graduate | PyTorch, Python, FastAPI | Accelerating Medical Diagnostic Speeds via Deep Learning Classification Model Development"

---

### 3. Cover Letter Tailoring Guide

*   **Purpose**: Tailor a generic cover letter to a specific job description, ensuring maximum alignment with company culture and requirements.
*   **Prompt**:
    ```text
    You are an expert executive recruiter. Your task is to customize a cover letter to fit a specific target job description, ensuring it highlights my relevant experience and matches the company's tone.

    My Core Experience / Resume:
    [INSERT_RESUME_TEXT]

    Target Job Description:
    [INSERT_JOB_DESCRIPTION]

    Target Company Name & Culture (if known): [COMPANY_DETAILS]

    Requirements:
    1. Limit response to 300-400 words.
    2. Start with a compelling hook referencing the company's recent work or core mission.
    3. Match candidate achievements directly to the top 3 requirements in the job description.
    4. Maintain a professional yet enthusiastic tone.
    5. Output the completed letter, plus a list of **Top 3 Alignment Matches** explaining why those specific matches were highlighted.
    ```
*   **Tips for Better Results**:
    *   Include details of recent news about the target company (e.g., funding round, product release) to show deep research.
*   **Example Use Case**:
    *   **Input**: Resume showing PyTorch project experience and a job posting for a Computer Vision Engineer at a robotics company.
    *   **Output**: Custom letter addressing the robotics firm's autonomous driving challenges, matching candidate's PyTorch CNN experience directly.

---

### 4. Mock Interview Simulator

*   **Purpose**: Conduct a realistic, interactive interview simulation for a target role, providing grading and constructive feedback.
*   **Prompt**:
    ```text
    You are the Lead Hiring Manager for a [ROLE_NAME] role at a tech company.
    You will conduct a mock interview with me, focusing on both technical design and behavioral questions.

    Target Job Description:
    [INSERT_JOB_DESCRIPTION]

    My Resume:
    [INSERT_RESUME_TEXT]

    Guidelines:
    1. Start the simulation by greeting me and asking a single, typical opening interview question (behavioral or technical).
    2. Wait for my response.
    3. Respond to my answer by:
       - Giving brief, silent inline feedback on my response quality (delivery, completeness, alignment with STAR method).
       - Asking the next logical follow-up question.
    4. Only ask ONE question at a time.
    5. Do not write the answers for me. Keep the simulation active until I say "End Simulation".
    ```
*   **Tips for Better Results**:
    *   Tell the model to probe deeply into project details to simulate a high-intensity technical loop.
*   **Example Use Case**:
    *   **Input**: Mock interview for Junior Backend Engineer role, candidate knows Go and Postgres.
    *   **Output**: "Hello! Welcome to the interview. Looking at your resume, you built a distributed task queue in Go. Can you walk me through how you handled worker failures and duplicate task execution?"

---

### 5. Salary Negotiation Coach

*   **Purpose**: Script strategic, professional negotiation emails and talking points for tech job offers.
*   **Prompt**:
    ```text
    You are a professional salary negotiation coach and talent agent.
    Help me structure a counter-offer strategy to negotiate the terms of a new job offer.

    Initial Offer Details:
    - Base Salary: [INITIAL_BASE]
    - Equity/RSUs: [INITIAL_EQUITY]
    - Sign-on Bonus: [INITIAL_SIGN_ON]
    - Location/Remote Status: [LOCATION]

    My Target Compensation:
    - Target Base: [TARGET_BASE]
    - Other demands: [e.g., remote days, learning budget]

    My Leverage / Counter Arguments: [e.g., competing offer, specialized niche skill, market average data]

    Please output:
    1. **Strategic Negotiation Roadmap**: The steps to handle the negotiation call/email.
    2. **Negotiation Email Template**: A polite, professional email counter-offer proposing the target compensation.
    3. **Objection Handling Scripts**: 3 common HR pushbacks (e.g., "This is the band limit", "We cannot change equity") and how to answer them verbally.
    ```
*   **Tips for Better Results**:
    *   Maintain a collaborative, excited tone rather than combative to keep HR on your side.
*   **Example Use Case**:
    *   **Input**: Offer of $105k base, requesting $115k, using specialized PyTorch edge-quantization skills as leverage.
    *   **Output**: Script emphasizing appreciation, stating how Edge ML fits their core product roadmap, and requesting base adjustments or a sign-on buffer.

---

### 6. Career Transition Roadmap

*   **Purpose**: Formulate a step-by-step career pivot path from a non-technical or different technical field into a target role.
*   **Prompt**:
    ```text
    You are a Career Transition Coach. Help me draft a step-by-step pivot strategy to transition from my current role to my target role.

    Current Role/Background: [CURRENT_ROLE] (e.g., Manual QA, Mechanical Engineer)
    Target Role: [TARGET_ROLE] (e.g., Cloud Data Engineer)
    Timeframe to Transition: [TIMEFRAME] (e.g., 6 Months, 1 Year)

    Please produce:
    1. **Transferable Skills Matrix**: A table mapping skills in my current background that are highly valuable in the target role.
    2. **Core Skills to Acquire**: Top 5 technical competencies I need to learn, ranked by priority.
    3. **Phase-by-Phase Roadmap**: Monthly/Quarterly breakdown of learning milestones, certification strategies, and networking objectives.
    4. **Portfolio Strategy**: Describe 2 custom projects that will demonstrate to recruiters that I can perform target role tasks despite a non-traditional background.
    ```
*   **Tips for Better Results**:
    *   Provide details on your daily schedule, so the plan is realistic (e.g., "I can study 2 hours every evening").
*   **Example Use Case**:
    *   **Input**: Transitioning from Mechanical Engineering to Machine Learning Engineer in 9 months.
    *   **Output**: Maps mathematical skills (linear algebra, calculus) to ML modeling, outlines learning PyTorch, and suggests building an ML pipelines project.

---

### 7. Portfolio Project Planner

*   **Purpose**: Design highly unique, resume-worthy projects that showcase advanced skills instead of generic tutorial projects.
*   **Prompt**:
    ```text
    You are a Senior Project Mentor. Design 3 unique, portfolio-worthy project ideas that I can build to showcase my skills to recruiters.

    My Skills/Stack: [INSERT_SKILLS] (e.g., React, FastAPI, Docker, Python)
    Target Role: [TARGET_ROLE] (e.g., Full Stack Engineer)
    Niche Preference (optional): [e.g., Financial Tech, Healthcare, Dev Tools]

    For each project proposal, provide:
    1. **Project Concept & Overview**: A unique, non-trivial application concept (avoid standard ToDo lists, weather apps, or generic chat apps).
    2. **Architecture Stack**: Specific libraries, database models, and cloud services to integrate.
    3. **Advanced Showcase Feature**: What specific complex technical problem this project solves (e.g., rate-limiting, custom web scraping, distributed locking, model evaluation).
    4. **Step-by-Step Implementation Guide**: An outline of development order.
    5. **Resume Bullet Point**: How to write this project on a resume using the XYZ formula.
    ```
*   **Tips for Better Results**:
    *   Focus on projects that showcase integration between frontend, backend, and database caching rather than standalone scripts.
*   **Example Use Case**:
    *   **Input**: React, FastAPI, Python, target Full Stack role.
    *   **Output**: Suggests building an automated LLM evaluation playground, details using Celery task queues for concurrent evaluations, and writes a sample XYZ bullet.

---

### 8. Cold Outreach Email Draft

*   **Purpose**: Write high-conversion cold emails and LinkedIn messages to recruiters, alumni, or hiring managers.
*   **Prompt**:
    ```text
    You are a professional networker. Write 3 templates for cold outreach targeting professionals in my industry.

    Target Recipient: [RECIPIENT_TYPE] (e.g., Recruiter, Engineering Manager, College Alumnus)
    Target Company: [COMPANY_NAME]
    My Current Status: [e.g., Graduate student seeking summer internship, Junior Developer looking for roles]
    Reason for Contact: [e.g., Requesting a 15-minute informational interview, asking about an open role]

    Provide:
    1. **Template 1: LinkedIn Connection Message (140-300 chars)**: Short, non-demanding, personalized.
    2. **Template 2: Cold Email (Subject + Body, <150 words)**: Focused on mutual interest, brief introduction, clear call to action.
    3. **Template 3: Follow-up Message**: Sent 5 days later if no response was received.
    ```
*   **Tips for Better Results**:
    *   Provide a link to a specific project or your GitHub profile so recipients can quickly gauge your competence.
*   **Example Use Case**:
    *   **Input**: Graduate AI student reaching out to a Machine Learning Lead at a health-tech company.
    *   **Output**: Professional email mentioning their recent research, highlighting candidate's health-tech project, and requesting a 10-minute chat.

---

### 9. Resume-to-Job Fit Gap Analyzer

*   **Purpose**: Audit a resume against a target job description to identify missing keywords, skills, and experience gaps.
*   **Prompt**:
    ```text
    You are an Applicant Tracking System (ATS) optimization expert and recruiter.
    Analyze the provided resume against the job description and output a gap analysis report.

    My Resume:
    [INSERT_RESUME_TEXT]

    Target Job Description:
    [INSERT_JOB_DESCRIPTION]

    Your report must contain:
    1. **Match Score (1-100)**: Estimate how closely the resume aligns with the job requirements.
    2. **Missing Key Tech Stack/Keywords**: Specific technical terms, libraries, or methodologies mentioned in the job description that are missing from the resume.
    3. **Experience Gaps**: Discrepancies in years of experience, leadership scope, or pipeline ownership.
    4. **ATS Recommendations**: Actionable suggestions on where to integrate missing terms and how to restructure experience bullets to match requirements.
    ```
*   **Tips for Better Results**:
    *   Copy the entire job description text including the company description, as sometimes soft skills or company values are hidden there.
*   **Example Use Case**:
    *   **Input**: Python backend developer resume matched with a Senior Django backend developer post.
    *   **Output**: Identifies missing Django ORM, celery task queue keywords, scores it at 65%, and suggests adding Django-specific metrics.

---

### 10. STAR Interview Response Writer

*   **Purpose**: Format behavioral accomplishments into structured STAR (Situation, Task, Action, Result) answers for interviews.
*   **Prompt**:
    ```text
    You are an expert interviewer. Help me structure my behavioral story into the STAR (Situation, Task, Action, Result) format.

    Raw Story/Experience:
    [INSERT_RAW_STORY] (e.g., "I solved a bug that was crashing our database during Black Friday.")

    Target Question: [e.g., "Tell me about a time you handled a crisis under pressure."]

    Please output:
    1. **Situation**: 2-3 sentences setting the context (what company, what scale, what was the stakes).
    2. **Task**: 1-2 sentences defining the challenge (what was *your* direct responsibility).
    3. **Action**: Detailed bulleted steps outlining what *you* specifically did (tools used, technical reasoning, collaboration).
    4. **Result**: 2 sentences detailing the measurable outcome (quantifiable business metrics, learnings, prevention actions).
    5. **Delivery Notes**: Key points to emphasize during the verbal delivery of this story.
    ```
*   **Tips for Better Results**:
    *   Ensure the "Result" section contains at least one percentage or dollar metric to demonstrate quantifiable impact.
*   **Example Use Case**:
    *   **Input**: Solved database overload on an e-commerce platform.
    *   **Output**: Structures context (Q4 traffic), tasks (identifying DB lockups), action (optimizing SQL indexes and implementing Redis queues), and results (99.9% uptime, $12k server cost savings).
