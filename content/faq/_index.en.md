---
date: 2016-04-09T16:50:16+02:00
title: Frequently Asked Questions
pre: "<b>4. </b>"
weight: 4
---

## Before Your Venue

#### Proposal

{{%expand "How do I submit a proposal?" %}}
Answer will go here.
{{% /expand%}}
{{%expand "When will I know my proposal has been accepted?" %}}
Answer will go here.
{{% /expand%}}
{{%expand "My proposal has been rejected, what to do next?" %}}
Answer will go here.
{{% /expand%}}

#### Samples

{{%expand "Can I bring my samples?" %}}
answer here
{{% /expand%}}
{{%expand "Can I leave with my samples?" %}}
answer here
{{% /expand%}}

## During your Experiment

{{%expand "Where can I stay?" %}}
A few options are available off-site and on-site. Check the <a href='https://neutrons.ornl.gov/users/daily-living#stay'>
neutron.ornl.gov users page</a> for more infos.
{{% /expand%}}

## Data Analysis
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
After double clicking the **start jupyter** icon, I get an **Firefox** error message telling me that I have another
Firefox window opened. 

The short way to fix that is by starting the **Help me** application.

<img src='/faq/images/firefox2.png' />

Then go to the **Desperate Actions**

<img src='/faq/images/firefox3.png' />

and click the **Fix Firefox**!

<img src='/faq/images/firefox4.png' />
<img src='/faq/images/firefox5.png' />

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
<tr><td><strong>Tag Name</td><td><strong>Description</td></tr>
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

{{% /expand %}}

## Work With Us

{{%expand "Visiting Researcher Program"%}}
<a href='http://swc.ornl.gov/visiting'>Link here</a>
{{%/expand%}}
{{%expand "Minority Serving Institutions Partnership Program" %}}
<a href='https://orise.orau.gov/msipp/'>Link here</a>
{{%/expand%}}