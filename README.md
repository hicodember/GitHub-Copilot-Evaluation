# GitHub-Copilot-Evaluation
This project presents a structured evaluation of GitHub Copilot as a production AI-assisted development tool.

# CS 530 - AI Principles and Applications
### 9-1 Final Project: GitHub Copilot Evaluation

---

## Project Overview

This project presents a structured evaluation of **GitHub Copilot** as a production AI-assisted development tool for a fictional enterprise client, **TechNova Solutions** a mid-sized software company in the healthcare and finance sectors. The evaluation covers code analysis, prompt engineering, debugging, code generation, and ethical risk assessment.

> **Course:** CS-530 AI Principles and Applications  
> **Student:** Amber (Ember) Foster  
> **Instructor:** Joshua Andrews  
> **Date:** April 2026  

---

## Repository Structure

```
cs530-copilot-evaluation/
│
├── README.md                        ← You are here
│
├── chat-logs/
│   ├── PartOne.json                 ← Part 1: Evaluate & debug chat logs (5 conversations)
│   └── PartTwo.json                 ← Part 2: Code generation chat logs (5 pipeline steps)
│
└── report/
    └── 9-1_Project.docx             ← Full written evaluation summary (APA cited)
```

---

## Part One: AI Tool Evaluation (Chat Logs)

Five separate chat contexts were created in GitHub Copilot. Each began with a fresh context window, an initial prompt, iterative refinements, and a corrected/generated output.

| Chat   | Task                | Snippet Topic                                                      |
|--------|---------------------|--------------------------------------------------------------------|
| Chat 1 | Evaluate + Debug    | Two layer neural network with broken slicing, missing return value |
| Chat 2 | Evaluate + Debug    | Employee payroll processor for syntax, logic, and runtime errors   |
| Chat 3 | Generate + Evaluate | Single neuron with sigmoid and ReLU activation functions           |
| Chat 4 | Generate + Evaluate | Binary classifier + synthetic dataset generator                    |
| Chat 5 | Generate + Evaluate | Gradient descent weight calculator + full test suite               |

**Prompt Engineering Techniques Applied:**
- Role scoped context setting before each snippet
- Iterative refinement to reduce hallucinations
- Explicit requests for header comment generation
- Constraint framing ("use only basic math and Python lists")
- Step by step decomposition for complex generation tasks

---

## Part Two: Code Generation Pipeline (Chat Logs)

A complete neural network inference pipeline was generated incrementally using GitHub Copilot in a single conversation thread and each step building on the functions defined previously.

```
Step A → single_neuron()         Weighted sum + sigmoid/ReLU activation
Step B → binary_classifier()     Thresholded output from neuron
Step C → generate_dataset()      Deterministic synthetic binary dataset
Step D → compute_simple_weights() Centroid based heuristic weight calculator
Step E → run_demo()              End to end pipeline orchestration
```

All functions were generated without NumPy or external libraries and pure Python only.

---

## Evaluation Summary (Written Report)

The written report addresses the following for a non-technical audience:

| No | Topic                                                                           |
| -- | --------------------------------------------------------------------------------|
| 1  | Machine learning vs. deep learning in Copilot's underlying model                |
| 2  | How NLP interprets developer input to produce code                              |
| 3  | Copilot vs. other AI dev tools (Tabnine, CodeWhisperer, Cursor)                 |
| 4  | Real world problem solving across programming domains                           |
| 5  | Copilot attributes and limitations                                              |
| 6  | Ethical risks of AI-generated code                                              |
| 7  | Training data bias and its effect on recommendations                            |
| 8  | Privacy and transparency risks in AI-assisted development                       |
| 9  | Legal and security risk mitigation strategies                                   |
| 10 | Long term impact on workforce roles, developer autonomy, and industry standards |

---

## Key Findings

- **Code generation quality** is strongest for well-scoped, pattern consistent tasks (activation functions, classifiers, utility functions) and degrades on ambiguous or highly novel prompts.
- **Hallucination reduction** is most effective when prompts include explicit constraints, expected output format, and domain scope.
- **Bias in training data** can manifest as stylistic defaults (e.g., preferring NumPy) or subtly incorrect assumptions about data distributions.
- **Intellectual property risk** remains unresolved and Copilot occasionally reproduces training code verbatim without attribution.
- **Developer autonomy** is enhanced for boilerplate and accelerated for ideation, but critical review of all generated output remains essential.

---

## Ethical Considerations

This project surfaces several ethical concerns relevant to enterprise deployment:

- **Copyright & IP:** Generated code may include fragments from licensed open source repositories
- **Security vulnerabilities:** AI may reproduce insecure patterns (e.g., SQL injection, hardcoded credentials)
- **Bias propagation:** Dominant languages and frameworks in training data skew recommendations
- **Privacy:** Prompts containing proprietary logic may influence future model training
- **Transparency:** Developers may not recognize when suggestions are statistically plausible but logically incorrect

---

## References

- Géron, A. (2019). *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (2nd ed.). O'Reilly Media.
- zyBooks. (2026). *Artificial Intelligence: Principles and Applications* (Modules 1–11).

---

*This project was completed as part of the M.S. Computer Science program (2026). All AI interactions were conducted using Microsoft GitHub Copilot.*
