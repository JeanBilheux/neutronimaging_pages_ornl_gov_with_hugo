---
title: Circular Profile of a Ring
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: circular_profile_of_a_ring.ipynb

## Description

This notebook will create an ASCII output file of the average counts of the pixel within a given ring versus
angle position. Top vertical being the angle 0 and going clockwise. 

<img src='/tutorial/notebooks/circular_profile_of_a_ring/images/description_figure.png' />
<img src='/tutorial/notebooks/circular_profile_of_a_ring/images/preview_of_output.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Images

Select a folder that contains all the images to get profile from. The radiographs will be loaded in memory and a 
progress bar will display the progress of the loading. 

{{% notice info %}}
Check this tutorial if you need help using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})
{{% /notice %}}

### launch the user interface

The user interface contains 3 main parts:
 * on the left - preview of the radiographs loaded + grid + ring selection 
 * on the right - ring, grid and angle bin settings
 * hiding in the slider on the far right - result of circular profile of the ring

#### ring selection

Using the mouse and a simple constant left click, you can move the ring around and use the grid tool (size and color
can be modified) in order to place with high precision the center of the ring. Feel free to use the mouse wheel to
zoom in and/or out the image. 

<<gif here>>

Then you can modify the ring size using either the mouse directly on the plot, or the widgets on the
right of the preview. Via the plot, click and little square box on the bottom right of the ring to change the size
of the ring. You can also play with the **inner radius** slider on the right to change the size.

<<gif here>>

To change the thickness of the ring, play with the **thickness** slider on the right of the preview.

<<gif here>>

#### profile generator tool

The notebook will create a table of counts versus angles. The **angles bins (degrees)** slider allows you to get a 
thinner or coarser profile. To visualize the angle value of each pixel of the ring, click the "angles matrix of ring" 
radio button on top of the preview image. 

<<gif here>>

### calculate profiles

Click the **calculate profiles** button to produce the profile of the ring. A progress bar displayed at the bottom
of the ui will show the progress of the calculation as the program extracts the profile for every single radiograph
your loaded.

<<png here>>

<<explain math behind the profile calculator>>




Once the process is done, the right part of the UI will expand and display the list of images loaded. Select any, one 
or more, of those images to display the profile of mean counts versus angle value.

<<gif here>>

Feel free to play with the plot style widgets, as well as zoom and pan of the plot.

<<gif here>>

### Export profiles ###

Once you are done, click **export profiles ...** to export the profiles data into an ASCII file.