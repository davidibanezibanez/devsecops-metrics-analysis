## **Report 4: Filtering Unique and Valid Links**

## **Objective**

To optimize the consolidated international links dataset by applying two fundamental filters:

1. Remove duplicate links, keeping only the first occurrence.
2. Retain only links with HTTP status **200 (valid and accessible)**.

## **Summary of Work Performed**

### **1. Input File**

The consolidated file containing HTTP status codes was used as the base:

* **Location:**
  `data-international-searches/linksallwithhttpcode/links_all_withhttpcode.csv`

* **Existing columns:**

  * `Link`
  * `country`
  * `httpcode`

---

### **2. Filtering Process**

A code cell was implemented in the notebook **`notebook-international-searches.ipynb`** that:

* Removed duplicates in the `Link` column, keeping only the first occurrence regardless of country.
* Filtered the dataset to retain only links with `httpcode` equal to **200** (or `200.0` in float format).

---

### **3. Output File**

The resulting file was saved in the following location:

* **Folder:**
  `data-international-searches/linksallwithhttpcodeonlyunique200/`

* **File name:**
  `links_all_withhttpcode_onlyunique200.csv`

This file contains only **unique and valid links**, representing a clean and reliable dataset for further analysis.

## **Current Result**

The project now includes a refined dataset with:

* **`Link` column:** unique links.
* **`country` column:** country from which the link was extracted.
* **`httpcode` column:** accessibility confirmation (200).

The total number of rows was reduced after removing duplicates and discarding invalid links, leaving only those that are **active and accessible**.
