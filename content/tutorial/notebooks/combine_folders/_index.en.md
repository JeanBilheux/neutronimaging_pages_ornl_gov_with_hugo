---
title: Combine Folders
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: combine_folders.ipynb

## Description

There are situations where you want to combine similar images from different folders. This
is the notebook you were looking for. 

You will need to select the **input** folders first. The program will let you know if 
they do not have the same number of images and will stop there. 

Then you will just need to specify the kind of combination you are looking for (add, mean) and
then the output folder

<img src='/tutorial/notebooks/combine_folders/images/example_combination.png' />
<center>Fig 1: Example of input folders</center>

<img src='/tutorial/notebooks/combine_folders/images/output_folders.png' />
<center>Fig 2: What the output may look like</center>

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the Input Folders

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), you
select all the folders you want to combine. You can interrupt this selection at any time, after having selected at 
least **2 folders**, by pressing **the  button** named 
**<html><span style="font-size: 20px; color:green">Click me when done selecting folders!</span></html>.**

<img src='/tutorial/notebooks/combine_folders/images/select_folders.gif' />

The program will then automatically check that the input folders have the same number of files. 

If they do, you will see the following **<html><span style="color:green">green message</span></html>**, as well
as the list of folders you selected.

<img src='/tutorial/notebooks/combine_folders/images/same_number_of_files.png' />

But if they don't, you will quickly see that something is wrong when
you see the **red message**

<img src='/tutorial/notebooks/combine_folders/images/not_same_number_of_files_new_message.png' />

The only requirement of this notebook is that the folders **must contain the same number of images**.

### How many folders do you want to combine together?

According to the number of folders selected, the program will let you choose the way you want them combined.

For example, if you select **4** folders, you will have the option to combine them by **2, 3 or 4**. If you select 3,
the 4th folder won't be used.

<img src='/tutorial/notebooks/combine_folders/images/how_to_combine.png' />

### How do you want to combine the folders

What algorithm do you want to use to combine them:
 
 * **add**
 * **mean**
 * **median**

<img src='/tutorial/notebooks/combine_folders/images/combine_3algorithms.png' />

{{% notice info %}}
Not seeing the algorithm you want to use? Please let me know and I will add it (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)
{{% /notice %}}

### Do you want to copy over extra files (.txt)

Folders created using the MCP detector contains extra files such as 
 
 * **###_Spectra.txt**
 * **###_ShutterTimes.txt** 
 * **###_ShutterCount.txt**
 
 If you want to conserve those files, make sure the option is turned on. The program will use 
the extra files found in the first folder selected.

<img src='/tutorial/notebooks/combine_folders/images/extra_files.png' />

### Select output folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the output location.

A double progress bar (folder and file progress) will show you the progress of the combination of the folders. 

<img src='/tutorial/notebooks/combine_folders/images/progress_bar.png' />

In our example, let's pretend we selected to combine the folders 2 by 2, the output will look like this

<img src='/tutorial/notebooks/combine_folders/images/output_folders.png' />

