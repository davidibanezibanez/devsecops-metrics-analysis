## **Report 10: Relevance Filtering in Specialized Website Searches**

## **Objective**

To perform a manual analysis of the complementary dataset obtained from technical discussion platforms (Stack Overflow, Reddit, Security Stack Exchange), in order to determine whether community discussions contained formal definitions or security metrics usable for the research.

---

## **Summary of Work Performed**

### **1. Working File**

The unified dataset of website-based searches was processed:

* **File name:** `data-website-searches_links_all_withhttpcode_onlyunique200.xlsx`
* **Location:** `data-website-searches/`
* **Content:** A single main sheet containing **448 links** derived from targeted queries on forums and community platforms.

---

### **2. Manual Review Process**

Control columns were added to evaluate each link individually:

* **`topic`**: Thematic relevance assessment.
* **`english`**: Language verification.
* **`access (yes/no)`**: Manual accessibility check.

The analysis focused on determining whether discussion threads or posts contained explicit security metrics for CI/CD pipelines.

---

## **Current Result**

### **Complete Source Rejection**

After reviewing all **448 records**, the outcome was:

* **100% of the links (448/448)** were classified as **`no-topic`**.
