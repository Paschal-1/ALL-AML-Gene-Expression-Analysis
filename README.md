# ALL vs AML Gene Expression Analysis and Machine Learning Classification

## Project Overview

This project investigates gene expression patterns in **Acute Lymphoblastic Leukemia (ALL)** and **Acute Myeloid Leukemia (AML)** using statistical analysis, data visualization, and machine learning techniques.

The study utilizes one of the most widely used benchmark datasets in bioinformatics, containing expression measurements of **7,129 genes** across leukemia patient samples. The aim of this project is to identify differences in gene expression between ALL and AML, explore potential biomarker genes, and evaluate the ability of machine learning algorithms to classify leukemia subtypes.

This project represents my first hands-on application of computational biology and bioinformatics methods and marks an important step in my transition into genomics and data-driven biological research.

---

## Research Objectives

* Investigate differences in gene expression profiles between ALL and AML patients.
* Perform exploratory and statistical analysis of high-dimensional genomic data.
* Visualize sample clustering using dimensionality reduction techniques.
* Build predictive machine learning models for leukemia classification.
* Identify potential biomarker genes associated with disease differentiation.
* Develop practical experience in computational genomics workflows.

---

## Dataset Description

The dataset contains:

* **7,129 gene expression measurements**
* **72 leukemia patient samples**
* Two disease classes:

  * Acute Lymphoblastic Leukemia (ALL)
  * Acute Myeloid Leukemia (AML)

### Dataset Files

| File                               | Description                      |
| ---------------------------------- | -------------------------------- |
| `data_set_ALL_AML_train.csv`       | Training gene expression dataset |
| `data_set_ALL_AML_independent.csv` | Independent test dataset         |
| `actual.csv`                       | Patient diagnosis labels         |

---

## Methodology

### 1. Data Preprocessing

* Data inspection and cleaning
* Removal of non-expression columns
* Data transposition for machine learning compatibility
* Label encoding
* Missing value assessment
* Standardization of gene expression values

### 2. Exploratory Data Analysis (EDA)

* Summary statistics
* Distribution analysis
* Correlation assessment

### 3. Dimensionality Reduction

* Principal Component Analysis (PCA)
* t-distributed Stochastic Neighbor Embedding (t-SNE)

### 4. Differential Gene Expression Analysis

* Statistical comparison between ALL and AML samples
* Identification of significantly expressed genes
* Volcano plot visualization

### 5. Machine Learning Classification

* Random Forest Classifier
* Support Vector Machine (SVM)
* Model evaluation using:

  * Accuracy
  * Confusion Matrix
  * Classification Report

### 6. Biomarker Identification

* Feature importance analysis
* Identification of genes with high predictive contribution

---

## Repository Structure

```text
ALL-AML-Gene-Expression-Analysis
│
├── data
│   ├── data_set_ALL_AML_train.csv
│   ├── data_set_ALL_AML_independent.csv
│   └── actual.csv
│
├── notebooks
│   └── ALL_AML_Gene_Expression_Analysis.ipynb
│
├── figures
│   ├── pca_plot.png
│   ├── tsne_plot.png
│   ├── volcano_plot.png
│   ├── heatmap.png
│   └── confusion_matrix.png
│
├── results
│   ├── differential_expression.csv
│   └── feature_importance.csv
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Technologies and Tools

* Python
* Pandas
* NumPy
* Scikit-Learn
* SciPy
* Matplotlib
* Seaborn
* Google Colab
* GitHub

---

## Project Outputs

* Cleaned and processed gene expression dataset
* PCA visualization of leukemia samples
* t-SNE clustering analysis
* Differential gene expression analysis results
* Heatmap and clustering visualizations
* Machine learning classification models
* Biomarker identification results

---

## Skills Demonstrated

* Data Cleaning and Preprocessing
* Statistical Analysis
* Machine Learning
* Data Visualization
* Bioinformatics Workflow Development
* Reproducible Research Practices
* Scientific Computing with Python
* Genomic Data Analysis

---

## Results and Findings

### Principal Component Analysis (PCA)

The PCA plot below summarizes the expression of 7,129 genes into two principal components (PC1 and PC2).

![PCA Plot](figures/pca_plot.png)

**Interpretation**

* Each point represents one patient sample.
* Blue and red points represent different leukemia classes.
* The plot shows partial separation between ALL and AML samples.
* Some overlap exists, indicating that while the two leukemia types have distinct gene expression patterns, they are not completely separable.

**Key Finding:** Gene expression profiles contain meaningful biological information that can help distinguish between ALL and AML.

---

### t-SNE Visualization

t-SNE was used to further explore similarities among patient samples.

![t-SNE Plot](figures/tsne_plot.png)

**Interpretation**

* Samples belonging to similar disease types tend to cluster together.
* The clustering patterns suggest the presence of subtype-specific gene expression signatures.
* Some overlap remains, which is expected in real biological datasets.

**Key Finding:** The data contains meaningful structure and evidence of molecular differences between ALL and AML.

---

### Differential Gene Expression Analysis

The volcano plot displays the statistical significance of each gene.

![Volcano Plot](figures/volcano_plot.png)

**Interpretation**

* Each point represents one gene.
* Genes higher on the plot are more statistically significant.
* Only a relatively small number of genes show highly significant differences between ALL and AML.
* Most genes exhibit minimal differences in expression.

**Key Finding:** A subset of genes may serve as potential biomarkers capable of distinguishing the two leukemia subtypes.

---

### Heatmap and Hierarchical Clustering

The heatmap below shows the expression patterns of the most significant genes across patient samples.

![Heatmap](figures/heatmap.png)

**Interpretation**

* Yellow colors represent high gene expression.
* Purple colors represent low gene expression.
* Several groups of patients display similar expression patterns.
* Certain genes appear to be highly expressed only in specific patient groups.

**Key Finding:** These expression patterns indicate the presence of disease-specific transcriptional signatures and potential biomarker genes.

---

### Machine Learning Classification

The confusion matrix below summarizes the performance of the Random Forest classifier.

![Confusion Matrix](figures/confusion_matrix.png)

#### Model Performance

| Metric   | Value |
| -------- | ----- |
| Accuracy | 67.6% |

#### Confusion Matrix

| Actual Class | Predicted ALL | Predicted AML |
| ------------ | ------------- | ------------- |
| ALL          | 19            | 1             |
| AML          | 10            | 4             |

**Interpretation**

* 19 ALL samples were correctly classified.
* 4 AML samples were correctly classified.
* 1 ALL sample was incorrectly classified as AML.
* 10 AML samples were incorrectly classified as ALL.

The model demonstrated stronger performance in identifying ALL than AML samples.

Although the predictive performance can be improved through advanced feature selection, hyperparameter tuning, and larger datasets, the results demonstrate the potential of gene expression data for disease classification.

---

### Overall Conclusion

This project successfully implemented an end-to-end bioinformatics workflow involving:

* Data preprocessing and cleaning
* Exploratory data analysis
* Dimensionality reduction using PCA and t-SNE
* Differential gene expression analysis
* Heatmap visualization and hierarchical clustering
* Machine learning classification
* Preliminary biomarker identification

The findings demonstrate that gene expression data contains biologically meaningful information that can partially distinguish between ALL and AML leukemia samples.

As my first genomics and bioinformatics project, this work provided valuable hands-on experience in computational biology, statistical analysis, and machine learning applications in healthcare. It also strengthened my interest in applying computational methods to real-world biological problems and serves as a foundation for future work in bioinformatics, genomics, and precision medicine.


## Learning Outcomes

Through this project, I gained practical experience in:

* Handling high-dimensional genomic datasets.
* Applying statistical methods to biological data.
* Building reproducible bioinformatics workflows.
* Using machine learning techniques for disease classification.
* Interpreting biological data through computational approaches.
* Documenting and organizing scientific analyses for reproducibility.

---

## Future Work

This project serves as a foundation for further exploration in:

* RNA-Seq analysis pipelines
* Functional enrichment analysis
* Pathway analysis
* Gene regulatory network analysis
* Deep learning applications in genomics
* Multi-omics data integration

I am particularly interested in applying computational approaches to real-world biological and healthcare challenges and look forward to contributing to research projects that bridge data science and life sciences.

---

## Personal Statement

As a biochemistry graduate transitioning into bioinformatics and genomics, this project represents both a learning experience and a commitment to continuous growth in computational biology.

While this project is exploratory in nature, it reflects my curiosity, willingness to learn, and determination to develop the technical and scientific skills necessary to contribute meaningfully to genomics research and data-driven biological discovery.

I remain eager to collaborate, continue learning, and take on increasingly challenging real-world projects that expand my understanding of biological systems and computational methods.

---

## Author

**Paschal Chukwunonso Ofodile**

Data Analyst | Biochemist | Aspiring Bioinformatician and Genomics Researcher

GitHub: https://github.com/Paschal-1

LinkedIn: *Add your LinkedIn profile here*

---

## Acknowledgements

This project uses the publicly available ALL vs AML leukemia gene expression dataset, which has been widely used for educational purposes and methodological demonstrations in bioinformatics and machine learning research.
