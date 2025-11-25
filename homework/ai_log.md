# AI Log - Homework 2: Logistic Regression

## Date
2025-11-25

## AI Tool Used
Claude Code (Anthropic's Claude Sonnet)

## Summary of Assistance
I used Claude Code to help with understanding concepts, debugging code, and learning best practices for this assignment.

---

## Prompts and Usage

### 1. Environment Setup
**Prompt:** "Install conda and make an env BME i94"
**What I used:**
- Installed Miniconda
- Created conda environment with required packages (numpy, pandas, matplotlib, scikit-learn)
- Set up Jupyter kernel

### 2. Concept Explanations
**Prompt:** "Explain standardscaler, logisticregression, and pipeline functions in python"
**What I used:**
- Understanding of StandardScaler (z-score normalization)
- When to use LogisticRegression parameters (penalty, C, solver)
- Pipeline best practices to prevent data leakage
- Proper workflow order (split → pipeline → fit → evaluate)

**Prompt:** "What is training accuracy"
**What I used:**
- Understanding difference between training and testing accuracy
- How to identify overfitting vs underfitting
- Interpreting accuracy gaps

### 3. Debugging Assistance
**Prompt:** "Double check i did not make a logical error in l1 and l2 log reg models"
**What I used:**
- Learned key differences between L1 and L2 regularization
- L1 uses solver='liblinear', L2 uses solver='lbfgs'
- Understanding sparsity (non-zero coefficients)

**Prompt:** "How do i avoid tuple errors in this probabilities and roc procedure"
**What I used:**
- Understanding predict_proba() returns 2D array
- Extracting positive class probabilities with [:, 1]
- Proper usage of roc_curve() function

**Prompt:** "Still tuple error" / TypeError: 'tuple' object is not callable
**What I used:**
- Learned about variable name conflicts (don't overwrite function names)
- Fixed: `fpr, tpr, thresholds = roc_curve(...)` instead of `roc_curve = roc_curve(...)`
- Understanding tuple unpacking

### 4. Conceptual Understanding
**Prompt:** "If the threshold is an output of the roc function, how can i just 'use a threshold of 0.4'"
**What I used:**
- Understanding ROC curve shows all possible thresholds
- Manual threshold application: `(probabilities >= 0.4).astype(int)`
- When to use lower thresholds (medical screening - minimize false negatives)

---

## Code I Wrote Myself
- All data loading and exploration (Task 1)
- Train/test split and baseline model (Task 2)
- GridSearchCV implementation for L2 regularization (Task 3)
- L1 regularization pipeline (Task 4)
- ROC curve plotting and threshold analysis (Task 5)
- All analysis and written answers

## Code Snippets Used from AI
- Syntax for extracting positive class probabilities: `[:, 1]`
- ROC curve plotting template with proper labels
- Custom threshold application: `(probs >= threshold).astype(int)`
- Confusion matrix display formatting

---

## Declaration
I confirm that:
- I understood all code before using it
- All analysis and interpretations are my own
- I used AI only for syntax help, debugging, and concept clarification
- I did not ask for complete solutions to homework problems
