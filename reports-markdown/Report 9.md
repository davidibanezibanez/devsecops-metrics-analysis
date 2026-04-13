## **Report 9: Paper Selection and Snowballing (Scientific Literature)**

## **Objective**

To refine the scientific literature dataset through a manual filtering process, complemented by the **Snowballing technique** (both backward and forward citation tracking), in order to ensure a comprehensive review and finalize the selection of relevant papers.

---

## **Summary of Work Performed**

### **1. Working File**

All decision-making processes were centralized in a single master file, which contains full traceability from the raw dataset to the final accepted papers:

* **File name:** `data-science-searches_links_normalized_clean_withdatabasesource_all_withfilters.xlsx`
* **Location:** root of the scientific search working directory

The file is structured into multiple sheets representing the **four-stage selection workflow**.

---

### **Stage 1: Initial Screening (Sheet `1 - all`)**

The process began with a consolidated list of approximately **726 records**. Manual exclusion criteria were applied by introducing control columns:

* **`topic`**: Thematic relevance classification. Records marked as `yes-topic` were directly related to security metrics in CI/CD pipelines.
* **`english`**: Language verification.
* **`paper`**: Confirmation that the document is a scientific article (excluding indexes, front matter, etc.).

Documents that passed this filtering constituted the **Round 1 selection**.

---

### **Stage 2: Snowballing Process (Sheets `2 - ...` and `3 - ...`)**

For the Round 1 selected documents, the Snowballing technique was applied iteratively to identify additional relevant studies not captured in the initial search.

#### **Iteration 2 (Round 2)**

* **Backward Snowballing (`2 - snowballing-back`)**: Review of references cited by Round 1 papers.
* **Forward Snowballing (`2 - snowballing-forward`)**: Review of papers citing Round 1 papers.

#### **Iteration 3 (Round 3)**

* The same process was repeated (`3 - snowballing-back` and `3 - snowballing-forward`) on newly identified relevant papers from Round 2, expanding the literature network further.

Each snowballing sheet recorded full references and assigned a relevance decision (`yes-topic` / `no-topic`).

---

### **Stage 3: Candidate Consolidation (Sheet `selected-papers`)**

A unified list of **23 candidate papers** was created after title and abstract screening across all previous stages.

* **Content:** Includes both initial search results (Round 1) and snowballing discoveries (Round 2).
* **Key metadata:** Title, Authors, DOI, Source (Journal/Conference), and Origin Round.
* **Status:** Entries were tracked using markers such as `x` or `Review` for full-text evaluation management.

---

### **Stage 4: Final Selection (Sheet `ok-papers`)**

After full-text reading and quality assessment of the 23 candidate papers, the final set of primary studies was established:

* **Total selected papers:** **7 papers**
* **Criteria:** These `ok-papers` are those that effectively contribute security metrics or models for CI/CD pipelines and satisfy all inclusion criteria.
* **Traceability:** Each entry includes a verified source link and validated DOI.
