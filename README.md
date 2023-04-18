# Rest Based Grid for Cumulocity [<img width="35" src="https://user-images.githubusercontent.com/32765455/211497905-561e9197-18b9-43d5-a023-071d3635f4eb.png"/>](https://github.com/SoftwareAG/cumulocity-rest-based-grid-widget-plugin/releases/download/1.0.0/sag-ps-pkg-rest-based-grid-widget-1.0.0.zip)



The Rest Based Grid Widget is the Cumulocity module federation plugin created using c8ycli. This plugin can be used in Application Builder or Cockpit. This Rest Based Grid Widget help you to display API data in Grid view with configurable columns and headings. This widget also supports Nested lists, search and server side pagination, etc.

### Please choose Rest Based Grid release based on Cumulocity/Application builder version:

|APPLICATION BUILDER | CUMULOCITY  | REST BASED GRID WIDGET |
|--------------------|-------------|------------------------|
| 2.0.x              | >= 1016.x.x | 1.x.x                  |


## Prerequisite
   Cumulocity c8ycli >=1016.x.x


## Features

  
*  **Display API data:** Displays API Data for provided API URL in Grid mode. It also supports Nested List.

*  **Pagination:** Configurable Paginations and also option to set default page size.

*  **Configurable Columns:** User can choose what to display in Table from list and also option to display custom Headings.

*  **Device/ Asset:** Ability to select device or asset to pass as input to URL.

   
## Installation

  
### Runtime Widget Deployment?

* This widget support runtime deployment. Download [Runtime Binary](https://github.com/SoftwareAG/cumulocity-rest-based-grid-widget-plugin/releases/download/1.0.0/sag-ps-pkg-rest-based-grid-widget-1.0.0.zip) and install via Administrations --> Ecosystems --> Applications --> Packages 


## QuickStart
  

This guide will teach you how to add plugin in your existing or new dashboard.
  

1. Open you application from App Switcher
  

2. Add new dashboard or navigate to existing dashboard
  

3. Click `Add Widget`
  

4. Search for `Rest Based Grid`


5. Select `Target Assets or Devices`


6. Click `Save`


Congratulations! Rest Based Grid widget Plugin is configured.

  

## User Guide

 
*  **Display API data:** Displays API Data for provided API URL in Grid mode. It also supports Nested List.

*  **Pagination:** Configurable Paginations and also option to set default page size.

*  **Configurable Columns:** User can choose what to display in Table from list and also option to display custom Headings.

*  **Device/ Asset:** Ability to select device or asset to pass as input to URL.
*  **Target assets or devices:** User can select a device/asset. If device/asset is selected, then the External ID of that device will be passed as input along with URL. 
*  **Data Source URL:** User has to pass the API URL from where the data needs to be fetched.
*  **Device Specific:** User can select this button, if the external Id of selected device/asset needs to be passed as part of the URL (deviceId = '' will be added in to the URL params).
*  **Name of the Main document List from API:** User has to pass the name of the List that needs to be picked from the API output to dispaly the data in table.
*  **Table Column Headings:** User has to pass the Header names (comma separated) for the table. These names can be different from the API output field names.
*  **Table Column Names From API:** User has to pass the field names (comma separated) from API for the above corresponding Table headings.
*  **Page Size:** Select records per page.

*  **Expandable Table with Nested List:** User can select this option if the API has nested List and the user wants to display it as part of the main grid.
*  **Name of the Sub document List from API:** User has to pass the name of the Nested List that needs to be picked from the API output to dispaly the data on click of main grid.
*  **Table Column Headings:** User has to pass the Header names (comma separated) for the Nested table. These names can be different from the API output field names.
*  **Table Column Names From API:** User has to pass the field names (comma separated) from API for the above corresponding Nested Table headings.



**Rest Based Grid On Screen Options:**

*  **Nested List VIew**: If the API has Nested List and confirgured as part of the table then on click of main grid a nested list can be seen as Expanded Grid.
*  **Search**: Smart Search filter. User can search by device/asset name, external id, device id, alert type, etc.
*  **Refresh**: Useful for force reload/refresh devices.
*  **Pagination**: Page navigation options.

 


------------------------------

This Widget is provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________________
For more information you can Ask a Question in the [TECH Community Forums](https://tech.forums.softwareag.com/tag/Cumulocity-IoT).
