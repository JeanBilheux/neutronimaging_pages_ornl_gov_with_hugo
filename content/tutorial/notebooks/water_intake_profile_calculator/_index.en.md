---
title: Water Intake Profile Calculator
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: water_intake_profile_calculator.ipynb

## Description

This notebook will calculate the water intake profile vs time of a sample.

{{% notice info %}}
This application is still under heavy development. The look of the UI will differ from the screenshot you
can see in this tutorial and features are added on a regular basis. The tutorial will be fully rewrite once the development
is done.
<img src='/tutorial/notebooks/water_intake_profile_calculator/images/new_ui.png' />
{{% /notice %}}

Here are the steps (**bold** for user input/manipulation)

 * **select the normalized images**
 * images sorted by time (by default)
 * User Interface pops up!
 * **region of interest selected**
 * (optional) change the sorting algorithm
    * by name
    * by date
 * (optional) select a folder containing the original .dsc files (which contain the right time stamp)
 * profile of counts vs vertical-pixel calculated (**select integrated algorithm: mean/median/sum**)
 * water intake profile vs file index or vs time
 * **export profiles**
 
## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Images to Process

Select the images you want to process using the **File Selector**. Once you **click** the **Select** button, the time
stamp and the images will be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

<h2 id='select_profile'></h2>
### Water Intake Calculator UI

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/description_of_ui.png' />

#### Resizing widgets

It's possible to resize or move any of the plots.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/resizing_windows.gif' />

#### Sorting Algorithm

By default, all the images are sorted using their time stamps. But in some cases (old IPTS), the time stamp may
be wrong. So It's possible to:

  * either sort them using their name and let you define the time interval between the runs
  * define a folder that contains the *.dsc* files created by the MCP. Those files contain in all cases, the correct
time stamp.
<img src='/tutorial/notebooks/water_intake_profile_calculator/images/sorting_algorithm.gif' />

#### Profile Algorithm

You can select the profile algorithm to use (to integrate over the x-axis of the region selected) using the
profile algorithms available

 * add
 * mean
 * median

The profile is calculated using the following method:

 * retrieve the region you defined in the top left image
 * using the profile algorithm you selected, will integrate over the x-axis of the ROI
 * display the profile vs the y-pixels.

#### Using Pixel or Size Reference

By default the water intake profile display the position of the "wave" as a pixel number vs the time. But it's also
possible to display this one using a real dimension (mm). To do so, just click the **water intake y_axis -> distance**
check box and define the dimension of the pixel.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/pixel_size.gif' />

#### Integration Direction

In the new version of the application, it is now possible to specify the direction of integration of the profiles.
Select either **y_axis** or **x_axis** to change this direction.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/integration_direction.gif' />

#### Water Intake Algorithms

It's possible to chose between 2 different algorithms to calculate the "wave" front position.

##### **Sliding Average**

This method is fully demonstrated in this [PDF document](/tutorial/notebooks/water_intake_profile_calculator/images/water_intake_calculation.pdf)

##### **Error Function Fitting**

The signal is fitted using a modified version of the error function as shown here

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/error_function.png' />

##### **Change Point**

You can now select a 3rd algorithm based on the following python library ([changepy](https://github.com/ruipgil/changepy))

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/change_point.png' />

### Rebin

For very poor statistics data, you can rebin the data by 2, 3 or more pixels. This will decrease the resolution of the
water intake peak position, but will improve its calculation by the various algorithms (sliding average, error function, ...)


### Live Demo

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/live_demo.gif' />

#### Export Results

You can export the following data

 * profile (**Export > Profiles ...**)
 * water intake (**Export > Water Intake ...**)
 * Table (**Export Table ...**, on the right of the table)

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/export_files.png' />

{{% notice tip %}}
**For Advanced Users**. keep reading!
{{% /notice%}}

#### Want to Work on the Data in the Notebook?


If you want to play yourself with the data loaded, you can easily access all the data and metadata loaded

```python
list_of_data = o_gui.dict_data['list_data']
```
<img src='/tutorial/notebooks/water_intake_profile_calculator/images/list_data.png' />

```python
list_of_files = o_gui.dict_data['list_images']
```
<img src='/tutorial/notebooks/water_intake_profile_calculator/images/list_files.png' />

```python
list_of_time_stamp = o_gui.dict_data['list_time_stamp']
list_of_time_stamp_user_format = o_gui.dict_data['list_time_stamp_user_format']
```

