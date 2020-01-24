---
title: Combine All Images Selected
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: combine_all_images_selected.ipynb

## Description

This notebook allows you to combine the images selected. 3 algorithms are currently
available

 * Arithmetic Mean
 
<img src='/tutorial/notebooks/combine_all_images_selected/images/arithmetic_mean.png' />
 
 * Geometric Mean

<img src='/tutorial/notebooks/combine_all_images_selected/images/geometric_mean.png' />

 * Add
 
{{% notice info %}}
Not seeing the algorithm you want to use? Please let me know and I will add it (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)
{{% /notice %}}
 
**Example:**

**Input**

 * image001.fits
 * image002.fits
 * image003.fits

**Output**

 * image001_image002_image003.fits

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the images to merge

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the images you want to combine. 

### Merging method

It's time to select your merging algorithm (check the description at the top of this web page for
the explanation of the algorithms). 

<img src='/tutorial/notebooks/combine_all_images_selected/images/merging_methods.png' />

### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the combine image.

### Personalize the output file name

If you don't like the default output file name offered, you have here the option to define
your own.

<img src='/tutorial/notebooks/combine_all_images_selected/images/output_filename.png' />

### Merging

Running the next cell will create the merge image and will inform you of the progress via a progress bar. 

<img src='/tutorial/notebooks/combine_all_images_selected/images/merging_in_progress.png' />
