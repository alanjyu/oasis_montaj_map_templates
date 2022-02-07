# Templates and control files for Geosoft Oasis Montaj

This repository provides template and controls files for map producction in Geosoft Oasis Montaj. The aim of this project is to optimize and standardize the process so that it requires as few user inputs as possible. Click [here](https://github.com/alanjyu/MontajTemplates/archive/refs/heads/main.zip) to download the package. 

## Environment
- [Geosoft Oasis Montaj 2021.2](https://www.seequent.com/products-solutions/geosoft-oasis-montaj/)

## Package structure

This package is separated by catergories: 

- [Templates/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag) contains map templates.
  - [Mag/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag) for magnetic survey maps.
  - [IP/](https://github.com/alanjyu/MontajTemplates/tree/main/IP) for induced polarization survey lines and ties. 
  - [No prompts/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag/No%20prompts) contains templates with textboxes instead of prompts, used to create a custom template for an entire project. 
- [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) contains logos used in the templates. 
- [MAPPLOT/](https://github.com/alanjyu/MontajTemplates/tree/main/MAPPLOT) contains MAPPLOT control files used for further adjustments, and are meant to be used once you have created a map from a template.

## Templates

### Modifying templates
The templates in [Mag/](https://github.com/alanjyu/MontajTemplates/tree/main/Mag) and [IP/](https://github.com/alanjyu/MontajTemplates/tree/main/IP) contain prompts on which you input a series of information pieces before creating a map. If you do not wish to enter them every time, you can customize a template used for an entire project.

1. Open the template by clicking "Map Tools" → "Map Template" → "Open Map Template…"
2. All template folders contain a "No Prompt" folder, specifically for modifying. It is also recommended to back up the templates before modifying them. 
3. Open your desired template in the folder.
4. Double-click the text elements to edit them.
5. Click the "Save" icon on the top left of the template view. Note that this will overwrite your original file.
6. To add the modified template to the library, refer to *Adding templates to library*.

**NOTE**: Geosoft templates are fundamentally XML files. You can edit them with a notepad. Notably, "media" changes the page size.


### Adding templates to library

Montaj scans templates (.geosoft_maptemplate) in "C:\Users\\[USERNAME\]\Documents\Geosoft\Desktop Applications\maptemplate". You can directly copy the templates to this directory. 

In case the template files are not detected, or you are modifying the templates:

1. Open the template in Montaj by clicking "Map Tools" → "Map Template" → "Open Map Template…".
2. Right-click on the template → "Properties".
3. In the properties tab, click "Template".
4. Enter the description and name of your template, then click "Add to library".


### Logos
You can move [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) in "C:\Users\\[USERNAME\]\Documents\Geosoft\Desktop Applications\maptemplate", as they are linked to this directory in the templates.


### Using templates

1. To use the template, in Montaj click "Map Tools" → "New Map from…" → "Template Library".
2. Select one of the templates from your library, click "OK". If no templates show up in the library, refer to *Adding templates to library*.
3. The template itself does not store any coordinate data. Click "Define from X,Y" or "Define from Lat, Lon" → "Scan" from "Grid" or "Geosoft GDB database". Recalculate scale.
4. The template searches for [Logos/](https://github.com/alanjyu/MontajTemplates/tree/main/Logos) in the template library (Refer to *Logos*). If you wish to use a different logo, click on the column to the right of "Image name" → "…" and select the image. You may need to change the image file type in the file explorer in the bottom right. However, if no logo is needed, click "delete".
5. Select where you want to save the map.
6. Enter the questions according to prompt. You can always change them later while editing the map. If you want to modify the template for the entire project, refer to *Modifying templates*.

## MAPPLOT Control files

Files ending with .con are MAPPLOT control files. They provide slightly finer controls than templates. Read documentation [here](https://help.seequent.com/Oasis-montaj/9.9/en/Content/gxhelp/mapplot/mapplot_overview.htm?tocpath=Oasis%20montaj%7CWorkflow%7CAnalyse%20Data%7CEdit%20and%20Manipulate%20Maps%7CWork%20with%20Map%20Templates%7CFigure%20and%20Full%20Map%20Templates%20(MAPPLOT%20Template%20Manager)%7CMAPPLOT%20Topics%20and%20Command%20Reference%7C_____0). 

## Map layer

### Displaying map layer data
Map data are to be displayed into the predefined space (blue rectangles in template view).

1. Click "Grind and Image" → "Display on Map…" → "Grid".
2. Select your **.grd** file.

You can also simply drag your opened grid file to the blue rectangle.

### Adjusting coordinate size

1. Click on the map layer, right-click → "Select all". 
2. Right-click again → "Text attributes", and adjust font sizes.

Alternatively, if you wish to use MAPPLOT files:

1. Click "Map Tools" → "Base Map" → "MAPPLOT Control File...".
2. Select **_basemap.con** in [MAPPLOT/](https://github.com/alanjyu/MontajTemplates/tree/main/MAPPLOT).

### Colourbar

1. Click "Grid and Image" → "Display on Map…" → "Colour Legend Bar...".
2. Select the corresponding data layer.
3. Click "Locate" and click on the map to select the location of the colourbar.
4. To further adjust the colourbar, click "More". Two notable values are "Label decimals" and "Maximum bar height (mm)". For an A4 paper, the recommended value for maximum bar height is 80.

### Contouring

1. Click "Map Tools" → "Contour" and choose one of the contouring options.
2. Choose "Contour" if you want finer controls. Select your input layer and parameters.

Alternatively, if you wish to use MAPPLOT files:

1. Click "Map Tools" → "Contour" → "Have control file". 
2. Select the grid file and cooresponding contouring method in [MAPPLOT/](https://github.com/alanjyu/MontajTemplates/tree/main/MAPPLOT) (**CVG.con**, **GI.con**, **IP.con**, **MF.con**, **RES.con**, and **TF.con**). These parameters are from the previously-made maps.

## Notes
-	I've yet to find an easy way to create a vicinity map view.
-	GX scripting depending on how capable MAPPLOT control files are.
