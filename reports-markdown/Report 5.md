## **Report 5: Searches on Specialized Websites**

## **Objective**

To expand the link collection strategy through a complementary approach to international searches. Instead of filtering by country, this phase focused on collecting links from **specific websites relevant to the technical community**.

## **Summary of Work Performed**

### **1. New Notebook Created**

A standalone notebook was developed:

* **Name:** `notebook-website-searches.ipynb`
* **Associated data folder:** `data-website-searches/`

This notebook follows the same structure and steps as `notebook-international-searches.ipynb`, with the key difference that instead of the `"country"` column, a **`website`** column is added, identifying the source platform of each link.

### **2. Websites Consulted**

Searches were conducted on the following specialized platforms:

* [Stack Overflow](https://stackoverflow.com/)
* [Security Stack Exchange](https://security.stackexchange.com/)
* [Reddit](https://www.reddit.com/)

### **3. Search Strategy**

Unlike Google, where a complex Boolean search string was used, this phase relied on **three specific queries** applied across all platforms:

1. `CI/CD pipeline security`
2. `CI/CD security build pipeline`
3. `CI/CD security performance`

Each search generated results that were collected and exported as CSV files, following the same processing workflow (merging, adding the `website` column, HTTP accessibility verification, etc.).

### **4. Result**

The process resulted in a unified dataset following the same structure as the international search dataset, but adapted to this new analysis axis:

* **Final dataset columns:**

  * `Link`
  * `website`
  * `httpcode`

* **Containing folder:**
  `data-website-searches/`

This dataset represents a complementary collection capturing the perspective of **grey literature and community discussions** around CI/CD security.
