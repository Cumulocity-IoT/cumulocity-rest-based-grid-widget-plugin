# Cumulocity Rest Based Grid Widget Plugin [<img width="35" src="https://user-images.githubusercontent.com/67993842/97668428-f360cc80-1aa7-11eb-8801-da578bda4334.png"/>](https://github.com/SoftwareAG/cumulocity-rest-based-grid-runtime-widget-plugin/releases/download/1.0.0-beta/rest-based-grid-runtime-widget-1.0.0-beta.zip)

This Cumulocity Rest Based Grid Widget Plugin is the Cumulocity module federation plugin created using c8ycli. This plugin can be used in Application Builder or Cockpit. This Plugins help you to display API data in Grid view with configurable columns and headings. This widget also supports Nested lists, search and server side pagination, etc.

### Please note that this plugin is in currently under BETA mode.

### Please choose Cumulocity Rest Based Grid Widget Plugin release based on Cumulocity/Application builder version:

|APPLICATION BUILDER | CUMULOCITY  | CUMULOCITY REST BASED GRID WIDGET PLUGIN  |
|--------------------|-------------|-------------------------------------------|
| 2.0.x(coming soon) | >= 1016.x.x | 1.x.x                                     |


## Prerequisites:
   Cumulocity c8ycli >=1016.x.x


## Features

  
*  **Display API data:** Displays API Data for provided API URL in Grid mode. It also supports Nested List.

*  **Pagination:** Configurable Paginations and also option to set default page size.

*  **Configurable Columns:** User can choose what to display in Table from list and also option to display custom Headings.

*  **Device/ Asset:** Ability to select device or asset to pass as input to URL.

   
## Installation

  
### Runtime Deployment?

* This plugin support runtime deployment. Download [Runtime Binary](https://github.com/SoftwareAG/cumulocity-rest-based-grid-runtime-widget-plugin/releases/download/1.0.0-beta/rest-based-grid-runtime-widget-1.0.0-beta.zip) and install via Administrations(Beta mode) --> Ecosystems --> Applications --> Packages 

### Installation of widget through App Builder
  

**Supported Cumulocity Environments:**
  

*  **App Builder:** Tested with Cumulocity App Builder version 1.3.0.

### Local Development?

**Requirements:**
* Git
* NodeJS (release builds are currently built with `v14.18.0`)
* NPM (Included with NodeJS)

**External dependencies:**

```

"@angular/material": "^11.1.2"

"ngx-bootstrap": "6.2.0"

```

**Installation Steps For App Builder:**


**Note:** If you are new to App Builder or not yet downloaded/clone app builder code then please follow [App builder documentation(Build Instructions)](https://github.com/SoftwareAG/cumulocity-app-builder) before proceeding further.



1. Open Your existing App Builder project and install external dependencies by executing below command or install it manually.

    ```

    npm i @angular/material@11.1.2 ngx-bootstrap@6.2.0

    ```
2. Grab the Rest Based Grid widget **[Latest Release Binary](  https://github.com/SoftwareAG/cumulocity-rest-based-grid-widget/releases/download/2.0.1/gp-rest-based-grid-widget-2.0.1.tgz)**.


3. Install the Binary file in app builder.

    ```
    
    npm i <binary file path>/gp-rest-based-grid-widget-x.x.x.tgz

    ```

4. Import GpRestBasedGridWidgetModule in custom-widget.module.ts file located at /cumulocity-app-builder/custom-widgets/

    ```  

    import {GpRestBasedGridWidgetModule} from  'gp-rest-based-grid-widget';

    @NgModule({

    imports: [

    GpRestBasedGridWidgetModule

    ]

    })

    ```

9. Congratulation! Installation is now completed. Now you can run app builder locally or build and deploy it into your tenant.

    ```

    //Start App Builder

    
    npm run start

    // Build App


    npm run build


    // Deploy App


    npm run deploy


    ```

## Build Instructions

**Note:** It is only necessary to follow these instructions if you are modifying/extending this widget, otherwise see the [Installation Guide](#Installation).

**Requirements:**
  * Git  
  * NodeJS (release builds are currently built with `v14.18.0`)
  * NPM (Included with NodeJS)


**Instructions**
1. Clone the repository: 
```
git clone https://github.com/SoftwareAG/cumulocity-rest-based-grid-widget-plugin.git
```
2. Change directory: 
```
cd cumulocity-rest-based-grid-widget-plugin
```
3. Install the dependencies: 
```
npm install
```
4. (Optional) Local development server: 
```
npm start -- --shell cockpit
```
5. Build the app: 
```
npm run build
```
6. Deploy the app: 
```
npm run deploy
```

## QuickStart
  

This guide will teach you how to add plugin in your existing or new dashboard.

  

**NOTE:** This guide assumes you have followed the [Installation instructions](#Installation)

  

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



**Asset Viewer On Screen Options:**

*  **Nested List VIew**: If the API has Nested List and confirgured as part of the table then on click of main grid a nested list can be seen as Expanded Grid.
*  **Search**: Smart Search filter. User can search by device/asset name, external id, device id, alert type, etc.
*  **Refresh**: Useful for force reload/refresh devices.
*  **Pagination**: Page navigation options.

 


------------------------------

These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________________
For more information you can Ask a Question in the [TECH Community Forums](https://tech.forums.softwareag.com/tag/Cumulocity-IoT).
