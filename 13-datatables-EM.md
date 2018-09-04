---
permalink: /eventmeasure-datatables
title: "Generating datatables from Eventmeasure"
---
This function is designed to export data tables that contain all the information held within EventMeasure data files (.EMObs files) to facilitate uploading to and archiving data in GlobalArchive. Full details are given in the “EM Database export manual.pdf” found within the GlobalArchive google drive folder or supplied with the EM software.			

The component is an option and you will need a specific licence to access it. To check if you have this, on the EventMeasure window go to the menu About then Version. Under the Installed components, Database output should be listed. Otherwise contact James Seager.

The datatable export function (Program>Generate database output) will generate 9 data tables from a discrete set of .EMObs files that make up a Campaign. 

If you have used comments instead of periods to mark the start time for each BRUV deployment (common in older datasets), ensure you use the “auto-period” function to correct the time for all observations (see instructions here).

You also specify the Base name for the generated tables. For imports into GlobalArchive the Base name should be the CampaignID. If the Base name is “2015-01_Montes.transect_stereoBRUVs”, the function generates the following table files:		

* 2015-01_Montes.transect_stereoBRUVs_Source.txt
* 2015-01_Montes.transect_stereoBRUVs_Info.txt
* 2015-01_Montes.transect_stereoBRUVs_Period.txt
* 2015-01_Montes.transect_stereoBRUVs_MovieSeq.txt
* 2015-01_Montes.transect_stereoBRUVs_Points.txt
* 2015-01_Montes.transect_stereoBRUVs_3DPoints.txt
* 2015-01_Montes.transect_stereoBRUVs_Lengths.txt
* 2015-01_Montes.transect_stereoBRUVs_ImagePtPair.txt
* 2015-01_Montes.transect_stereoBRUVs_Camera.txt 

##### <a name="Troubleshooting-tips2"></a>Troubleshooting tips
* Duplicate OpCodes across .EMObs files will cause an error.
