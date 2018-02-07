---
title: TOPAZ config file generator
---

**Notebook name**: TOPAZ_config_generator.ipynb

## Start the Notebook

If you need help to access this notebook, check the [How To > Start the python notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## First Time Look

If you are using the notebook for the first time, it should look like this

<img src='/tutorial/notebooks/topaz_config_generator/images/notebook_first_time.png' />

## Define IPTS

Starting from the top **SHIFT + ENTER** the cells in order to run them. The 4th cell will ask you to select the
**IPTS** of your experiment.

<img src='/tutorial/notebooks/topaz_config_generator/images/select_ipts.gif' />

## Run All Cells at Once

Select the **next cell** and click **Cell > Run All Below**.

<img src='/tutorial/notebooks/topaz_config_generator/images/notebook_run_all_cells.gif' />

## File or Folder Selection Tool

In order to select a file or a folder you need to know the following:

 * one dot (**.**) means current folder
 * 2 dots (**..**) means above folder
 * click **select** to validate your file or folder selection
 * selection made will be display above the selection tool
<img src='/tutorial/notebooks/topaz_config_generator/images/file_selection.gif' />

## Widget Interaction

You will find that some of the widgets display depends on your input in other widgets. This has been
implemented to help you in your choice of parameters.

<img src='/tutorial/notebooks/topaz_config_generator/images/widgets_interaction.gif' />

## Advanced Options

Instrument scientists and super users can have access to advanced options by entering a pasword in the **Advanced
Options** cell.

<img src='/tutorial/notebooks/topaz_config_generator/images/advanced_users.gif' />

## Create Config File

And finally, re-run the last cell **Export the Config File** in order to produce the config file. If any information
is missing, a text will show you what is missing. Just click on this link to quickly jump to the widgets in the
notebook.

<img src='/tutorial/notebooks/topaz_config_generator/images/create_config.gif' />

If nothing is missing, the full path to the config file created will be displayed!