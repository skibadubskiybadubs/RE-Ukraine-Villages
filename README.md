# RE-Ukraine-Villages
 Revit and Grasshopper Interconnection to Automate Drawing Creation

![](https://images.squarespace-cdn.com/content/v1/5ab705d1f407b4b46a9e7fa5/1542746636064-GIGN0KX9N9JUX9N5BDHW/balbek_logo_new.png?format=1000w)


<p> This workflow allows massive-production of geometries using different software, hooked up to Revit via Grasshopper.
<p> Tested geometries using the following software:
- Revit -> Rhino -> Grasshopper -> Revit [Needs additional script, provided in this repo]
- Archicad -> Rhino -> Grasshopper -> Revit [No additional work need]
- Sketchup -> Rhino -> Grasshopper -> Revit [Works well with low-poly geometry mostly]

### HOW TO USE
<p>All .gh files are aimed to work with **REU_VILLAGES_TEMPLATE_REGION_R24_central.rvt**
<p>When starting a new project, use **0reset_sheet_parameters.gh** to reset any possible parameters used by the other scripts, left from previous projects.

#### ReUkraineVillages_RhinoToRevit.gh
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/ReUkraineVillages_RhinoToRevit.png)
<p>The main file to create and place views on Revit sheets.
<p>It uses asynchronious proceses inside Grasshopper and scheduled transactions inside Revit document.

![#f03c15]()<font color="red">Everything marked with RED is for the user input

![#1589F0]()<font color="blue">BLUE - data analysis. If something is missing in Revit document, or something is wrong in Rhino/Grasshopper - it will popup an error (works in Windows only)

<img src="https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/error2.jpg" alt="err" width="20%"/>

![#FDDA0D]()<font color="yellow">Everything marked with YELLOW is dependent on the chosen geometry type

Types of geometry:

**winDec**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/winDec.gif)

**pilaster**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/pilaster.gif)

**cornice**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/cornice.gif)

**winShutters**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/winShutters.gif)

**winPorch**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/winPorch.gif)

**winRoof**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/winRoof.gif)

**winHouse**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/winHouse.gif)

**other**
![](https://github.com/skibadubskiybadubs/RE-Ukraine-Villages/blob/main/utils/gifs/other.gif)


#### 0Revit-to-Rhino.gh
Exports geometry from Revit to Rhino

#### 0explode_view_outline.gh
After manual processing of axonometry view "Explode view", use this script to automatically draw the geometry outline using <Wide Lines>