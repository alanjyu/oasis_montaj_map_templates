# Templates for Montaj

This repository provides template and controls files for faster map producction in Geosoft Oasis Montaj. The aim of this project is to streamline the project so that it requires as few user inputs to make standardized maps as possible. Click [here](https://github.com/alanjyu/MontajTemplates/archive/refs/heads/main.zip) to download the package. 

## Environment
- Geosoft Oasis Montaj 2021.2

## Package structure
The templates are separated by catergories: [Mag/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag) for magnetic survey maps; [IP/](https://github.com/alanjyu/MontajTemplates/tree/main/IP) for induced polarization survey lines and ties. Each folder also has a sub-folder named [No prompts/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag/No%20prompts) with templates used to modify and create custom templates for each project. [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) contain logo images used in the templates. [MAPPLOT/](https://github.com/alanjyu/MontajTemplates/tree/main/MAPPLOT) contains MAPPLOT control files used for further adjustments once you create a map from a template.

## Modifying templates
By default, the templates are introduced with prompts on which you answer questions while creating maps. If you do not wish to enter them every time, you can customize a template used for the entire project.
1. Open the template by clicking "Map Tools" → "Map Template" → "Open Map Template…"
2. All template folders contain a "No Prompt" folder, specifically for modifying. It is also recommended to back up the templates before modifying them. 
3. Open your desired template in the folder.
4. Double-click the text elements to edit them.
5. Click the "Save" icon on the top left of the template view. Note that this will overwrite your original file.
6. To add the modified template to the library, refer to *Adding templates to library*.

**NOTE**: Geosoft templates are essentially .xml files. You can open them with a notepad if you know how to edit them. Notably, "media" changes the page size.


### Adding templates to library

Montaj scans map template files (.geosoft_maptemplate as extension) in the directory "C:\Users\\[USERNAME\]\Documents\Geosoft\Desktop Applications\maptemplate" by default. You can try to copy these files to that directory. 

In the cases where template files are not detected, or you are modifying the templates:

1. Open the template in Montaj by clicking "Map Tools" → "Map Template" → "Open Map Template…".
2. Right-click on the template → "Properties".
3. In the properties tab, click "Template".
4. Enter the description and name of your template, then click "Add to library".


### Logos
You can move [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) to Geosoft's template directory at "C:\Users\\[USERNAME\]\Documents\Geosoft\Desktop Applications\maptemplate", so that they are linked automatically in the templates.


## Using templates

1. To use the template, in Montaj click "Map Tools" → "New Map from…" → "Template Library".
2. Select one of the templates from your library, click "OK". If no templates show up in the library, refer to *Adding templates to library*.
3. The template itself does not store any coordinate data. Click "Define from X,Y" or "Define from Lat, Lon" → "Scan" from "Grid" or "Geosoft GDB database". Recalculate scale.
4. The template searches for [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) in the template library (Refer to *Logos*). If you wish to use a different logo, click on the column to the right of "Image name" → "…" and select the image. You may need to change the image file type in the file explorer in the bottom right. However, if no logo is needed, click "delete".
5. Select where you want to save the map.
6. Enter the questions according to prompt. You can always change them later while editing the map. If you want to modify the template for the entire project, refer to *Modifying templates*.

## MAPPLOT Control files
Files with .con extensions are MAPPLOT control files. They provide finer controls than simple template files. You can see the documentation [here](https://help.seequent.com/Oasis-montaj/9.9/en/Content/gxhelp/mapplot/mapplot_overview.htm?tocpath=Oasis%20montaj%7CWorkflow%7CAnalyse%20Data%7CEdit%20and%20Manipulate%20Maps%7CWork%20with%20Map%20Templates%7CFigure%20and%20Full%20Map%20Templates%20(MAPPLOT%20Template%20Manager)%7CMAPPLOT%20Topics%20and%20Command%20Reference%7C_____0). 

## Map layer

### Displaying map layer data
Map data are displayed into the predefined space (blue rectangles in template view). Click "Grind and Image" → "Display on Map…" → "Grid", and select your **.grd** file.

### Adjusting coordinate size
To change coordinate font size, click on the map layer, right-click → "Select all". Right-click again → "Text attributes". Here you can adjust font sizes.

**NOTE**: Template files do not have access to viable information from the map layer data, so you have to edit them manually as of now.

Alternatively, if you wish to use MAPPLOT files, click "Map Tools" → "Base Map" → "MAPPLOT Control File..." and select **_basemap.con** in [MAPPLOT/](https://github.com/alanjyu/MontajTemplates/tree/main/MAPPLOT).

### Colourbar
Click "Grid and Image" → "Display on Map…" → "Colour Legend Map", and select the corresponding data layer. Click "Locate" and click on the map to select the location of the colourbar.

### Contouring
You can click "Map Tools" → "Contour" and choose one of the contouring options. Choose "Contour" if you want more controls.

Alternatively, if you wish to use MAPPLOT files, click "Map Tools" → "Contour" → "Have a control file". Select the grid file and cooresponding contouring parameters for your map (**CVG.con**, **GI.con**, **IP.con**, **MF.con**, **RES.con**, and **TF.con**). These parameters are from the previously-made maps.

## Notes
-	Vicinity map view.
-	GX scripting depending on how capable MAPPLOT control files are.
