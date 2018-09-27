---
title: Radial Profile
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: radial_profile.ipynb

## Description

This notebook allows you to display and export the **radial profile** of a set of images. **Radial profile** means
that, after defining the center of your profile region, the closest pixel to the center will produces the first
data point. Then the next ones will produces the second data point (average counts over the set of each pixels).

**Confusing!**

Well the following drawings should help you understand how that works.

### Full circle

* **Step1**: User defined the center of the profile (Red pixel in this example)
* **Step2**: User defined the sector to use (in this case, we used the entire sector 0 -> 360degrees)
* **Program** then calculate the position of each pixel relative to the new center defined
* **Program** order the pixels by their distance relative to the center. All the pixels at the same distance from the
center will have their counts averaged. Profile of Counts vs pixel index position is then calculated.
<img src='/tutorial/notebooks/radial_profile/images/radial_profile_schema1.png' />
<img src='/tutorial/notebooks/radial_profile/images/radial_profile_schema2.png' />

### Sector

* **Step1**: User defined the center of the profile (Red pixel in this example)
* **Step2**: User defined the sector to use
* **Program** keeps only the pixel that are within the sector defined
* **Program** then calculate the position of each pixel relative to the new center defined
* **Program** order the pixels by their distance relative to the center. All the pixels at the same distance from the
center will have their counts averaged. Profile of Counts vs pixel index position is then calculated.
<img src='/tutorial/notebooks/radial_profile/images/radial_profile_schema3.png' />

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

<img src='/tutorial/notebooks/calibrated_transmission/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## Profile UI Presentation

After running the **lauch User Interface** cell, the following GUI pops up.

<img src='/tutorial/notebooks/radial_profile/images/ui_presentation_1.png' />
<img src='/tutorial/notebooks/radial_profile/images/ui_presentation_2.png' />

## Selection of Sector Center

Using the mouse, **click** the **vertical** and then **horizontal** lines on the image window to define the
center of the sector.

<img src='/tutorial/notebooks/radial_profile/images/sector_center.gif' />

## Selection of Sector Range

<img src='/tutorial/notebooks/radial_profile/images/sector_range.gif' />

## Grid Settings

It's possible to change the settings of **the grid** (usefull when color of image and grid are too close).

<img src='/tutorial/notebooks/radial_profile/images/grid_settings.gif' />

## Calculate Radial Profiles

Jump to the **Profile** tab and click the **Calculate Profiles** to calculate the radial profile of each image loaded.
All those profiles will be displayed in the same plot below.

<img src='/tutorial/notebooks/radial_profile/images/calculate_profiles.gif' />

## Export Profiles

Once the **calculation of all profiles** has been performed, the **Export Profiles** button becomes available. Click
the **Export Profiles ...** and select where you want to create the ascii files.

### File Name Convention

The ASCII files creates will have the names bases such as

\<**name_of_image**>_profile_c_x\<**x_center**>_y<**y_center**>_angle_\<**from_angle_in_deg**>_to_\<**to_angle_in_deg**>.txt

__where__:

 * **name_of_image**: is the name of the source image without the extension (*20170811_Nautical_compass_0030_356_250_1875*)
 * **x_center**: the x axis position of the center (*1024.0*)
 * **y_center**: the y axis position of the center (*1024.0*)
 * **from_angle_in_deg**: starting sector angle in degrees (*24.0*)
 * **to_angle_in_deg**: ending sector angle in degrees (*137.0*)

**giving a name of**

20170811_Nautical_compass_0030_356_250_1875_profile_c_x1024.0_y1024.0_angle_24.0_to_137.0.txt

### File Format

Each ASCII file produced start with the following metadata

```
# source image: /Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19621-CLOCK/CT/20170811_Nautical_compass_0030_356_250_1875.tiff
# center [x0, y0]: [1024.0,1024.0]
# angular range from 24.0degrees to 137.0degrees

#pixel_from_center, Average_counts
```

<img src='/tutorial/notebooks/radial_profile/images/profiles_ascii_files.png' />


