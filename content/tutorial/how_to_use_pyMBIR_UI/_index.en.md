---
title: Use pyMBIR_UI
weight: 1100
pre: "<b>5.11 </b>"

---

pyMBIR_UI is a user interface that allows you to easily launch a pyMBIR job, pyMBIR being the AI reconstruction software
developed by Venkat.

## Connect to the GPU analysis computer

In a terminal, type the following command

```
ssh neutrons-dgx01.ornl.gov -Y
```

You will need to enter your UCAMS/XCAMS password and will end up on a window that looks like this.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/login_to_dgx01.png' />

## Launch the application

In order to launch the application, type the following command in the terminal

```
/home/j35/bin/launch_pyMBIR_UI.sh
```

After a few seconds you will see a user interface (UI) showing up, welcome to pyMBIR_UI!

## Presentation of the UI

Every time you start the application you will have the option to reload the previous session, that means
recover the user interface in the same state your left it. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/load_previous_session.png' />

For first time use, selecting either **yes** or **no** will give you a blank UI. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/blank_ui.png' />

### log book 

A log book allows you to get a detail history of the work done in the UI. To activate the log book, either select in 
the menu **Help > Log** or use the shortcut **COMMAND** + **L**. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/log_book.png' />

### Selection of the data

The UI guides you by using <html><font color='green'><strong>green</strong></font></html> markers/clues such as the 
first one you see when starting a new interface (no previous sessions loaded).  

<img src='/tutorial/how_to_use_pyMBIR_UI/images/start_input.png' />

You can either manually defined the projections folder, or click **Select ...** to browse and navigate to the 
raw projections. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/select_projections.gif' />

From there you can either load the next data set, the open beam **OB**, or visualize the data you already loaded by
clicking the **Preview ...** button. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/preview_of_images.gif' />

Following the same principle, Select the **Open Beam (OB)**, the **Dark Field (DF)** folders.

Next, select the **Output** folder where the reconstructed data will be created.

Once the **projections**, **ob**, **df** and output folder have been selected, the next tab **Reconstruction Setup** 
becomes enabled.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/data_selection_done.png' />

{{% notice info %}}
The status bar of the user interface display various messages to inform the user of the workflow, such as
result of loading the data, if any error was raised....etc. 
<img src='/tutorial/how_to_use_pyMBIR_UI/images/status_bar.png' />
{{% /notice %}}

### Reconstruction Setup

This tab will allow you:

* crop the region to reconstruct
* define the center of rotation
* define the tilt correction

{{% notice info %}}
You can disable any of those 3 settings by unchecking the top left button next to the settings name.
<img src='/tutorial/how_to_use_pyMBIR_UI/images/enable_settings.png' />
{{% /notice %}}

#### Crop

The **crop** tab allows you to define the range of slices (projections) you want to reconstruct, as well as the width
of the slices. You can browse through the projections to make sure the width you are using does not cut part by
mistake any part of the sample. 

##### Range of slices

To select the range of slice you want to use you can either 

 * **click** and **drag** any of the top and/or bottom <html><font color='cyan'><strong>cyan</strong></font></html>
  lines on the image 
 * **enter manually** the from slice and/or to slice values (remember to hit **ENTER** after
manual input to validate the new slice values).

{{% notice warning %}}
Because of a bug in one of the library used, the original image displayed is zoom out. To get the projection in full
view, click the **A** logo in the bottom left corner of the plot.
<img src='/tutorial/how_to_use_pyMBIR_UI/images/bug_in_crop_zoom.gif' />
{{% /notice %}}

The following animation illustrates how the range of slices to use can be defined.
<img src='/tutorial/how_to_use_pyMBIR_UI/images/crop_slice_range.gif' />

#### Width

To select the width of the projections to use in the reconstruction, move the **width** slider. Feel free to play
with the **file index** slider to make sure your sample stays in the field of view.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/crop_width.gif' />

#### Center of Rotation

You can define the **center of rotation** manually using either:

 * **user defined** checkbox
 * TomoPy algorithm

The TomoPy algorithm request you to define the images at **0 degree and 180 degrees**. The program will make a guest
for you according to the name of the files. It's up to  you to confirm or not that selection. If you decide to manually
define the center of rotation, simply enter the new value in the field showing up when the **User defined** button
is checked.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/center_of_rotation.gif' />

{{% notice info %}}
If you want to learn more about the **TomoPy** algorithm to determine the center of rotation, please refer to
its [documentation](https://tomopy.readthedocs.io/en/latest/api/tomopy.recon.rotation.html)
{{% /notice %}}

#### Tilt Correction

3 algorithms are offered to estimate the tilt correction

 * direct minimization
 * phase correlation
 * use center

{{% notice info %}}
**Direct minimization**
In this algorithm, the 0 degree image is compared with the flip 180 degrees images. Various tilt values are 
applied in order to minimize the difference of those 2 images
{{% /notice %}}

{{% notice info %}}
**Phase correlation**
Same as **direct minimization** but in Fourier transform space.
{{% /notice %}}

{{% notice info %}}
**Use center**
TBD
{{% /notice %}}


 
 
 