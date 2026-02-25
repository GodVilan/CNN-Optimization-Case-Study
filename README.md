# CNN Optimization Case Study  
## Architecture vs Optimizer Impact on CIFAR-10  

**Author:** Srikant Reddy Nandireddy  
Graduate Student – Data Science & AI  

---

## 📌 Overview

This project investigates how architectural depth and optimizer selection impact Convolutional Neural Network (CNN) performance on the CIFAR-10 dataset.

Rather than simply increasing model complexity, this study evaluates how training dynamics and optimization strategy influence generalization.

---

## 🎯 Research Questions

1. Does increasing CNN depth improve performance?  
2. How significantly does optimizer choice affect convergence and generalization?  
3. How can overfitting be diagnosed using validation behavior?  

---

## 📊 Dataset

- CIFAR-10  
- 60,000 RGB images (32×32)  
- 10 object classes  
- 50,000 training samples  
- 10,000 test samples  

---

## 🏗 Model Architectures

### Baseline CNN
- Conv(32) → MaxPooling  
- Dense(128)  
- Softmax Output  

### Deep CNN
- 3 Convolutional Blocks (32 → 64 → 128 filters)  
- Dropout Regularization  
- Fully Connected Layers (1024 → 512)  
- Softmax Output  

**Total parameters:** ~2.9M  

---

## 🧪 Experiments & Results

| Model | Optimizer | Test Accuracy |
|-------|-----------|--------------|
| Baseline CNN | SGD | **60.05%** |
| Deep CNN | SGD | **69.90%** |
| Deep CNN | Adam | **77.04%** |

---

## 🔎 Key Findings

- Increasing architectural depth improved representational capacity (+9.85% over baseline).  
- Deep CNN trained with SGD exhibited validation divergence, indicating overfitting.  
- Replacing SGD with Adam improved performance by over 7%.  
- Optimization strategy had a larger impact on generalization than architectural complexity alone.  

---

## 📈 Training Analysis

Validation curves revealed:

- Training accuracy continued increasing.  
- Validation accuracy plateaued when using SGD.  
- Adam provided smoother convergence and better stability.  

This highlights the importance of monitoring validation behavior rather than relying solely on training accuracy.

---

## 🛠 Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  

---

## 🧠 Conclusion

This case study demonstrates that CNN performance is strongly influenced by optimization dynamics and training configuration.

While architectural depth increases representational power, effective generalization depends on:

- Optimizer selection  
- Validation monitoring  
- Controlled experimentation  
- Overfitting diagnosis  

Deep learning performance is driven by disciplined experimentation — not just stacking additional layers.

---

## 📬 Contact

**Srikant Reddy Nandireddy**  
Graduate Student – Data Science & AI  
Open to Data Science / Machine Learning opportunities  