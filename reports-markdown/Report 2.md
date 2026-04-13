## **Report 2: Adding Regions, Data Consolidation, and HTTP Status Code Verification**

### **Objective**

To continue the process of collecting scientific and grey literature links obtained through Google searches from different countries, by adding geographical information to the collected files, consolidating the results, and verifying the current status of each link using its HTTP response code.

### **Summary of Work Performed**

#### **1. Adding `country` Column to Individual CSV Files**

Based on the files manually extracted using the **Link Extractor** extension and organized by country in the `links/` folder, a Python script was developed to:

* Add a column named `"country"` to each CSV file.
* Assign the corresponding country name to each row.
* Save each new file in the `linkswithcountrycolumn/` folder using the following format:
  `links_<country>_withcountrycolumn.csv`

> Included countries: `brazil`, `chile`, `china`, `netherlands`, `newzealand`, `southafrica`, `usa`.

#### **2. Merging CSV Files into a Single Dataset**

A script was created to merge all CSV files from the `linkswithcountrycolumn/` folder into a single consolidated file:

* Output file: `links_all.csv`
* Destination folder: `linksall/`
* The final file contains all combined rows while preserving the `country` column.

#### **3. Link Status Verification**

Using the consolidated file `links_all.csv`, an optimized script was developed to:

* Check the status of each link via HTTP requests.
* Retrieve the HTTP status code (`200`, `404`, `500`, etc.).
* Add this information as a new column named `"httpcode"`.

The process leveraged **parallel execution using `ThreadPoolExecutor`** to speed up the validation of approximately ~7000 links.

* Final output file: `links_all_withhttpcode.csv`
* Destination folder: `linksallwithhttpcode/`
