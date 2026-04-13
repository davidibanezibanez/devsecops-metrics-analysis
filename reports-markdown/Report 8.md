## **Report 8: Topic Filtering and Metric Extraction (International Searches)**

## **Objective**

To perform a manual review of the international links dataset in order to filter content based on thematic relevance ("topic") and verify the existence of security metrics within the documents, generating a final list of identified metrics along with their descriptions.

---

## **Summary of Work Performed**

### **1. Creation of Working File**

The CSV file from the previous stage (`links_all_withhttpcode_onlyunique200.csv`) was converted into spreadsheet format to facilitate manual processing.

* **File name:** `data-international-searches_links_all_withhttpcode_onlyunique200_withfilters.xlsx`
* **Location:** `data-international-searches/`

---

### **2. Topic Filtering (Main Sheet)**

In the main sheet of the file, a first structuring step was performed by adding a new column:

* **`topic` column:** Each link was manually classified using two possible values:

  * **`yes-topic`**: The content is relevant to the research topic.
  * **`no-topic`**: The content is not related to the topic.

---

### **3. Review of Metric Existence (Sheet `review`)**

A sheet named `review` was created to perform a deeper analysis of the filtered links.

* **`metrics` column:** This column was added to indicate whether the document contains explicit metrics (value: `yes`).
* **Metric identification:** When the value was `yes`, the names of the identified metrics were recorded directly in the entry.

---

### **4. Consolidation of Documents with Metrics (Sheet `Metrics`)**

A sheet named `Metrics` was created as a filtered subset. This tab includes **only those records positively identified in the previous step**, meaning only documents that actually contain security metrics.

---

### **5. Metric Catalog (Sheet `List of metrics`)**

Finally, the extracted information was consolidated into a dedicated sheet named `List of metrics`.

* **Content:** A clean list of all identified metrics.
* **Structure:**

  * **Links:** Direct link to the source where the metric was found.
  * **Metric name:** Identifier of the metric.
  * **Description:** Definition or contextual explanation of the metric based on the source.
