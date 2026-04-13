## **Report 7: Consolidation of Scientific Literature**

In this stage of the project, we focused on processing and normalizing data obtained from scientific databases (ACM, IEEE, Scopus, and Springer Link). The main objective was to **standardize relevant headers and consolidate all results into a single file** to facilitate further analysis.

---

## **Steps Performed**

### **1. Initial Header Normalization**

* A directory named `data-science-searches/linksnormalizedheaders/` was created.

* The four `.csv` files generated from each data source were copied and renamed, resulting in:

  * `links_acm_normalized.csv`
  * `links_ieee_normalized.csv`
  * `links_scopus_normalized.csv`
  * `links_springerlink_normalized.csv`

* In each file, the column names were standardized to ensure compatibility across all sources.

---

### **2. Cleaning and Column Reduction**

* A notebook cell was implemented in `notebook-science-searches.ipynb` to filter and retain only the relevant columns:

  * `title`
  * `authors`
  * `doi`
  * `source`
  * `year`
  * `keywords`

* The resulting files were stored in:
  `data-science-searches/linksnormalizedheadersclean/`

---

### **3. Addition of `database_source` Column**

* A new directory was created:
  `data-science-searches/linksnormalizedheaderscleanwithdatabasesource/`

* In this step, an additional column named **`database_source`** was added to each CSV, indicating the origin of the data:

  * `"acm"` for ACM Digital Library
  * `"ieee"` for IEEE Xplore
  * `"scopus"` for Scopus
  * `"springerlink"` for Springer Link

---

### **4. Final Consolidation of Results**

* Finally, all cleaned files with the `database_source` column were merged into a single consolidated dataset.

* This file was saved in:
  `data-science-searches/linksnormalizedheaderscleanwithdatabasesourceall/`

* Output file name:
  **`links_normalized_clean_withdatabasesource_all.csv`**

---

## **Final Result**

This workflow achieved:

* Standardization of headers across multiple scientific datasets.
* Reduction of each dataset to 6 core columns.
* Addition of a provenance column (`database_source`) to maintain traceability.
* Consolidation of all results into a single unified dataset.

This final file serves as a standardized foundation for performing comparative analysis and metric generation on scientific publications extracted from multiple sources.
