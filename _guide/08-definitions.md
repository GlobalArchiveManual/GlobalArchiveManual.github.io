---
permalink: /guide/definitions
title: "Definitions"
layout: single
toc: true
---
### <a name="Sample"></a>Sample
* Single observational unit (e.g. a single BRUV deployment or DOV transect).
* Sample/OpCode in the Metadata.csv must EXACTLY match the Sample/OpCode in any associated generic annotation files or standardised datatables.

### <a name="Method"></a>Method
* Any sampling method can be defined by a User, e.g. stereo-BRUVs (baited remote underwater stereo-video), stereo-DOVs (diver operated stereo-video) or UVC (underwater visual sampling) using the “Methods” tab.

### <a name="Campaign"></a>Campaign
* Discrete set (temporal and spatial) of Samples.
* Uses the same sampling and image analysis methods.
* CampaignID is a unique identifier for a Campaign made up of YYYY-MM_Project.name_Method ($ is used to denote a CampaignID throughout this guide).
* All files that are to be uploaded in GlobalArchive need to start with the CampaignID (YYYY-MM_Project.name-Method_Metdata.csv). 

### <a name="Project"></a>Project
* Contains one to multiple Campaigns with a shared purpose/objective (e.g. monitoring of a Marine Park, a bioregional study).
* Project is a unique identifier and the name should be carefully chosen (e.g. “MarineParkMonitoring” is not a good Project name but “Houtman Abrolhos Reef Observation Areas long-term monitoring” is a great Project name)
* Sampling and image analysis methods are generally standardised within a Project but sampling method for each Campaign can be different (e.g. one Campaign could use DOV whereas another Campaign could use BRUV or UVC).

### <a name="Collaboration"></a>Collaboration
* Selective sharing of Campaign data between a group of Users.
