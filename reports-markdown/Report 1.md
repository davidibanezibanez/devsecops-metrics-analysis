## **Report 1: Intercontinental Google Search Algorithm for Scientific and Grey Literature**

## **Objective**

To perform Google searches from different countries across the five continents using queries related to data science research (e.g., `"security ci/cd"`), filtering out unwanted links using regular expressions and exporting the results into a CSV file.

Three **free VPN services** (Proton VPN, Windscribe, and TunnelBear) will be used to ensure geographical diversity, along with the **Link Extractor** Firefox extension to extract links.

## **VPN Selection**

The following free VPNs were selected based on security criteria and geographical availability:

### **1. Proton VPN**

* **Security level**: High (based in Switzerland, no-logs policy).
* **Geographical flexibility**:

  * Does not allow manual country selection in the free version.
  * In our tests, it only connected automatically to the United States and the Netherlands.
* **Limitations**: Suitable for Europe and North America, but without location control.

### **2. Windscribe**

* **Security level**: Medium-High (no-logs policy, but fewer audits than Proton).
* **Geographical flexibility**:

  * Allows selection of some countries in North America, Europe, and Asia.
  * **Does not include** Oceania, Africa, or South America in the free version.
* **Limitations**: Provides a limited amount of free data (GBs).

### **3. TunnelBear**

* **Security level**: Medium (independently audited, but with data restrictions).
* **Geographical flexibility**:

  * Allows manual selection of countries across **all continents**, including Africa and Oceania.
* **Limitations**:

  * Limited free data allowance.
  * May stop working after reaching the data limit.

**Note on other VPNs**:
Some options were discarded due to unclear security policies.

## **Prerequisites**

1. **Browser**: Firefox (recommended for extension compatibility).
2. **Extensions**:

   * **Link Extractor**
3. **VPNs**:

   * Proton VPN
   * Windscribe
   * TunnelBear

## **Step-by-Step Guide**

### **1. VPN Installation and Setup**

#### **Proton VPN**

1. Download and install from the official website.
2. Create a free account.
3. Connect (country selection is not available; it will be assigned automatically).

#### **Windscribe**

1. Install and register.
2. Select an available country.
3. Connect (restricted countries are not available in the free version).

#### **TunnelBear**

1. Install and create an account.
2. Manually select a country.
3. Connect (monitor data usage limits).

### **2. Firefox and Link Extractor Configuration**

1. **Install Link Extractor**:

   * Search for "Link Extractor" in the Firefox extensions store and install it.

2. **Add Host Permissions**:

   * Locate the host permissions option in the extension settings.

3. **Regex Filter to Exclude Unwanted Links**:

   * Open the Link Extractor extension.
   * In "Filter Patterns", enter:

     ```regex
     ^((?!google|youtube).)*$
     ```
   * This will exclude links such as `google.com/support`, `youtube.com`, etc.

### **3. Performing Searches**

1. **Connect to VPN**

2. **Search on Google**:

   * Open Google.com (verify the location shown at the bottom-left of the page matches the desired country).
   * Run the search (e.g., `"security ci/cd"`).

3. **Extract Links**:

   * Right-click on the page and click the Link Extractor icon.
   * Apply the preconfigured regex filter.
   * Export results as a CSV file.

### **4. Repeat the Process by Continent**

To cover all five continents, the following setup is recommended:

#### **North America**

* **Recommended VPN**: Proton VPN (United States)

#### **South America**

* **Recommended VPN**: TunnelBear (Brazil)

#### **Europe**

* **Recommended VPN**: Proton VPN (Netherlands)

#### **Asia**

* **Recommended VPN**: Windscribe (Hong Kong, China)

#### **Africa**

* **Recommended VPN**: TunnelBear (South Africa)

#### **Oceania**

* **Recommended VPN**: TunnelBear (New Zealand)

## **Final Considerations**

* **Limitations of free VPNs**:

  * Proton VPN does not allow manual country selection.
  * Windscribe excludes key regions.
  * TunnelBear has very limited bandwidth.
