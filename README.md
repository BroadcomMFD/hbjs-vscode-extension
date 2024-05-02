# HB.js

<!-- We can generalize this overview as more functionality is added -->
The HostBridge JavaScript Engine (HB.js) VS Code extension modernizes the way you interact with HB.js and offers a friendly and convenient way to work with HB.js Primitives, the Cobol CopyBook to Javascript object generation tool, and the Application Explorer. 

How can we improve the HB.js VSCode Extension? ![Let us know on our Git repository](https://github.com/BroadcomMFD/hbjs-vscode-extension/issues)

The extension includes the following features:

- Execution of HB.js Primitives (Make/Put/Run)
- Access to the Integrated Application Explorer
- Native generation of a JavaScript object from a COBOL copybook 

## Table of Contents

- [HB.js](#hbjs)
  - [Table of Contents](#table-of-contents)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
    - [Set a VS Code Workspace](#set-a-vs-code-workspace)
    - [Add New Host Connection](#add-new-host-connection)
    - [Select a Default Repository](#select-a-default-repository)
    - [Execute Primitives](#execute-primitives)
    - [Access the Integrated Application Explorer](#access-the-integrated-application-explorer)
    - [Generate a JavaScript object from a COBOL copybook](#generate-a-javascript-object-from-a-cobol-copybook)
  - [List of Limitations](#list-of-limitations)
  - [Privacy Notice](#privacy-notice)
  - [Technical Assistance and Support for HB.js](#technical-assistance-and-support-for-hbjs)


## Prerequisites

Ensure that you meet the following prerequisites before you use the HostBridge JavaScript Engine VS Code extension:

- Access to HostBridge JavaScript Engine


## Getting Started

### Set a VS Code Workspace
The HB.js extension requires a VSCode Workspace for full functionality. To associate a folder with a workspace, open a folder in the Explorer view.

![Set a Workspace](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/setWorkspace.gif)

### Add New Host Connection 
To add a new host connection, click the + (plus) icon in the HB.JS: HOSTS window. A host connection requires the following information:
- HB.js Host URL, including the port number. For example: http://example.com:9000
- A Host Name and a Region Name to help you identify the connection in the Hosts window.
- A Default User ID, which is a user ID already defined in CICS on the host. When you connect to the host, you'll be prompted to enter the password for this user ID.

![Add New Host Connection](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/AddNewHost.gif)

### Select a Default Repository
Host > Region > [Right Click] Chosen Repository > Set Default Repository

![Set Default Repository](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/setDefaultRepo.gif)

### Execute Primitives

  - Navigate to the HBJS Terminal, which shows HB.js command output and messages
  - Open a file in the explorer window ("right-click > Get" or double click a Host file)
  - Right-click in explorer window and select HB.js Commands > (Make|Put|Run) (there are also listed keyboard shortcuts for each) 
  
![Execute Primitive](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/executePrimitve.gif)

### Access the Integrated Application Explorer

To access the Application Explorer:
  - Click the Application Explorer icon next to the region where you want to run the Application Explorer.
  - In the Application Explorer tab, enter the transaction ID for the initial transaction that you want to analyze.
  
  For information about using the Application Explorer, see [Analyzing Applications](https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/hostbridge-javascript-engine/8-0/using/introduction-to-application-analysis.html) in the HB.js documentation.
  
![Application Explorer](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/appExplorer.gif)

### Generate a JavaScript object from a COBOL copybook

- Right-click on a COBOL file in the editor or in the explorer window and select HB.js Commands > Generate JS Object.  
  **Note:** You can select either COBOL field names to use COBOL-style field names or JavaScript field names to use JavaScript-style field names in the generated file.

The generated HB.js JavaScript function is opened in the editor and saved to the workspace folder using a filename similar to `filename_(COBOL|JavaScript)_JSOBJ.hbx`
- *filename* is the filename of the original COBOL file
- (COBOL | JavaScript) indicates whether the HB.js function is created using COBOL-style or JavaScript-style field names for the object.

![JS Object Generation](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/jsObjGen.gif)


## List of Limitations
The following features exist in the HB.js Eclipse plugin that have not yet been added to this extension. 
- Application Explorer Playback 
- Hex dump view 
- Worklog view 

## Privacy Notice

The extensions for Visual Studio Code developed by Broadcom Inc., including its corporate affiliates and subsidiaries, ("Broadcom") are provided free of charge, but in order to better understand and meet its users’ needs, Broadcom may collect, use, analyze and retain anonymous users’ metadata and interaction data, (collectively, “Usage Data”) and aggregate such Usage Data with similar Usage Data of other Broadcom customers. Please find more detailed information in [License and Service Terms & Repository](https://www.broadcom.com/company/legal/licensing).


## Technical Assistance and Support for HB.js

The HB.js is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).

If you are on active support for HostBridge JavaScript Engine, you get technical assistance and support in accordance with the terms, guidelines, details, and parameters that are located within the Broadcom [Working with Support](https://techdocs.broadcom.com/us/product-content/admin-content/ca-support-policies.html?intcmp=footernav) guide.

This support generally includes:

- Telephone and online access to technical support
- Ability to submit new incidents 24x7x365
- 24x7x365 continuous support for Severity 1 incidents
- 24x7x365 access to Broadcom Support
- Interactive remote diagnostic support

Technical support cases must be submitted to Broadcom in accordance with guidance provided in “Working with Support”.

Note: To receive technical assistance and support, you must remain compliant with “Working with Support”, be current on all applicable licensing and maintenance requirements, and maintain an environment in which all computer hardware, operating systems, and third party software associated with the affected Broadcom software are on the releases and version levels from the manufacturer that Broadcom designates as compatible with the software. Changes you elect to make to your operating environment could detrimentally affect the performance of Broadcom software and Broadcom shall not be responsible for these effects or any resulting degradation in performance of the Broadcom software. Severity 1 cases must be opened via telephone and elevations of lower severity incidents to Severity 1 status must be requested via telephone.

---
Copyright © 2024 Broadcom. The term "Broadcom" refers to Broadcom Inc. and/or its subsidiaries.
