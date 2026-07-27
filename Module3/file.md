# Module 3: Machine Learning

Welcome to Module 3 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 3 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)]((https://youtu.be/z5YYcroRDtg))  

---
# ISTQB CT-AI Syllabus: Machine Learning, Data, Metrics, and Neural Networks

## Machine Learning

### Introduction to Machine Learning
* Machine Learning (ML) enables systems to learn from data to make predictions or decisions without being explicitly programmed for the specific task.
* Testers must verify that the selected ML approach properly aligns with the problem domain, the operational design domain, and the available dataset.
* Unlike traditional deterministic systems, the logic is derived during the training phase, shifting testing efforts heavily towards data validation and pipeline integrity.
* QA must rigorously assess the underlying assumptions of the ML model to ensure it behaves safely within its defined architectural boundaries.

### Different Forms of Machine Learning
* Supervised learning requires testers to validate outputs against labeled data, focusing heavily on establishing and verifying ground truth accuracy.
* Unsupervised learning challenges testers to evaluate groupings or patterns without predefined correct answers, often requiring specialized clustering metrics.
* Reinforcement learning necessitates testing the specific reward function to prevent unintended, potentially harmful behaviors like reward hacking.
* Understanding these distinct paradigms is absolutely essential for QA to select the appropriate functional performance metrics and construct valid test oracles.

### Machine Learning Workflow
* The ML workflow is an iterative lifecycle encompassing requirements analysis, data preparation, modeling, evaluation, and eventual deployment.
* Testers must be integrated early in the pipeline to validate data quality, assess risks, and define appropriate statistical acceptance criteria.
* During the modeling phase, QA focuses on back-to-back testing and closely monitoring how hyperparameter tuning impacts the model's functional performance.
* Post-deployment, continuous testing and live monitoring are mandatory to detect data drift, concept drift, and overall model degradation over time.

### Hands-on Exercise: Create a Machine Learning Model
* The practical creation of a model allows testers to understand architectural dependencies, algorithmic behaviors, and deployment constraints firsthand.
* Testers practice dividing datasets into strict training, validation, and testing sets to prevent the critical defect of data leakage.
* The exercise emphasizes the absolute necessity of version-controlling both the code and the data to maintain reproducible and reliable test environments.
* It provides tangible, hands-on experience in identifying how different algorithmic choices directly dictate the types of defects that will manifest.

### Pretrained Models, Fine-Tuning, and Retrieval-Augmented Generation
* Leveraging pretrained models accelerates architecture development but introduces inherited biases and external security vulnerabilities that must be explicitly tested.
* Fine-tuning requires testers to validate that domain-specific updates do not cause "catastrophic forgetting" of the base model's fundamental capabilities.
* Retrieval-Augmented Generation (RAG) pipelines must be tested for the relevance of the retrieved context and the absolute factual accuracy of the generated response.
* QA strategies for RAG include injecting adversarial and out-of-domain queries to ensure the system strictly relies on provided context to mitigate hallucinations.

---

## Data for Machine Learning

### Activities in Data Preparation
* Data preparation is often the most critical phase; testers must actively verify data completeness, consistency, accuracy, and timeliness.
* QA involves validating data cleaning processes to ensure outliers and missing values are handled appropriately without introducing statistical bias.
* Testers must audit data labeling efforts to ensure high inter-annotator agreement and the establishment of a truly reliable ground truth.
* Exploratory Data Analysis (EDA) techniques are utilized by QA to identify underlying data distributions and potential ethical biases before any training begins.

### Hands-on Exercise: Data Preparation in Support of the Creation of a Machine Learning Model
* Engaging in active data wrangling helps QA understand how preprocessing steps like normalization, scaling, or encoding directly influence model predictions.
* Testers practice actively identifying and mitigating skewed or imbalanced datasets to ensure algorithmic fairness across all demographic slices.
* The exercise highlights the direct, undeniable correlation between poor data quality ("garbage in") and degraded functional performance metrics ("garbage out").
* It reinforces the architectural necessity of building automated, testable data pipelines (DataOps) as a core component of the continuous integration lifecycle.

---

## ML Functional Performance Metrics for Classification

### Calculation of Machine Learning Functional Performance Metrics
* Testers must master the confusion matrix to accurately extract and analyze True Positives, True Negatives, False Positives, and False Negatives.
* Accuracy is often a misleading metric for imbalanced datasets, requiring testers to meticulously calculate and analyze Precision and Recall instead.
* The F1-Score is utilized by QA as a harmonic mean to provide a balanced, single-value evaluation when Precision and Recall constraints are at odds.
* QA must collaborate with architectural and business stakeholders to determine which specific metric (e.g., minimizing False Positives vs. False Negatives) aligns with the system's risk profile.

### Hands-on Exercise: Evaluate a Machine Learning Model using Selected ML Functional Performance Metrics
* Practically applying these metrics allows testers to effectively map abstract mathematical outputs to real-world acceptance criteria and business risks.
* Testers gain crucial experience in plotting and interpreting ROC curves and AUC scores to evaluate the model's performance across various classification thresholds.
* The exercise reinforces how to translate and communicate complex statistical performance results to non-technical stakeholders transparently.
* It provides deep insight into how slight, deliberate shifts in the decision threshold can drastically alter the resulting functional performance metrics.

### Hands-on Exercise: Show the Impact of Different Machine Learning Models and Dataset Combinations
* This exercise proves that changing the underlying algorithm (e.g., Decision Tree vs. Support Vector Machine) fundamentally alters the system's defect profile and failure modes.
* Testers observe how feeding identical, unaltered data to different model architectures yields vastly different levels of accuracy, precision, and recall.
* It highlights the critical importance of robustness testing by demonstrating how small perturbations or noise in the dataset can drastically impact predictions.
* QA learns to systematically document these variations to justify architectural choices, establish baseline performance expectations, and validate the model selection process.

---

## Neural Networks

### Structure and Working of a Deep Neural Network
* Testers must understand the foundational architecture of DNNs, including input layers, multiple hidden processing layers, and the final output layer.
* Knowledge of how mathematical weights, biases, and non-linear activation functions interact helps QA theorize why certain inputs trigger unexpected outputs.
* Understanding backpropagation and loss functions aids testers in grasping how the network actually learns and where issues like vanishing gradients might occur.
* This structural architectural insight is absolutely crucial for QA when designing targeted adversarial attacks intended to exploit complex decision boundaries.

### Hands-on Exercise: Experience the Implementation of a Perceptron
* Building a single-layer perceptron from scratch demystifies the fundamental, mathematical building block of all complex deep learning architectures.
* Testers gain hands-on experience by manually configuring weights and biases to solve basic, linearly separable logic gates like AND and OR.
* The exercise explicitly demonstrates the mathematical limitations of simple networks (such as the inability to solve the XOR problem) without relying on hidden layers.
* It provides the foundational, low-level understanding necessary for grasping the complexities of the multi-layer, deep networks evaluated later in the syllabus.

### Coverage Measures for Neural Networks
* Traditional code coverage (statement/branch) is highly insufficient for neural networks because the routing logic is embedded in the weights, not the source code.
* Testers utilize specialized structural ML metrics like Neuron Coverage to measure the specific percentage of activated neurons during test suite execution.
* More advanced metrics, such as Threshold Coverage and Sign Coverage, are evaluated by QA to ensure a diverse range of internal network states are successfully triggered.
* While these metrics effectively guide test data generation, QA must recognize that achieving high neuron coverage does not inherently guarantee high functional correctness or overall system safety.
---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 4 ➡️](../Module4/file.md)
