# Optimization Dynamics Study in CNNs  
## An Empirical Investigation of Optimizer Behavior on CIFAR-10  

**Author:** Srikant Reddy Nandireddy  
Graduate Student – Data Science & AI  

---

## 📌 Overview

This project investigates how optimization strategy influences convergence behavior, stability, and generalization performance in Convolutional Neural Networks (CNNs).

Rather than simply increasing architectural complexity, I conduct controlled experiments where the model architecture is fixed and only optimization dynamics are varied.

The goal is to understand how learning rate, momentum, adaptive updates, and weight decay affect training behavior and final performance.

---

## 🎯 Research Objectives

1. How sensitive is SGD to learning rate selection?  
2. Does momentum stabilize convergence in deep CNNs?  
3. How do adaptive optimizers (Adam) compare to non-adaptive methods (SGD)?  
4. Does decoupled weight decay (AdamW) improve generalization?  
5. How does optimizer choice affect the generalization gap?

---

## 📊 Dataset

- CIFAR-10  
- 60,000 RGB images (32×32)  
- 10 object classes  
- 50,000 training samples  
- 10,000 test samples  

Images are normalized to [0,1] and labels are one-hot encoded.

---

## 🏗 Controlled Architecture

The CNN architecture remains constant across all experiments:

- 2 Convolutional Blocks (32 → 64 filters)
- Batch Normalization
- Max Pooling
- Dropout Regularization
- Fully Connected Layer (512 units)
- Softmax Output Layer

Regularization:
- Dropout
- L2 Weight Decay

This ensures performance differences arise from optimization dynamics rather than architectural changes.

---

## 🧪 Optimization Experiments

I evaluated:

- SGD (learning rate sensitivity: 0.01 vs 0.001)
- SGD + Momentum (0.9)
- Adam
- AdamW (decoupled weight decay)

All experiments used:
- Same batch size
- Same epoch limit
- Early stopping
- Same validation split

---

## 📊 Evaluation Metrics

- Training Accuracy  
- Validation Accuracy  
- Test Accuracy  
- Generalization Gap (Train − Validation)  
- Training Time  
- Confusion Matrix  
- Per-Class Precision, Recall, F1-score  

---

## 📈 Key Findings

- SGD is highly sensitive to learning rate selection.
- Momentum significantly stabilizes convergence.
- Adam accelerates convergence and narrows the generalization gap.
- AdamW improves stability through decoupled weight decay.
- Optimization dynamics influence performance as much as architectural depth.

In this controlled setup, optimizer selection produced larger performance gains than increasing architectural complexity alone.

---

## 🛠 Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  

---

## 🧠 Conclusion

Deep learning performance is not solely determined by model depth.

Effective generalization depends on:

- Careful optimizer selection  
- Learning rate tuning  
- Momentum control  
- Regularization strategy  
- Monitoring validation divergence  

This study highlights the importance of disciplined experimentation when training deep neural networks.

---

## 🚀 How to Run

1. Clone the repository  
2. Install required dependencies  
3. Run the notebook: `CNN_Optimization_Study.ipynb`  

---

## 📬 Contact

Srikant Reddy Nandireddy  
Open to Data Science | Machine Learning | Generative AI opportunities