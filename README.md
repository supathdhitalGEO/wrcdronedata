# Complete Process of Drone Image to JOSM TMS Tile for Mapping
## WRC Drone Data Processing
This repository contains the grid drone data of Western Region Campus, Lamachaur Pokhara. We have collected 1041 image of an altitude of average  of 54m from ground, Ground resolution 1.35cm/pix and coverage area of 0.277 square KM. Along with the drone images six Ground Control Points(GCPs) were also taken 
using DGPS. These GCPs were post processing using RTKlib and the centimeter level accurate coordiates were used while preparing the orthophoto. The MetaShapePro sotware is used to process these images and it takes more than 12 hours to complete.The final report of data processing can be accessed from [here](https://github.com/supathdhitalGEO/wrcdronedata/blob/main/Report/Finalreport.pdf).The complete workflow of drone data aqisition to final preparation and its application can be accessed from [here](https://www.researchgate.net/profile/Supath-Dhital/publication/363948628_UAV_technology_its_application_principle_and_workflow_to_disaster_monitoring_and_emergency_response/links/6335b9bf76e39959d68559f5/UAV-technology-its-application-principle-and-workflow-to-disaster-monitoring-and-emergency-response.pdf).
Here is the orthophoto final look. 
<br>
<img src="https://github.com/supathdhitalGEO/wrcdronedata/blob/main/Report/Orthophoto.png"/> 
 
 ## Making Grids
 To make the data online, First we have to change to the small grids and this can be done usinf <b> QGIS </b>, an open source grographic data processing software. The .tif format orthophoto from MetaShapePro was loaded to the QGIS and do following steps on application to make the small grids.
 <li>To activate the Processing toolbox first: Go to View>Panels> Processing ToolBox </li>
 <li>Search XYZ > Raster Tools(Generate XYZ Tiles) </li>
 <li>Fill the Parameters As <br><br> <ul>Extent : Give the orthomosaic layer directory </ul>
 <ul>Set  Minimun and Maximum zoom level of image you want like Min:10 and Max: 20</ul>
 <ul>Set DPI to between 100-500(basically it denotes the pixel dots numbers so high the number~ higher will be the resolution of grid.</ul>
 <ul>Give the saving directory and takes some time to save.</ul>
 </li>
 
 <img src="https://github.com/supathdhitalGEO/wrcdronedata/blob/main/Report/XYZtiles.png"/>
 
 
 Now to make these small grids online, upload all these small grids images to an github and make public. 
 ## Hosting at JOSM
  Open JOSM and goto the Imagery>Imagery Preferences>Tile Map Service(+TMS). Now fill the black space. In first space place a link of your git repo where the map tiles are uploaded and online at, in this format <b>https://supathdhitalGEO.github.io/wrcdronedata/{z}/{x}/{y}.png</b>.The layer name is filled with any what you want the layer name that appears and do OK.
  
 <img src="https://github.com/supathdhitalGEO/wrcdronedata/blob/main/Report/TMSLayer.png"/>
 After that this will be online to JOSM. 

## The report can be found from [Here](https://www.researchgate.net/publication/368535959_Orthophoto_Generation_Using_UAVA_Case_Study_of_Pashchimanchal_Campus_Pokhara).

