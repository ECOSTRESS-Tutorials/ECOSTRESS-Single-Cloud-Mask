> *This tutorial will show you how to use code to apply a cloud mask to
> a single ECOSTRESS image. This code applies a cloud mask to a Land
> Surface Temperature (LST) image, but it can be modified for other
> ECOSTRESS products.*

# Table of Contents

[What is a Cloud Mask?](#what-is-a-cloud-mask)

[Applying a Cloud Mask to a Single Image](#applying-a-cloud-mask-to-a-single-image)

# What is a Cloud Mask?

A cloud mask is an image used to help determine if there is cloud
presence in remotely sensed imagery. The mask is binary, meaning it
either indicates the presence of a cloud or it does not. If it does
indicate the presence of a cloud, that pixel can be removed from the
remotely sensed image to improve the accuracy of the overall image.

**Tip**: Make sure you have **Cloud Mask files** downloaded in addition
to your ECOSTRESS product files. If you do not know how to download
these files, see the **Downloading from AppEEARS** tutorial.

## Applying a Cloud Mask to a Single Image

1.  Download the **Single_Cloud_Mask** code from
    <https://github.com/ECOSTRESS-Tutorials/ECOSTRESS-Single-Cloud-Mask>.

2.  Open your **finder**. Create a **project folder** to store all the
    files for this project by **right clicking** and selecting **New
    Folder**. Name your new folder so that you know it is the main
    project folder.

<img src="Applying_a_Single_Cloud_Mask_images/media/image1.png"
style="width:3.45064in;height:2.13306in"
alt="Graphical user interface, application Description automatically generated" />

3.  **Move** the **downloaded code** file into the project folder.

<img src="Applying_a_Single_Cloud_Mask_images/media/image2.png"
style="width:3.78438in;height:2.38141in"
alt="Graphical user interface, application, Word Description automatically generated" />

4.  **Move** the folder with your **downloaded ECOSTRESS data** into the
    project folder.

<img src="Applying_a_Single_Cloud_Mask_images/media/image3.png"
style="width:3.75064in;height:2.3718in"
alt="Graphical user interface, application Description automatically generated" />

5.  In the project folder, create a new **sub folder** to store the
    completed cloud masked file. To do this, go inside the project
    folder, **right click**, and select **New Folder**. Then name the
    folder so that you know it is for the **outputs**.

<img src="Applying_a_Single_Cloud_Mask_images/media/image4.png"
style="width:3.87308in;height:2.39254in"
alt="Graphical user interface, application Description automatically generated" />

6.  Next, open **Visual Studio Code** and use **File \> Open Folder…**
    to get connected to the main project folder that contains the
    downloaded ECOSTRESS files, the Single_Cloud_Mask code, and the
    output subfolder.

| <img src="Applying_a_Single_Cloud_Mask_images/media/image5.png"
style="width:1.66667in;height:1.89461in"
alt="Graphical user interface, text, application Description automatically generated" /> | <img src="Applying_a_Single_Cloud_Mask_images/media/image6.png"
style="width:2.125in;height:1.89712in"
alt="Graphical user interface, text, application Description automatically generated" /> |
|----|----|

1.  In the **EXPLORER** tab, find the **Single_Cloud_Mask** code and
    click on it to open it.

<img src="Applying_a_Single_Cloud_Mask_images/media/image7.png"
style="width:4.88681in;height:2.7953in"
alt="Text Description automatically generated" />

**Tip**: If you want to know more about what each line of the code does,
read the **comments** in the code. Comments in the code are identified
by **\#**. These comments do not actually change how the code runs, but
they can be helpful to put notes on how the code works for yourself or
other users. This can also be helpful if you want to customize the code
because it will guide you to which parts you may want to change!

**Examples** of comments (**green text following the \#):**

<img src="Applying_a_Single_Cloud_Mask_images/media/image80.png"
style="width:5.0891in;height:1.14621in"
alt="Text Description automatically generated" />

2.  Find the section of the code titled **Load and View the Surface
    Temperature Image**. Find the variable called **ST_filepath**.
    Change the text that says **"Replace_this_text_with_file_path"** to
    the path to the ECOSTRESS LST image that you want to cloud mask.

<img src="Applying_a_Single_Cloud_Mask_images/media/image9.png"
style="width:5.24295in;height:1.16902in"
alt="Text Description automatically generated" />

1.  To **copy the file path**, use the **EXPLORER** panel on the left
    side of Visual Studio Code to find the file you are interested in.
    Once you have found it, **right click** on it and select **Copy
    Path**. Now you can paste the path into your code. Make sure it is
    still **wrapped in quotes** and has **r** outside the first quote.

<img src="Applying_a_Single_Cloud_Mask_images/media/image10.png"
style="width:2.30449in;height:3.51822in"
alt="Text Description automatically generated" />

**Example:**

<img src="Applying_a_Single_Cloud_Mask_images/media/image11.png"
style="width:6.5in;height:0.47014in" />

3.  Now, find the section of the code titled **Load and View the Cloud
    Mask**. Find the variable called **cloud_filepath**. Change the text
    that says **"Replace_this_text_with_file_path"** to the whole file
    path of the corresponding **Cloud Mask** image for your LST image.
    To make sure it is the corresponding Cloud Mask image, make sure
    that the **date codes** of both the LST and Cloud Mask images
    **match**. The date code is the string of numbers listed after
    **doy** in the file names. Make sure it is still **wrapped in
    quotes** and has **r** outside the first quote.

> <img src="Applying_a_Single_Cloud_Mask_images/media/image12.png"
> style="width:6.05064in;height:1.25085in"
> alt="Graphical user interface, text Description automatically generated" />
>
> **Example:**
>
> <img src="Applying_a_Single_Cloud_Mask_images/media/image13.png"
> style="width:6.5in;height:0.36528in" />

4.  Finally, scroll down to the section titled **Save the Masked
    Image**. Find the variable titled **output_folder_path**. Change the
    text that says **"Replace_this_text_with_folder_path"** to the name
    of the folder where you want the output file to be stored. Make sure
    it is still **wrapped in quotes** and has **r** outside the first
    quote.

<img src="Applying_a_Single_Cloud_Mask_images/media/image14.png"
style="width:6.2837in;height:1.23526in"
alt="Text Description automatically generated" />

**Example:**

<img src="Applying_a_Single_Cloud_Mask_images/media/image15.png"
style="width:6.5in;height:0.41528in" />

5.  Now the code should be set up to be run with your desired image.
    Scroll back to the top to the section titled **Import the Libraries
    we Need to Apply the Cloud Mask**. This is the first block of code
    we want to run. Click into the box with the library importing code
    and press **Shift+Return** to run it.

<img src="Applying_a_Single_Cloud_Mask_images/media/image16.png"
style="width:4.66602in;height:1.3674in"
alt="Text Description automatically generated" />

6.  At the top of the window, a pop up will appear prompting you to
    **select a kernel** to run your code with. Click on **Python
    Environments …**

<img src="Applying_a_Single_Cloud_Mask_images/media/image17.png"
style="width:4.68141in;height:0.89927in"
alt="Graphical user interface Description automatically generated with medium confidence" />

7.  Select the **ECOSTRESS** environment that you created, or another
    one if you have a different one you want to use.

<img src="Applying_a_Single_Cloud_Mask_images/media/image18.png"
style="width:4.84295in;height:1.47772in"
alt="Graphical user interface, text, application, email Description automatically generated" />

**Tip**: If you do not have an ECOSTRESS environment set up, follow the
**Creating an Environment** tutorial to make one.

8.  Let the code run for a few seconds. You will see the **seconds
    counting up** in the bottom left of the cell. You will know it is
    done when a **green check mark** appears.

<img src="Applying_a_Single_Cloud_Mask_images/media/image19.png"
style="width:3.21183in;height:1.2891in"
alt="Text Description automatically generated" />

9.  Continue this process of running each block of code, in order from
    top to bottom, by clicking into the module with the code and
    pressing **Shift+Return**.

    1.  The **Load and View the Surface Temperature Image** section will
        generate a map showing the surface temperature of the LST file
        you uploaded. **Example:**

<img src="Applying_a_Single_Cloud_Mask_images/media/image20.png"
style="width:4.23919in;height:2.91218in" />

2.  The **Load and View the Cloud Mask** section will map the binary
    image of the cloud mask you uploaded. The blue shows areas that are
    good to be kept, and the **red** shows areas that **should be
    removed** due to possible cloud cover. **Example:**

<img src="Applying_a_Single_Cloud_Mask_images/media/image21.png"
style="width:4.48141in;height:3.0757in"
alt="Map Description automatically generated" />

3.  The **Apply the Cloud Mask to the Surface Temperature Image**
    section will generate a map of surface temperature, but with areas
    where clouds are indicated removed. This is the image that will be
    saved to your output folder when you run the final **Save the Masked
    Image** section of the code. **Example:**

> <img src="Applying_a_Single_Cloud_Mask_images/media/image22.png"
> style="width:4.43393in;height:3.04454in"
> alt="Map Description automatically generated" />

4.  Finally, the **Save the Masked Image** section will save the masked
    image as a .tif file into the folder that you specified as your
    outputs folder. You can check to make sure that a file is present in
    that folder so that you know your code ran correctly.

<img src="Applying_a_Single_Cloud_Mask_images/media/image23.png"
style="width:5.40661in;height:1.34068in"
alt="Graphical user interface, text, application Description automatically generated" />

You have now cloud masked an individual ECOSTRESS image!
