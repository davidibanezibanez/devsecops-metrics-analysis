# Internship: DevSecOps Metrics Analysis

**Duration:** Second Semester 2025 (264 hours)  
**Contact:** [David Ibáñez](https://www.linkedin.com/in/davidibanezibanez)  
**Project Link:** [GitHub Repository](https://github.com/davidibanezibanez/devsecops-metrics-analysis)  

---

## Project Context

This internship was conducted at the Universidad de La Frontera under the supervision of a Ph.D. in Computer Science, as part of a research project focused on security in Continuous Integration and Continuous Deployment (CI/CD) environments. The fundamental purpose of this project was the construction of versatile datasets through diverse criteria, aiming to identify, collect, and catalog security metrics, indicators, and KPIs to measure the performance and robustness of modern software pipelines. 

My role in this project centered on data engineering and technical analysis. This ranged from configuring the collection infrastructure and developing Python automation scripts, to the rigorous selection, normalization, and filtering of the resulting datasets for the final extraction of security metrics.

## Problem Statement and Objectives

In modern software development, security within Continuous Integration and Continuous Deployment (CI/CD) pipelines is critical, yet information on how to measure and evaluate it is scattered and fragmented. There is no centralized repository or single standard for metrics; instead, knowledge is diluted across formal scientific papers and a vast amount of grey literature accessible only through complex web searches. 

This dispersion, coupled with the geographical biases of search engines, makes identifying reliable security indicators difficult. The core problem, therefore, lies in the need to design data engineering strategies capable of collecting, normalizing, and cleaning large volumes of information to separate valid metrics from irrelevant noise.

### General Objective
Develop and implement data engineering workflows for the collection, normalization, and analysis of information from scientific and web sources, in order to build refined datasets that enable the identification of security metrics for CI/CD pipelines.

### Specific Objectives
* Implement a geolocated web search infrastructure to enable global data extraction, mitigating regional biases in results through the use of Virtual Private Networks (VPNs).
* Develop automation algorithms in Python for the unification, cleaning, and technical validation of the collected data, ensuring data quality and accessibility.
* Consolidate and normalize datasets from multiple academic repositories (Scopus, IEEE, ACM), standardizing metadata to facilitate comparative analysis.
* Execute filtering processes (Snowballing techniques and topic review) to segregate relevant information and extract a final catalog of explicit security metrics.

## Main Activities

1. **Configuration of Infrastructure for Geolocated Searches:** Implemented a workspace utilizing three VPN services (Proton, Windscribe, TunnelBear) to simulate locations across 5 continents, enabling unbiased extraction of geographical links.
2. **Development and Execution of International Search Algorithms:** Designed and executed complex boolean queries (e.g., `"CI/CD pipeline security"`), filtering results via regular expressions to collect grey literature from various countries (USA, Chile, China, Netherlands, etc.).
3. **Data Processing and Technical Cleaning (Grey Literature):** Developed Python scripts to merge multiple CSV files, add geographical metadata (`country` column), and verify the accessibility of thousands of links by checking HTTP status codes (filtering only `200 OK`).
4. **Data Mining in Specialized Technical Communities:** Created a specific search workflow for technical discussion sites (Stack Overflow, Reddit, Security Stack Exchange), using targeted queries to capture community perspectives on CI/CD security.
5. **Extraction of Scientific Literature:** Conducted searches and exported bibliographic references from high-impact repositories (Scopus, Springer Link, ACM, IEEE Xplore), obtaining data in CSV and BibTeX formats.
6. **Normalization and Consolidation of Scientific Datasets:** Processed raw files from scientific sources to standardize headers (title, authors, DOI, year), clean irrelevant columns, and unify everything into a master dataset with origin traceability (`database_source`).
7. **Relevance Analysis of Community Sources:** Reviewed 448 links from technical forums to determine their utility, ultimately discarding this source entirely due to a lack of formal definitions or applicable metrics.
8. **Thematic Filtering and Metric Extraction (International Searches):** Analyzed the international search dataset, classifying documents by topic (`yes-topic`/`no-topic`) and cataloging explicit security metrics found alongside their descriptions.
9. **Selection of Primary Studies and Snowballing:** Executed a rigorous scientific selection process that included inclusion/exclusion filters and Snowballing techniques (backward and forward) to ensure exhaustiveness.
10. **Structuring and Organization of the Data Repository:** Maintained and reorganized the directory and file structure throughout the project (e.g., `data-international-searches/`, `data-science-searches/`) to guarantee order, version traceability, and analysis reproducibility.

## Results

As a result of the data engineering and analysis work, the following main outcomes were achieved:

1. **Consolidation of Grey Literature and International Metrics:** Generated a unified dataset of 2,200 unique and valid links (HTTP 200 code) from geolocated searches across 7 countries. After reviewing this set, a list of explicit security metrics and their descriptions was successfully extracted and cataloged, capturing the practical knowledge of the global industry.
2. **Selection of High-Impact Scientific Literature:** From an initial database of approximately 726 documents across four academic databases, exclusion filters and Snowballing techniques were applied. This rigorous process led to the identification of 23 candidates and a final selection of 7 primary studies that provide formally defined security models and metrics for CI/CD.
3. **Evaluation of Community Sources:** The analysis of 448 links collected from specialized forums yielded a negative result regarding relevance. 100% of the records were classified as `no-topic` after review, concluding that these platforms, while useful for specific troubleshooting, lack the necessary rigor to define standardized security metrics for this research.

---

## What does this software do?

This repository contains the complete **reproduction package** for a Multivocal Literature Review (MLR) focused on identifying and analyzing **DevSecOps metrics**.

Unlike traditional systematic reviews, this study integrates both **scientific literature** (formal academic papers) and **grey literature** (practitioner insights from blogs, forums, and Q&A sites). The goal is to bridge the gap between academic theory and industrial practice regarding how security is measured in DevOps environments.

## Repository Structure

The project is organized to reflect the three main pillars of the data collection process:

```text
.
├── data-international-searches/   # Raw data from Google searches across different countries (Zones).
├── data-science-searches/         # Data from academic databases (IEEE, ACM, Scopus, Springer).
├── data-website-searches/         # Data from specialized sites (StackOverflow, Reddit, SecuritySE).
├── data-final/                    # Final curated datasets used for analysis.
├── reports-markdown/              # Detailed methodology reports (Step-by-step audit trail).
├── notebook-*.ipynb               # Jupyter Notebooks for data cleaning, filtering, and analysis.
└── requirements.txt               # Python dependencies.
```

## Methodology & Process

The research process is documented in detail within the `reports-markdown` folder. The workflow follows a rigorous pipeline:

### 1. International Google Searches
* **Objective:** Capture the "state of the practice" worldwide.
* **Method:** Utilized a search algorithm adapted for different geographic zones (Chile, USA, China, etc.) to avoid location bias.
* **Reports:** See `Report 1`, `Report 2`, `Report 8`.

### 2. Scientific Literature Search
* **Sources:** IEEE Xplore, ACM Digital Library, Scopus, and SpringerLink.
* **Process:** Automated extraction, normalization of headers, and duplicate removal.
* **Refinement:** Applied **Snowballing** (backward and forward) to discover related papers.
* **Reports:** See `Report 6`, `Report 7`, `Report 9`.

### 3. Specialized Websites Mining
* **Sources:** StackOverflow, Reddit, and Security StackExchange.
* **Process:** Extracted discussions and Q&A threads relevant to DevSecOps metrics.
* **Reports:** See `Report 5`, `Report 10`.

## Usage

To reproduce the data processing or run the analysis notebooks:

1. **Clone the repository**
```bash
git clone [https://github.com/davidibanezibanez/devsecops-metrics-analysis.git](https://github.com/davidibanezibanez/devsecops-metrics-analysis.git)
cd mlr-devsecops-metrics
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the Notebooks**
Each notebook corresponds to a specific data source. Open them with Jupyter:
* `notebook-international-searches.ipynb`: Processing Google search results.
* `notebook-science-searches.ipynb`: Handling academic papers and snowballing.
* `notebook-website-searches.ipynb`: Analyzing community discussions.

```bash
jupyter notebook
```

## Final Datasets

If you are looking for the culmination of the data engineering process, check the `data-final` directory. This folder contains the curated and consolidated results of the Multivocal Literature Review (MLR), including:

* **Consolidated Grey Literature:** The refined dataset of valid links and information extracted from international web searches.
* **Selected Scientific Studies:** The final set of primary academic papers obtained after the filtering and snowballing processes.
* **Extracted Metrics:** The resulting catalog of security metrics and their descriptions identified throughout the research.

---

## Conclusions and Remarks

* The development of this internship confirmed that the application of data engineering and automation strategies is fundamental for addressing research that requires processing large volumes of data. The implementation of geolocated search algorithms and mass validation scripts proved to be an effective solution to mitigate geographic biases and the noise inherent in web searches, successfully transforming thousands of raw results into high-quality datasets.
* Furthermore, it is concluded that there is a clear dichotomy in the sources of information regarding CI/CD security. While scientific literature provides formal and structured models (albeit in smaller quantities), international grey literature offers a voluminous and pragmatic view of industry needs. Conversely, technical discussion communities, although valuable for solving specific errors, lack the rigor necessary to define standardized metrics.
* Finally, the main contribution of this work is not solely the resulting catalog of metrics, but the consolidation of a reproducible methodology and a refined data repository. These elements lay a solid foundation for future research in the field of DevSecOps security.
