# AI-Prompt-Library

<p align="center">
  <svg width="800" height="220" viewBox="0 0 800 220" fill="none" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="grad" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" style="stop-color:#4158D0;stop-opacity:1" />
        <stop offset="46%" style="stop-color:#C850C0;stop-opacity:1" />
        <stop offset="100%" style="stop-color:#FFCC70;stop-opacity:1" />
      </linearGradient>
      <style>
        .title { font-family: 'Outfit', 'Inter', system-ui, sans-serif; font-weight: 800; font-size: 42px; fill: #ffffff; letter-spacing: 2px; }
        .subtitle { font-family: 'Inter', system-ui, sans-serif; font-weight: 400; font-size: 16px; fill: #f8f9fa; opacity: 0.95; }
        .version-badge { font-family: monospace; font-size: 12px; fill: #ffffff; opacity: 0.8; }
      </style>
    </defs>
    <!-- Card Background -->
    <rect width="800" height="220" rx="16" fill="url(#grad)"/>
    <!-- Glassmorphic overlays/shapes -->
    <circle cx="100" cy="180" r="80" fill="#ffffff" opacity="0.1"/>
    <circle cx="700" cy="40" r="60" fill="#ffffff" opacity="0.08"/>
    <!-- Text Elements -->
    <text x="50%" y="42%" dominant-baseline="middle" text-anchor="middle" class="title">AI-PROMPT-LIBRARY</text>
    <text x="50%" y="65%" dominant-baseline="middle" text-anchor="middle" class="subtitle">Production-Grade Prompts for Software Engineers, Researchers & AI/ML Students</text>
    <rect x="365" y="160" width="70" height="24" rx="12" fill="#ffffff" opacity="0.2"/>
    <text x="50%" y="176%" dominant-baseline="middle" text-anchor="middle" class="version-badge" y="172">v1.0.0</text>
  </svg>
</p>

<p align="center">
  <img src="https://img.shields.io/github/license/yashcodess/AI-Prompt-Library?style=for-the-badge&color=8A2387" alt="MIT License"/>
  <img src="https://img.shields.io/github/stars/yashcodess/AI-Prompt-Library?style=for-the-badge&color=E94057" alt="GitHub Stars"/>
  <img src="https://img.shields.io/github/issues/yashcodess/AI-Prompt-Library?style=for-the-badge&color=F27121" alt="GitHub Issues"/>
</p>

---

## 📖 Project Overview

Welcome to the **AI-Prompt-Library**, a collection of highly structured, production-grade AI prompts. Unlike generic, single-sentence prompts, this library focuses on **system-grade prompt engineering** techniques, including role-prompting, few-shot structures, output schema enforcement, and parameter injection.

This repository is designed for developers, data scientists, and students who want to unlock the full potential of large language models (such as GPT-4o, Claude 3.5 Sonnet, and Gemini 1.5 Pro) in their daily workflows.

---

## 🗂️ Table of Contents
* [Folder Navigation](#-folder-navigation)
* [Quick Start Guide](#🚀-quick-start-guide)
* [Prompt Engineering Best Practices](#💡-prompt-engineering-best-practices)
* [Contributing Guide](#🤝-contributing-guide)
* [Future Improvements](#🔮-future-improvements)
* [License](#📄-license)

---

## 📁 Folder Navigation

Click on a category to view its 10 dedicated, high-quality prompts complete with purposes, configurations, and realistic input/output examples.

| Category | Icon | Prompts Count | Target Focus Area |
| :--- | :---: | :---: | :--- |
| **[Coding](Coding/README.md)** | 💻 | 10 | Refactoring, Unit Testing, Debugging, SQL, Systems Architecture, and CI/CD. |
| **[AI & Machine Learning](AI_Machine_Learning/README.md)** | 🤖 | 10 | Feature Engineering, PyTorch Architectures, PEFT/QLoRA Tuning, RAG, and Evaluation. |
| **[Study & Learning](Study_and_Learning/README.md)** | 📚 | 10 | Feynman technique, Anki Flashcards, Socratic tutoring, and active recall. |
| **[Resume & Career](Resume_and_Career/README.md)** | 💼 | 10 | Google XYZ bullets, cover letters, mock interviews, salary negotiation, and STAR stories. |
| **[LinkedIn & Personal Branding](LinkedIn_and_Personal_Branding/README.md)** | 📱 | 10 | Engineering stories, launch updates, learning logs, and viral hooks. |
| **[Productivity](Productivity/README.md)** | ⚡ | 10 | Time-blocking, Eisenhower matrix, deconstructors, and standups. |
| **[Research](Research/README.md)** | 🔬 | 10 | Lit reviews, hypothesis planning, survey designs, and peer reviews. |
| **[Content Writing](Content_Writing/README.md)** | ✍️ | 10 | SEO articles, AIDA/PAS frameworks, newsletters, and scripts. |

---

## 🚀 Quick Start Guide

Using the prompts in this library is simple:

### Step 1: Browse and Select
Navigate to one of our 8 categories above and pick a prompt tailored to your task (e.g., [SQL Query Optimizer](Coding/README.md#8-sql-query-optimizer)).

### Step 2: Copy and Customize
Each prompt contains placeholders highlighted in uppercase brackets like `[INSERT_CODE_HERE]` or `[LANGUAGE]`. Copy the code block from the prompt:

```text
You are an expert polyglot software engineer. Translate the following code snippet...
Source Language: Python
Target Language: Rust
Source Code:
[INSERT_YOUR_CODE_HERE]
```

### Step 3: Run the Model
Paste the customized prompt into your target AI model (we recommend **Claude 3.5 Sonnet** for coding/reasoning, **GPT-4o** for general tasks, and **Gemini 1.5 Pro** for massive contexts).

---

## 💡 Prompt Engineering Best Practices

To get the most out of these prompts, keep these core principles in mind:

1.  **Assign a Role**: Always give the model a specific persona (e.g., "You are a Principal Cloud Architect"). This prompts the model to adopt the correct jargon and rigor.
2.  **Separate Context**: Use XML tags or markdown blockquotes to clearly separate instructions from user-provided data inputs.
3.  **Specify the Output Format**: Clearly define whether you expect JSON, a Markdown table, code blocks, or hidden elements.
4.  **Control Temperature**:
    *   Set **Low Temperature (0.0 - 0.3)** for coding, math, refactoring, and database queries.
    *   Set **High Temperature (0.7 - 1.0)** for brainstorms, copywriting, and personal branding hooks.

---

## 🤝 Contributing Guide

We welcome contributions to expand the library! To maintain our premium standard, please follow these guidelines:

1.  **Format Consistency**: All new prompts must use our standard template:
    *   **Title**
    *   **Purpose**
    *   **Prompt** (using a clean copyable code block)
    *   **Tips for Better Results**
    *   **Example Use Case** (Input & Output blocks)
2.  **No Placeholders**: Do not include unfinished sections or `TODO` tags in prompts.
3.  **Submit a Pull Request**:
    *   Fork the repository.
    *   Create a branch (`git checkout -b feat/new-prompt`).
    *   Commit your changes (`git commit -m "feat(category): add custom prompt for X"`).
    *   Push and open a Pull Request.

---

## 🔮 Future Improvements
*   [ ] Integrate a web-based prompt copy utility for one-click clipboards.
*   [ ] Add screenshots and visual UI mockups to the `assets/` directory.
*   [ ] Create automated prompt verification tests to check placeholders.
*   [ ] Expand categories to include Product Management and Data Analytics.

---

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.
