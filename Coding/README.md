# 💻 Coding & Development Prompts

A curated collection of advanced, professional prompts designed to accelerate software engineering, system design, code quality, and security auditing.

## Table of Contents
* [1. Code Refactoring & Clean Code](#1-code-refactoring--clean-code)
* [2. Unit Test Generator](#2-unit-test-generator)
* [3. Debugging Companion](#3-debugging-companion)
* [4. Algorithm Optimizer](#4-algorithm-optimizer)
* [5. System Design Architect](#5-system-design-architect)
* [6. API Design & Documentation](#6-api-design--documentation)
* [7. Code Translation](#7-code-translation)
* [8. SQL Query Optimizer](#8-sql-query-optimizer)
* [9. Dockerfile & CI/CD Pipeline Creator](#9-dockerfile--cicd-pipeline-creator)
* [10. Security Vulnerability Auditor](#10-security-vulnerability-auditor)

---

### 1. Code Refactoring & Clean Code

*   **Purpose**: Refactor messy, legacy, or suboptimal code to adhere to clean code principles, DRY, and SOLID design patterns.
*   **Prompt**:
    ```text
    You are an expert staff software engineer specializing in software craftsmanship and clean code.
    Your task is to refactor the provided code snippet to improve readability, maintainability, and extensibility.

    Ensure that your refactoring strictly follows:
    1. SOLID Principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion)
    2. DRY (Don't Repeat Yourself) & KISS (Keep It Simple, Stupid)
    3. Proper naming conventions (descriptive, clear variable/function names)
    4. Proper error handling and edge-case management

    Input Code Language: [LANGUAGE]
    Input Code:
    [INSERT_CODE_HERE]

    Please structure your output as follows:
    1. **Code Analysis**: A brief explanation of code smells, architectural weaknesses, or performance bottlenecks in the original code.
    2. **Refactored Code**: The clean, refactored code enclosed in a markdown code block.
    3. **Design Decisions**: A list explaining why you made specific changes (e.g., extracting classes, moving logic, using a design pattern).
    ```
*   **Tips for Better Results**:
    *   Works best with models like GPT-4o, Claude 3.5 Sonnet, or Gemini 1.5 Pro.
    *   Provide the context of the surrounding application if the snippet interacts with other classes.
*   **Example Use Case**:
    *   **Input**: A 50-line JavaScript function handling user checkout, db saving, and email alerts all in one block.
    *   **Output**: 
        *   Analysis: Identifies violation of SRP (Single Responsibility Principle) and lack of error handling.
        *   Refactored Code: Splitted into `CheckoutService`, `DatabaseGateway`, and `NotificationService`.
        *   Design Decisions: Explains dependency injection and how modular components can be unit-tested.

---

### 2. Unit Test Generator

*   **Purpose**: Generate comprehensive unit tests covering happy paths, edge cases, error conditions, and boundary values.
*   **Prompt**:
    ```text
    You are a meticulous QA Engineer and Developer. Your goal is to write a suite of unit tests for the following code snippet.

    Target Language/Framework: [FRAMEWORK_AND_LANGUAGE] (e.g., Python Pytest, JavaScript Jest, Java JUnit)
    Code to Test:
    [INSERT_CODE_HERE]

    Requirements:
    1. Include test cases for:
       - Happy path (normal input/expected output)
       - Boundary values (min, max, null, empty array/string)
       - Error handling (verifying correct exceptions are raised for invalid inputs)
       - Performance/stress boundaries (if applicable)
    2. Structure tests logically with setup/teardown if required.
    3. Use mock databases/APIs where necessary.
    4. Provide clear assertions with descriptive failure messages.

    Output format:
    1. **Testing Strategy**: Short list of testing goals and edge cases addressed.
    2. **Test Suite Code**: Complete, copy-pasteable test file.
    ```
*   **Tips for Better Results**:
    *   If using mocks, specify which library (e.g., `unittest.mock`, `jest.mock`) you prefer.
    *   For languages with type safety (TypeScript, Go, Rust), ensure the test code compiles by matching exact signatures.
*   **Example Use Case**:
    *   **Input**: A Python function calculating compound interest with boundary parameters.
    *   **Output**: A suite of `pytest` test cases checking negative rates, zero compounding periods, and typical floating-point assertions.

---

### 3. Debugging Companion

*   **Purpose**: Analyze stack traces, error messages, and buggy source code to diagnose logical and technical errors.
*   **Prompt**:
    ```text
    You are an expert debugger and system diagnostician. Analyze the following bug report, code snippet, and stack trace to identify the root cause and provide a robust fix.

    Language/Runtime Environment: [ENVIRONMENT] (e.g., Node.js v18, Python 3.10, Docker Alpine)
    Source Code:
    [INSERT_CODE_HERE]

    Stack Trace / Error Message:
    [INSERT_STACK_TRACE_HERE]

    Context/Expected Behavior:
    [INSERT_EXPECTED_BEHAVIOR]

    Please respond with:
    1. **Root Cause Analysis (RCA)**: Explain why this error occurred, references to memory models, async behavior, or type coercion.
    2. **The Fix**: Provide the modified, corrected code.
    3. **Prevention Advice**: How to prevent this bug in the future (e.g., typescript compiler flags, linting rules, or defensive coding techniques).
    ```
*   **Tips for Better Results**:
    *   Always paste the raw, unedited stack trace.
    *   Specify the state of variables at the time of execution if known.
*   **Example Use Case**:
    *   **Input**: Node.js `TypeError: Cannot read properties of undefined (reading 'map')` stack trace and an async data-fetching function.
    *   **Output**: RCA highlighting missing API response checking, followed by a robust optional chaining and fallback assignment implementation.

---

### 4. Algorithm Optimizer

*   **Purpose**: Optimize algorithms for better time ($O$) and space complexity while maintaining correctness.
*   **Prompt**:
    ```text
    You are a competitive programmer and performance tuning engineer.
    Analyze the following code snippet and optimize it for execution speed and memory consumption.

    Target Language: [LANGUAGE]
    Original Code:
    [INSERT_CODE_HERE]

    Analyze the original code's Big-O complexity (Time and Space) and refactor the code to achieve optimal performance.

    Output Format:
    1. **Complexity Analysis**:
       - Original Time Complexity: [Big-O]
       - Original Space Complexity: [Big-O]
       - Optimized Time Complexity: [Big-O]
       - Optimized Space Complexity: [Big-O]
    2. **Optimization Strategy**: Describe the data structures or mathematical optimizations used (e.g., HashMaps, Memoization, Bit manipulation, Two pointers).
    3. **Optimized Code**: The refined code block.
    4. **Safety & Correctness**: Highlight any assumptions (e.g., inputs are sorted) required for this optimization to hold true.
    ```
*   **Tips for Better Results**:
    *   Specify constraints such as "input array length $N \le 10^7$" to guide the model towards the correct asymptotic threshold.
*   **Example Use Case**:
    *   **Input**: A nested-loop array duplicate checker ($O(N^2)$).
    *   **Output**: An optimized set-based solution ($O(N)$ time, $O(N)$ space) with a step-by-step breakdown.

---

### 5. System Design Architect

*   **Purpose**: Design robust, scalable, and secure system architectures, databases, and microservices.
*   **Prompt**:
    ```text
    You are a Principal Cloud Architect. Design a production-grade system architecture for the following system requirement.

    System Requirements:
    [DESCRIBE_SYSTEM_REQUIREMENTS] (e.g., "A real-time ride-sharing matches engine serving 10,000 requests per second.")

    Scale Constraints:
    - Daily Active Users: [DAU]
    - Read/Write Ratio: [READ_WRITE_RATIO]
    - Target SLA: [SLA_TARGET] (e.g., 99.99% availability, <100ms latency)

    Please output a comprehensive architectural proposal containing:
    1. **High-Level Architecture**: Describe the components (CDN, load balancer, API gateways, microservices, cache layers).
    2. **Data Model & Storage Strategy**:
       - Relational vs NoSQL database selection.
       - Database schema design (primary/foreign keys, indexes, partitioning keys).
       - Caching strategy (Redis/Memcached eviction, TTL strategies).
    3. **Scalability & Resiliency Plan**: How the system handles traffic spikes, failovers, partitioning, and service discovery.
    4. **Tech Stack Recommendations**: Suggest specific technologies (e.g., Kubernetes, Kafka, PostgreSQL, DynamoDB) with justifications.
    ```
*   **Tips for Better Results**:
    *   State your cloud provider preference (AWS, GCP, Azure) to get tailor-made managed service suggestions.
*   **Example Use Case**:
    *   **Input**: A system design for a collaborative document editor like Google Docs.
    *   **Output**: Detailed design proposing Operational Transformation (OT) or CRDTs, WebSocket servers, Redis Pub/Sub, and document sharding mechanisms.

---

### 6. API Design & Documentation

*   **Purpose**: Write clean, standard-compliant REST/GraphQL APIs and generate OpenAPI/Swagger documentation.
*   **Prompt**:
    ```text
    You are a senior backend developer and API designer.
    Design a clean, RESTful API interface for managing the following resource entity.

    Resource/Entity Name: [RESOURCE_NAME] (e.g., "E-Commerce Shopping Cart")
    Supported Actions: [ACTIONS_LIST] (e.g., Create cart, add items, apply discount, checkout)

    Your design must output:
    1. **HTTP Routes Table**: Include HTTP Method, URL Path, Query Params, Request Headers, Status Codes (200, 201, 400, 401, 404, 500).
    2. **JSON Schemas**: Request Body and Response Body payload structures for each endpoint.
    3. **OpenAPI 3.0 Specification**: Provide the complete API design in YAML OpenAPI 3.0 format.
    4. **Best Practices Checklist**: Implementation guidelines (rate-limiting headers, idempotency keys for mutate calls).
    ```
*   **Tips for Better Results**:
    *   Mention specific validation requirements (e.g., `email` field must match regex) so the model adds them to the OpenAPI specs.
*   **Example Use Case**:
    *   **Input**: API for an airline seat reservation system.
    *   **Output**: Restful paths `/flights/{id}/seats` with Swagger YAML, error payloads, and optimistic locking header specifications.

---

### 7. Code Translation

*   **Purpose**: Translate source code from one programming language to another while preserving idioms and performance.
*   **Prompt**:
    ```text
    You are an expert polyglot software engineer. Translate the following code snippet from the source language to the target language, adopting the idiomatic conventions of the target language.

    Source Language: [SOURCE_LANG]
    Target Language: [TARGET_LANG]
    Source Code:
    [INSERT_CODE_HERE]

    Requirements:
    1. Write code that is native to the target language (e.g., use Go routines for concurrency in Go, async/await in JS, list comprehensions in Python).
    2. Retain all performance traits and logical accuracy of the original algorithm.
    3. Map type systems accurately (e.g., translate JavaScript dynamic objects to TypeScript interfaces or Rust Structs).
    4. Include instructions for installing dependencies or building the translated code.

    Output format:
    1. **Translated Code**: Complete source code in the target language.
    2. **Idiomatic Adaptations**: Explain how you restructured code features (like loops, exceptions, threads) to fit target language idioms.
    ```
*   **Tips for Better Results**:
    *   Specify if you want the translation to use specific target language standard library packages or third-party libraries.
*   **Example Use Case**:
    *   **Input**: A Python data processing script using Pandas, translating to Rust using `polars`.
    *   **Output**: Optimized Rust translation with error handling and explanation of memory ownership.

---

### 8. SQL Query Optimizer

*   **Purpose**: Optimize slow SQL queries, database indexing, and execution paths.
*   **Prompt**:
    ```text
    You are a Database Administrator (DBA) and SQL Optimization expert.
    Analyze the following SQL query and database schema to suggest performance optimizations.

    Database Engine: [DB_ENGINE] (e.g., PostgreSQL, MySQL, MS SQL Server)
    Database Schema:
    [INSERT_SCHEMA_HERE]

    Slow SQL Query:
    [INSERT_QUERY_HERE]

    Target Execution constraint: [e.g., "Must execute in <50ms with 10,000,000 rows"]

    Provide a diagnostic report detailing:
    1. **Performance Bottlenecks**: Explain issues like index scans vs table scans, temporary table generation, subquery overhead, or missing indexes.
    2. **Optimized Query**: The rewritten SQL query.
    3. **DDL Modifications**: DDL statements for creating indexes (indexes, composite indexes, partial indexes) or schema adjustments (denormalization, partitioning).
    4. **EXPLAIN Plan Checklist**: What key indicators (e.g., `Seq Scan`, `Nested Loop`, `Filesort`) should the developer look for in their execution plan.
    ```
*   **Tips for Better Results**:
    *   Provide estimates of table sizes (e.g., Table A has 5 million rows, Table B has 100 rows) so the model suggests appropriate join indexes.
*   **Example Use Case**:
    *   **Input**: A PostgreSQL query with multiple nested joins and `LIKE` filters.
    *   **Output**: Optimized query replacing subqueries with CTEs/Window functions, index definitions, and recommendations for pg_trgm GIN indexing.

---

### 9. Dockerfile & CI/CD Pipeline Creator

*   **Purpose**: Design secure, lightweight container images and fast CI/CD pipelines.
*   **Prompt**:
    ```text
    You are a DevOps and DevSecOps Architect. Your goal is to write an optimized, multi-stage Dockerfile and a corresponding CI/CD pipeline configuration file for the following application.

    Tech Stack: [STACK_DETAIL] (e.g., Node.js with Next.js, Python with FastAPI)
    CI/CD Platform: [PLATFORM] (e.g., GitHub Actions, GitLab CI, CircleCI)
    Target Environment: [ENVIRONMENT] (e.g., AWS ECS, Kubernetes, Vercel)

    Requirements:
    1. **Dockerfile**:
       - Multi-stage build to separate build dependencies from runtime assets.
       - Use specific, lightweight base images (e.g., `alpine`, `slim`).
       - Set appropriate permissions (do not run as root user).
       - Cache packages efficiently (layer cache optimization).
    2. **CI/CD Configuration**:
       - Set up build, test, lint, security vulnerability scan (e.g., Trivy/Snyk), and deployment steps.
       - Implement caching for dependencies/docker layers to minimize run time.

    Output format:
    1. **Dockerfile**: Copy-pasteable docker file.
    2. **CI/CD Config**: YAML configuration for the target runner.
    3. **Design Decisions**: Explanation of security choices and build-time optimization details.
    ```
*   **Tips for Better Results**:
    *   Provide the package management files (e.g., `package.json`, `requirements.txt`, `Cargo.toml`) for precise dependency caching setup.
*   **Example Use Case**:
    *   **Input**: A React SPA built with Vite needing a GitHub Actions workflow that deploys to AWS S3.
    *   **Output**: Multi-stage Dockerfile serving assets via Nginx alpine, and GitHub Actions workflow with caching, ESLint, and AWS CLI sync.

---

### 10. Security Vulnerability Auditor

*   **Purpose**: Audit source code for potential security vulnerabilities, logic flaws, and credential leaks.
*   **Prompt**:
    ```text
    You are an expert Security Engineer and Pen-Tester.
    Audit the following code snippet for security vulnerabilities, compliance issues, and OWASP Top 10 risks.

    Language/Framework: [LANGUAGE/FRAMEWORK]
    Source Code:
    [INSERT_CODE_HERE]

    Generate a Security Audit Report covering:
    1. **Vulnerability Summary Table**: List of vulnerabilities, their CWE/OWASP mapping, severity (Critical/High/Medium/Low), and status.
    2. **Vulnerability Analysis**: For each finding, explain:
       - The exploit vector (how an attacker would abuse this code).
       - Impact (RCE, SQL Injection, XSS, PrivEsc, Data Leak).
    3. **Remediation**:
       - Code fix showing secure implementation.
       - Best practices (e.g., input sanitization, output encoding, security headers).
    ```
*   **Tips for Better Results**:
    *   Prompt the auditor with the context of how input data enters the system (e.g., URL parameters, database inputs, third-party hooks).
*   **Example Use Case**:
    *   **Input**: A Python flask endpoint processing database queries using raw SQL string formatting.
    *   **Output**: Identifies SQL Injection (CWE-89), explains how `admin' --` exploits the database, provides parameterized cursor execution fix.
