## **Report 6: Searches in Scientific Literature**

## **Objective**

To extend the search strategy to **scientific literature sources** in order to incorporate academic articles and publications indexed in high-impact repositories.

## **Summary of Work Performed**

### **1. New Notebook Created**

A standalone notebook was developed:

* **Name:** `notebook-science-searches.ipynb`
* **Location:** project root
* **Associated data folder:** `data-science-searches/links/`

This notebook contains the necessary cells to transform and unify results obtained in different formats from academic search platforms.

---

### **2. Sources Consulted**

The same search string used in the international workflow was applied:

```
("CI/CD" OR "DevSecOps" OR "Continuous Integration" OR "Continuous Delivery" OR "Pipeline security")
AND
("security metrics" OR "security indicators" OR "security KPIs" OR "vulnerability metrics" OR "security measurement" OR "security score" OR "pipeline security" OR "security performance" OR "security build pipeline")
```

The platforms and resulting files were:

* **Scopus** → direct CSV export (`links_scopus.csv`)
* **Springer Link** → direct CSV export (`links_springerlink.csv`)
* **ACM** → BibTeX export (`links_acm.bib`), later converted to CSV (`links_acm.csv`)
* **IEEE Xplore** → BibTeX export (`links_ieee.bib`), later converted to CSV (`links_ieee.csv`)

---

### **3. Generated Files**

All extracted and processed files are located in:

```
data-science-searches/links/
```

Resulting files:

* `links_acm.csv`
* `links_ieee.csv`
* `links_scopus.csv`
* `links_springerlink.csv`

---

## **Header Compatibility Analysis**

After generating the CSV files, their headers were analyzed in order to plan a **future unified consolidated dataset**.

---

### **1. links_acm.csv**

```
series, location, keywords, numpages, articleno, booktitle, doi, url,
address, publisher, isbn, year, title, author, ENTRYTYPE, ID, pages,
month, journal, issn, number, volume, issue_date, note
```

---

### **2. links_ieee.csv**

```
doi, keywords, pages, number, volume, year, title, booktitle,
author, ENTRYTYPE, ID, journal
```

---

### **3. links_scopus.csv**

```
Authors, Author full names, Author(s) ID, Title, Year, Source title,
Volume, Issue, Art. No., Page start, Page end, Page count, Cited by,
DOI, Link, Document Type, Publication Stage, Open Access, Source, EID
```

---

### **4. links_springerlink.csv**

```
Item Title, Publication Title, Book Series Title, Journal Volume,
Journal Issue, Item DOI, Authors, Publication Year, URL, Content Type
```

---

### **Preliminary Compatibility Analysis**

* **Title:**

  * ACM → `title`
  * IEEE → `title`
  * Scopus → `Title`
  * Springer → `Item Title`
    → Can be standardized as: `title`

* **Authors:**

  * ACM → `author`
  * IEEE → `author`
  * Scopus → `Authors`
  * Springer → `Authors`
    → Can be standardized as: `authors` (with normalization)

* **DOI:**

  * ACM → `doi`
  * IEEE → `doi`
  * Scopus → `DOI`
  * Springer → `Item DOI`
    → Can be standardized as: `doi`

* **Source / Publication:**

  * ACM → `booktitle`
  * IEEE → `booktitle`
  * Scopus → `Source title`
  * Springer → `Publication Title`
    → Can be standardized as: `source`

* **Publication Year:**

  * ACM → `year`
  * IEEE → `year`
  * Scopus → `Year`
  * Springer → `Publication Year`
    → Can be standardized as: `year`

* **Keywords:**

  * ACM → `keywords`
  * IEEE → `keywords`
  * Scopus → *(not available)*
  * Springer → *(not available)*
    → Can be standardized as: `keywords`
