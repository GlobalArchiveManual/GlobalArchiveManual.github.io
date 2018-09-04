---
permalink: /metadata-file
title: "Creating the Metadata file"
---
The Metadata file can be prepared in excel or google sheets and must be saved as a comma-separated values file (.csv). 

**The “Format” and “On import checks” described in Table 1 indicate the format and requirement of fields for the YYYY-MM_Project.name_Method_Metadata.csv file to be successfully uploaded.**

An example template is provided [here](https://docs.google.com/spreadsheets/d/10N9d1bSo7Y-DPvp7xigQwlzH68wZ8rR_LXIETSNGKTE/edit?usp=sharing), the head of which is shown in Table 2. Additional columns with project specific information can be added to the end of the sheet as required.

Two example R workflows are provided, to create multiple $Metadata.csv files from either:
* [GoogleSheet or excel files](https://drive.google.com/open?id=0B3r8G-BQG6W8WU1mQmdaUnFTSmc)
* [Access database](https://drive.google.com/open?id=0B3r8G-BQG6W8ck8tN1pNclgyVXc)

And examples of how to fix common formatting issues for YYYY-MM_Project.name_Method_Metadata.csv files are given:
* [Fix format issues in $Metadata.csv](https://drive.google.com/open?id=0B3r8G-BQG6W8TF9yVzJxU3Z3Qjg)

**Table 1.** <i>Format of the $Metadata.csv file, note the tables described below are transposed (rows for columns) for formatting convenience. </i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>Required. Cannot be blank</td>
  </tr>
  <tr>
    <td>Latitude</td>
    <td>Decimal degrees</td>
    <td>Required. Is numeric between -90 to 90</td>
  </tr>
  <tr>
    <td>Longitude</td>
    <td>Decimal degrees</td>
    <td>Required. Is numeric between -180 to 180</td>
  </tr>
  <tr>
    <td>Date</td>
    <td>String in YYYYMMDD format e.g. 19990101 for 1st of January 1999</td>
    <td>Required. Is YYYYMMDD</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>hh:mm:ss</td>
    <td>Required. Is hh:mm:ss</td>
  </tr>
    <tr>
    <td>Location</td>
    <td>String</td>
    <td>Column name but can be blank</td>
  </tr>
    <tr>
    <td>Status</td>
    <td>MPA status (must be Fished, No-take, I, II, III, IV, V, VI)</td>
    <td>Column name but can be blank</td>
  </tr>
  <tr>
    <td>Site</td>
    <td>String</td>
    <td>Column name but can be blank</td>
  </tr>
  <tr>
    <td>Depth</td>
    <td>Numeric</td>
    <td>Required. Is numeric</td>
  </tr>
    <tr>
    <td>Observer</td>
    <td>String</td>
    <td>Column name but can be blank</td>
  </tr>
    <tr>
    <td>Successful.count</td>
    <td>String (must be Yes or No)</td>
    <td>Required. Cannot be blank</td>
  </tr>
  <tr>
    <td>Successful.length</td>
    <td>String (must be Yes or No)</td>
    <td>Required. Cannot be blank</td>
  </tr>
    <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>Can be blank</td>
  </tr>
</table>
<br>

**Table 2.**<i> Head of example YYYY-MM_Project.name_Method_Metadata.csv file 
([2015-01_Montes.transect-stereoBRUVs_Metadata.csv](https://docs.google.com/spreadsheets/d/10N9d1bSo7Y-DPvp7xigQwlzH68wZ8rR_LXIETSNGKTE/edit?usp=sharing)) </i><br>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Latitude</th> 
    <th>Longitude</th>
    <th>Date</th>
    <th>Time</th> 
    <th>Location</th>
    <th>Status</th>
    <th>Site</th> 
    <th>Depth</th>
    <th>Observer</th>
    <th>Successful.count</th> 
    <th>Successful.length</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>-20.408</td>
    <td>115.48192</td>
    <td>20150117</td>
    <td>08:45:00</td>
    <td>Montes</td>
    <td>Fished</td>
    <td>1</td>
    <td>25.7</td>
    <td>Tim</td>
    <td>Yes</td> 
    <td>Yes</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>-20.407</td>
    <td>115.47612</td>
    <td>20150117</td>
    <td>08:48:00</td>
    <td>Montes</td>
    <td>Fished</td>
    <td>1</td>
    <td>29</td>
    <td>Tim</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>NCB608</td>
    <td>-20.405</td>
    <td>115.46842</td>
    <td>20150117</td>
    <td>08:56:00</td>
    <td>Montes</td>
    <td>Fished</td>
    <td>1</td>
    <td>30.4</td>
    <td>Tim</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<br>

##### <a name="Troubleshooting-tips"></a>Troubleshooting tips
Changing the default program that opens .txt files to Excel may help with this process.
* Beware - Excel will parse any recognisable date and time data into the computer's system default format - which may not match the required format for the $Metadata.csv.
* You may think you have the date format correct  - but if you open the file in Excel - it will change the format!
* You can use R to format your metadata.csv file.
* Another option is to set Windows system defaults, Click on Start>Control Panel>Region and Language (this will differ between versions of Windows) and ensure the defaults match those below: 

* It is recommended that the above template for Metadata is used for new Campaigns to reduce data manipulation and re-formatting before uploading to GlobalArchive. 
* If any required data is missing, enter obvious dummy values that can be corrected in the future (e.g. for Depth enter 0, for Latitude or Longitude enter a site position or local port position, Time enter 00:00:00).
* If your longitude and latitude are in the wrong format use a batch converter tool such as: https://www.earthpoint.us/SignIn.aspx. A free account can be requested if it is for educational purposes. 
* For an EM/Stereo import, the “Sample” value must match the OpCode in EventMeasure exactly and is case sensitive. 

TIP: To make sure these match use the list of OpCodes in the Info file to create your Metadata file (the Info file is exported during the EventMeasure datatable process outlined below). If any of these do not match open the corresponding .EMObs file in EventMeasure, edit the OpCode in the information field and save the file before exporting [datatables](https://globalarchivemanual.github.io/guide/eventmeasure-datatables).
* To fix formatting issues using R, see  [Fix format issues in $Metadata.csv](https://drive.google.com/open?id=0B3r8G-BQG6W8TF9yVzJxU3Z3Qjg)
