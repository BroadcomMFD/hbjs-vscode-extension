<div align="center">

[![Code4z](https://img.shields.io/badge/Code4z-marketplace-cc092f)](https://marketplace.visualstudio.com/search?term=code4z&target=VSCode)
[![OpenIssues](https://img.shields.io/github/issues-raw/BroadcomMFD/hbjs-vscode-extension?label=open%20issues
)](https://github.com/BroadcomMFD/hbjs-vscode-extension/issues)

</div>

# HB.js for VS Code

<!-- We can generalize this overview as more functionality is added. -->
The HB.js for VS Code extension modernizes the way you interact with HostBridge JavaScript Engine (HB.js) and offers a friendly and convenient way to work with HB.js. The HB.js for VS Code extension includes the following features:

- Using HB.js Commands (Make/Put/Run)
- Native generation of a JavaScript object from a COBOL copybook and from an OpenAPI file 
- Access to the Application Explorer (AE) and the AE Playback
- Generating and running automated tests

**Business value**:

- **Accelerated Mainframe Modernization**: Empowers developers to rapidly transform complex CICS transactions into reusable REST/JSON APIs without requiring changes to underlying COBOL code or relying on screen-scraping.

- **Enhanced Developer Productivity and Agility**: Modernizes the mainframe experience by bringing HB.js features directly into VS Code, eliminating the need for traditional "green screen" navigation.

- **Reduced Quality Assurance Cycle Times**: Automatically generates 3270 testing APIs to enable shift-left testing, allowing teams to validate mainframe logic early in the development cycle and replace slow, manual terminal testing with high-speed automated suites.
<br />

<img align="left" alt="This extension is part of the Code4z experience" width="80" height="82" src="https://raw.githubusercontent.com/BroadcomMFD/code4z/refs/heads/main/icon5.png" />

HB.js for VS Code is part of the [Code4z](https://techdocs.broadcom.com/code4z) experience from Broadcom, which offers a modern experience for mainframe application developers. To get started with Code4z, check out our foundational [extension pack](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack).

<br />

We encourage you to share ideas to help improve the HB.js for VS Code Extension. You can also report extension issues, using the following link.

> [Share an idea or open an issue in our Git repository](https://github.com/BroadcomMFD/hbjs-vscode-extension/issues).

<details>
<summary id="addresss-software-requirements"><span style="font-size: 1.5em"><b>Address Software Requirements</b></span><hr></summary>

<p style="margin-left: 20px;"> Before you use the HB.js for VS Code extension, ensure that you meet the following requirements:</p>

### <p style="margin-left: 20px;">   Server</p>

   - HB.js installed on the mainframe
   - A valid mainframe user ID

</details>

 <details>
 <summary id="getting-started"><span style="font-size: 1.5em"><b>Getting Started</b></span><hr></summary> 
  
 <details style="margin-left: 20px;">
 <summary id="specify-a-vs-code-workspace"><span style="margin-left: 20px;"style="font-size: 1.3em">Specify a VS Code Workspace</span></summary>

 <p style="margin-left: 33px;"> The HB.js extension requires a VS Code Workspace for full functionality. To associate a folder with a workspace, open a folder in the <b>Explorer</b> view. </p>

![Specify a Workspace](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/setWorkspace.gif)

</details>

<details style="margin-left: 20px;">
 <summary id="add-a-host-connection"><span style="margin-left: 20px;" style="font-size: 1.3em">Add a Host Connection</span></summary>

 <p style="margin-left: 33px;"> To add a new host connection, select the + (plus) icon in the <b>HB.JS: HOSTS</b> view and enter the following information:</p>

1. The HB.js Host URL, including the port number, and press **Enter**. For example: *http[]()://example.com:9000*
<p style="margin-left: 33px;">The CICS systems programmer responsible for the CICS regions can provide the host URL, including the port number.</p>

2. A Host Name and a Region Name to identify the connection in the **HB.JS: HOSTS** view. These names are labels only, so they can be anything; the URL specifies the connection information. 
3. A Default User ID, which is a user ID that is already defined in CICS on the host. When you connect to the host, you are prompted to enter the password for this user ID.
4. Select **Add Host**.

![Add New Host Connection](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/AddHost251208.gif)

</details>

<details style="margin-left: 20px;">
 <summary id="select-a-default-repository"><span style="margin-left: 20px;" style="font-size: 1.3em">Select a Default Repository</span></summary>
 
<p style="margin-left: 33px;"> In the <b>HB.JS HOSTS</b> view, select a host and a region, right-click the chosen region, and select <b>Set Default Repository</b>.

![Set Default Repository](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/setDefaultRepo.gif)

</details>


<details style="margin-left: 20px;">
 <summary id="use-hb.js-commands"><span style="margin-left: 20px;" style="font-size: 1.3em">Use HB.js Commands</span></summary>

 
 1. Navigate to the **HBJS Terminal** panel, which shows HB.js command output and messages.
  2. To open a file in the **HB.JS: HOSTS** view, right-click the file and select **Get** or double-click a Host file.
  3. Right-click in the editor and select **HB.js Commands > (Make|Put|Run)**.
  
![Execute Primitive](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/primitives251208.gif)

</details>
</details>

<details>

 <summary id="use-the-application-explorer-to-examine-cics-applications"><span style="font-size: 1.5em"><b>Use the Application Explorer to Examine CICS Applications</b></span><hr></summary>

<details style="margin-left: 20px;">
<summary id="access-the-application-explorer"><span style="margin-left: 20px;" style="font-size: 1.3em">Access the Application Explorer</span></summary>
 
<p style="margin-left: 33px;"> To access the Application Explorer, perform the following steps:</p>

  1. Select the Application Explorer icon for the region where you want to run the Application Explorer.
  2. In the **App Explorer** tab, enter the CICS transaction ID for the initial transaction to analyze, and then press **Enter**.

<p style="margin-left: 33px;"> For information about using the Application Explorer, see <a href="https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/hostbridge-javascript-engine/8-0/using/analyze-applications.html">Analyze Applications</a> in the HB.js documentation. </p>
  
![Application Explorer](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/AccessAE251208.gif)
 
</details>

<details style="margin-left: 20px;">
<summary id="access-the-application-explorer-settings"><span style="margin-left: 20px;" style="font-size: 1.3em">Access the Application Explorer Settings</span></summary>

<p style="margin-left: 33px;"> To access the settings for the Application Explorer, perform the following steps:</p>

1. Select the Application Explorer Settings icon for a region.
2. Enter your values and then select **Submit** to save your settings for the selected region.

<p style="margin-left: 33px;"> For information about the Application Explorer settings, see <a href="https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/hostbridge-javascript-engine/8-0/using/analyze-applications/use-the-application-explorer.html">Use the Application Explorer</a> in the HB.js documentation. </p>

![Application Explorer Settings](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/accessAESettings251208.gif)

</details>


<details style="margin-left: 20px;">
<summary id="save-an-application-explorer-session-to-json-file"><span style="margin-left: 20px;" style="font-size: 1.3em">Save an Application Explorer Session to a JSON File</span></summary>

  1. In the Application Explorer, navigate to an active terminal session.
  2. Close the **App Explorer** tab and select **Save** in the pop-up window.
  3. The saved session is stored in the Explorer view under your workspace as <code>App Explorer Playback > [today's date] > *filename*.json</code>.
  
![Execute Primitive](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/generatePlayback251208.gif)

</details>

<details style="margin-left: 20px;">

<summary id="open-an-application-explorer-playback-session-from-json-file"><span style="margin-left: 20px;" style="font-size: 1.3em">Open an Application Explorer Playback Session from a JSON File</span></summary>

  1. In the **Explorer** view, navigate to the saved JSON file.
  > **Note:** If you do not have a saved JSON file, see the preceding section, **Save an Application Explorer Session to a JSON File**.
  2. Right-click on the file and select **HB.js Commands > Application Explorer Playback**. An **Application Explorer Playback** tab opens.
  3. You can access screens directly in the playback by selecting the screen icons.
  
  <p style="margin-left: 33px;"> To progress through the screens sequentially, use the <b>Page Up</b> and <b>Page Down</b> keys. </p>

  <p style="margin-left: 33px;"> For information about the Application Explorer settings, see <a href="https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/hostbridge-javascript-engine/8-0/using/analyze-applications/save-an-application-explorer-session.html">Save an Application Explorer Session</a> in the HB.js documentation. </p>
  
![Execute Primitive](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/accessPlayback251208.gif)

</details>
</details>

<details>
 <summary id="generate-javascript-objects"><span style="font-size: 1.5em"><b>Generate JavaScript Objects</b></span><hr></summary>

 <details style="margin-left: 20px;">
<summary id="generate-a-javascript-object-from-a-cobol-copybook"><span style="margin-left: 20px;" style="font-size: 1.3em">Generate a JavaScript Object from a COBOL Copybook</span></summary>

1. Right-click on a COBOL file in the editor or explorer view and select **HB.js Commands > Generate JS Object**.  
  >**Note:** You can select either COBOL field names to use COBOL-style field names or JavaScript field names to use JavaScript-style field names in the generated file.

<p style="margin-left: 33px;"> The generated HB.js JavaScript object is opened in the editor and is saved to the workspace folder using a filename similar to <code><i>filename</i>_(COBOL|JavaScript)_JSOBJ.hbx</code>.</p>

<p style="margin-left: 33px;">  - <i>filename</i> is the name of the original COBOL file<br>
  - (COBOL | JavaScript) indicates whether the HB.js function is created using COBOL-style or JavaScript-style field names for the object.</p>

2. Select **HB.js Commands > Make** to store the file in the utility repository on the connected mainframe region.
3. Add the following code to your HB.js scripts to access the newly created JavaScript object.

> **Note:** Be sure to replace *filename* and *utility repository* in the require statement with actual values. 
```js
//COBOL Copybook Utilities
var copybookFactory = require('[filename_(COBOL|JavaScript)_JSOBJ]', '[utility repository]');

var demoCopybook = new copybookFactory.commareaBuffer();
var pgm = new CommareaProgram();

//Initialize
demoCopybook.initialize();
pgm.program = 'TRADERBL';

//Commands 
demoCopybook.get()
demoCopybook.set()
pgm.run(demoCopybook.buffer);
```

![JS Object Generation](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/cbGen251208.gif)

</details>

<details style="margin-left: 20px;">
<summary id="generate-a-javascript-object-from-an-openapi-json-file"><span style="margin-left: 20px;" style="font-size: 1.3em">Generate a JavaScript Object from an OpenAPI JSON File</span></summary>

1. In the editor, right-click on an OpenAPI JSON file and select **HB.js Commands > Generate JS Object from OpenAPI**.  
> **Note:** Not all formats are supported at this time. Any unsupported formats are flagged as failed tests.

<p style="margin-left: 33px;"> The generated HB.js JavaScript object is opened in the editor and is saved to the workspace folder using a filename similar to <code><i>filename</i>_OpenAPI_JSOBJ.hbx</code>.</p>

<p style="margin-left: 33px;"><i>filename</i> is the name of the original OpenAPI JSON file.</p>

2. Right-click on the file and select **HB.js Commands > Make** to store the file in the utility repository on the connected mainframe region. 
3. Add the following code to your HB.js scripts to access the newly created JavaScript object.

> **Note:** Be sure to replace *filename* and *utility repository* in the require statement with actual values.

```js
//OpenAPI Utility
var openAPIUtil = require('filename_OpenAPI_JSOBJ', '[utility repository]');

//Retrieve the required schema from your utility file 
var openAPIDefinition = new openAPIUtil.filename();
var openAPISchema = openAPIDefinition.['your files dot notation'].schema;

//Set your object or array of objects that you want to validate against your schema
var sampleData = "your object or array of objects here"; 

//Call the validate function from your generated JS Object 
//This example will write out the output 
writeln (JSON.stringify(openAPIUtil.validate(sampleData, openAPISchema)));

//Sample Output 
  //Pass
  {
    "pass": {
      "type": {
        "message": {
          "expected": "string",
          "found": "string"
        }
      }
    },
    "fail": {},
    "summary": "1 validations have passed, 0 failed"
  }
  //Fail
  {
    "pass": {},
    "fail": {
      "type": {
        "message": {
          "expected": "string",
          "found": "object"
        }
      }
    },
    "summary": "0 validations have passed, 1 failed"
  }

```

![Open API JS Object Generation](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/openAPI251208.gif)

</details>
</details>

<details>
 <summary id="generate-and-run-automated-tests"><span style="font-size: 1.5em"><b>Generate and Run Automated Tests</b></span><hr></summary>


  1. Open an Application Explorer Playback session.
  2. In the upper-left of the playback view, select **Test Mode**.
  3. Add fields to test from one or more application screens:

      a. On a screen to test, select **Field on Screen > Named Fields**.

      b. Right-click on the name of the field to text and select **Toggle Static** to add the field to the test script.
      
      Test scripts populate in the **Tests by Screen** drop-down to the right of each screen that has tests.
  4. To generate all of the tests in a single test script, select **Export Tests** in the upper-left of the playback view.
  5. Select **Save** in the pop-up window to confirm creation of the test script. 
  6. The test script should open in the editor. If it does not open automatically, open the file saved under **App Explorer Test Files > [today’s date]**.
  7. To run the test script, right-click **HB.js Commands > Run**.  
  > **Note**: If your Application Explorer Playback captures the exit of a host application, be sure that all screens where you have selected fields for testing have an active host connection. For information about generating and running automated tests, see <a href="https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/hostbridge-javascript-engine/8-0/programming/generate-and-run-automated-tests.html">Generate and Run Automated Tests</a> in the HB.js documentation.
  8. The output of the test results is displayed in the **HBJS Terminal** panel.
   <p style="margin-left: 38px;"> When you close the recorded session, you have the option to save the selected tests as part of the recording. If you save the tests, they show up when you open the saved session and activate <b>Test Mode</b> in the upper-left of the playback view.</p>
  


  
![Execute Primitive](https://broadcommfd.github.io/hbjs-vscode-extension/GIFs/3270TestGenerator260105.gif)

</details>
</details>

<details>
<summary id="list-of-limitations"><span style="font-size: 1.5em"><b>List of Limitations</b></span><hr></summary>

<p style="margin-left: 18px;"> The following features exist in the HB.js for Eclipse plug-in that are not available in this extension.</p>

- Hex dump view 
- Worklog view

</details>
<details>
<summary id="technical-assistance-and-support-for-hbjs"><span style="font-size: 1.5em"><b>Technical Assistance and Support for HB.js</b></span><hr></summary>

<p style="margin-left: 18px;"> The HB.js extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).</p>

<p style="margin-left: 18px;"> If you are on active support for HostBridge JavaScript Engine, you get technical assistance and support in accordance with the terms, guidelines, details, and parameters that are located within the Broadcom <a href="[url](https://techdocs.broadcom.com/us/product-content/admin-content/ca-support-policies.html?intcmp=footernav)"> Working with Support</a> guide.</p>

<p style="margin-left: 18px;"> This support generally includes:</p>

- Telephone and online access to technical support
- Ability to submit new incidents 24x7x365
- 24x7x365 continuous support for Severity 1 incidents
- 24x7x365 access to Broadcom Support
- Interactive remote diagnostic support
- Technical support cases must be submitted to Broadcom in accordance with guidance provided in “Working with Support”.


<p style="margin-left: 18px;"> Note: To receive technical assistance and support, you must remain compliant with “Working with Support”; be current on all applicable licensing and maintenance requirements; and maintain an environment in which all computer hardware, operating systems, and third-party software associated with the affected Broadcom software are on the releases and version levels from the manufacturer that Broadcom designates as compatible with the software. Changes you elect to make to your operating environment could detrimentally affect the performance of Broadcom software and Broadcom shall not be responsible for these effects or any resulting degradation in performance of the Broadcom software. Severity 1 cases must be opened via telephone and elevations of lower severity incidents to Severity 1 status must be requested via telephone.</p>

---
Copyright © 2026 Broadcom. The term "Broadcom" refers to Broadcom Inc. and/or its subsidiaries.
</details>

<details>
<summary id="privacy-notice"><span style="font-size: 1.5em"><b>Privacy Notice</b></span><hr></summary>

<p style="margin-left: 20px;"> The extensions for Visual Studio Code developed by Broadcom Inc., including its corporate affiliates and subsidiaries, ("Broadcom") are provided free of charge, but in order to better understand and meet its users’ needs, Broadcom may collect, use, analyze and retain anonymous users’ metadata and interaction data, (collectively, “Usage Data”) and aggregate such Usage Data with similar Usage Data of other Broadcom customers. Please find more detailed information in <a href="[url](https://www.broadcom.com/company/legal/licensing)"> License and Service Terms & Repository</a>. </p>


</details>

[def]: #generate-a-javascript-object-from-a-cobol-copybook
