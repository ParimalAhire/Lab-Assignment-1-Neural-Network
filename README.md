# Lab-Assignment-1-Neural-Network

## Description
This project implements a **Feedforward Neural Network** in three ways:
1. **From Scratch** using Python and NumPy only — manual forward pass, backpropagation, and gradient descent
2. **Using Keras** — high-level TensorFlow/Keras Sequential API
3. **Using Scikit-learn** — MLPClassifier with MultiOutputClassifier

The network is trained to learn **five logical gate functions simultaneously** (XOR, AND, OR, NAND, NOR) and results are compared across all three implementations.

---

## Objective
To understand and implement neural networks at different levels of abstraction:
- Forward propagation
- Loss calculation (MSE)
- Backpropagation
- Gradient descent weight updates
- Using high-level libraries (Keras, Scikit-learn) for the same task
- Comparing all three approaches

---

## Algorithm Used
**Feedforward Neural Network with Backpropagation**

The network architecture is the same across all three parts:
- Input layer — 2 neurons
- Hidden layer — 5 neurons (sigmoid activation)
- Output layer — 5 neurons (sigmoid activation)

| Part | Method | Optimizer |
|---|---|---|
| From Scratch | Manual backpropagation | Gradient Descent |
| Keras | Sequential API | Adam |
| Scikit-learn | MLPClassifier | lbfgs |

---

## Dataset
A single shared dataset is used across all three implementations:

| Input (A, B) | XOR | AND | OR | NAND | NOR |
|:---:|:---:|:---:|:---:|:---:|:---:|
| [0, 0] | 0 | 0 | 0 | 1 | 1 |
| [0, 1] | 1 | 0 | 1 | 1 | 0 |
| [1, 0] | 1 | 0 | 1 | 1 | 0 |
| [1, 1] | 0 | 1 | 1 | 0 | 0 |

All binary combinations of two inputs are used. The network learns 5 logical gate outputs simultaneously.

---

## Notebook Structure

```
Step 1  → Import all libraries (once, shared)
Step 2  → Define shared dataset (once, shared)
─────────────────────────────────────────────
Part 1  → ANN From Scratch       (Steps 3–6)
Part 2  → ANN Using Keras        (Steps 7–8)
Part 3  → ANN Using Sklearn      (Steps 9–10)
─────────────────────────────────────────────
Part 4  → Comparison of results  (Steps 11–12)
─────────────────────────────────────────────
Step 13 → Single combined user input test
          (all 3 models output together)
```

> **Note:** Imports and dataset are defined **once at the top** and shared by all three parts. To change the dataset, only edit Step 2.

---

## Features

- Three implementations of the same ANN for direct comparison
- Single shared dataset and imports — no repetition
- Weight updates printed every 100 epochs (from scratch)
- Loss vs Epoch graph for both From Scratch and Keras
- Combined loss curve comparison (Scratch vs Keras)
- Single user input cell tests all three models at once

---

## How to Run

1. Open the notebook:
   ```
   NN_Assignment1_Final.ipynb
   ```

2. Run all cells in order (Runtime → Run All in Colab)

3. Observe:
   - Weight updates every 100 epochs (Part 1)
   - Loss decreasing over time (all parts)
   - Prediction tables vs expected values
   - Side-by-side comparison of all three models

4. At **Step 13**, enter custom binary input values (0 or 1) when prompted — all three models will output results together

---

## Requirements

```
numpy
matplotlib
tensorflow / keras
scikit-learn
```

Install with:
```bash
pip install numpy matplotlib tensorflow scikit-learn
```

---

## Results

All three approaches successfully learn all five logic gate functions:

| Model | Accuracy |
|---|---|
| From Scratch | ~100% |
| Keras | ~100% |
| Scikit-learn | ~100% |

---

## Applications of Neural Networks

- **Image recognition** — Facial recognition, object detection, medical imaging
- **Speech processing** — Voice assistants, speech-to-text
- **Fraud detection** — Identifying suspicious transactions
- **Medical diagnosis** — Disease prediction from patient data
- **Recommendation systems** — Netflix, YouTube, Amazon suggestions
- **Autonomous systems** — Self-driving cars, robotics

---

## Conclusion

This assignment implemented a feedforward neural network in three ways to learn five logic gates simultaneously:

1. **From Scratch (NumPy):** Manually coded forward pass, backpropagation, and gradient descent. Provides full transparency into how weights are updated at each step.

2. **Keras:** High-level API with minimal code. Adam optimizer gave faster convergence compared to plain gradient descent.

3. **Scikit-learn:** MLPClassifier with MultiOutputClassifier wrapper. Simplest to implement for quick baselines.

All three approaches successfully learned all five gate functions, demonstrating how the same neural network concept can be implemented at different levels of abstraction. The key takeaway is that while From Scratch gives full control and understanding, Keras and Scikit-learn offer speed and simplicity for real-world use.

---

**Name:** Parimal Ahire  
**PRN:** 202301040067  
**Course:** Deep Learning Lab
