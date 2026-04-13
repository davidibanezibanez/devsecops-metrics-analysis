## **Report 3: Final Algorithm Adjustments and Definitive Search Execution**

## **Objective**

To consolidate links obtained from Google searches across different countries, organize the project within a single directory (`data-international-searches/`), and generate a final CSV file containing unified links labeled by country and enriched with their HTTP response codes.

## **Summary of Modifications and Progress**

### **1. Folder Structure Reorganization**

A main directory named `data-international-searches/` was created within the project. All previous folders were moved into this location while preserving their hierarchy:

* `data-international-searches/links/`
* `data-international-searches/linkswithcountrycolumn/`
* `data-international-searches/linksall/`
* `data-international-searches/linksallwithhttpcode/`

### **2. Merging Multiple CSV Files per Country**

Each Google search (performed from each country using its corresponding VPN) generated multiple CSV files (one per results page).

A Python script was implemented to:

* Iterate through all CSV files within each country folder.
* Merge them into a single file per country.
* Remove duplicates.
* Save the result in `data-international-searches/links/` as `links_<country>.csv`.

### **3. Execution of Advanced Google Searches**

The following advanced Google query was used:

```
("CI/CD" OR "DevSecOps" OR "Continuous Integration" OR "Continuous Delivery" OR "Pipeline security") 
AND 
("security metrics" OR "security indicators" OR "security KPIs" OR "vulnerability metrics" OR "security measurement" OR "security score" OR "pipeline security" OR "security performance" OR "security build pipeline")
```

Each search was performed while connected to the VPN corresponding to the target country.

### **4. Final File Generation**

After completing the previous steps (adding the `country` column, consolidating into `links_all.csv`, and adding the `httpcode` column), the final dataset was generated with:

* **2200 unique links**
* Columns:

  * `Link`
  * `country`
  * `httpcode`

## **Current Result**

A single consolidated CSV file that combines links from 7 countries, labeled by country and enriched with the HTTP status of each link.
