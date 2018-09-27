---
title: Registration
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: registration.ipynb

# Description

This notebook will allow the registration (alignment) of a set of images using a reference image of
your choice.

Here are the steps (**bold** for user input/manipulation)

 * **Select the stack of images**
 * launch application
 * Perform Auto alignment
 * and/or
 * Align images manually
 * use profile to help in the alignment and sliders to check images overlap

# Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

## Select Images to Process

Select the images you want to process using the **File Selector**. Once you **click** the **Select** button, the time
stamp and the images will be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## Registration UI

<img src='/tutorial/notebooks/registration/images/description_of_ui.png' />

## Registration Methods

You will find 4 ways to register your data

* <a href='#auto'>Automatic mode</a> (let the program try to align your data for you)
* <a href='#manual'>Manual mode</a> (you have full control of how to move each of the image manually)
* <a href='#marker'>Marker mode</a> (define markers on the images and align them)
* <a href='#profile'>Profile mode</a> (use high contrast feature to align horizontally and vertically images)

<h2 id='auto'></h2>
### Auto Registration

Let the program perform auto-registration of all the images selected using the default first image as a 
reference by clicking **Auto Registration**

<img src='/tutorial/notebooks/registration/images/auto_registration.gif' />

<h2 id='manual'></h2>
### Manual Registration

If you choose to manually align the images (except the reference image), click the **Manual Registration**
button. Then move manually the images selected using the **manual registration tool widgets**. 

<img src='/tutorial/notebooks/registration/images/manual_registration.gif' />

<h2 id='marker'></h2>
### Registration using Markers

Click the **Markers...** button to launch a new window.

<img src='/tutorial/notebooks/registration/images/marker_registration.gif' />

You can define as manay markers as you want for each image. Then using **Align images Using Markers** button will
align all the images according to the best overlap value of the markers.

You can copy/paste markers position using right click on the table.

<img src='/tutorial/notebooks/registration/images/right_click_marker_registration.gif' />

<h2 id='profile'></h2>
### Registration using Profiles

<img src='/tutorial/notebooks/registration/images/registration_profile_description_of_ui.png' />

Using a high contrast feature of the images (like a man made marker on the side of the sample), the program
calculates the edge of this feature for all the images. This edge position (vertically and horizontally) is then
used to register the images. If you are curious about the algorithm used to define the edge position, we are using the
same algorithm as the water intake algorithm called <a href='/tutorial/notebooks/water_intake_profile_calculator/images/water_intake_calculation.pdf'>**sliding average**</a>.

* position the horizontal and vertical profiles on top of high contrast object
* change size (lenght and width) of profile regions if needed
* calculate edge (peak position) of marker in all images

<img src='/tutorial/notebooks/registration/images/registration_profile_tab2_description_of_ui.png' />

* select one of the bottom 3 options to export, save registered images.

## Tools to Help You

### Grid

You can add a **grid** on top of your images to help you in the manual alignment. Click the **Grid > display**
at the top left corner of the UI. Then play with the **slider** to change the size of the grid.

<img src='/tutorial/notebooks/registration/images/grid.gif' />

### Profile

You can display the profile of the image selected and of the reference image to help align the images. 

Simply move the edge of the profile lines. The profile of all the images selected (+ reference image) will be 
displayed.

<img src='/tutorial/notebooks/registration/images/profile.gif' />

### Opacity Slider

The UI provides two types of **opacity sliders**. 

 * Selection vs Reference Image
 * Images Selected
 
#### Selection vs Reference Image
 
 This slider will show up whenever at least one file, other than the reference image, is selected in the
 table (bottom of UI). 
  
  - When the cursor is at the top of the slider, the **mean** of all the images selected 
 is displayed (100% of selection is displayed) 
  - When the cursor is at the bottom of the slider, only the reference image is displayed (0% of selection
  is displayed)
  - All other position will display a *x%* of the selected images and then *(1-x)%* of the reference image.
  
<img src='/tutorial/notebooks/registration/images/reference_selection_slider.gif' />

#### Images Selected 

 Whenever at least two images are selected (other than reference image), a checkbox labeled **all** and \
 a slider will show up on the left of the UI. 
 
 By default all the images selected are display (mean of all images). But if you uncheck the **all** 
 checkbox, then you can gradually display the imagess from the first one to the last one. 
 
 This slider will allow to go from the first image selected to the second by increasing
 the opacity of the first one, and decreasing the opacity of the second one. Once only the second image
 is display, keep moving the cursor will bring to display the third image and the second image will vanish.
 
 The goal of this slider is to gradually display the images one by one. 
 
{{% notice info %}}
The right slider to display current image vs reference image is always available.
{{% /notice %}}
 
 <img src='/tutorial/notebooks/registration/images/images_selected_slider.gif' />
 
## Export

By clicking the **Export ...** button (bottom right) you will export the images registered into a folder you select.

## Advanced users

All the data registered can be access from the python notebook

```python
 >>> data_registered = o_registration.data_dict
 >>> print(np.shape(data_registered['data']))
(8, 2048, 2048)
```

you can also reach the list of file names and their metadata

```python
>>> import pprint
>>> pprint.pprint(data_registered['file_name'])
['/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0000.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0031.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0032.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0033.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0034.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0035.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0036.tif',
 '/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-19921-Charles/02/im0037.tif']
>>> pprint.pprint(data_registered['metadata'][0])
{256: 2048,
 257: 2048,
 258: (16,),
 259: 1,
 262: 1,
 270: 'slope = 2.13626E-05 \roffset = 0.00000E+00\r',
 273: (8,),
 277: 1,
 278: 2048,
 279: (8388608,),
 282: 10.0,
 283: 10.0,
 296: 3,
 320: (0,),
 339: (1,)}
```

