# Multivocal Literature Review (MLR): DevSecOps Metrics

## Overview

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
├── reportes-markdown/             # Detailed methodology reports (Step-by-step audit trail).
├── notebook-*.ipynb               # Jupyter Notebooks for data cleaning, filtering, and analysis.
└── requirements.txt               # Python dependencies.

```

## Methodology & Process

The research process is documented in detail within the `reportes-markdown` folder. The workflow follows a rigorous pipeline:

### 1. International Google Searches

* **Objective:** Capture the "state of the practice" worldwide.
* **Method:** Utilized a search algorithm adapted for different geographic zones (Chile, USA, China, etc.) to avoid location bias.
* **Reports:** See `Reporte 1`, `Reporte 2`, `Reporte 8`.

### 2. Scientific Literature Search

* **Sources:** IEEE Xplore, ACM Digital Library, Scopus, and SpringerLink.
* **Process:** Automated extraction, normalization of headers, and duplicate removal.
* **Refinement:** Applied **Snowballing** (backward and forward) to discover related papers.
* **Reports:** See `Reporte 6`, `Reporte 7`, `Reporte 9`.

### 3. Specialized Websites Mining

* **Sources:** StackOverflow, Reddit, and Security StackExchange.
* **Process:** Extracted discussions and Q&A threads relevant to DevSecOps metrics.
* **Reports:** See `Reporte 5`, `Reporte 10`.

## Usage

To reproduce the data processing or run the analysis notebooks:

1. **Clone the repository**
```bash
git clone [https://github.com/davidibanezibanez/mlr-devsecops-metrics.git](https://github.com/davidibanezibanez/mlr-devsecops-metrics.git)
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



## Key Datasets

If you are looking for the final list of metrics or selected papers, check the `data-final` directory:

* `selected-papers.csv`: The final set of included academic studies.
* `Metrics.csv`: The consolidated list of identified DevSecOps metrics.

## Contact

David Ibáñez - https://www.linkedin.com/in/davidibanezibanez/

Project Link: [https://github.com/davidibanezibanez/mlr-devsecops-metrics](https://www.google.com/search?q=https://github.com/davidibanezibanez/mlr-devsecops-metrics)
