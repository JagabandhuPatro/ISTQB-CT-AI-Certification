
# Module 2: Quality Characteristics for AI-Based Systems

Welcome to Module 2 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 2 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)](https://youtu.be/esx6esJAAiE)  

---
# ISTQB CT-AI Syllabus: Quality Characteristics and Acceptance Criteria

## Quality Characteristics for AI-Based Systems: AI-Specific Quality Characteristics
* AI systems introduce unique, domain-specific quality characteristics beyond standard ISO/IEC 25010 models, most notably adaptability, autonomy, and flexibility.
* Testers must meticulously evaluate *adaptability* to verify that the machine learning model correctly evolves its behavior when exposed to new data without degrading existing performance.
* Validating *autonomy* requires designing test scenarios that ensure the AI can operate safely and make decisions without human intervention strictly within its defined operational design domain.
* Traditional software quality metrics, such as reliability and maintainability, must be redefined to account for the probabilistic nature, data dependency, and non-determinism inherent to ML architectures.

## Quality Characteristics for AI-Based Systems: AI and Safety
* Safety testing for AI-based systems extends far beyond physical harm, requiring QA to also mitigate psychological, financial, and societal risks caused by unintended algorithmic behaviors.
* Testers must actively design adversarial test cases to identify "reward hacking," a failure mode where a reinforcement learning model optimizes its objective function using unsafe or unintended shortcuts.
* Robust safety assessment demands the generation of extreme edge-cases and out-of-distribution data sets to ensure the AI degrades gracefully rather than failing catastrophically.
* Compliance with emerging AI safety standards dictates that QA must verify that fail-safe mechanisms and human-in-the-loop override controls function flawlessly during critical anomalies.

## Acceptance Criteria for AI-Based Systems
* Defining acceptance criteria for AI components is inherently complex because absolute determinism and 100% correctness are mathematically impossible in probabilistic systems.
* Instead of binary pass/fail conditions, QA and architectural stakeholders must collaborate to establish statistically significant thresholds, such as minimum precision or maximum false positive rates.
* Comprehensive acceptance criteria must explicitly include fairness constraints, guaranteeing the model performs equitably and avoids algorithmic bias across all demographic slices in the test dataset.
* To ensure end-to-end reliability, the criteria must mandate specific performance levels for both the isolated machine learning model and the broader architectural ecosystem it integrates into.

---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 3 ➡️](../Module3/file.md)
