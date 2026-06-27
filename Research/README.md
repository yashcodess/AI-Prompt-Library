# 🔬 Research & Academic Prompts

A curated collection of academic-grade prompts designed to assist researchers, students, and analysts in literature mapping, hypothesis formulation, experimental design, credibility analysis, and peer review simulation.

## Table of Contents
* [1. Literature Review Strategy](#1-literature-review-strategy)
* [2. Scientific Hypothesis Planner](#2-scientific-hypothesis-planner)
* [3. Methodology Selection Guide](#3-methodology-selection-guide)
* [4. Academic Abstract Outline](#4-academic-abstract-outline)
* [5. Source Credibility Checker](#5-source-credibility-checker)
* [6. Competitor & Prior Art Analysis](#6-competitor--prior-art-analysis)
* [7. Unbiased Survey Questionnaire](#7-unbiased-survey-questionnaire)
* [8. Research Question Refiner](#8-research-question-refiner)
* [9. Statistical Test Selector](#9-statistical-test-selector)
* [10. Peer Review Simulator](#10-peer-review-simulator)

---

### 1. Literature Review Strategy

*   **Purpose**: Design a comprehensive strategy to map existing academic literature, formulating query terms and classification criteria for databases.
*   **Prompt**:
    ```text
    You are an Academic Librarian and Research Lead.
    Design a literature review strategy for the following research topic.

    Research Topic: [RESEARCH_TOPIC] (e.g., "The impact of microplastics on agricultural soil microbiome")
    Target Databases: [DATABASES] (e.g., Google Scholar, PubMed, IEEE Xplore)

    Please output:
    1. **Search Query Matrix**: A table listing search strings using Boolean operators (AND, OR, NOT) and wildcards tailored to various databases.
    2. **Inclusion & Exclusion Criteria**: Define strict parameters (e.g., publication date ranges, language constraints, research type) to filter irrelevant articles.
    3. **Key Authors & Core Journals**: List top journals and leading research groups/authors in this field to track.
    4. **Classification Taxonomy**: Suggest 4 key themes/tags to categorize the papers during the review phase.
    ```
*   **Tips for Better Results**:
    *   Works best when you provide 2-3 baseline papers that you already know are relevant, so the model can analyze their keywords.
*   **Example Use Case**:
    *   **Input**: "Graph neural networks for drug discovery."
    *   **Output**: Query string `("graph neural network" OR "GNN") AND ("drug discovery" OR "molecular property prediction")`, plus journals like *Bioinformatics* and *Journal of Chemical Information and Modeling*.

---

### 2. Scientific Hypothesis Planner

*   **Purpose**: Formulate testable scientific hypotheses and outline control-group experimental designs to validate them.
*   **Prompt**:
    ```text
    You are a Scientific Researcher. Help me translate a general scientific observation into a testable hypothesis and design a validating experiment.

    Observation/Research Question: [INSERT_OBSERVATION] (e.g., "AI assistants seem to make developers write buggy code but finish faster.")

    Provide:
    1. **Hypothesis Formulation**:
       - Null Hypothesis ($H_0$): Formal statement of no effect.
       - Alternative Hypothesis ($H_1$): Testable, directional statement of effect.
    2. **Variable Definitions**: Identify the Independent Variable, Dependent Variable, and key Control Variables.
    3. **Experimental Setup**: Outline the control group vs experimental group, participant criteria, and testing protocol.
    4. **Data Metrics**: What specific metrics will be measured, and how will they be collected?
    ```
*   **Tips for Better Results**:
    *   Be specific about sample size constraints or budget limitations so the model suggests feasible experimental frameworks.
*   **Example Use Case**:
    *   **Input**: "Using dark mode on code editors might reduce eye strain."
    *   **Output**: $H_0$ (No difference in eye strain), $H_1$ (Dark mode reduces eye strain compared to light mode), Independent (editor theme), Dependent (eye fatigue scale survey), Control (ambient lighting, screen brightness).

---

### 3. Methodology Selection Guide

*   **Purpose**: Evaluate and recommend qualitative or quantitative research methodologies based on study goals.
*   **Prompt**:
    ```text
    You are a Research Methodology Consultant.
    Suggest the optimal research methodology and justify the choices for my study.

    Research Question: [RESEARCH_QUESTION]
    Target Population: [POPULATION] (e.g., "Junior software developers working remotely")
    Expected Constraints: [CONSTRAINTS] (e.g., "No budget, 30 days total timeline")

    Provide:
    1. **Methodology Recommendation**: (e.g., Mixed-methods, Survey, Grounded Theory Case Study).
    2. **Data Collection Plan**: Detail how data will be gathered (e.g., semi-structured interviews, online forms, system logs).
    3. **Data Analysis Strategy**: How to analyze the gathered data (e.g., thematic analysis for text, ANOVA for numeric metrics).
    4. **Methodological Trade-offs**: Explain the limitations of this choice (e.g., lower generalizability but deeper qualitative insight).
    ```
*   **Tips for Better Results**:
    *   Indicate whether your target audience is difficult to reach (e.g., C-level executives) to get customized recruiting strategies.
*   **Example Use Case**:
    *   **Input**: Study on how remote developers manage focus time.
    *   **Output**: Recommends a mixed-methods design (quantitative surveys for scale and qualitative follow-up interviews for depth), explaining thematic code analysis steps.

---

### 4. Academic Abstract Outline

*   **Purpose**: Structure and write a concise, impactful abstract for research papers or conference presentations.
*   **Prompt**:
    ```text
    You are a Senior Editor for a prestigious scientific journal.
    Write a structured academic abstract based on my raw research findings.

    Background Context: [CONTEXT]
    Methodology: [METHODS]
    Key Results: [RESULTS]
    Primary Conclusion/Impact: [CONCLUSION]

    Requirements:
    1. Maximum 250 words.
    2. Follow the standard structured flow: Background -> Problem Statement -> Methods -> Findings -> Conclusion.
    3. Keep the language objective, precise, and active (e.g., use "We present" instead of "It is presented").
    4. Provide 5 index keywords for indexing services.
    ```
*   **Tips for Better Results**:
    *   Make sure to include specific numbers and statistical results (e.g., "improved precision by 14%") to make the abstract compelling.
*   **Example Use Case**:
    *   **Input**: Research on a new CNN model diagnosing tree diseases from aerial drone pictures.
    *   **Output**: Structured abstract summarizing the CNN architecture, drone dataset size (12k images), classification accuracy (94.2%), and environmental management impacts.

---

### 5. Source Credibility Checker

*   **Purpose**: Evaluate the reliability, impact, citations, and potential bias of academic references or sources.
*   **Prompt**:
    ```text
    You are a Peer Reviewer and Fact-Checker.
    Evaluate the credibility of the provided source context.

    Source Citation / Abstract:
    [INSERT_SOURCE_DETAILS]

    Please evaluate and output:
    1. **Credibility Score Indicators**:
       - Publisher Reputation (Is it peer-reviewed, preprint, or predatory journal?)
       - Citation Count & Impact context (If known, or general research footprint)
    2. **Methodological Validity**: Spot any potential flaws in the study (e.g., small sample sizes, lack of control group, conflict of interest/funding).
    3. **Bias & Tone Check**: Analyze whether the author uses neutral, objective terminology or displays emotional/commercial bias.
    4. **Reliability Recommendation**: Should this source be cited as a primary foundation, secondary support, or discarded?
    ```
*   **Tips for Better Results**:
    *   Paste the bibliography details including the journal title and DOI if available, as the model can evaluate the reputation of major publishers.
*   **Example Use Case**:
    *   **Input**: Abstract of a study claiming a new herbal supplement cures ADHD, published in an unindexed open-access journal.
    *   **Output**: Flags critical methodological flaws (no blind testing, tiny cohort size $N=12$), notes commercial publisher bias, recommends discarding as a primary source.

---

### 6. Competitor & Prior Art Analysis

*   **Purpose**: Structure a systematic comparison of existing tools, research papers, patents, or prior art.
*   **Prompt**:
    ```text
    You are a Patent Attorney and Innovation Analyst.
    Perform a Prior Art and Competitor Analysis for the following product or research idea.

    My Innovation Idea:
    [DESCRIBE_YOUR_IDEA]

    Known Competitors / Existing Solutions:
    [INSERT_KNOWN_SOLUTIONS]

    Provide:
    1. **Feature Comparison Matrix**: A detailed markdown table comparing your idea against competitors across 5 metrics (e.g., scalability, cost, accuracy).
    2. **Novelty Check**: What specific technical differentiation or claims make your idea novel compared to the prior art?
    3. **Patent Obstacles**: Potential infringement risks or similarity flags.
    4. **Development Recommendations**: How to refine the design to increase its patentability or uniqueness.
    ```
*   **Tips for Better Results**:
    *   Detail the "secret sauce" of your design (e.g., custom database indexing mechanism) to get a targeted novelty audit.
*   **Example Use Case**:
    *   **Input**: A lightweight browser extension summarizing YouTube tutorials using local LLMs.
    *   **Output**: Highlights similarity to general summarizers, but identifies local processing without server APIs as the core novelty claim.

---

### 7. Unbiased Survey Questionnaire

*   **Purpose**: Write clear, non-leading survey questions to collect reliable quantitative or qualitative study data.
*   **Prompt**:
    ```text
    You are a Survey Design Expert and Psychometrician.
    Design a survey questionnaire to collect data on the following topic.

    Survey Goal: [GOAL] (e.g., "Measure developer burnout in remote startup companies")
    Target Respondents: [RESPONDENTS] (e.g., "Software engineers with <3 years experience")

    Your design must include:
    1. **Demographic Questions**: Short, standardized options (e.g., years of experience, team size).
    2. **Likert Scale Questions (Quantitative)**: 5 balanced, non-leading questions using a 5-point Likert scale (Strongly Disagree to Strongly Agree).
    3. **Open-Ended Questions (Qualitative)**: 2 deep, reflective questions.
    4. **Bias Guard Checklist**: Explain how your questions avoid specific biases (e.g., Acquiescence Bias, Double-barreled questions, Social Desirability Bias).
    ```
*   **Tips for Better Results**:
    *   Explicitly specify what platform you plan to host the survey on (e.g., Google Forms, Qualtrics) so formatting can be tailored.
*   **Example Use Case**:
    *   **Input**: Surveying student attitudes towards using AI coding assistants in exams.
    *   **Output**: Likert queries ("Using AI during homework helps me learn core syntax"), open-ended queries, and explanations of how we avoided framing AI as "cheating" in the questions to prevent social bias.

---

### 8. Research Question Refiner

*   **Purpose**: Narrow down broad, vague research topics into precise, testable, and academic-grade research questions.
*   **Prompt**:
    ```text
    You are a Director of Graduate Studies. Help me refine my broad research interest into 3 specific, academic-grade research questions.

    My Broad Interest:
    [INSERT_BROAD_INTEREST] (e.g., "I want to study AI bias")

    Academic Discipline: [DISCIPLINE] (e.g., Computer Science, Sociology, Law)

    For each of the 3 refined options, provide:
    1. **Refined Research Question**: A clear, single-sentence question.
    2. **Feasibility Check**: How this question can be answered (suggested datasets, experiments).
    3. **Academic Significance**: Why this question matters to the scientific community.
    4. **Potential Methodology**: Which mathematical or analytical models would be required to study it.
    ```
*   **Tips for Better Results**:
    *   Provide details on your access to special datasets or APIs, as the model will design more feasible questions.
*   **Example Use Case**:
    *   **Input**: Broad interest: "Why do programmers write bad code?"
    *   **Output**: Specific question: "How does the frequency of context-switching in remote developers correlate with the density of syntax errors in commits?" Suggests git log analysis methodology.

---

### 9. Statistical Test Selector

*   **Purpose**: Recommend the correct statistical models and tests (ANOVA, t-test, Chi-Square) based on data formats and assumptions.
*   **Prompt**:
    ```text
    You are a Biostatistician and Data Analyst.
    Recommend the appropriate statistical test to analyze my experimental results.

    My Research Goal: [GOAL] (e.g., "See if developers using tool X are faster than tool Y")
    Independent Variable (IV) & Scale: [IV_DETAILS] (e.g., "Tool Type: Categorical - Group A vs Group B")
    Dependent Variable (DV) & Scale: [DV_DETAILS] (e.g., "Completion time: Continuous - minutes")
    Data Distribution (if known): [e.g., Normal distribution, heavily skewed, unknown]

    Provide:
    1. **Recommended Test**: The name of the primary statistical test (e.g., Two-sample t-test, Mann-Whitney U test, Chi-square).
    2. **Underlying Assumptions**: List of mathematical assumptions that *must* be true for this test to be valid (e.g., homoscedasticity, normality).
    3. **Python Code**: A Python script using `scipy.stats` to load sample data, run validation tests (e.g., Shapiro-Wilk for normality), and execute the main statistical test.
    4. **How to Interpret Results**: A brief guide on how to read the $p$-value and effect size.
    ```
*   **Tips for Better Results**:
    *   If your dataset contains multiple independent variables, indicate this, as it requires moving from a t-test to ANOVA or regression modeling.
*   **Example Use Case**:
    *   **Input**: Comparing execution speeds of 3 different database setups (PostgreSQL, MySQL, SQLite) on identical queries.
    *   **Output**: Recommends One-way ANOVA (if normal) or Kruskal-Wallis test (non-parametric), with python script testing normality.

---

### 10. Peer Review Simulator

*   **Purpose**: Act as a constructive academic peer reviewer to audit draft research papers for weaknesses, structure, and readability.
*   **Prompt**:
    ```text
    You are a Peer Reviewer for a top academic journal.
    Evaluate the provided draft excerpt of a research paper and write a constructive reviewer report.

    Draft Paper Section:
    [INSERT_DRAFT_TEXT]

    Please structure your reviewer report into:
    1. **Summary of the Paper**: A brief summary of the paper's contribution as you understand it.
    2. **Major Concerns**: Critical issues (e.g., flawed assumptions, missing controls, logical leaps, unsupported claims).
    3. **Minor Concerns**: Stylistic errors, grammatical suggestions, citation omissions, or table formatting issues.
    4. **Recommendation**: (Accept, Minor Revision, Major Revision, or Reject) with a clear summary justification.
    ```
*   **Tips for Better Results**:
    *   Paste your "Introduction" or "Discussion" sections, as these are the most critical sections where logical flow is evaluated.
*   **Example Use Case**:
    *   **Input**: Draft introduction claiming machine learning makes database indexing perfect, without citing classical B-Tree literature.
    *   **Output**: Reviewer report noting major concern about lack of comparison to standard B-Tree indexing benchmarks, suggesting Major Revision.
