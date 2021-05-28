---
title: Wave Front Dynamics
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: wave_front_dynamics.ipynb

## Description

The main goal of this notebook is to follow the evolution of a wave front over time. 

<img src='/tutorial/notebooks/wave_front_dynamics/images/wave_edge_principle.png' />

The ASCII input data files are produced by other notebooks such as the 
[Radial Profile]({{%relref "/tutorial/notebooks/radial_profile/_index.md#activate-search" %}}) notebook.

This notebook will produce **an ASCII file** of the edge position according to the selected algorithms.

<img src='/tutorial/notebooks/wave_front_dynamics/images/example_of_output.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Profiles Files to Process

Select the profiles files you created (using [Radial Profile]({{%relref "/tutorial/notebooks/radial_profile/_index.md#activate-search" %}})) 
using the **File Selector**. 

<img src='/tutorial/notebooks/wave_front_dynamics/images/loading_ascii_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## UI Presentation

Running the next cell will bring the user interface (UI) to life. 

<img src='/tutorial/notebooks/wave_front_dynamics/images/prepare_data_tab.png' />
<img src='/tutorial/notebooks/wave_front_dynamics/images/edge_calculation_tab.png' />

### Prepare Data Tab

#### Step 1
 
 Make sure you want to perform the calculation on all the files loaded. If you want to exclude any of the files, 
 select the file using the **file index slider** and **turn off** the **Use this file** checkbox. 
 
<img src='/tutorial/notebooks/wave_front_dynamics/images/use_this_file.gif' />
 
#### Step 2
 
 To help the algorithm, select the range of data to use to detect the edge and try to exclude any signal you don't care.
 
<img src='/tutorial/notebooks/wave_front_dynamics/images/select_range.gif' />
  
#### Step 3

 To improve **statistics** and **speed**, play with the **rebin** parameters (size and type). We noticed that in 
 nearly all cases, binning will speed up the algorithms and will help finding the right edge. 
 
<img src='/tutorial/notebooks/wave_front_dynamics/images/rebin.gif' />
  
### Edge Calculation Tab

Once you are done preparing the data, it's time to detect the edge position. 3 algorithms are available and can be
used at the same time to compare the results. Depending on the signal, such or such algorithm may work better than
another one. 

#### List of algorithms available

##### Sliding Average

Check the following document to learn about the algorithm behind it
 [PDF document](/tutorial/notebooks/water_intake_profile_calculator/images/water_intake_calculation.pdf)

##### Error function

The signal is fitted using a modified version of the error function as shown here
<img src='/tutorial/notebooks/water_intake_profile_calculator/images/error_function.png' />

##### Change point

This algorithm uses the following python library ([changepy](https://github.com/ruipgil/changepy))

#### Run algorithms

Select the algorithms you want to use, or click **ALL* to use all of them, then click **Run Algorithm Selected**

<img src='/tutorial/notebooks/wave_front_dynamics/images/run_algorithms.gif' />

#### Export Data

Click the **Export ...** button to create the final ascii file. Select the output folder and click **OK**. 

<img src='/tutorial/notebooks/wave_front_dynamics/images/output_format_explained.png' />
