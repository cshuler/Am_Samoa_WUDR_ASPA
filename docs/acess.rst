Accessing the Data
====================

Introduction
------------
A guide to accessing the processed data. The tables are posted to an object endpoint space through Digital Ocean and are publically accessible.

Data Endpoint URLs ~

https://aspa-wudr.sfo3.digitaloceanspaces.com/Final_Aggregated_Data.csv

https://aspa-wudr.sfo3.digitaloceanspaces.com/Organization.csv

https://aspa-wudr.sfo3.digitaloceanspaces.com/Sites.csv

https://aspa-wudr.sfo3.digitaloceanspaces.com/Variables.csv

https://aspa-wudr.sfo3.digitaloceanspaces.com/WaterSources.csv


Example Access with Python
------------------

To access the endpoints within Python, you'll need this Python library

- **Requests**: A simple and elegant HTTP library for Python, perfect for making HTTP requests to your endpoints.

You can install the `requests` library using pip:

bash
pip install requests

Here is a basic GET request code snippet:

import requests

url = "https://your-endpoint-space-url.com/api/resource"
response = requests.get(url)

if response.status_code == 200:
    data = response.json()
    print("Data retrieved:", data)
else:
    print(f"Failed to retrieve data. Status code: {response.status_code}")



Accessible Tables
-----------------
There are multiple .CSVs available for download. Following are high-level descriptions.


Final Aggregated Data
----------------------
This is the main table with the required water use data
Final_Aggregated_Data.csv

**SiteNativeID**

Unique identifier code / ID used by the data provider to distinguish the data site in the source data set.: Aasu		


**BeneficialUseCategory**

The use category for which the water is being allocated to: E.g. (Commercial)

			
**TimeframeStart**

The datetime start of the recorded usage.: E.g. (2021-12-01)


**TimeframeEnd** 

The datetime end of the recorded usage:  E.g. (2021-12-31)


**Amount**

Usage of water reported for the specific time frame, village, and use. :  E.g. (5008.0)


**VariableCV**

This is a high-level variable used for site-specific water data. :  E.g. (Consumptive Use)


**ReportYear**
	
Year associated with data.:  E.g. (2021)


URL ~

https://aspa-wudr.sfo3.digitaloceanspaces.com/Final_Aggregated_Data.csv





The following tables are specified metadata tables used to support the main data table. 
Accompanied by a description of American Samoan specific examples of what each field corresponds to.

Sites
-------------
Sites.csv

**SiteNativeID**

Unique identifier code / ID used by the data provider to distinguish the data site in the source data set. :  E.g. (Pago Pago Village)


**Latitude**

Latitude coordinate of the data site. :  E.g. (-14.274006)


**Longitude**

Longitude coordinate of the data site. :  E.g. (-170.70403)


**SiteTypeCV**

The high level description of the site type recognized by the data provider. :  E.g. (Village (aggregation of individual water meter use within each village boundary)) 


URL ~ 

https://aspa-wudr.sfo3.digitaloceanspaces.com/Sites.csv

Note: This also contains site-specific well data.

Organization
------------
Organization.csv

**OrganizationName**

Name corresponding to unique organization and the organization ID. :  E.g. (American Samoa Power Authority)



**OrganizationContactEmail**

Email information for organization contact person. :  E.g. ( @aspower.com)


**OrganizationContactName**

Name of the contact person. :  E.g. (Wei Hua-Hsien)


**OrganizationPhoneNumber**

The organization's phone number for general information. :  E.g. (1 (684) 699-1234)


**OrganizationWebsite**

A hyperlink back to the organization's website. :  E.g. (https://www.aspower.com)

**StateCV**

Two digit state abbreviation where the organization is.:  E.g. (AS)


**OrganizationPurview**

A description of the purview of the agency (i.e. water rights, consumptive use, etc.).  :  E.g. (water utility, production, delivery, consumptive use)


URL ~

https://aspa-wudr.sfo3.digitaloceanspaces.com/Organization.csv

Variables
----------
Variables.csv

**VariableCV**

This is a high-level variable used for site-specific water data. :  E.g. (Consumptive Use)


**AmountUnitCV**

Unit of the site-specific  amount. :  E.g. (Gallons)


**AggregationIntervalUnitCV**

The aggregation unit (e.g., day ,month, year). :    E.g. (Month)



URL ~

https://aspa-wudr.sfo3.digitaloceanspaces.com/Variables.csv

Water Sources
--------------
WaterSources.csv


**WaterSourceTypeCV**

The high level description of the water source type. :  E.g. (Groundwater)

URL ~


https://aspa-wudr.sfo3.digitaloceanspaces.com/WaterSources.csv


