# Integrative Machine Learning Analysis of Genomic and Clinical Data for Breast Cancer

To develop an integrative machine learning model that can analyze and interpret the complex relationships between genomic data and clinical outcomes in breast cancer patients.

### Project Description:
Breast cancer, a complex and heterogeneous disease, presents significant challenges in diagnosis, treatment, and prognosis. Advances in genomic sequencing and clinical data collection have opened new avenues for understanding this disease at a molecular level. However, the sheer volume and complexity of the data demand sophisticated analytical approaches.

This project aims to harness the power of machine learning to integrate and analyze extensive genomic and clinical data, specifically focusing on breast cancer. Utilizing the METABRIC (Molecular Taxonomy of Breast Cancer International Consortium) dataset, which includes comprehensive gene expression profiles and clinical information from breast cancer patients, this research seeks to uncover novel insights and patterns that could contribute to personalized medicine and improved treatment strategies.

***Dataset source:***  [Breast-Cancer-Dataset](https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric/data)

This dataset will facilitate meaningful insights and potentially reveal new correlations and patterns important for personalized medicine and therapeutic advancements.

*METABRIC_RNA_Mutation_without_Mutation_Data_3.csv*: 520 columns (498-Genomic Profiles), 1904 entries, 
Note: 173 mutation columns are removed from the original [Breast-Cancer-Dataset]

***Dataset Structure:*** It contains 1904 entries and 693 (520 excluding mutation data) columns. Columns include a mix of numerical and categorical data types.

1. Data Exploration and Preprocessing
2. Exploratory Data Analysis (EDA) 



***Clinical Data Columns:***
Clinical Data are vital for understanding patient demographics, cancer characteristics, treatment types, and outcomes. These variables can be used to correlate with genomic data and identify patterns in treatment response, survival rates, and cancer subtypes.

These columns are related to patient information, clinical characteristics, and treatment details.

- Patient Information: 
    patient_id, age_at_diagnosis
- Cancer and Treatment Details: 
    type_of_breast_surgery, cancer_type, cancer_type_detailed, cellularity chemotherapy, hormone_therapy, radio_therapy
- Biological and Clinical Markers: 
    er_status_measured_by_ihc, er_status, pr_status, her2_status_measured_by_snp6, her2_status, 3-gene_classifier_subtype
- Cancer Characteristics:(Clinical metrics important in cancer diagnosis and staging) 
    neoplasm_histologic_grade, tumor_other_histologic_subtype, tumor_size, tumor_stage primary_tumor_laterality, lymph_nodes_examined_positive
- Prognostic Indices: 
    nottingham_prognostic_index, integrative_cluster
- Outcome Data: 
    overall_survival_months, overall_survival, death_from_cancer
- Cohort Information: 
    cohort, oncotree_code
- Genomic Profiles: 
    498 columns consists of float64 types, representing gene expression levels, mutation counts, other genomic measurements for various genes, and other molecular measurements.
    *The naming convention (e.g., ugt2b7, srd5a1) typically corresponds to gene symbols or identifiers, which is common in genomic datasets*

***Genomic Data Columns:***
Genomic Data are crucial for identifying genetic factors associated with breast cancer. Analyzing gene expression and mutations can help in understanding the molecular mechanisms of the disease and in the development of targeted therapies.

These columns are predominantly gene names or are related to genetic mutations, which are key to understanding the molecular underpinnings of cancer.

1. Gene Expression Data: Columns named after genes (like brca1, tp53, palb2, pten, and others) indicate gene expression levels or statuses.


***Gene Expression Profile Data:*** these profiles can help in understanding the molecular basis of diseases like cancer.

***Preprocessing steps:***
- Normalization/Standardization of Numerical Features:
- Encoding Categorical Variables:
- Handling Missing Values:
- Feature Selection/Dimensionality Reduction:

For simplicity and to avoid introducing too many dimensions:
- We apply label encoding to ordinal variables and variables with a high number of categories,
- One-hot encoding to nominal variables with a lower number of categories.

#### Note: 
Standardizing the numerical features involves **subtracting the mean and dividing by the standard deviation for each feature**, which makes the data suitable for many machine learning algorithms, especially those sensitive to the scale of input features.

The EDA will help us understand the relationships and distributions within the data further, while feature selection can reduce dimensionality and focus the analysis on the most informative features for predicting breast cancer outcomes.