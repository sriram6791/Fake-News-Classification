# **Fake News Classification**  

Welcome to the **Fake News Classification** project! This repository showcases a machine learning approach to detecting fake news using two powerful models: **LSTM** and **Transformer**.  

The project includes detailed comparisons of performance on single and multi-GPU setups, illustrating the capabilities and trade-offs of distributed training.  

---  

## **Dataset**  
The dataset used in this project is the **Fake News Classification Dataset**, sourced from [Kaggle](https://www.kaggle.com/datasets/aadyasingh55/fake-news-classification).  

### **Key Features of the Dataset**  
- **Size**: Over 45,000 unique news articles.  
- **Language**: English (en-US).  
- **Structure**:  
  - `Title`: The title of the news article.  
  - `Text`: The full content of the article.  
  - `Label`: Binary classification indicating whether the news is fake (0) or true (1).  
- **Splits**:  
  - Train: 24,353 instances  
  - Validation: 8,117 instances  
  - Test: 8,117 instances  

### **Why This Dataset?**  
This dataset is well-suited for tasks like:  
- Text classification  
- Fact-checking  
- Intent classification  

Special thanks to **Kaggle** for providing this valuable resource! 🙌  

---  

## **Approach**  

This project explores two deep learning architectures:  

### **1. LSTM Model**  
- **Architecture**: A Bidirectional LSTM (Long Short-Term Memory) model was used to capture both forward and backward dependencies in the text data.  
- **Performance**: Achieved a remarkable **accuracy of 99.96%** on the test set.  
- **Training Time**: Approximately **364 seconds per epoch** on a single GPU.  

### **2. Transformer Model**  
- **Architecture**: A simplified Transformer model with multi-head attention and feed-forward layers, optimized to fit GPU memory constraints on a local machine.  
- **Performance**: Achieved an accuracy of **98.3%** on the test set.  
- **Training Time**: Approximately **478 milliseconds per step** on a single GPU.  

---

## **Results and Key Insights**  

| **Metric**            | **LSTM**                 | **Transformer**           |  
|-----------------------|--------------------------|----------------------------|  
| **Accuracy**          | **99.96%**              | **98.3%**                 |  
| **Training Time**     | 364 seconds per epoch   | 478 milliseconds per step |  
| **Suitability**       | Sequential data tasks   | Long-range dependencies and parallel processing |  

### **Analysis**  
- **Accuracy**: The LSTM model outperformed the Transformer in this task, achieving higher test accuracy.  
- **Speed**: The Transformer model demonstrated faster training per step due to its parallel processing capabilities.  
- **Constraints**: The simplified Transformer architecture was used to fit within GPU memory constraints, which may have affected its performance.  

---

## **Why This Project?**  
This project serves as a practical demonstration of:  
1. **Deep Learning for NLP**: Applying state-of-the-art models to a real-world problem.  
2. **Model Trade-Offs**: Evaluating the strengths and weaknesses of LSTM and Transformer architectures.  

---

## **Credits**  
- **Dataset**: Thanks to [Kaggle](https://www.kaggle.com/datasets/aadyasingh55/fake-news-classification) for providing the dataset.  
---  
## **Hardware Specifications**  

The local GPU training was conducted on the following hardware:  

- **Processor**: Intel Core **i7-13650H**  
- **GPU**: NVIDIA **RTX 3070 Laptop GPU** (8GB VRAM)  
- **RAM**: 16GB  

### **Training Time**  
- **Total Training Time**:
  - Approximately **5 hours** for 50 epochs (Transformer model) on the local GPU. 🚀
  - Approximately **40 minutes** for 5 epochs (LSTM model) 
---
## **Conclusion**  
This project highlights the power of machine learning in tackling fake news detection. Both the **LSTM** and **Transformer** models demonstrated strong performance, with the choice between them depending on task-specific requirements.  

Feel free to explore, experiment, and adapt this project for your own use cases. 📰✨
