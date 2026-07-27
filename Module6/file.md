
# Module 6: Model Testing for Machine Learning Systems


Welcome to Module 6 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 2 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)](https://youtu.be/Jdvk2dZAoBw)  

---
# ISTQB CT-AI Syllabus: Model Testing for Machine Learning Systems

## Machine Learning Model Risks and Mitigations
* Model risks include algorithmic bias, vulnerability to evasion attacks, and the degradation of accuracy over time due to changing real-world environments.
* Architecturally, mitigating these risks requires building robust security boundaries, implementing human-in-the-loop oversight, and integrating continuous anomaly detection.
* QA must transition from static risk assessments to dynamic threat modeling, evaluating how probabilistic models fail under unprecedented and complex conditions.
* Testers prioritize defining acceptable risk thresholds with business stakeholders, ensuring the model fails safely and gracefully rather than catastrophically.

## Machine Learning Model Documentation and Review
* Comprehensive documentation, such as "Model Cards," is an architectural necessity for tracking the model's intended use, training data, and known limitations.
* QA conducts rigorous static reviews of these artifacts to ensure ethical compliance, regulatory alignment, and transparency across the development lifecycle.
* Effective reviews mandate that the operational design domain (ODD) is explicitly documented so testers can accurately map test scenarios to the model's intended environment.
* This documentation serves as the ultimate test oracle for non-functional requirements, guiding QA in verifying fairness, explainability, and security constraints.

## ML Functional Performance Testing of Probabilistic Machine Learning Systems
* Testing probabilistic systems requires QA to evaluate aggregate statistical outcomes across vast datasets rather than expecting deterministic, single-input correctness.
* Architects and testers must collaborate to define specific confidence intervals and error margins as the primary acceptance criteria for model deployment.
* Performance testing evaluates not just accuracy, but how the model's confidence scores align with actual correctness to prevent overconfident, incorrect predictions.
* QA utilizes automated, scalable test execution frameworks to continuously measure precision, recall, and F1-scores against historical baseline distributions.

## Adversarial Testing of Machine Learning Systems
* Adversarial testing is a proactive security and QA practice designed to intentionally deceive the model using maliciously crafted, imperceptible input perturbations.
* Testers simulate evasion and poisoning attacks to evaluate the resilience of the model's decision boundaries and the robustness of its data ingestion pipeline.
* From an architectural standpoint, this testing identifies critical vulnerabilities that necessitate the implementation of input sanitization and robust filtering layers.
* By systematically attacking the AI component, QA ensures the system can withstand hostile real-world environments without suffering catastrophic misclassification.

## Metamorphic Testing
* Metamorphic testing resolves the "oracle problem" by validating the relationships between multiple inputs and their corresponding outputs, rather than checking exact values.
* Testers define Metamorphic Relations (MRs)—such as altering the gender on a resume—and verify that the model's underlying prediction remains logically consistent.
* This technique is highly effective for automating the testing of complex, non-deterministic architectures where the absolute ground truth is unknown or highly subjective.
* QA leverages metamorphic testing to expose hidden algorithmic biases and logical inconsistencies that traditional assertion-based testing fundamentally cannot detect.

## Hands-on Exercise: Apply Metamorphic Testing
* This practical exercise bridges QA theory and architectural validation, allowing testers to actively design and execute Metamorphic Relations against a live model.
* Testers gain hands-on experience identifying which input transformations should preserve the output (invariance) versus those that should alter it predictably.
* The exercise demonstrates how to programmatically scale test coverage across millions of data points without requiring human-labeled ground truth for each test case.
* By implementing automated metamorphic checks, testers learn how to continuously validate model logic within modern CI/CD pipelines.

## Drift Testing
* Drift testing is the continuous validation process used to detect when a deployed model's statistical properties diverge from its original training baseline.
* QA must architecturally monitor both Data Drift (shifts in input distribution) and Concept Drift (changes in the underlying relationship between inputs and outputs).
* Testers implement automated threshold alerts to notify stakeholders when the model's functional performance degrades, signaling the need for immediate retraining.
* This testing strategy shifts QA heavily into the production environment, establishing MLOps as a critical component of the ongoing AI quality lifecycle.

## Testing for Overfitting and Underfitting
* QA evaluates overfitting to ensure the model hasn't simply memorized the training data, which leads to catastrophic failure when processing unseen production inputs.
* Underfitting is tested by verifying whether the architectural capacity of the model is sufficient to capture the underlying mathematical complexity of the training data.
* Testers utilize strict data separation (training, validation, and holdout sets) to systematically measure and compare error rates across different data partitions.
* Monitoring learning curves allows QA to pinpoint precisely when model training should be halted to achieve the optimal balance of generalization and accuracy.

## A/B Testing
* A/B testing evaluates an AI model's performance by routing a subset of live production traffic to a new model variant and comparing it against the existing baseline.
* Architecturally, this requires robust load balancers and deployment infrastructure to safely orchestrate traffic splitting without impacting overall system stability.
* QA analyzes statistical telemetry to determine if the new model drives tangible improvements in business metrics and user acceptance before a full rollout.
* This strategy minimizes deployment risk for non-deterministic systems by relying on empirical, real-world user data rather than synthetic staging environments.

## Back-to-Back Testing
* Back-to-back testing validates complex AI models by executing identical test suites against both the new model and a legacy system (or previous model version).
* Testers utilize the legacy system's outputs as a pseudo-oracle, automatically flagging significant deviations in predictions for targeted human review.
* This method is critical for architectural migrations, ensuring that introducing a new ML component does not regress or silently alter established business logic.
* QA employs back-to-back testing within automated regression pipelines to confidently guarantee the stability and consistency of the AI integration over time.
---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 7 ➡️](../Module7/file.md)
