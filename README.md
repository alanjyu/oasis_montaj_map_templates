# Montaj Map Templates

This repository provides templates for faster map creation in Geosoft Oasis Montaj.

## Environment
- Geosoft Oasis 2021.2

## To use

1. In Geosoft Oasis Montaj, on the top bar find "Map Tools..." &rarr; "New Map from..." &rarr; "Template Library...".
2. Select one of the above template files, click "OK" to continute. Note: If they are not in the library, you can move the .geosoft_maptemplate files to the library directory (by default, “C:\Users\\[USERNAME\]\Documents\Geosoft\Desktop Applications\maptemplate”).
3. A prompt will show that the template needs coordinates information. This means that map coordinates are undefined, click "OK" to continute.
4. Click "Define from X,Y" or "Define from Lat, Lon". Here you can manually define the coordinates, or choose to scan from either Geosoft GDB or Grid. Recalculate the map scale if necessary. Click "OK" to continute.
5. If the logo file (by default, "logoeng.jpg" at the directory of the project files) cannot be found, a prompt will also show. If that is the case, select the column to the right of "Image name" &rarr; "…" and locate the logo. If no logo is needed, click "delete".
6. Choose the directory for the new map.
7. A series of questions regarding the map will be asked. I strongly recommend to answer them because the texts will be auto-adjusted based on the length of the answer, but you can also change texts on the map later. Leave the answer box blank if you want to remove that piece of information from the map.

## Grid data

To display grid data in the map, on the top bar find "Grind and Image" &rarr; "Display on Map" &rarr; "Grid..." and choose your desired grid file. The grid will then be displayed in the predefined space. Click "Current Map" if you have already created the map with a template.

## Colourbar

You can also choose to add a colourbar while displaying the grid on your map. Enter the location of the colourbar manually or click "Locate" then choose a location you want on the map.

## Note
I’ve defined a series of links that position the elements relative to its surrounding elements so that everything will still look neat once you adjust an element. By default, the grid data takes 75% of the map and information such as titles takes the remaning 25%. However, the links do not carry on once the map is created. This means that every element position becomes absolute.

## Limitation

- Geosoft templates cannot define the sizes of coordinate labels or legends, or any elements related to the data before creating the map.
- Geosoft templates does not include any images which must be stored externally (refer to Step 5).