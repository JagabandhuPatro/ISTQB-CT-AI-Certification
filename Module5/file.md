
# Module 5: Input Data Testing for Machine Learning Systems

Welcome to Module 5 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 5 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)](https://youtu.be/HiVWjAlnkSk)  

---
# ISTQB CT-AI Syllabus: Input Data Testing for Machine Learning Systems

## Input Data Testing for Machine Learning Systems

### Input Data Risks and Mitigations
* Poor quality input data fundamentally degrades the architectural integrity of the ML model, causing severe "garbage in, garbage out" scenarios.
* Testers must proactively mitigate risks such as data poisoning, missing values, and data leakage by establishing rigorous validation gates.
* Architecturally, this requires implementing automated data sanitization and monitoring pipelines before raw data ever reaches the model training environment.
* QA strategies must shift left to evaluate the raw data sources directly, ensuring integrity, security, and traceability at the very boundaries of the system.

### Testing for Bias
* Bias testing ensures the system does not learn, amplify, or execute prejudiced behaviors against specific demographic slices within its operational domain.
* Testers must actively search for historical, sampling, or measurement biases embedded deep within the datasets prior to model training.
* From a QA perspective, this involves utilizing specialized statistical tools to measure fairness metrics like disparate impact or equal opportunity.
* Architects and testers must collaborate to define acceptable fairness thresholds and implement mitigation strategies such as re-weighting or adversarial debiasing.

### Data Pipeline Testing
* The data pipeline is a critical architectural component that handles the extraction, transformation, and loading (ETL) of data into the ML ecosystem.
* Testing these pipelines requires validating the ETL logic to ensure automated transformations do not corrupt or unintentionally alter the semantic meaning of the data.
* QA must implement robust integration tests to verify pipeline resilience, fault tolerance, and end-to-end data lineage tracking.
* Treating "data as code" means the pipeline infrastructure itself must be subjected to the same rigorous version control and CI/CD validation as conventional software.

### Testing for Data Representativeness
* Testers must verify that the training, validation, and test datasets accurately and proportionally reflect the real-world operational design domain (ODD).
* If the data lacks representativeness, the resulting architecture will suffer from severe underperformance in production due to inevitable distribution shifts.
* QA employs Exploratory Data Analysis (EDA) and profiling tools to ensure all critical edge cases and minority classes are sufficiently captured in the dataset.
* Continuous monitoring in production is architecturally necessary to detect when real-world inputs begin to drift away from the baseline representativeness of the training data.

### Dataset Constraint Testing
* This involves validating that the incoming data strictly adheres to predefined schemas, formats, and statistical boundary constraints before ingestion.
* Testers define absolute rules—such as required fields, valid numerical ranges, and data type compliance—that the pipeline must enforce automatically.
* Architecturally, these constraints act as the first line of defense, rejecting anomalous, malformed, or malicious payloads before they corrupt the model's state.
* QA automation should leverage schema validation frameworks to perform continuous, real-time constraint checking on massive incoming data streams.

### Label Correctness Testing
* For supervised learning architectures, the predictive accuracy of the model is entirely bottlenecked by the absolute correctness of the target labels (ground truth).
* Testers must deeply evaluate the labeling process, auditing for high inter-annotator agreement and identifying systemic subjective errors by human labelers.
* QA strategies include programmatic label verification, cross-validation checks, and expert human-in-the-loop reviews of ambiguous or highly complex edge cases.
* Establishing a highly reliable ground truth is a fundamental architectural requirement for calculating valid and trustworthy functional performance metrics.

### Hands-on Exercise: Input Data Testing
* This practical exercise bridges architectural theory and QA practice, allowing testers to physically construct and execute validation tests against raw datasets.
* Testers gain hands-on experience using data profiling libraries to programmatically identify missing values, extreme outliers, and hidden constraint violations.
* The exercise emphasizes the architectural necessity of integrating these automated data validation scripts directly into the continuous testing pipeline.
* By actively finding and fixing data defects, testers solidify their understanding of how proactive data QA directly prevents catastrophic downstream model failures.
---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 6 ➡️](../Module6/file.md)
