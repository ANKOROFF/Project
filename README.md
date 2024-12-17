
# **Vision Transformer Optimization with Decomposition Methods**

## **Overview**  
This project focuses on optimizing Vision Transformer (ViT) models by reducing the computational cost of the **Multi-Head Self-Attention (MSA)** mechanism. We leverage advanced mathematical techniques, including **Cholesky decomposition**, **Singular Value Decomposition (SVD)**, **Principal Component Analysis (PCA)**, and **Tensor Decomposition**, to enhance efficiency, scalability, and numerical stability.

---

## **Key Features**  
- **Cholesky Decomposition**: Simplifies positive-definite matrix operations for computational efficiency.  
- **Low-Rank SVD Approximation**: Reduces attention matrix rank, retaining only the most significant components.  
- **PCA for Dimensionality Reduction**: Compresses attention matrices while preserving essential information.  
- **Tensor Decomposition**: Optimizes higher-dimensional representations for improved memory and computational performance.

---

## **Motivation**  
The Multi-Head Self-Attention mechanism in ViT models introduces quadratic complexity \( O(N^2) \), where \( N \) is the sequence length (number of image patches). This becomes computationally expensive for high-resolution images. To address this:  
1. We employ decomposition techniques to reduce attention matrix dimensions.  
2. We enhance computational efficiency and reduce memory overhead.  
3. The proposed methods ensure the model remains scalable and interpretable.

---

## **Repository Structure**  

```
/VisionTransformer-Optimization
│
├── data/                         # Input datasets for training and evaluation
├── src/                          # Source code
│   ├── attention_optimization.py # Core code for MSA optimization
│   ├── svd_decomposition.py      # SVD implementation
│   ├── cholesky_optimization.py  # Cholesky decomposition implementation
│   ├── pca_optimization.py       # PCA for attention matrices
│   ├── tensor_decomposition.py   # Tensor decomposition techniques
│
├── notebooks/                    # Jupyter Notebooks for analysis and experiments
│   ├── ViT_optimization_demo.ipynb
│
├── results/                      # Results, logs, and model performance metrics
│   ├── attention_comparison.png  # Visual comparison before/after optimization
│   └── metrics.csv               # Numerical performance results
│
├── README.md                     # Project documentation
└── requirements.txt              # Python dependencies
```

---

## **Installation**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/VisionTransformer-Optimization.git
   cd VisionTransformer-Optimization
   ```

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

---

## **Usage**  
### **Running the Optimization**  
Execute the main optimization script to apply decomposition methods to the ViT:  
```bash
python src/attention_optimization.py --method svd --input data/sample_image.png
```

### **Available Decomposition Methods**:  
- `svd` - Singular Value Decomposition  
- `cholesky` - Cholesky Decomposition  
- `pca` - Principal Component Analysis  
- `tensor` - Tensor Decomposition  

Example with Cholesky:  
```bash
python src/attention_optimization.py --method cholesky
```

---

## **Results**  
1. **Computational Complexity Reduction**:  
   - SVD and PCA significantly reduce the size of the attention matrices.  
2. **Performance Metrics**:  
   - Improvements in FLOPs and model inference time.  
   - Comparisons before and after applying decomposition methods.  


---

## **Future Work**  
- Explore adaptive sparsity in attention matrices.  
- Integrate quantization techniques for further efficiency.  
- Apply methods to other transformer-based architectures.

---

## **Contributors**  
Kornienko Dmitrii
Lukina Svetlana
Rahmatulin Oleg
Zavadskaya Lyudmila
Filin Andrey 

---

## **License**  
This project is licensed under the **Skoltech License**.  

---

## **References**  
1. Dosovitskiy, A., et al. *An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale.*  
2. Yu, C., et al. *Boost Vision Transformer with GPU-Friendly Sparsity and Quantization.*  
3. Lin, Z., et al. *Efficient Self-Attention Mechanisms for Transformers.*  

---

This structure provides clarity, easy navigation, and highlights the methods, motivation, and results of your project.
