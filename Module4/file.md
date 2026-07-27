# Module 4: Testing AI-Based Systems 

Welcome to Module 4 of the ISTQB CT-AI study guide. In this section, we cover the foundational concepts of Artificial Intelligence, how it differs from traditional software, and the implications for Quality Assurance. 

## 📺 Video Lecture

> **Watch the Chapter Video:**  
> [![Module 4 Video](https://img.shields.io/badge/Watch_on-YouTube-red?style=for-the-badge&logo=youtube)](https://youtu.be/rkpcI4grbcw)

---
# ISTQB CT-AI Syllabus: Testing AI-Based Systems and Test Levels

## Testing AI-Based Systems

### Introduction to Testing AI-Based Systems
* Testing AI requires a paradigm shift from verifying deterministic logic to validating probabilistic behaviors governed by trained weights and massive datasets.
* QA must adapt traditional testing techniques to account for non-determinism, complex decision boundaries, and inherent black-box architectures.
* Testers face unique challenges such as defining the operational design domain and evaluating system performance when 100% accuracy is mathematically impossible.
* The process heavily relies on combining traditional testing for conventional application layers with statistical and metamorphic testing for the AI components.

### Locked and Adaptive AI-Based Systems
* Locked AI models have fixed parameters post-deployment, allowing testers to validate a stable baseline of behavior during system integration.
* Adaptive (or continuously learning) systems evolve in production, making traditional regression testing entirely insufficient without continuous live monitoring.
* For adaptive architectures, QA must stringently test the guardrails and safety bounds to prevent uncontrolled divergence or "catastrophic forgetting."
* Architecturally, adaptive models demand robust automated pipelines (MLOps) that automatically trigger re-testing and anomaly detection as new data updates the model weights.

### Rationale for a Statistical Approach to Testing AI-Based Systems
* Because AI systems generalize from data rather than executing hardcoded rules, individual test case failures do not necessarily indicate a definitive system defect.
* QA must rely on statistical approaches, aggregating results across large datasets to determine if the model meets predefined confidence intervals and variance thresholds.
* Architecturally, this means acceptance criteria are defined by probabilistic thresholds (e.g., minimum 95% accuracy with a 2% margin of error) rather than absolute binary outcomes.
* Testers use these statistical distributions to identify systemic biases and differentiate between expected probabilistic variance and genuine model degradation.

### Test Oracles for AI-Based Systems
* The "oracle problem" is severely magnified in AI, as the correct expected outcome for complex or novel inputs is often unknown, highly subjective, or completely open-ended.
* Testers frequently employ Metamorphic Testing, verifying relations between inputs and outputs (e.g., translating a sentence back and forth should yield the original meaning) rather than checking exact values.
* Pseudo-oracles, such as running an older version of the model side-by-side (back-to-back testing) or utilizing human-in-the-loop expert evaluations, become critical QA tools.
* Architects and testers must collaborate to design statistical oracles that evaluate the aggregate distribution of outputs against established historical baselines.

---

## Testing Generative AI and Large Language Models

### Testing Generative AI
* Generative models introduce open-ended, highly varied outputs, requiring QA to evaluate complex attributes like fluency, coherence, and factual grounding.
* Unlike traditional predictive AI, generative testing must heavily emphasize prompt engineering strategies to map the boundaries of expected system behavior.
* Validation requires designing test suites specifically targeted at identifying hallucinations, ensuring the model does not confidently invent incorrect information.
* QA pipelines must integrate automated evaluation frameworks (like LLM-as-a-judge) alongside rigorous human evaluation to scale the testing of non-deterministic content.

### Red Teaming
* Red teaming is a proactive, adversarial testing strategy where QA actively attempts to bypass the model's safety guardrails and alignment protocols.
* Testers construct malicious prompts to expose vulnerabilities such as prompt injection, data exfiltration, or the generation of toxic and biased content.
* From a security architecture perspective, red teaming evaluates the robustness of the input/output filtering layers wrapped around the core LLM component.
* The findings from continuous red teaming directly inform iterative fine-tuning and the reinforcement of ethical constraints within the system boundary.

### Hands-on Exercise: Exploratory Testing of a Large Language Model
* This practical exercise encourages QA to dynamically interact with the LLM, intuitively probing its conceptual boundaries and logical reasoning limits.
* Testers learn to identify context-window constraints by observing how the model handles extended conversations and potential loss of initial system instructions.
* The exercise highlights the critical difference between syntactic correctness (good grammar) and semantic accuracy (factual truth) in generated responses.
* By manipulating system prompts and temperature settings, testers directly observe how architectural configurations impact the model's creativity versus its reliability.

---

## Test Levels and Machine Learning Systems

### Test Levels for Machine Learning Systems
* Component testing in ML focuses strictly on the isolated model, verifying data pipelines, hyperparameter configurations, and core mathematical functional performance.
* Integration testing validates the critical interfaces between the non-deterministic ML model and the deterministic, conventional software ecosystem (e.g., APIs, databases, UI).
* System testing evaluates the entire architecture end-to-end, ensuring the AI subsystem meets overarching functional, non-functional, and security requirements.
* Acceptance testing shifts the focus to the business stakeholders, validating that the statistical performance of the AI translates to tangible user value and legal compliance.

### Risk-Based Testing of Machine Learning systems
* Due to the vast, virtually infinite input space of AI, risk-based testing is essential for prioritizing test efforts based on the probability and impact of model failures.
* Testers must categorize risks unique to ML, such as data poisoning, model evasion attacks, and the ethical implications of biased predictions impacting users.
* High-risk architectural components require more stringent statistical thresholds, extensive adversarial testing, and strict human-in-the-loop oversight mechanisms.
* Risk assessments must be continuously updated post-deployment, as data drift and environmental changes can rapidly elevate previously low-priority failure modes to critical threats.
---
[⬅️ Back to Main Guide](../README.md) | [Next: Module 5 ➡️](../Module5/file.md)
