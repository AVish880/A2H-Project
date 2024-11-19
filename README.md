
# A2H Project - Preclinical to Clinical Trial Translation

## Project Overview

The **A2H (Animal to Human)** project focuses on bridging the gap between preclinical research and clinical applications using machine learning (ML) and data extraction techniques. It aims to enhance the predictability of translational success for various diseases by systematically gathering data from sources like **ClinicalTrials.gov**, **PubMed**, and **PMC**, and using this data to model the outcomes of clinical trials based on preclinical findings.

The project includes two key phases:
1. **Systematic Data Collection:** Automated extraction of relevant data from preclinical studies.
2. **Predictive Modeling:** Development of machine learning models to match preclinical findings with clinical trial outcomes.

---

## Files and Descriptions

### 1. **Scripts for Data Extraction**
- **`disease_drug_script.ipynb`**
  - Automates searching for diseases and drugs from ClinicalTrials.gov.
  - Uses APIs to query and extract data related to diseases and their corresponding drugs.
  - Processes mentions of drugs in trials to identify the most frequently used ones.

- **`XML_data_extraction.ipynb`**
  - Parses XML data to extract key study information such as animal models, endpoints, dosage, and duration.
  - Uses libraries like BeautifulSoup for XML parsing.

- **`Clinicaltrials-data-script.ipynb`**
  - Focuses on querying clinical trial data for diseases like Crohn’s Disease, IBS, and Celiac Disease.
  - Extracts study metadata and consolidates findings for downstream analysis.

- **`PMC-data.ipynb`**
  - Uses FTP services to download PMC database entries.
  - Extracts and processes large-scale full-text articles for identifying preclinical data.

- **`Pubmed-data.ipynb`**
  - Searches and retrieves PubMed articles based on disease-specific keywords.
  - Filters papers to include only those meeting specific criteria for analysis.

---

### 2. **Documents**
- **`A2H - Data Querying.pdf`**
  - Explains data sources, objectives, and methodologies.
  - Lists specific tasks such as identifying animal models, endpoints, and dosage durations.
  - Provides links to related trials and research papers.

- **`A2H Extension for Gut Diseases.pdf`**
  - Proposes extending the project to diseases like IBS, Crohn's Disease, and Celiac Disease.
  - Highlights challenges and opportunities in translating preclinical findings to clinical outcomes.
  - Suggests machine learning approaches, such as Random Forest and Gradient Boosting, for predictive modeling.

---

## Project Goals

1. **Data Curation**:
   - Collect and standardize datasets from diverse sources for diseases like IBS, Crohn's Disease, and Celiac Disease.
   - Extract data points such as animal models, biomarkers, dosage, and duration.

2. **Model Development**:
   - Build predictive models using preclinical data to forecast clinical trial outcomes.
   - Achieve high precision and recall (F1 score) through robust validation.

3. **Automation and Efficiency**:
   - Use transformer-based language models to automate data extraction from preclinical literature.
   - Implement preprocessing techniques like SMOTE to address class imbalances.

---

## Setup Instructions

### 1. **Dependencies**
Install the required Python libraries:
```bash
pip install pandas numpy beautifulsoup4 requests sklearn
```

Additional tools:
- **GPU server:** Necessary for large-scale model training.
- **FTP client:** For downloading PubMed Central data.
- **APIs:** Obtain keys for ClinicalTrials.gov and PubMed APIs.

### 2. **Running the Scripts**
- **Data Extraction:**
  - Start with `disease_drug_script.ipynb` to query and list relevant trials.
  - Use `XML_data_extraction.ipynb` to parse trial data for specific parameters.
  - Leverage `PMC-data.ipynb` and `Pubmed-data.ipynb` to retrieve and process literature.

- **Modeling:**
  - Preprocess the curated datasets using feature scaling, outlier removal, and data augmentation.
  - Experiment with classifiers like Support Vector Machine and Gradient Boosting.

---

## Outputs and Deliverables

1. **Datasets:**
   - Comprehensive datasets enriched with multi-omics information for targeted diseases.

2. **Predictive Model:**
   - A machine learning model capable of forecasting clinical outcomes based on preclinical inputs.

3. **Documentation:**
   - Detailed reports on methodology, results, and key findings.

4. **Research Publications:**
   - Insights from the project may contribute to academic and industry-focused research.

---

## Timeline and Milestones

- **Week 1-2:** Literature review, setup, and preliminary data extraction.
- **Week 3-4:** Data cleaning, standardization, and initial model development.
- **Week 5-6:** Model evaluation and refinement.
- **Week 7:** Documentation and presentation of results.

---

## Contribution Guidelines

1. **Fork the Repository:**
   Clone and work on your local machine.
2. **Raise Issues:**
   If you encounter bugs or have suggestions.
3. **Submit Pull Requests:**
   Ensure your code follows the project’s style guidelines.

---

## Future Work

- Expand the dataset to include more diseases and clinical outcomes.
- Enhance model explainability to address the "black box" nature of ML models.
- Incorporate real-time data feeds for continuous learning.

---

## References

For a detailed list of references, see the attached project documents. Highlights include:
- **Camilleri M. (2021):** IBS Diagnosis and Treatment.
- **Torres J. et al. (2017):** Insights into Crohn's Disease.
- **Catassi C. et al. (2022):** Research on Celiac Disease.

---

## Contact

**Project Leads:**  
Anant Vishwakarma, Fangzhou Li  
**Email:** abvishwakarma@ucdavis.edu
