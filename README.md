# Integrative Machine Learning Analysis of Genomic and Clinical Data for Breast Cancer

To develop an integrative machine learning model that can analyze and interpret the complex relationships between genomic data and clinical outcomes in breast cancer patients.

### Project Description:
Breast cancer, a complex and heterogeneous disease, presents significant challenges in diagnosis, treatment, and prognosis. Advances in genomic sequencing and clinical data collection have opened new avenues for understanding this disease at a molecular level. However, the sheer volume and complexity of the data demand sophisticated analytical approaches.

This project aims to harness the power of machine learning to integrate and analyze extensive genomic and clinical data, specifically focusing on breast cancer. Utilizing the METABRIC (Molecular Taxonomy of Breast Cancer International Consortium) dataset, which includes comprehensive gene expression profiles and clinical information from breast cancer patients, this research seeks to uncover novel insights and patterns that could contribute to personalized medicine and improved treatment strategies.

### Dataset source: 
https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric/data

This dataset will facilitate meaningful insights and potentially reveal new correlations and patterns important for personalized medicine and therapeutic advancements.

***Dataset Structure:*** It contains 1904 entries and 693 (520 excluding mutation data) columns. Columns include a mix of numerical and categorical data types.

1. Data Exploration
2. Data Preprocessing and Exploratory Data Analysis (EDA)



***Clinical Data Columns:***
Clinical Data are vital for understanding patient demographics, cancer characteristics, treatment types, and outcomes. These variables can be used to correlate with genomic data and identify patterns in treatment response, survival rates, and cancer subtypes.

These columns are related to patient information, clinical characteristics, and treatment details.

- Patient Information: patient_id, age_at_diagnosis
- Cancer and Treatment Details: type_of_breast_surgery, cancer_type, cancer_type_detailed, cellularity chemotherapy, hormone_therapy, radio_therapy
- Biological and Clinical Markers: er_status_measured_by_ihc, er_status, pr_status, her2_status_measured_by_snp6, her2_status, 3-gene_classifier_subtype
- Cancer Characteristics: neoplasm_histologic_grade, tumor_other_histologic_subtype, tumor_size, tumor_stage primary_tumor_laterality, lymph_nodes_examined_positive
- Prognostic Indices: nottingham_prognostic_index, integrative_cluster
- Outcome Data: overall_survival_months, overall_survival, death_from_cancer
- Cohort Information: cohort, oncotree_code

***Genomic Data Columns:***
Genomic Data are crucial for identifying genetic factors associated with breast cancer. Analyzing gene expression and mutations can help in understanding the molecular mechanisms of the disease and in the development of targeted therapies.

These columns are predominantly gene names or are related to genetic mutations, which are key to understanding the molecular underpinnings of cancer.

1. Gene Expression Data: Columns named after genes (like brca1, tp53, palb2, pten, and others) indicate gene expression levels or statuses.
2. Mutation Data: Columns ending with _mut (like pik3ca_mut, tp53_mut, brca1_mut, brca2_mut, etc.) are indicative of mutation data for those genes.

From the dataFrame, '1' indicates the presence of a mutation and '0' indicates its absence. 
There are also specific mutation types listed (like "1069Lfs5", "199Yext60", etc.), which indicate specific mutation events.
Sparse Data: Many columns seem to have a high frequency of '0' values, suggesting that most mutations are not present in the majority of samples. This is common in mutation data due to the unique nature of cancer genomes.

***Gene Expression Profile Data:*** these profiles can help in understanding the molecular basis of diseases like cancer.

