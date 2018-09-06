---
permalink: /habitat
title: "Habitat data"
---
The strongly recommend associated habitat data is imported a as point scores. Following this standard format:

* <a href="https://drive.google.com/open?id=1wt48ftW7r_s4hIR3071Y8Dw6QSCIEY5ox0SVW_wrIwM" target= "_blank">Point scores</a>

This example also include estimates of relief following these <a href="https://github.com/TimLanglois/HabitatAnnotation/blob/master/README.md" target= "_blank">methods</a>. 

For habitat annotation that has been conducted for stereo-BRUV or stereo-DOV deployments there are extensive instructions in this GitHub <a href="https://github.com/TimLanglois/HabitatAnnotation" target= "_blank">repository</a> and <a href="https://github.com/TimLanglois/HabitatAnnotation/blob/master/RWorkflow.md" target= "_blank">R workflows</a> for formatting the data outputs. In addition, for point score habitat annotations of stereo-DOV transects, multiple images are typically analysed throughout a transect and the “Transect” name should be included in the habitat data.

The format and example templates for <a href="https://drive.google.com/open?id=1wt48ftW7r_s4hIR3071Y8Dw6QSCIEY5ox0SVW_wrIwM" target= "_blank">$Habitat.point.score.txt</a> and are shown in Table 9 and Table 10. 

**Table 9.** <i>Format of the <a href="https://drive.google.com/open?id=1wt48ftW7r_s4hIR3071Y8Dw6QSCIEY5ox0SVW_wrIwM" target= "_blank">$Habitat.point.score.txt</a> file</i>
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
    <td>Transect</td>
    <td>String</td>
    <td>Can be blank</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>Can be blank</td>
  </tr>
</table>
<br>

**Table 10.** <i>Head of the <a href="https://drive.google.com/open?id=1wt48ftW7r_s4hIR3071Y8Dw6QSCIEY5ox0SVW_wrIwM" target= "_blank">$Habitat.point.score.txt</a> file</i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Biota: Consolidated</th>
    <th>Biota: Macroalgae</th> 
    <th>Biota: Octocoral.Black</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>0</td>
    <td>9</td>
    <td>1</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>0</td>
    <td>10</td>
    <td>0</td>
  </tr>
  <tr>
    <td><i>NCB608</i></td>
    <td>0</td>
    <td>14</td>
    <td>0</td>
  </tr>
</table>
<br>

##### <a name="Habitat-classes-from-historical-datasets"></a>Habitat classes from historical datasets
We strongly encourage a standardised import of associated habitat information as point scores. However, for historical data sets you may also import habitat data as percent cover and or abiotic and biotic classes. We have not suggested any standards for these classes but examples are included here for <a href="https://drive.google.com/open?id=1JuPXGbkIVeaZqxxh_yAGHVdpicujFAcx8aYwWFP02xw" target= "_blank">$Habitat.percent.cover.txt</a> (Table 11 and 12) and <a href="https://drive.google.com/open?id=1Y9Ut5UOwHB5gvua8xWXNTlNERgAi26aypDkrAISXIHY" target= "_blank">$Habitat.classes.txt</a> (see Table 13 and 14). For data synthesis, standardisation between habitat classes used will have to be made using a custom translation table that can be generated on a case-by-case basis.

**Table 11.** <i>Format of the <a href="https://drive.google.com/open?id=1JuPXGbkIVeaZqxxh_yAGHVdpicujFAcx8aYwWFP02xw" target= "_blank">$Habitat.percent.cover.txt</a> file</i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>None</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>None</td>
  </tr>
</table>
<br>

**Table 12.** <i>Head of <a href="https://drive.google.com/open?id=1JuPXGbkIVeaZqxxh_yAGHVdpicujFAcx8aYwWFP02xw" target= "_blank">$Habitat.percent.cover.txt</a></i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Biota: Consolidated</th>
    <th>Biota: Macroalgae</th> 
    <th>Biota: Octocoral.Black</th>
  </tr>
  <tr>
    <td>NCB606</td>
    <td>0</td>
    <td>0.9</td>
    <td>0.1</td>
  </tr>
  <tr>
    <td>NCB607</td>
    <td>0</td>
    <td>1.0</td>
    <td>0</td>
  </tr>
  <tr>
    <td><i>NCB608</i></td>
    <td>0</td>
    <td>1.0</td>
    <td>0</td>
  </tr>
</table>
<br>
  
**Table 13.** <i>Format of the <a href="https://drive.google.com/open?id=1Y9Ut5UOwHB5gvua8xWXNTlNERgAi26aypDkrAISXIHY" target= "_blank">$Habitat.classes.txt</a> file</i>
<table class="simpleTable">
  <tr>
    <th>Name</th>
    <th>Format</th> 
    <th>On Import checks</th>
  </tr>
  <tr>
    <td>Sample</td>
    <td>String</td>
    <td>None</td>
  </tr>
  <tr>
    <td><i>Others</i></td>
    <td>As many other user defined column names as required</td>
    <td>None</td>
  </tr>
</table>
<br>
  
**Table 14.** <i>Head of <a href="https://drive.google.com/open?id=1Y9Ut5UOwHB5gvua8xWXNTlNERgAi26aypDkrAISXIHY" target= "_blank">$Habitat.classes.txt</a></i>
<table class="simpleTable">
  <tr>
    <th>Sample</th>
    <th>Relief</th>
    <th>Abiotic/Biotic</th> 
  </tr>
  <tr>
    <td>MF-RN02</td>
    <td>Sand</td>
    <td>Sand</td>
  </tr>
  <tr>
    <td>MF-RN05</td>
    <td>HighProfileReef</td>
    <td>Kelp</td>
  </tr>
  <tr>
    <td><i>MF-RN06</i></td>
    <td>LowProfileReef</td>
    <td>Macroalgae</td>
  </tr>
</table>
<br>
