# Module 1: Introduction to AI for Testing

Welcome to Module 1 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 1 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)](https://youtu.be/pnII5Vcm2Q0)  

---
# ISTQB CT-AI Syllabus: Key Topics Overview

## AI-Based and Conventional Systems
* AI-based systems rely on data-driven learning and probabilistic models, differentiating them from conventional systems that execute explicit, deterministic logic.
* Testing strategies must adapt from traditional assertion-based checks to statistical evaluations of non-deterministic behavior.
* Quality assurance for these systems demands verifying unique characteristics like flexibility, adaptability, and autonomy.
* Unlike conventional software, AI system updates heavily depend on data evolution, meaning testers must manage both datasets and code as testable artifacts.

## Narrow AI, General AI, and Super AI
* The ISTQB syllabus differentiates between Narrow AI (specialized tasks), General AI (human-level cognition), and Super AI (surpassing human intelligence).
* Current testing practices focus almost entirely on Narrow AI, requiring testers to evaluate domain-specific functional performance metrics.
* Distinguishing these types helps testers appropriately scope acceptance criteria and avoid hypothetical testing of theoretical AI capabilities.
* Testers must also understand how the "AI effect" influences definitions over time, as capabilities once considered intelligent become standard.

## Different Types of AI Technologies
* Testers must recognize various technologies utilized to implement AI, such as machine learning and deep neural networks.
* Understanding whether a system uses supervised learning (classification/regression) or unsupervised learning (clustering/association) dictates the required testing approach.
* The choice of underlying technology directly impacts how testers select test data and calculate functional performance metrics.
* QA professionals use this knowledge to identify potential failure modes like underfitting, overfitting, or algorithmic biases.

## Generative AI
* Generative AI introduces non-deterministic, open-ended outputs, requiring specialized validation unlike traditional predictive classification models.
* Testers must apply techniques like prompt engineering and Retrieval-Augmented Generation (RAG) evaluation to properly verify content generation.
* Risk management is crucial, as QA focuses heavily on identifying hallucinations, reasoning errors, and potential biases in LLM outputs.
* This domain requires shifting to systematic evaluations of generated artifacts using dynamic metrics and iterative refinement rather than static test oracles.

## Hardware for Machine Learning Systems
* Testers must compare and understand the specific hardware choices available for implementing and executing AI-based systems.
* The selected infrastructure directly influences non-functional characteristics such as latency, scalability, and system performance during execution.
* Evaluating hardware dependencies is crucial to ensure both the computational efficiency and the cost-effectiveness of the deployed pipeline.
* Testers should also consider how task characteristics and hardware usage affect energy consumption and overall environmental impact.

## Development and Hosting of AI Models
* The syllabus emphasizes evaluating concepts like AI as a Service (AIaaS) and the use of pre-trained models within the testing lifecycle.
* Utilizing pre-trained models or external hosting introduces specific integration risks and security vulnerabilities that testers must explicitly validate.
* Testers must be involved throughout the machine learning workflow, ensuring continuous quality from data preparation through to deployment.
* Effective testing strategies must account for continuous monitoring to detect performance degradation or data drift once the model is hosted.

## Machine Learning Development Frameworks
* QA professionals are required to identify popular AI development frameworks utilized in building ML architectures.
* Familiarity with these specific infrastructure tools helps testers design resilient test environments and conduct effective back-to-back testing.
* Understanding the framework architecture empowers testers to pinpoint integration flaws and better manage complex external dependencies.
* Knowledge of these frameworks bridges the gap between software developers and testers, facilitating smoother integration and AI validation phases.

## Regulations and Standards for AI
* The syllabus mandates that testers describe how industry standards and legal regulations apply to AI-based systems.
* Testers must incorporate ethical considerations and verify compliance with frameworks like GDPR regarding the processing of data.
* Evaluating AI systems requires auditing for safety, transparency, interpretability, and explainability to secure regulatory approval.
* QA plays a critical role in ensuring responsible AI use, actively mitigating severe risks such as algorithmic bias and unauthorized data exposure.

---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 2 ➡️](../Module2/file.md)
