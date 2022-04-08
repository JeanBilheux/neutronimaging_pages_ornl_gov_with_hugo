---
title: Table of contents
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: A_TABLE_OF_CONTENTS.ipynb

## Description

**Top part** of the notebook gives a quick way to access the notebooks.

**Bottom part** allows **super users** (who knows the secret access code) to edit the configuration file and changed

 * turn on and off **debugging** mode
 * list folders to look for when working in debugging mode
 * defined the percentage of images to use when using [ROI selection tool]({{%relref "/tutorial/notebooks/roi_selection_tool/_index.md#activate-search" %}})
 
## Super User

Enter the **secret code** to enable all the widgets. To get this code, please contact <a href="/credits#jean_bilheux">Jean Bilheux</a>.

### Debugging mode

Once activated, the notebooks won't start looking at the usual file structure found on our analysis machine (/HFIR/CG1D, /SNS/SNAP, /SNS/VENUS), 
but instead at the list of folders provided in the following widgets. If the first folder can be found, this folder 
will be used as the default entry point of any file dialog box. Otherwise, it moves to the next one and so on.

### List of folders

It's possible to **remove** folfers from the list or to **add** new ones using the widgets under the selection tool.
To add a new folder, define the folder in the **New folder** field and click **+**. The folder is added to the list
**only if the folder path exists in the current OS**. 

### Percentage of images to use

A few notebooks, such as the [normalization]({{%relref "/tutorial/notebooks/normalization/_index.md#activate-search" %}}) and
[normalization_with_simplify_selection]({{%relref "/tutorial/notebooks/normalization_with_simplify_selection/_index.md#activate-search" %}}) notebooks,
you may need to select a region of interest of the background in the sample data set. Instead of loading
the entire stack of images provided, the program uses **a percentage**, represented by this number here, of the entire stack. 
Only that percentage of images will be combined, using mean, and used as integrated image to facilitate
the ROI selection. Those images will be chosen randomly. 

### Save changes

Click the **Save Changes** button to validate and record your changes. 

<img src='/tutorial/notebooks/table_of_contents/images/advanced_user_demo.gif' />


{{% notice info %}}
If you are working from the analysis machine,
those changes will be reset next time you restart the notebooks from the shortcut menu button.
{{% /notice %}}
