---
permalink: /generic-datatables
title: "Generating generic count, length and mass data"
---
If you do not use EventMeasure or have historical data that pre-dates EventMeasure or you have made changes to data or corrected errors outside of the annotation files (.EMObs) and this changed data is now the “true” copy of the data (e.g. in excel) you will have to import generic files (e.g. Count, Length and Mass).

An example R workflow is provided, to create multiple YYYY-MM_Project.name_Method_Count.txt and YYYY-MM_Project.name_Method_Length.txt files from multiple Campaigns from an Access database:

* [Access database R workflow](https://drive.google.com/open?id=0B3r8G-BQG6W8ck8tN1pNclgyVXc)

**The “Format” and “On import checks” described for the $Count.txt (Table 3), $Length.txt (Table 5) and $Mass.txt (Table 7) indicate the format and requirement of fields for the file to be successfully uploaded. **

An example template for [$Count.txt](https://docs.google.com/spreadsheets/d/190Ury_ORjjUHicIDUQV4QwVsvrGqqdS9jlobgkV6C-o/edit?usp=sharing), [$Length.txt](https://docs.google.com/spreadsheets/d/1PtDiuVhesGo25D6GEMTLGZbzAJ6kjLjhE8KVkgy9us0/edit?usp=sharing) and [$Mass.txt](https://docs.google.com/spreadsheets/d/12XSnvSmXH9aq3vVlQvEtbUUypxY-Ycg5J1w14T23B-o/edit?usp=sharing) are provided, the head of which are shown in Tables 4, 6 and 8 respectively.

For historical BRUV data - if a user wanted to import cumulative MaxN data - they could upload an additional $Points.txt file such as found in a EM datatable output.

**Table 3.** <i>Format of the YYYY-MM_Project.name_Method_Count.txt file</i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Family</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Genus</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Species</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Count</td>
    <td>Numeric</td>
    <td>Is numeric</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>Can be blank</td>
  </tr>
</table>
<br>

**Table 4.** <i>Head of 2015-01-Montes.transect-stereoBRUVs_Count.txt</i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Family</th> 
    <th>Genus</th>
    <th>Species</th>
    <th>Count</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>2</td>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>Labridae</td>
    <td>Coris</td>
    <td>caudimacula</td>
    <td>4</td>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>2</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>3</td>
  </tr>
</table>
<br>

**Table 5.** <i>Format of the YYYY-MM_Project.name_Method_Length.txt file</i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Family</td>
    <td>String</td>
    <td>Can be blank</td>
  </tr>
  <tr>
    <td>Genus</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Species</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Count</td>
    <td>Numeric</td>
    <td>Is numeric</td>
  </tr>
    <tr>
    <td>Length</td>
    <td>Numeric</td>
    <td>Is numeric</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>Can be blank</td>
  </tr>
</table>
<br>

**Table 6.** <i>Head of 2015-01-Montes.transect-stereoBRUVs_Length.txt</i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Family</th> 
    <th>Genus</th>
    <th>Species</th>
    <th>Count</th>
    <th>Length</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>1</td>
    <td>150</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>1</td>
    <td>140</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>Labridae</td>
    <td>Coris</td>
    <td>caudimacula</td>
    <td>1</td>
    <td>190</td>
  </tr>
  <tr>
    <td>NCB608</td>
    <td>Labridae</td>
    <td>Coris</td>
    <td>caudimacula</td>
    <td>1</td>
    <td>180</td>
  </tr>
</table>
<br>

**Table 7.** <i>Format of the YYYY-MM_Project.name_Method_Mass.txt file </i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Family</td>
    <td>String</td>
    <td>Can be blank</td>
  </tr>
  <tr>
    <td>Genus</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Species</td>
    <td>String</td>
    <td>Cannot be blank</td>
  </tr>
  <tr>
    <td>Mass</td>
    <td>Numeric</td>
    <td>Is numeric</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>Can be blank</td>
  </tr>
</table>
<br>

**Table 8.** <i>Head of 2015-01-Montes.transect-stereoBRUVs_Mass.txt</i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Family</th> 
    <th>Genus</th>
    <th>Species</th>
    <th>Mass</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>1.484175026</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>Labridae</td>
    <td>Coris</td>
    <td>caudimacula</td>
    <td>0.2356908879</td>
  </tr>
  <tr>
    <td>NCB608</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>0.941117226</td>
  </tr>
  <tr>
    <td>NCB609</td>
    <td>Nemipteridae</td>
    <td>Pentapodus</td>
    <td>porosus</td>
    <td>1.560714043</td>
  </tr>
</table>
<br>
