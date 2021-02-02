---
title: HFIR reactor elements analysis tool
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: hfir_reactor_element_analysis.ipynb

## Description

This notebook will use the output ASCII file created by the 
[circular profile of a ring]({{%relref "/tutorial/notebooks/circular_profile_of_a_ring/_index.md#activate-search" %}}) 
notebook and will display the peak of each element for each file, side by sided, to study any displacement of the
elements.

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/preview_of_result.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the ASCII file 

Select the profile ASCII file created by the [circular_profile_of_a_ring]({{%relref "/tutorial/notebooks/circular_profile_of_a_ring/_index.md#activate-search" %}})
notebook.

{{% notice info %}}
Check this tutorial if you need help using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})
{{% /notice %}}

### launch the user interface

The interface contains 2 tabs. The first tab **Profiles**, will allow you to select the threshold to use to isolate
the peaks. The second tab **Elements Position** will display the position of each peak for each file loaded. 

#### Profiles tab

First thing to do is to visualize the profile of the tif file loaded (left table) and remove the rows that do not
need to be part of the calculation, for example like the second row selected in the following screenshot.

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/remove_that_data_set.png' />

A default threshold has been selected for the data set loaded. Make sure that threshold makes a clear center cut of
every single data set to use. 

For example, the following examples shows what kind of selection to avoid, and then a better one.

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/seems_like_a_good_choice_but_bad.png' />
<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/better_choice.png' />

Once you are satisfy with the selection, click **Calculate Elements Position**. The program isolate all the 
local maximum, representing the center of each element (red symbols).

Make sure you browse through a random list of input data profile files to make sure you don't see any 
**out of position** peaks, as shown in the following case.

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/bad_minimum_number_of_points_in_peak.png' />

In this case, increase the **minimum number of points in a peak** number in order to force the program to treat
only the real peaks of at least **n** data points. 

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/calculate_elements_position.gif' />

Once the **elements positions** have been calculated, clicking the **Display ideal positions of n elements** will
show in the top plot the ideal positions of those n elements by using the full 360 degrees span starting at the
first element found. 

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/display_ideal_positions.png' />

#### Elements Position tab

This tab displays the peak position of each element for each file. y-axis is the file index and x-axis is the
angular position. Zoom in the top plot to really isolate each element and compare their angular position through
the slices (projections). 

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/second_tab.gif' />

2 tabs are provided at the bottom to quickly locate possible issues. 
 
  * **all peaks found**
  * **missing peaks**
 
The first tab called **all peaks found** displays in red the element position that are outside of the tolerance range
(defined at the bottom of the window).

The second tab called **missing peaks** considers the perfect table of number of files per ideal number of elements and 
shows in red the elements that have not been located in that particular "ideal" location.

{{% notice warning %}}
One should starts worried when the red pattern repeats over multiple images!
{{% /notice %}}

Right click any of the cells of those 2 tables will display the **angle value** and the corresponding **file name**. 

#### Export

You can then just export the data into an ASCII data file by clicking the **Export table data ...** button at the
bottom right corner. 

<img src='/tutorial/notebooks/hfir_reactor_element_analysis/images/output_file.png' />
