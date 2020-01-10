---
date: 2016-04-09T16:50:16+02:00
title: Frequently Asked Questions
pre: "<b>3. </b>"
weight: 300
---

## Before Your Venue

#### Proposal

{{%expand "How do I submit a proposal?" %}}
<ul>
<li>To learn more about submitting a proposal for beam time, go to <a href='https://neutrons.ornl.gov/users'>neutrons.ornl.gov/users</a>.</li>
<li>To submit your proposal, go to the <a href='https://snsapp1.sns.ornl.gov/xprod/f?p=100'>proposal system</a>.</li>
</ul>
{{% /expand%}}

## During your Experiment

{{%expand "Where can I stay?" %}}
A few options are available off-site and on-site. Check the <a href='https://neutrons.ornl.gov/users/daily-living#stay'>
neutron.ornl.gov users page</a> for more infos.
{{% /expand%}}

## Data Analysis
{{%expand "I forgot my XCAMS password" %}}
Simply go to <a href='https://user.ornl.gov/Account/ForgottenPassword?reqid='>How to reset password</a> web page. 
{{% /expand%}}
{{%expand "How can I browse my data?" %}}
Using <a href='https://oncat.ornl.gov/#/'>ONCat</a>, you will be able to
<ul>
 <li>view your data</li>
 <li>view the metadata and get infos about such or such data set</li>
 <li>find an experiment using keyword</li>
 <li>More features coming soon</li>
</ul>
<img src='/faq/images/oncat.png' />

{{% /expand%}}
{{%expand "How can I get help analyzing my data?" %}}Just contact [Jean Bilheux](/en/credits#jean_bilheux) to discuss
your needs.

By going over your experiment together, Jean will show you how to run the current tools and will develop customed python
notebooks if needed.
{{% /expand%}}
{{%expand "What are those 'jupyter notebooks'?" %}}
The *jupyter notebook* developed by [jupyter](http://jupyter.org/) are an easy way to run python code using only a browser.
By accessing our analysis computer, you won't have anythign to install. Refer to our [How To](/en/tutorial/) page to
learn how to do that.
{{% /expand%}}
{{%expand "Where are my data and how can I access them?" %}}
The following tutorial will show you where are you data and how you can access them. Just go to [How To > Access your data](/en/tutorial/how_to_access_data/)
{{% /expand%}}
{{%expand "I get a firefox error message when trying to start the jupyter notebooks on the analysis machine." %}}
After double clicking the [start jupyter] icon, I get an Firefox error message telling me that I have another
Firefox window opened.

To fix this issue, just open a terminal and type `>rm -rf ~/.mozilla` 

<img src='/faq/images/fixFirefoxIssue.gif' />

This should fix your issue and you should be able to start the jupyter notebooks now.
{{% /expand%}}
{{%expand "Where do I find ImageJ (or Fiji) on the analysis computer?" %}}
Just follow the following path to find and start ImageJ.
<img src='/faq/images/imagej.png' />
If you need to learn how to use ImageJ, check their <a href='https://imagej.nih.gov/ij/docs/examples/index.html'>tutorial
web site</a>
{{% /expand%}}
{{%expand "How to cite our work?" %}}
<ul>
<li>Use of CG1D beam line</li>
<li>iMars3D</li>
<li>iBeatles</li>
</ul>
{{% /expand%}}
{{%expand "Metadata of the images and their meaning" %}}
You can retrieve the metadata of your TIFF images using:
<ul>
 <li><a href='https://oncat.ornl.gov/#/'>ONCat</a></li>
 <li>the jupyter notebook **list_tiff_metadata.ipynb**. Check [How To > Start the python notebooks](/en/tutorial/how_to_start_notebooks)</li>
</ul>

<table>
<tr><td width="250"><strong>Tag Name</td><td><strong>Description</td></tr>
<tr><td>ImageWidth</td><td>The number of columns in the image</td></tr>
<tr><td>ImageHeight</td><td>The number of rows in the image</td></tr>
<tr><td>BitsPerSample</td><td>The number of bits per component (ie. 16-bits or 32-bits for each greyscale pixel in our case)</td></tr>
<tr><td>SampleFormat</td><td>Specifies how to interpret each data sample in a pixel (1 = unsigned integer)</td></tr>
<tr><td>SamplesPerPixel</td><td>The number of components per pixel (1 in our case, which is grey scale)</td></tr>
<tr><td>Compression</td><td>1 = None</td></tr>
<tr><td>PhotometricInterpretation</td><td>1 = Min is black</td></tr>
<tr><td>MakeStr</td><td>The detector manufacture (eg. 'Andor' or 'SBIG')</td></tr>
<tr><td>ModelStr</td><td>The detector model number</td></tr>
<tr><td>SoftwareStr</td><td>EPICS areaDetector</td></tr>
</table>

<br>
Tags 65000 to 650009 have no name and are used for timestamps and a unique ID

<table>
<tr><td width="250"><strong>Tag Name</td><td><strong>Description</td></tr>
<tr><td>65000</td><td>EPICS timestamp. The timestamp is made when the image is read out from the camera. Format is seconds.nanoseconds since Jan 1st 00:00 1990.</td></tr>
<tr><td>65001</td><td>Unique ID for the image. Always 1 for single image acquisition, and incrementing up for camera and CT scans. Should always match the ImageCounter value.</td></tr>
<tr><td>65002</td><td>EPICS timestamp (seconds part only)</td></tr>
<tr><td>65003</td><td>EPICS timestamp (nanoseconds part only)</td></tr>
</table>

### Scan Information

<table>
<tr><td width="250"><strong>Tag Name</td><td><strong>Description</td></tr>
<tr><td>FileNameStr</td><td>The original file name part of the constructed file name (see below)</td></tr>
<tr><td>InstrumentStr</td><td>'CG1D' or 'VENUS'</td></tr>
<tr><td>IPTS</td><td>IPTS Number</td></tr>
<tr><td>ITEMS</td><td>ITEMS Number</td></tr>
<tr><td>SampleDescStr</td><td>Sample description (user entered)</td></tr>
<tr><td>NotesStr</td><td>User notes</td></tr>
<tr><td>DataSetStr</td><td>'2D' or '3D'</td></tr>
<tr><td>DataAcqModeStr</td><td>'White Beam', 'TOF-cold/thermal', 'Epithermal' or 'Monochromatic'</td></tr>
<tr><td>DataTypeStr</td><td>'OB', 'Raw' or 'DF'</td></tr>
</table>

### Camera/Image Information

<table>
<tr><td width="250"><strong>Tag Name</td><td><strong>Description</td></tr>
<tr><td>ExposureTime</td><td>Exposure time for the image (in seconds)</td></tr>
<tr><td>ExposurePeriod</td><td>Exposure period for the image (Exposure Time + Readout Time in seconds). Not relevant for single image exposures.</td></tr>
<tr><td>NumImages</td><td>1= single image exposure (our normal mode of operation)</td></tr>
<tr><td>ImageCounter</td><td>Always 1 for single image acquisition, and incrementing up for camera and CT scans.</td></tr>
<tr><td>MinX</td><td>Min X pixel (0 for full frame images)</td></tr>
<tr><td>MinY</td><td>Min Y pixel (0 for full frame images)</td></tr>
<tr><td>SizeX</td><td>Size of image in X dimension (should be equal to the ImageWidth value)</td></tr>
<tr><td>SizeY</td><td>Size of image in Y dimension (should be equal to the ImageLength value)</td></tr>
<tr><td>Temperature</td><td>The setpoint temperature (in C)</td></tr>
<tr><td>TemperatureActual</td><td>The actual temperature read from the detector (in C)</td></tr>
</table>

### Motor Position & Scan Device

<table>
<tr><td width="250"><strong>Tag Name</td><td><strong>Description</td></tr>
<tr><td>MotScanDeviceStr</td><td>'Small Rot' or 'Large Rot' used for this CT scan (if we are doing a camera scan or single image acquisition, this is not relevant)</td></tr>
<tr><td>RotationActual</td><td>Actual position of the rotation stage used in the CT scan (or the previous scan if we are doing a camera scan or single image acquisition)</td></tr>
<tr><td>MotRotTable.RBV</td><td>Large rotation table actual position</td></tr>
<tr><td>MotRotTable</td><td>Large rotation table setpoint</td></tr>
<tr><td>MotSmallRotTable.RBV</td><td>Small rotation table actual position</td></tr>
<tr><td>MotSmallRotTable</td><td>Small rotation table setpoint</td></tr>
<tr><td>MotLiftTable.RBV</td><td>Lift Table actual position</td></tr>
<tr><td>MotLiftTable</td><td>Lift table setpoint</td></tr>
<tr><td>MotShortAxis.RBV</td><td>Short axis actual posiiton</td></tr>
<tr><td>...</td><td></td></tr>
</table>

## TIFF File Header Example

<pre>
TIFF Directory at offset 0x800008 (8388616)
  Image Width: 2048 Image Length: 2048
  Bits/Sample: 16
  Sample Format: unsigned integer
  Compression Scheme: None
  Photometric Interpretation: min-is-black
  Samples/Pixel: 1
  Rows/Strip: 2048
  Planar Configuration: single image plane
  Make: Unknown
  Model: Unknown
  Software: EPICS areaDetector
  Tag 65000: 837380408.136687
  Tag 65001: 1
  Tag 65002: 837380408
  Tag 65003: 148080423
  Tag 65010: FileNameStr:TiffHeaderTests
  Tag 65011: InstrumentStr:CG1D
  Tag 65012: IPTS:17255
  Tag 65013: ITEMS:-1
  Tag 65014: SampleDescStr:polarization test
  Tag 65015: NotesStr:polarization test
  Tag 65016: DataSetStr:2D
  Tag 65017: DataAcqModeStr:White Beam
  Tag 65018: DataTypeStr:Raw
  Tag 65019: ModelStr:DW936_BV
  Tag 65020: ManufacturerStr:Andor
  Tag 65021: ExposureTime:1.000000
  Tag 65022: ExposurePeriod:5.451660
  Tag 65023: NumExposures:1
  Tag 65024: NumImages:1
  Tag 65025: ImageCounter:1
  Tag 65026: MinX:0
  Tag 65027: MinY:0
  Tag 65028: SizeX:2048
  Tag 65029: SizeY:2048
  Tag 65030: Temperature:-60.000000
  Tag 65031: TemperatureActual:-57.830002
  Tag 65032: MotScanDeviceStr:Small Rot
  Tag 65033: RotationActual:183.000132
  Tag 65034: MotLiftTable.RBV:247.500452
  Tag 65035: MotLiftTable:247.500452
  Tag 65036: MotShortAxis.RBV:76.000000
  Tag 65037: MotShortAxis:76.000000
  Tag 65038: MotLongAxis.RBV:193.016000
  Tag 65039: MotLongAxis:193.016000
  Tag 65040: MotRotTable.RBV:182.996500
  Tag 65041: MotRotTable:183.000000
  Tag 65042: MotSmallRotTable.RBV:183.000132
  Tag 65043: MotSmallRotTable:183.000000
  Tag 65044: MotDetTable.RBV:200.000000
  Tag 65045: MotDetTable:200.000000
  Tag 65046: MotCameraVert.RBV:-51.699796
  Tag 65047: MotCameraVert:-51.699796
  Tag 65048: MotHoriTrans.RBV:28.000000
  Tag 65049: MotHoriTrans:28.000000
  Tag 65050: MotVertTrans.RBV:60.000000
  Tag 65051: MotVertTrans:60.000000
  Tag 65052: MotDiffuser.RBV:86.300000
  Tag 65053: MotDiffuser:86.300000
  Tag 65054: MotAperture.RBV:138.700000
  Tag 65055: MotAperture:138.700000
  Tag 65056: MotSlitVB.RBV:39.969938
  Tag 65057: MotSlitVB:39.969938
  Tag 65058: MotSlitVT.RBV:39.860484
  Tag 65059: MotSlitVT:39.860484
  Tag 65060: MotSlitHR.RBV:40.000000
  Tag 65061: MotSlitHR:40.000000
  Tag 65062: MotSlitHL.RBV:39.977781
  Tag 65063: MotSlitHL:39.977781
  Tag 65064: AndorCCDCooler:1
  Tag 65065: AndorCCDTempStatusStr:Not stabilized at set point
  Tag 65066: AndorCCDPreAmpGain:0
  Tag 65067: AndorCCDADCSpeed:2
</pre>


{{% /expand %}}

## Work With Us

{{%expand "Visiting Researcher Program"%}}
<a href='http://swc.ornl.gov/visiting'>Link here</a>
{{%/expand%}}
{{%expand "Minority Serving Institutions Partnership Program" %}}
<a href='https://orise.orau.gov/msipp/'>Link here</a>
{{%/expand%}}