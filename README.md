# Advanced Linear Algebra: Principal Component Analysis (PCA) Assignment

## 📋 Overview

This formative assignment guides you through implementing Principal Component Analysis (PCA) from scratch using NumPy. You'll work with an Africanized economic dataset to understand dimensionality reduction, feature relationships, and the mathematical foundations of PCA.

## 🎯 Learning Objectives

By completing this assignment, you will:
- Understand the importance of data standardization in PCA
- Learn to calculate covariance matrices and perform eigendecomposition
- Implement PCA step-by-step without using sklearn
- Analyze explained variance and component selection
- Visualize high-dimensional data reduction
- Work with real-world African economic crisis data

## 📊 Dataset

**Source**: Africa Economic, Banking and Systemic Crisis Data
- **Kaggle**: [Africa Economic Crisis Dataset](https://www.kaggle.com/datasets/chirin/africa-economic-banking-and-systemic-crisis-data)
- **Google Drive**: Accessible via the provided file ID in the notebook
- **Features**: Economic indicators including GDP, inflation, currency crises, debt defaults, and systemic crises across African countries

## 🛠️ Requirements

### Python Libraries
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt  # For visualization
```

### Key Concepts Covered
- Data standardization (Z-score normalization)
- Covariance matrix calculation
- Eigenvalue decomposition
- Principal component selection
- Data projection and dimensionality reduction
- Explained variance analysis

## 📝 Assignment Steps

### Step 1: Data Loading and Standardization
- Load the African economic crisis dataset from Google Drive
- Remove non-numeric columns
- **Implement standardization manually** using NumPy (not sklearn)
- Formula: `(X - μ) / σ` where μ is mean and σ is standard deviation

### Step 2: Covariance Matrix Calculation
- Calculate the covariance matrix of standardized data
- Understand feature relationships through covariance values

### Step 3: Eigendecomposition
- Perform eigenvalue decomposition on the covariance matrix
- Extract eigenvalues and eigenvectors

### Step 4: Principal Component Sorting
- Sort eigenvectors by eigenvalues in descending order
- Understand the concept of explained variance
- Answer: "How Is Explained Variance Used In PCA?"

### Step 5: Data Projection
- **Complete the missing code** to:
  - Choose the number of principal components
  - Project original data onto selected components
  - Reduce dimensionality

### Step 6: Results Analysis
- Display reduced data dimensions
- Compare original vs. reduced data

### Step 7: Visualization
- **Complete the missing code** to:
  - Plot original data (first two features)
  - Plot reduced data after PCA
  - Compare visual representations

## ✅ Submission Requirements

### Code Completion
Complete the following missing sections:
1. **Step 6**: Define `num_components` and implement `reduced_data` calculation
2. **Step 8**: Create visualization plots for before/after PCA comparison

### Output Display
- Ensure all code cells show their outputs when executed
- Include printed results, arrays, and visualizations
- Display the first 5 rows of transformed data

### Theoretical Understanding
Answer the question: **"How Is Explained Variance Used In PCA?"**

## 🔍 Key Implementation Notes

### Standardization (Step 1)
```python
# Manual implementation required - no sklearn
mean = np.mean(data, axis=0)
std = np.std(data, axis=0)
standardized_data = (data - mean) / std
```

### PCA Transformation (Step 6)
You need to complete:
```python
num_components = ?  # Choose appropriate number
reduced_data = ?    # Project using: standardized_data @ eigenvectors[:, :num_components]
```

### Visualization (Step 8)
Create comparative plots showing:
- Original data scatter plot (2D)
- PCA-transformed data scatter plot (2D)

## 📈 Expected Outcomes

After completion, you should have:
- Standardized dataset with mean=0, std=1
- 11×11 covariance matrix showing feature relationships
- Sorted eigenvalues indicating component importance
- Reduced dataset with chosen dimensionality
- Visual comparison of original vs. PCA-transformed data

## 🎓 Assessment Criteria

- **Code Implementation** (40%): Correct completion of missing code sections
- **Output Display** (20%): All cells show proper execution results
- **Theoretical Understanding** (20%): Explained variance question answer
- **Visualization** (20%): Clear, labeled plots comparing before/after PCA

## 💡 Tips for Success

1. **Choose components wisely**: Look at eigenvalues to determine how many components capture most variance
2. **Understand the math**: Each step builds on the previous - understand why standardization is crucial
3. **Interpret results**: Consider what the principal components represent in terms of the original economic features
4. **Visualize effectively**: Use clear labels, titles, and legends in your plots

## 🔗 Additional Resources

- **Anthropic Documentation**: For prompting and API usage
- **NumPy Documentation**: For array operations and linear algebra functions
- **Matplotlib Documentation**: For creating effective visualizations
- **PCA Theory**: Review eigenvalue decomposition and linear transformations
