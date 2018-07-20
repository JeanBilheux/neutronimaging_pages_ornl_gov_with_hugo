---
title: Radial Profile
post: "<i class='fa fa-battery-full'></i> "
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

**Comig Soon**