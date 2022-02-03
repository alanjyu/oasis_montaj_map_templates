# Templates for Montaj

This repository provides template files for faster map producction in Geosoft Oasis Montaj.

## Environment
- Geosoft Oasis 2021.2

## Package structure
The templates are separated by three folders: “Mag/” for magnetic survey maps; “IP/” for induced polarization survey lines and ties. Each folder also has a “No prompts/” sub-folder used to modify and create custom templates for each project.

## Modifying templates
By default, the templates are introduced with prompts on which you answer questions for creating maps. If you do not wish to enter them every time, you can create a template suited for the entire project.
1.	Open the template in Oasis by clicking “Map Tools” → “Map Template” →”Open Map Template…”
2.	All template folders contain a “No Prompt” folder, specifically for modifying. It is also recommended to back up the files before modifying them. 
3.	Open your desired template in the folder.
4.	Double-click the text elements to edit them.
5.	Click the “Save” icon on the top left of the template view.
6.	To add the modified template to the library, refer to Adding to library.


**NOTE**: Geosoft templates are essentially .xml files. You can open them with a notepad if you know how to edit them. Notably, “media” changes the page size.

## Adding to library

Montaj scans map template files (.geosoft_maptemplate as extension) in the directory “C:\Users\[USERNAME]\Documents\Geosoft\Desktop Applications\maptemplate”. You can try to copy these files to that directory. In the cases where template files are not detected, or you are modifying the templates:

1.	Open the template in Oasis by clicking “Map Tools” → “Map Template” →”Open Map Template…”
2.	Right click on the template → “Properties”.
3.	In the properties tab, click “Template”.
4.	In this page, you can enter the description and name of your template, then click “Add to library”.
Logos
You can move the “Logos” folder to the template directory at “C:\Users\[USERNAME]\Documents\Geosoft\Desktop Applications\maptemplate”, so that they are referred automatically in the templates.

## Using templates

1.	To use the template, in Montaj click “Map Tools” → “New Map from…” → “Template Library”.
2.	Select one of the templates from your library, click “OK”. If no templates show up in the library, refer to Adding to library.
3.	The template itself does not store any coordinate data. Click “Define from X,Y” or “Define from Lat, Lon” → “Scan” from “Grid” or “Geosoft GDB database”. Recalculate scale.
4.	The template searches for the “Logos/” folder in the template library (Refer to Logos). If you wish to use a different logo, click on the column to the right of “Image name” → “…” and select the image. You may need to change the image file type in the file explorer in the bottom right. However, if no logo is needed, click “delete”.
5.	Select where you want to save the map.
6.	Enter the questions according to prompt. You can always change them later while editing the map. If you want to modify the template for the entire project, refer to Modifying templates.
Displaying map layer data
1.	To display map data into the predefined space (blue rectangles in the template view), click “Grind and Image” →  “Display on Map…” →  “Grid”, and choose your .grd file.
2.	To edit the coordinate font sizes, 
Colourbar
1.	To create a colourbar, click “Grid and Image” → “Display on Map…” → “Colour Legend Map”, and select the corresponding data layer.
2.	Click “Locate” and click on the map to select the location of the colourbar.
3.	Click “Okay”.


## Notes
-	I am working on the vicinity map view.
-	I have found solutions to adjust font weight, coordinate font sizes, and automation using MAPPLOT (.con files). I am currently learning it – it might take a while.
-	I am thinking about GX scripting to produce map templates so that user only needs to enter the project information once, depending on how much I can complete with MAPPLOT control files.
