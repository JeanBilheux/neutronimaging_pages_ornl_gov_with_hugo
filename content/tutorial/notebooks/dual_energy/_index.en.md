---
title: Dual Energy
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: dual_energy.ipynb

## Description

This notebook provides an automated way to determine the best contrast within an energy range of a region of 
interest selected.

((add link to paper describing the technique here))

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select data input folder

Select the input data folder. This folder should contain all the images recorded by the MCP detector. By default this
folder will contain the time spectra file needed by the program. If it does not, a new window will ask you to browse
for this file once the data have been loaded.

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder that contains the images you need to work on. 

### launch the user interface (UI)

A user interface will show up and may be hidden behind the current browser, make sure you check for it if you don't see
it coming to life. 

<img here>

This UI will allow you to select the region of the image you want to investigate. Then the size of the bin to use and
then launch the calculation. 

#### Select your region of interest

Using your mouse, **move** and **resize** the region of interest displayed on top of the preview (left part of the UI). 
Any action on this box will update the right plot of the Mean transmission vs file index / TOF or lambda. 

<img src='/tutorial/notebooks/dual_energy/images/roi.gif' />

#### Select profile range and size of bins

Using range selection in right plot, select the range you want to work on as well as the size of the bins to use. Those
bins will be displayed inside the range you selected. All images within each bin will be group into one image of average 
counts and used in the next step.

<img src='/tutorial/notebooks/dual_energy/images/range_and_bin_selection.gif' />

#### Calculation

As soon as your click the **Calculation** tab, the algorithm will run. This algorithm will use the region of interest
you selected in the left image and will average the counts of this region, then bin all the images within each bin and 
calculate the ratio of any combination of bins. The ratio with the difference to 1 will be highlighted in the table and 
the corresponding ratio of images displayed in the right side of the **Calculation** tab. 

<img src='/tutorial/notebooks/dual_energy/images/calculation.gif' />

Below the master table, you will find a smaller table that summarizes the infos related to the 'optimum' bin ratio such
as the file index used in the bins, TOF range and lambda ranges.

<img src='/tutorial/notebooks/dual_energy/images/summary_table.png' />

#### Export image

You have the possibility to export the current image displayed in the table by clicking the **Export image ...** button
below the image on the right. Simply select the location where you want to create that image and click **OK**. The
image will be, by default, named using the input folder name as prefix and then the bins used to calculate it. 

for example: IPTS-25778_normalized_bin18_divided_by_bin9.tif