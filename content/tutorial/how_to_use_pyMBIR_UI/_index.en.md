---
title: Use pyMBIR_UI
weight: 1100
pre: "<b>5.11 </b>"

---

pyMBIR_UI is a user interface that allows you to easily launch a pyMBIR job, pyMBIR being the AI reconstruction software
developed by Venkat.

<a href='#table_of_contents'></a>
<h1 id="table_of_contents"></h1>

## Table of contents

<ul>
    <li><a href='#connect_to_computer'>Connect to the GPU analysis computer</a></li>
    <li><a href='#launch_the_application'>Launch the application</a></li>
    <li><a href='#presentation_of_the_ui'>Presentation of the UI</a></li>
    <ul>
        <li><a href='#log_book'>Log book</a></li>
        <li><a href='#selection_of_the_data'>Data selection</a></li>
        <li><a href='#reconstruction_setup'>Reconstruction setup</a></li>
        <ul>
            <li><a href='#crop'>Crop</a></li>
            <ul>
                <li><a href="Range of slices">Range of slices</a></li>
                <li><a href="Width">Width</a></li>
            </ul>
            <li><a href='#center_of_rotation'>Center of rotation</a></li>
            <li><a href='#tilt_correction'>Tilt correction</a></li>
        </ul>
        <li><a href='#run_reconstruction'>Run reconstruction</a></li>
        <ul>
            <li><a href="#input">Input</a></li>
            <ul>
                <li><a href="#live">Live reconstruction</a></li>
                <li><a href="#batch">Batch reconstruction</a></li>
            </ul>
            <li><a href="#output">Output</a></li>
        </ul>
        <li><a href="#advanced_settings">Advanced settings</a></li>
    </ul>
</ul>

<h1 id="connect_to_computer"></h1>

## Connect to the GPU analysis computer

In a terminal, type the following command

```
ssh neutrons-dgx01.ornl.gov -Y
```

You will need to enter your UCAMS/XCAMS password and will end up on a window that looks like this.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/login_to_dgx01.png' />

<h1 id="launch_the_application"></h1>

## Launch the application

In order to launch the application, type the following command in the terminal

```
/home/j35/bin/launch_pyMBIR_UI.sh
```

After a few seconds you will see a user interface (UI) showing up, welcome to pyMBIR_UI!

<h1 id="presentation_of_the_ui"></h1>

## Presentation of the UI

Every time you start the application you will have the option to reload the previous session, that means
recover the user interface in the same state your left it. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/load_previous_session.png' />

For first time use, selecting either **yes** or **no** will give you a blank UI. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/blank_ui.png' />

<h1 id="log_book"></h1>

### log book 

A log book allows you to get a detail history of the work done in the UI. To activate the log book, either select in 
the menu **Help > Log** or use the shortcut **COMMAND** + **L**. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/log_book.png' />

<h1 id="selection_of_the_data"></h1>

### Data selection

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

<h1 id="reconstruction_setup"></h1>

### Reconstruction Setup

This tab will allow you:

* crop the region to reconstruct
* define the center of rotation
* define the tilt correction

{{% notice info %}}
You can disable any of those 3 settings by unchecking the top left button next to the settings name.
<img src='/tutorial/how_to_use_pyMBIR_UI/images/enable_settings.png' />
{{% /notice %}}

<h1 id="crop"></h1>

#### Crop

The **crop** tab allows you to define the range of slices (projections) you want to reconstruct, as well as the width
of the slices. You can browse through the projections to make sure the width you are using does not cut part by
mistake any part of the sample. 

<h1 id="range_of_slices"></h1>

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

<h1 id="width"></h1>

##### Width

To select the width of the projections to use in the reconstruction, move the **width** slider. Feel free to play
with the **file index** slider to make sure your sample stays in the field of view.

<img src='/tutorial/how_to_use_pyMBIR_UI/images/crop_width.gif' />

<h1 id="center_of_rotation"></h1>

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

<h1 id="tilt_correction"></h1>

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

First you need to define the projection corresponding to angle 0, and the projection at 180 degrees (or the nearest
projection to 180). Use the button **Set Up Images at 0degree and 180degrees ...** to access a new window that will
allow you to make that selection. Select the **0 degree** image, select the **180 degrees** image and feel free to 
play with the slider to progressively move from the 0 degree projection to the 180 degrees projection in order to 
confirm your choice. Click **OK** when you are done. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/tilt_correction_0_and_180_images_selection.gif' />

Select any of the 3 algorithms and click **Refresh Calculation** to perform the calculation. The tilt correction value
calculated is displayed below the list of algorithms. You can choose to display or not a **guide** that shows the
value of the tilt calculated. Feel free to move this guide on the horizontal axis of the image to confirm the value
calculated. 

<img src='/tutorial/how_to_use_pyMBIR_UI/images/tilt_correction_algorithms.gif' />

<h1 id="run_reconstruction"></h1>

### Run reconstruction

This is where you will launch the reconstruction.

<h1 id="input"></h1>

#### Input

2 modes are proposed according to your needs

* running reconstruction live
* running reconstruction in the background (batch mode)

<h1 id="live"></h1>

#### live reconstruction

The images will be displayed in the Output tab as they are produced by the reconstruction software

<i class="fa fa-thumbs-up" aria-hidden="true"></i> new reconstructed slices are displayed live

<i class="fa fa-thumbs-down" aria-hidden="true"></i> slower than running reconstruction in batch mode

<h1 id="batch"></h1>

#### batch reconstruction

The reconstruction is launched in the background and you can check if any new files has been created by clicking the
**Display latest output file** button. 

<i class="fa fa-thumbs-up" aria-hidden="true"></i> faster than live mode

<i class="fa fa-thumbs-down" aria-hidden="true"></i> user has to manually click refresh to visualize the new reconstructed slices

<h1 id="output"></h1>

#### Output 

<h1 id="advanced_settings"></h1>

### Advanced Settings