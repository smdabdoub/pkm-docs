Data 
=====
ProkaryMetrics is designed to reconstruct volumetric image data by 
combining sets of 2D images known as z-stacks that represent optical 
slices of a physical data sample. Currently the default image format 
used by ProkaryMetrics is the Tagged Image File Format (TIFF), but 
the software also supports JPEG images.

Opening Files
-------------
Image data is added to the current rendering window through the 
File >> Open Image File(s)... menu item. Since a z-stack is expected, 
the file selection dialog will accept multiple file selection.

.. figure:: figures/data_fig1_openfile.png
   :scale: 80 %
   
Clicking the "Open" button will cause ProkaryMetrics to attempt to load 
the specified image files, and render a 3D surface representation of the 
fluorescent pixels (see the User Interface subsection in the Introduction 
section). Currently, ProkaryMetrics has a default pixel-brightness level 
it uses when performing the 3D reconstruction, which will not be 
appropriate for all image data. Particularly, 8-bit image data which only 
has pixel values between 0 and 127 will not be properly reconstructed 
initially. If the reconstructed data does not look right, or does not 
appear at all, you can modify the pixel value used to perform the 
reconstruction. This and other user-modifiable settings are described in 
detail in the Data Interaction section. Eventually the initial value will 
be intelligently chosen using the content of the image data itself, but 
users may still want to tweak the setting.
   
Projects
--------
Once you have loaded some image data and maybe marked some bacteria, 
you will want to save your work. ProkaryMetrics supports saving and 
loading of project files. A project consists of the current state of the 
program including all loaded image files, any recorded bacteria, and any 
modified settings. Both saving and loading projects can be done through 
the File menu. 

Note that ProkaryMetrics does not store a copy of the loaded image data, 
it merely stores the location of each loaded image file. This means when 
you load a previously saved project file ProkaryMetrics will look for the 
image data in the location it was when you saved the project. If the 
images have been moved or deleted it will pop up a message telling you it 
cannot locate them, and will give you the option to select the folder 
they have been moved to. If it can find all the images in the new 
location, it will load them and continue loading the rest of the project 
information.
 
Exporting
---------
Given that one of the main goals of ProkaryMetrics is to provide 
quantitative and statistical information about microbial communities, 
it is often useful to use that data in other software for additional 
analysis or display. To this end, ProkaryMetrics provides the facility to 
export certain data. Currently, this includes: bacteria and lengths. Both 
options are available through the File >> Export menu.

Bacteria
^^^^^^^^
Exporting bacteria will result in a file that lists the marked end and 
interior points for each bacterium. Each line corresponds to an 
individual bacterium, and each line is a comma-separated list of 3-tuples 
that indicate the X, Y, and Z coordinates of each marker that makes up 
the recorded bacterium.

::

	1.23, 3.44, 0.65, 18.36, 4.40, 2.21
	
This example shows a line of 6 numbers separated by commas. As mentioned 
above, the line is logically grouped into 3-tuples indicating axis values.
This line has 6 values, and so indicates two markers representing a 
single bacterium.

Lengths
^^^^^^^
The export lengths option creates a single-column CSV file with a header 
line of "len". Each line in the file gives the length of a single 
bacterium in micrometers.