# ⚡ Productivity & Workflow Prompts

A curated collection of prompts designed to optimize daily work routines, prioritize complex task lists, build sustainable habits, write action-oriented meeting agendas, and streamline professional communications.

## Table of Contents
* [1. Time-Blocking Planner](#1-time-blocking-planner)
* [2. Eisenhower Matrix Task Organizer](#2-eisenhower-matrix-task-organizer)
* [3. Action-Oriented Meeting Agenda](#3-action-oriented-meeting-agenda)
* [4. Task Deconstructor](#4-task-deconstructor)
* [5. Weighted Decision Matrix](#5-weighted-decision-matrix)
* [6. Transcript Action Item Extractor](#6-transcript-action-item-extractor)
* [7. Atomic Habit Loop Builder](#7-atomic-habit-loop-builder)
* [8. SMART Goal Translator](#8-smart-goal-translator)
* [9. Standup Message Formatter](#9-standup-message-formatter)
* [10. Pomodoro Sprint Planner](#10-pomodoro-sprint-planner)

---

### 1. Time-Blocking Planner

*   **Purpose**: Design a daily schedule based on time-blocking and energy levels to protect focus time and maximize cognitive capacity.
*   **Prompt**:
    ```text
    You are a productivity consultant specializing in deep work design.
    Design a time-blocked daily calendar optimized for my task list and cognitive energy peaks.

    My Tasks for Today:
    [INSERT_TASKS_LIST]

    My High-Energy/Focus Hours: [e.g., "9:00 AM - 12:00 PM"]
    My Total Work Hours: [e.g., "9:00 AM - 5:00 PM"]
    Meetings Scheduled: [e.g., "1:00 PM - 1:30 PM Standup"]

    Please output a daily schedule matching these rules:
    1. **Deep Work Blocks**: Dedicate your high-energy hours to the most cognitively demanding tasks. Zero interruptions allowed during these blocks.
    2. **Shallow Work Blocks**: Group administrative tasks (emails, Slack replies, documentation) into low-energy slots.
    3. **Buffer Time**: Add two 15-minute buffers for spillover tasks or unexpected requests.
    4. **Rest/Transition Breaks**: Include short breaks between blocks to prevent cognitive fatigue.

    Output format:
    1. **Time-Blocked Calendar**: A markdown table showing Time, Activity, and Category (Deep Work, Shallow Work, Break, Buffer).
    2. **Execution Strategy**: Tips to stick to this schedule (e.g., website blockers, notification rules).
    ```
*   **Tips for Better Results**:
    *   Be honest about when your energy drops (e.g., "3:00 PM slump") so the model can schedule trivial administrative tasks for that slot.
*   **Example Use Case**:
    *   **Input**: Tasks: Refactoring a database, answering emails, writing team briefs. High energy: 9 AM-11 AM.
    *   **Output**: Calendar blocking 9-11 AM for DB refactoring, lunch/walk breaks, 1-1:30 PM standup, and 3:30-4:30 PM for emails.

---

### 2. Eisenhower Matrix Task Organizer

*   **Purpose**: Organize a chaotic, overwhelming list of tasks into the Eisenhower Matrix (Urgent vs. Important) to establish clear execution priorities.
*   **Prompt**:
    ```text
    You are a professional operations manager.
    Organize the following unorganized list of tasks using the Eisenhower Matrix decision framework.

    Raw Task List:
    [INSERT_TASKS_LIST]

    Classify each task into one of the four quadrants:
    1. **Quadrant 1 (Do First)**: Urgent and Important (critical tasks needing immediate action).
    2. **Quadrant 2 (Schedule)**: Important, but Not Urgent (long-term strategic goals, deep study, system improvements).
    3. **Quadrant 3 (Delegate)**: Urgent, but Not Important (tasks you can automate, hand off, or batch).
    4. **Quadrant 4 (Eliminate)**: Not Urgent and Not Important (distractions, low-value requests).

    For each task, provide:
    - Task Name
    - Assigned Quadrant
    - Brief Justification (explaining why it sits in that category).
    - Suggested Next Action (e.g., "Set calendar event for Tuesday", "Write automation script").
    ```
*   **Tips for Better Results**:
    *   Providing context on *deadlines* and *business impact* will help the model classify the urgency correctly.
*   **Example Use Case**:
    *   **Input**: List of tasks including "fix production outage", "reply to recruiters", "browse Reddit for projects", "read a paper on LLMs".
    *   **Output**: Outage categorized as Q1, reading paper as Q2, recruiters as Q3 (batch), Reddit as Q4.

---

### 3. Action-Oriented Meeting Agenda

*   **Purpose**: Build lean, objective-driven meeting agendas that respect attendees' time and guarantee clear outcomes.
*   **Prompt**:
    ```text
    You are a chief of staff.
    Draft an action-oriented meeting agenda to ensure a highly productive session.

    Meeting Topic: [MEETING_TOPIC] (e.g., "Post-mortem on server outage", "Q3 product planning")
    Meeting Duration: [DURATION] (e.g., 30 minutes, 60 minutes)
    Key Attendees: [ATTENDEES] (e.g., Frontend lead, DB Administrator, Product Manager)
    Core Objective: [WHAT_SUCCESS_LOOKS_LIKE]

    Your response must provide:
    1. **Pre-Work Requirements**: What read-aheads or metrics attendees must review *before* joining.
    2. **Timed Agenda Blocks**: Segmented breakdown of minutes, topics, and owner (e.g., 5 mins: review log statistics - DB Admin).
    3. **Key Decision Questions**: The exact questions that *must* be answered by the end of the meeting.
    4. **Output/Follow-up Checklist Template**: A template to capture action items, assignees, and deadlines.
    ```
*   **Tips for Better Results**:
    *   Set the target duration to 30 minutes instead of an hour. This forces the model to create highly aggressive, outcome-driven agenda structures.
*   **Example Use Case**:
    *   **Input**: 30-minute meeting to choose between PostgreSQL or MongoDB for a project.
    *   **Output**: TIMED agenda starting with 5 mins of requirements review, 15 mins comparing schemas, 5 mins deciding, and 5 mins assigning tasks.

---

### 4. Task Deconstructor

*   **Purpose**: Break down massive, intimidating, or ambiguous tasks into small, actionable micro-steps to overcome procrastination.
*   **Prompt**:
    ```text
    You are a systems engineer and project scheduler.
    Analyze the following complex, high-level task and deconstruct it into atomic, actionable micro-steps.

    Ambiguous High-Level Task:
    [INSERT_HIGH_LEVEL_TASK] (e.g., "Deploy application to AWS", "Write final thesis chapter")

    Provide:
    1. **Deconstruction Phase List**: Group the micro-steps into sequential phases (e.g., Phase 1: Setup & Config, Phase 2: Implementation...).
    2. **Atomic Checklist**: A flat list of tasks, where each item can be completed in less than 45 minutes and has a clear definition of done.
    3. **First 3 Steps**: Highlight the absolute first 3 steps (requiring low cognitive effort) to build immediate momentum and overcome inertia.
    4. **Potential Friction Points**: Identify where I might get stuck (e.g., permissions, writing block) and provide a mitigation strategy for each.
    ```
*   **Tips for Better Results**:
    *   Use this when you feel overwhelmed by a project task and don't know where to start.
*   **Example Use Case**:
    *   **Input**: "Deploy app to AWS EC2."
    *   **Output**: 
        *   Phase 1: AWS Console setup.
        *   Atomic Checklist: Create AWS account, set up VPC, launch EC2 micro instance, configure security groups (SSH access only).
        *   First 3 steps: 1. Log into AWS Console, 2. Click "Launch Instance", 3. Choose Ubuntu AMI.

---

### 5. Weighted Decision Matrix

*   **Purpose**: Evaluate complex options (e.g., frameworks, job offers, tools) mathematically using a weighted decision matrix.
*   **Prompt**:
    ```text
    You are a management consultant specializing in decision analysis.
    Build a Weighted Decision Matrix to evaluate the provided options.

    Options to Compare:
    [INSERT_OPTIONS] (e.g., Option A: React Native, Option B: Flutter)

    My Core Decision Criteria:
    [INSERT_CRITERIA] (e.g., Developer speed, performance, community size, ease of hiring)

    Guidelines:
    1. Define weights for each criterion on a scale of 1 to 5 (based on importance provided by user context).
    2. Score each option against every criterion on a scale of 1 to 10.
    3. Build a markdown table calculating the weighted score (Weight * Score) for each cell, and provide a total column.
    4. Provide a qualitative analysis summarizing the trade-offs and recommending the winning option.
    ```
*   **Tips for Better Results**:
    *   Clearly specify which criteria are non-negotiable (e.g., "cost must be under $100/month") to help the model weight the grid appropriately.
*   **Example Use Case**:
    *   **Input**: Options: AWS vs GCP. Criteria: serverless maturity, billing simplicity, prior team knowledge.
    *   **Output**: A calculated matrix table showing GCP winning on billing simplicity but AWS winning overall due to prior team expertise weights.

---

### 6. Transcript Action Item Extractor

*   **Purpose**: Process raw, messy transcript texts (from Zoom, Teams, Otter.ai) to extract structured summaries and action points.
*   **Prompt**:
    ```text
    You are an administrative director.
    Analyze the following raw meeting transcript and extract a clean, structured summary with action items.

    Raw Transcript:
    [INSERT_TRANSCRIPT]

    Provide:
    1. **Meeting Summary**: A 3-sentence high-level overview of what was discussed.
    2. **Key Decisions Made**: Bulleted list of formal decisions agreed upon during the call.
    3. **Structured Action Item Table**: Include columns for:
       - Task Description (Clear, action-oriented verb start)
       - Assignee (Who is responsible, based on context)
       - Deadline (If mentioned, otherwise "TBD")
    4. **Parking Lot / Open Questions**: Any items mentioned that were unresolved and need follow-up.
    ```
*   **Tips for Better Results**:
    *   Paste the transcript raw, even if it has spelling mistakes or lacks punctuation. Models are excellent at filtering spelling noises.
*   **Example Use Case**:
    *   **Input**: Chat transcript of 3 developers arguing about database replication and assigning backups to Sarah.
    *   **Output**: Table listing "Setup DB Replication" assigned to DB Admin by next Friday, and "Configure Backups" assigned to Sarah.

---

### 7. Atomic Habit Loop Builder

*   **Purpose**: Design sustainable habits using the habit loop framework (Cue, Craving, Response, Reward) from James Clear's *Atomic Habits*.
*   **Prompt**:
    ```text
    You are a behavioral psychologist specializing in habit formation.
    Design a habit loop plan to help me establish a new routine.

    Target Habit: [HABIT] (e.g., "Code daily for 1 hour", "Read research papers")
    My Current Schedule/Environment: [CONTEXT] (e.g., "Work from home, busy from 9-5, relaxed evenings")
    My Common Distractions: [DISTRACTIONS] (e.g., Phone notifications, video games)

    Please design a complete Habit Loop blueprint containing:
    1. **Cue (Make it Obvious)**: Design a specific trigger using "Habit Stacking" (e.g., "After I [existing habit], I will [new habit]").
    2. **Craving (Make it Attractive)**: Use temptation bundling (pairing something you need to do with something you want to do).
    3. **Response (Make it Easy)**: Apply the "2-Minute Rule" (how to start the habit in under 2 minutes).
    4. **Reward (Make it Satisfying)**: Create an immediate, positive feedback mechanism.
    5. **Friction Strategy**: How to increase friction for your listed distractions.
    ```
*   **Tips for Better Results**:
    *   Define a micro-habit (e.g., "open code editor") rather than a massive goal (e.g., "build an app") to make the response loop easily achievable.
*   **Example Use Case**:
    *   **Input**: Habit: Reading research papers. Context: Post-work evening slump.
    *   **Output**: Stack: "After I close my work laptop, I will read 1 page of a paper." Temptation: drink favorite tea while reading. Easy rule: keep paper PDF open on desktop.

---

### 8. SMART Goal Translator

*   **Purpose**: Translate vague, high-level career desires into structured, actionable SMART (Specific, Measurable, Achievable, Relevant, Time-bound) goals.
*   **Prompt**:
    ```text
    You are an executive coach.
    Translate my vague, high-level ambition into a concrete SMART goal framework and execution plan.

    My Ambition:
    [INSERT_AMBITION] (e.g., "I want to get better at AI algorithms", "I want to contribute to open-source")

    Your response must contain:
    1. **SMART Breakdown Table**:
       - **Specific**: Detail exactly what target you will achieve.
       - **Measurable**: What metric or proof defines success?
       - **Achievable**: How is this realistic given my background?
       - **Relevant**: Why does this goal matter to my long-term career?
       - **Time-bound**: What is the hard deadline?
    2. **Milestone Schedule**: Break the timeframe into 3 equal checkpoints.
    3. **Daily Habit**: What is the daily 15-minute action that feeds this goal?
    ```
*   **Tips for Better Results**:
    *   Be realistic about your available time. The model will design lighter metrics if it knows you only have 3 hours a week.
*   **Example Use Case**:
    *   **Input**: "I want to get good at Python."
    *   **Output**: SMART Goal: "Build and deploy 3 FastAPI mini-projects on GitHub with test suites (Specific/Measurable) in 60 days (Time-bound) spending 5 hours/week (Achievable) to prepare for backend job applications (Relevant)."

---

### 9. Standup Message Formatter

*   **Purpose**: Format raw, chaotic daily accomplishments into clean, professional status updates (Yesterday, Today, Blockers) for Slack or Teams.
*   **Prompt**:
    ```text
    You are a team scrum master. Help me format my messy thoughts into a clean, professional daily standup update.

    Raw Accomplishments/Draft Notes:
    [INSERT_RAW_NOTES] (e.g., "Fixed that stupid user button bug, set up some postgres table backups, sat in meetings all afternoon, still waiting on security keys from DevOps")

    Target Slack Tone: [e.g., Professional, friendly but concise, engineering-focused]

    Please format this into:
    1. **Yesterday**: Bullet points of tasks completed.
    2. **Today**: Bullet points of planned tasks.
    3. **Blockers**: Any active bottlenecks (written politely and constructively).
    4. **Slack Copy-Paste Version**: Styled with emojis and code blocks for quick posting.
    ```
*   **Tips for Better Results**:
    *   Emphasize blockers clearly so the Scrum Master can resolve them, but keep the description objective rather than blaming.
*   **Example Use Case**:
    *   **Input**: Messy list of bug fixes and complaining about DevOps delays.
    *   **Output**: Clean standup stating "Yesterday: Resolved UI button click event handler. Today: PostgreSQL backup automation config. Blockers: Pending DevOps access keys."

---

### 10. Pomodoro Sprint Planner

*   **Purpose**: Organize a major project task into structured, 25-minute Pomodoro sprints with clear sub-deliverables.
*   **Prompt**:
    ```text
    You are a focus coach. Help me structure my project task into 4 Pomodoro sprints (each 25 minutes of work followed by a 5-minute break).

    Target Project/Task:
    [INSERT_TASK] (e.g., "Write unit tests for authentication logic", "Clean up CSV data in Jupyter")

    Provide:
    1. **Sprint 1 (Focus & Prep)**: Goal for the first 25 minutes.
    2. **Sprint 2 (Core Build)**: Goal for the second 25 minutes.
    3. **Sprint 3 (Edge Cases/Refine)**: Goal for the third 25 minutes.
    4. **Sprint 4 (Verification/Documentation)**: Goal for the fourth 25 minutes.
    5. **Sprint Guidelines**: What to do during the 5-minute breaks (energy recovery) and how to manage interruptions.
    ```
*   **Tips for Better Results**:
    *   This is highly effective when paired with physical Pomodoro timers to structure your coding afternoons.
*   **Example Use Case**:
    *   **Input**: Clean up CSV data in Jupyter notebook.
    *   **Output**: Sprint 1: Import data, check null values, write basic statistics. Sprint 2: Impute columns, handle date formats. Sprint 3: Set up encoding. Sprint 4: Verify datatypes, export clean CSV.
