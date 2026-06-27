# 🤖 AI & Machine Learning Prompts

A curated collection of production-grade prompts designed to aid data scientists, machine learning engineers, and prompt engineers in dataset engineering, model design, hyperparameter tuning, RAG systems, and LLM deployments.

## Table of Contents
* [1. Dataset Feature Engineering](#1-dataset-feature-engineering)
* [2. Model Architecture Designer](#2-model-architecture-designer)
* [3. Hyperparameter Tuning Strategy](#3-hyperparameter-tuning-strategy)
* [4. Prompt Engineering Optimizer](#4-prompt-engineering-optimizer)
* [5. RAG System Designer](#5-rag-system-designer)
* [6. Model Quantization Guide](#6-model-quantization-guide)
* [7. Ethics & Bias Auditor](#7-ethics-bias-auditor)
* [8. Transfer Learning Guide](#8-transfer-learning-guide)
* [9. LLM Fine-Tuning Recipe](#9-llm-fine-tuning-recipe)
* [10. LLM Evaluation Designer](#10-llm-evaluation-designer)

---

### 1. Dataset Feature Engineering

*   **Purpose**: Design feature extraction, transformation, and selection pipelines for complex, raw tabular, text, or time-series datasets.
*   **Prompt**:
    ```text
    You are an expert Data Scientist and Feature Engineer.
    Analyze the following dataset metadata, schema, and predictive goal, and design a comprehensive feature engineering pipeline.

    Dataset Name: [DATASET_NAME]
    Target Variable: [TARGET_VARIABLE]
    Machine Learning Task: [ML_TASK] (e.g., Binary Classification, Regression, Time-series Forecasting)
    Raw Data Columns & Types:
    [INSERT_COLUMNS_AND_TYPES]

    Your output should include:
    1. **Data Cleaning & Preprocessing**: Handling of missing values, outliers, and highly skewed distributions for specific columns.
    2. **Feature Transformations**:
       - Encoding techniques for categorical features (Target Encoding, One-Hot, Ordinal).
       - Scaling methods (Standardization, Robust Scaling).
    3. **Feature Creation**: Deriving new features (interaction terms, date-time decompositions, rolling window aggregations, text embeddings).
    4. **Feature Selection**: Dimensionality reduction (PCA, t-SNE) or feature importance techniques (SHAP, Mutual Info, LASSO) to prevent overfitting.
    5. **Python Pipeline Code**: Complete code block using `scikit-learn` Pipelines or `pandas` to implement the recommendations.
    ```
*   **Tips for Better Results**:
    *   Providing raw statistics of columns (mean, min, max, missing percentage) will lead to highly targeted transformations.
    *   Highlight any domain-specific details (e.g., transactional data, medical records).
*   **Example Use Case**:
    *   **Input**: E-commerce customer churn dataset schema containing transaction dates, payment types, and purchase amounts.
    *   **Output**: 
        *   Transforms transaction dates into "days since last purchase" and "purchase frequency".
        *   Handles missing values via median imputation for continuous and mode for categorical.
        *   Outputs a Scikit-Learn `ColumnTransformer` pipeline.

---

### 2. Model Architecture Designer

*   **Purpose**: Design custom deep learning neural network architectures in PyTorch or TensorFlow for specialized tasks.
*   **Prompt**:
    ```text
    You are a Deep Learning Research Scientist. Design a neural network architecture tailored to the specified problem constraints and inputs.

    Input Data Modality: [MODALITY] (e.g., 3-channel Images 226x226, Variable-length Text, Multichannel Time-series)
    Target Objective: [OBJECTIVE] (e.g., Multi-label Classification, Image Segmentation, Sequence-to-Sequence translation)
    Framework Preference: [PyTorch / TensorFlow]
    Computational Constraints: [e.g., "Must run on Edge GPU with <20M parameters"]

    Please design the architecture and provide:
    1. **Structural Diagram/Specification**: Layer-by-layer details (convolution kernels, stride, padding, attention heads, dropout rates, activation functions).
    2. **Mathematical Foundations**: Explain the choice of activation functions, normalization layers (Batch Norm, Layer Norm), and pooling mechanisms.
    3. **Implementation Code**: Fully functional PyTorch or TensorFlow class definition containing `__init__` and `forward`/`call` methods.
    4. **Training Recipe**: Recommendation for weight initialization, optimizer (AdamW, SGD), learning rate scheduler, and gradient clipping thresholds.
    ```
*   **Tips for Better Results**:
    *   Specify whether you need multi-GPU training support (e.g., PyTorch DDP) or specialized layer formats.
*   **Example Use Case**:
    *   **Input**: PyTorch architecture for 1D CNN + BiLSTM to classify ECG sensor data with low latency.
    *   **Output**: Clean PyTorch class specifying Conv1d, MaxPool1d, Bidirectional LSTM, Linear output layer, and dropout regularization.

---

### 3. Hyperparameter Tuning Strategy

*   **Purpose**: Design hyperparameter optimization strategies and Optuna search spaces for machine learning algorithms.
*   **Prompt**:
    ```text
    You are an ML Engineer specializing in model optimization.
    Design a hyperparameter tuning strategy and optimization script for the following algorithm and dataset.

    Model Type: [MODEL_TYPE] (e.g., XGBoost, LightGBM, Random Forest, PyTorch Transformer)
    Metric to Optimize: [METRIC] (e.g., F1-Score, ROC-AUC, Mean Absolute Percentage Error)
    Tuning Framework: Optuna

    Your response must contain:
    1. **Parameter Search Space Table**: List of parameters, type (categorical, integer, float), recommended search bounds, and scaling (log or linear).
    2. **Pruning Strategy**: Recommendations for trial pruning algorithms (e.g., MedianPruner, Hyperband) to stop bad trials early.
    3. **Optuna Script**: Python code demonstrating how to set up the objective function, define the study, configure pruning, and run the optimization trials.
    ```
*   **Tips for Better Results**:
    *   Provide the model's current baseline parameters and baseline metric score.
*   **Example Use Case**:
    *   **Input**: XGBoost classifier tuning ROC-AUC on tabular fraud detection data.
    *   **Output**: Optuna search space for `max_depth` (3-12), `learning_rate` (1e-3 to 1e-1 log), `subsample` (0.5-1.0), and a complete python execution script.

---

### 4. Prompt Engineering Optimizer

*   **Purpose**: Optimize raw, basic prompts into robust, production-grade instructions using meta-prompting, few-shot syntax, and XML delimiters.
*   **Prompt**:
    ```text
    You are an expert Prompt Engineer.
    Optimize the following raw user prompt into a high-performing, reliable system prompt.

    Target LLM: [LLM_NAME] (e.g., Claude 3.5 Sonnet, GPT-4o, Gemini 1.5 Pro)
    Raw Prompt:
    [INSERT_RAW_PROMPT]

    Apply the following techniques:
    1. **Role Definition**: Assign a clear, professional persona.
    2. **Structured Formatting**: Use XML tags (e.g., `<context>`, `<rules>`, `<examples>`) to separate instructions from dynamic inputs.
    3. **Few-Shot Examples**: Create realistic, high-quality input-output examples showcasing expected edge cases.
    4. **Guardrails**: Explicitly state negative constraints (what the AI *must not* do) to prevent hallucinations, jailbreaks, or format violations.
    5. **Chain of Thought (CoT)**: Force the model to reason step-by-step before producing output.

    Please provide:
    1. **Optimized System Prompt**: Ready to be copied.
    2. **User Input Template**: How the final variables should be passed to the prompt.
    3. **Engineering Rationale**: Explaining why you structured the prompt this way.
    ```
*   **Tips for Better Results**:
    *   If your target model is Claude, emphasize XML tags. For GPT models, markdown formatting works exceptionally well.
*   **Example Use Case**:
    *   **Input**: "Make this paragraph sound more professional."
    *   **Output**: A highly structured system prompt defining the persona of an executive editor, with XML nodes for inputs, tone parameters, and few-shot rewriting examples.

---

### 5. RAG System Designer

*   **Purpose**: Architect Retrieval-Augmented Generation (RAG) pipelines including document chunking, indexing, and reranking.
*   **Prompt**:
    ```text
    You are a RAG Architect. Design an end-to-end Retrieval-Augmented Generation system matching the requirements below.

    Document Type/Source: [DOCS_SOURCE] (e.g., 10,000 multi-page PDF financial reports, raw markdown code repositories)
    Query Profile: [QUERY_PROFILE] (e.g., "Synthesize financial tables and answer year-over-year revenue questions")
    Target Vector DB: [VECTOR_DB] (e.g., Pinecone, Chroma, pgvector)

    Design the system detailing:
    1. **Ingestion & Chunking Strategy**:
       - Document loading and parsing (e.g., OCR, PDF table extraction).
       - Chunking sizes, overlap, and splitting strategies (recursive character splitting, semantic chunking).
    2. **Indexing & Retrieval**:
       - Embedding model recommendations (e.g., `text-embedding-3-small`, `bge-large-en-v1.5`).
       - Dense vs sparse retrieval (Hybrid Search with BM25).
       - Reranking strategy (e.g., Cohere Rerank, BGE-Reranker).
    3. **Context Construction & Prompting**:
       - How retrieved context is ordered and fed to the LLM to mitigate "lost in the middle" effects.
       - Prompt structure for final generation.
    4. **Architectural Diagram**: ASCII or detailed text representing the ingestion, retrieval, and generation flows.
    ```
*   **Tips for Better Results**:
    *   Specify if your documents contain heavily nested tables or complex images, as this requires specialized parser designs (like Unstructured or LlamaParse).
*   **Example Use Case**:
    *   **Input**: Designing RAG for internal company HR policies.
    *   **Output**: Proposal suggesting semantic chunking, Pinecone index with cosine similarity, Hybrid Search (BM25 + Dense), and Cohere Rerank.

---

### 6. Model Quantization Guide

*   **Purpose**: Convert heavy deep learning models to lighter, faster versions using quantization techniques (INT8, FP16, AWQ, GGUF) for deployment.
*   **Prompt**:
    ```text
    You are an Edge AI and Inference Optimization Engineer.
    Write a guide and Python script to quantize the following model for deployment.

    Original Model: [MODEL_NAME] (e.g., llama-2-7b, ResNet50)
    Target Deployment Platform: [PLATFORM] (e.g., Raspberry Pi 4, Nvidia Triton Server, Mobile iOS App)
    Quantization Scheme: [SCHEME] (e.g., GGUF 4-bit, INT8 Post-Training Quantization, ONNX FP16)

    Please produce:
    1. **Methodology Overview**: Explain the differences between PTQ (Post-Training Quantization) and QAT (Quantization-Aware Training) for this target, along with expected accuracy trade-offs.
    2. **Quantization Pipeline Script**: Python/Bash commands to perform the quantization (e.g., using `llama.cpp`, `ONNX Runtime`, `TensorRT`, or `PyTorch FX Graph Mode`).
    3. **Calibration Strategy**: How to prepare calibration datasets to minimize accuracy loss in low-bit models.
    4. **Validation Checklist**: Steps to verify target speedup and track latency metrics (e.g., time-to-first-token).
    ```
*   **Tips for Better Results**:
    *   Provide details on hardware capabilities (e.g., support for AVX2 instructions, FP16 tensor cores) to target the quantization instructions.
*   **Example Use Case**:
    *   **Input**: Quantizing a custom PyTorch image classification model to run on an ONNX runtime edge device.
    *   **Output**: Post-training static INT8 quantization script in PyTorch, calibration loop code, and accuracy validation comparisons.

---

### 7. Ethics & Bias Auditor

*   **Purpose**: Audit datasets, prompts, and machine learning models for ethical risks, bias, and toxic outputs.
*   **Prompt**:
    ```text
    You are an AI Ethics and Safety Auditor.
    Audit the following ML/LLM system setup for bias, toxicity, discrimination, and privacy leakage.

    System Details: [SYSTEM_DETAILS] (e.g., "An LLM-based CV screening assistant prioritizing candidates for tech jobs.")
    Dataset details (if tabular): [DATA_DETAILS]
    System Prompt (if LLM): [PROMPT_DETAILS]

    Provide an Audit Report detailing:
    1. **Risk Identification**: Highlight demographics-based bias (gender, age, ethnicity), demographic parity issues, or data privacy risks (PII leakage).
    2. **Evaluation Metrics**: Suggest specific mathematical and operational metrics (e.g., Disparate Impact Ratio, Equalized Odds, Toxicity Scores).
    3. **Mitigation Blueprint**:
       - Pre-processing (re-weighing, synthetic sampling).
       - In-processing (adversarial debiasing).
       - Post-processing (threshold adjustment).
       - LLM Guardrails (moderation API integration, system constraints).
    ```
*   **Tips for Better Results**:
    *   Provide any corporate compliance frameworks (e.g., EU AI Act, NIST AI Risk Management Framework) that the system must comply with.
*   **Example Use Case**:
    *   **Input**: Credit scoring model predicting loan defaults using demographic features.
    *   **Output**: Audit highlighting risks of redlining via ZIP codes, recommendations for testing Equal Opportunity metrics, and mitigation code using `AIF360`.

---

### 8. Transfer Learning Guide

*   **Purpose**: Adapt pre-trained foundational models (CV or NLP) to specialized custom tasks with minimal data.
*   **Prompt**:
    ```text
    You are a Senior ML Research Engineer. Create a Transfer Learning implementation guide to adapt a pre-trained model to a new downstream task.

    Base Model: [BASE_MODEL] (e.g., ResNet50, BERT-base, ViT)
    Target Downstream Task: [TASK] (e.g., Classifying medical scans into 3 disease types, identifying custom legal clauses in contracts)
    Size of Custom Dataset: [DATASET_SIZE] (e.g., 500 labeled samples)

    Your guide must contain:
    1. **Adaptation Strategy**: Deciding which layers to freeze, which to fine-tune, and custom classification head structures.
    2. **Training Optimization**: Dealing with overfitting on small datasets (learning rate scaling, layer-wise learning rate decay, data augmentation).
    3. **Implementation Script**: Clean PyTorch/HuggingFace script loading the weights, adjusting the head layer, freezing parameters, and starting the training loop.
    ```
*   **Tips for Better Results**:
    *   Specify if the source dataset of the pre-trained model (e.g., ImageNet, WebText) is significantly different from your target dataset.
*   **Example Use Case**:
    *   **Input**: Fine-tuning BERT for classification of construction safety incident reports.
    *   **Output**: PyTorch code using `transformers` AutoModelForSequenceClassification, freezing transformer layers except the pooler, and defining weighted cross-entropy loss.

---

### 9. LLM Fine-Tuning Recipe

*   **Purpose**: Design parameter-efficient fine-tuning (PEFT) pipelines using QLoRA/LoRA to custom-train Large Language Models.
*   **Prompt**:
    ```text
    You are an LLM Infrastructure Engineer.
    Design a QLoRA/LoRA fine-tuning recipe to train a foundational LLM on a domain-specific dataset.

    Base Model: [BASE_MODEL] (e.g., Mistral-7B-v0.3, Llama-3-8B)
    Hardware Constraints: [HARDWARE] (e.g., Single NVIDIA A10G 24GB VRAM)
    Dataset Format: [FORMAT] (e.g., Instruction-tuning pairs, multi-turn chat dialogues)

    Please output:
    1. **Quantization & PEFT Configuration**:
       - BitsAndBytes configuration (4-bit double quantization parameters).
       - LoRA parameters (r, alpha, target modules, dropout).
    2. **Training Hyperparameters**: Learning rate, batch size, gradient accumulation steps, context length, optimizer (paged_adamw_8bit).
    3. **Complete Python Script**: Script utilizing HuggingFace `peft`, `bitsandbytes`, and `trl`'s `SFTTrainer`.
    4. **Memory Management Strategy**: Explaining how to prevent Out-Of-Memory (OOM) errors (deepspeed, activation checkpointing).
    ```
*   **Tips for Better Results**:
    *   Indicate if you need to use specific formats like ChatML or Llama-3 template formats.
*   **Example Use Case**:
    *   **Input**: Training Llama-3-8B on customer support transcripts on an A100.
    *   **Output**: Complete PEFT trainer configuration with target modules `[q_proj, k_proj, v_proj, o_proj]`, double quantization enabled, and custom evaluation callbacks.

---

### 10. LLM Evaluation Designer

*   **Purpose**: Define evaluation metrics, datasets, and frameworks (like G-Eval, RAGAS, or LLM-as-a-judge) to benchmark LLM applications.
*   **Prompt**:
    ```text
    You are an AI Quality Assurance Engineer.
    Design an automated evaluation pipeline to test the reliability, accuracy, and format conformance of an LLM agent.

    Agent Purpose: [AGENT_PURPOSE] (e.g., "An agent that reads database schemas and writes SQL queries")
    Expected Failure Modes: [FAILURE_MODES] (e.g., Hallucinating column names, writing syntactically invalid SQL, leaking schema data)

    Your design must output:
    1. **Evaluation Methodology**: Contrast model-based evaluations (LLM-as-a-judge) vs programmatic evaluations (regex checks, execution tests).
    2. **Test Dataset Schema**: Outline target inputs, gold-standard answers, and evaluation metadata.
    3. **Evaluation Criteria & Prompts**: Write specific system prompts for the LLM judge, complete with scoring rubrics (1-5 scale) for criteria (e.g., correctness, relevance, faithfulness).
    4. **Implementation Framework**: Python code structure demonstrating how to run the evaluation loop, query the judge, and aggregate performance metrics (e.g., using `Promptfoo`, `RAGAS`, or custom scripts).
    ```
*   **Tips for Better Results**:
    *   Define a small sample dataset representing actual user query failures to design a accurate test suite.
*   **Example Use Case**:
    *   **Input**: Evaluating a customer query summarizer for call center agents.
    *   **Output**: Prompts for a GPT-4 Judge evaluating "Conciseness" and "Information Fidelity" with a rigorous 5-point rubrics schema.
