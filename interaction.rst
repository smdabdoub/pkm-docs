Data Interaction
================
The main purpose behind 3D rendering of microbial communities is to be 
able to interact with the data (rotating, zooming, cropping, etc...) in 
order to gain an understanding of your data that may not be possible 
through viewing 2D slices. This section describes the facilities 
ProkaryMetrics provides to allow you to explore your data.

Exploring the Rendered Image Data
---------------------------------
The mouse is the main means of interacting with rendered image data. The 
few keyboard commands available will be discussed as appropriate in this 
section. A list of all the keyboard commands is at the end of this 
section with a short description of each key's purpose.

Rotating Image Data
^^^^^^^^^^^^^^^^^^^
Imagine the the rendered image data is contained within a transparent 
hamster ball floating in space. If you grab the hamster ball, you can 
rotate it in any direction and the image data will rotate along with it. 
In ProkaryMetrics, you can use the mouse to rotate the hamster ball. 
Begin by left-clicking (and holding the mouse button down) anywhere 
within the Visualization Window. While holding the button, move the mouse 
and any data in the window will rotate in the direction you are moving 
the mouse. The first example below shows an initial rendering of a sample 
image set with the cursor near one bacterium.

.. figure:: figures/di_rotating_before.png
   :scale: 50 %
   
In the next image, the data has been rotated counter-clockwise 
approximately 90 degrees, and rotated away from the user (into the 
screen) approximately 45 degrees.
   
.. figure:: figures/di_rotating_after.png
   :scale: 50 %
   
Magnification
^^^^^^^^^^^^^
Zooming in and out can be accomplished either with the mouse wheel (up to 
zoom in, down to zoom out) or by right-clicking and dragging with the 
mouse. Dragging up zooms in, dragging down zooms out. Zooming with the 
mouse wheel generally results in larger magnification steps. Zooming 
with the right mouse button gives you smoother magnification and slightly 
more control over how far it zooms in and out.

This screenshot shows the original data from above, magnified.

.. figure:: figures/di_zoom.png
   :scale: 50 %
   
Moving Data
^^^^^^^^^^^
Especially when magnifying data, in order to get the best view it is very 
useful to translocate the rendered data. In other words, moving the data 
up/down or left/right in order to center a particular section of interest 
within the Visualization Window. This can be accomplished with a third 
mouse button. Typically this button is in the middle of the mouse, and 
in mice with wheels, may be accessed by pressing down on the wheel 
itself. For mice with more than three buttons, this action is mapped 
to whichever button is assigned to be mouse button 3. The first image 
below shows the sample data set as was shown previously.

.. figure:: figures/di_rotating_before.png
   :scale: 50 %

The second image shows the data after being moved over to the right. 
Notice that neither the orientation nor the magnification level has 
changed.

.. figure:: figures/di_move.png
   :scale: 50 %
   
Rendering Settings
^^^^^^^^^^^^^^^^^^
You can.

.. figure:: figures/di_render_settings.png

Image Sets as Layers
--------------------


Marking and Recording Bacteria
------------------------------


Capturing Screenshots
---------------------
To export an image of the current state of the Visualization Window, 
click on the Tools >> Take Screenshot menu option. ProkaryMetrics 
supports saving screenshots as PNG, JPEG, TIFF, PNM, PostScript, or BMP.


Keyboard Commands Reference
----------------------------
**A**
	Toggle anti-aliasing mode. Anti-aliasing greatly improves image 
	quality at the expense of smooth interaction. Depending on the 
	graphics card and processor speed of your computer, turning this 
	mode on may make interacting with your data extremely slow. For most 
	computers it is only recommended for taking high-resolution 
	screen captures for publication or magnification (e.g. posters).

**D**
	Delete the recorded bacterium nearest to the cursor. This is only 
	effective to a certain radius around the cursor, so you should place 
	it fairly close, if not directly on, the bacterium you want to delete.
	
**I**
	Toggle the clipping box. This key displays and hides a wireframe box 
	that is drawn such that it initially contains within it all the 
	rendered image data. The box also includes spherical handles that you 
	can grab with the mouse and drag to expand or decrease the volume of 
	the box. If a plane of the box crosses over any rendered image data, 
	that data is made invisible. Expanding the box will reveal again any 
	previously hidden image data. This allows you to focus on specific 
	regions of your data, which can be helpful especially in large or 
	especially noisy data.

**X**
	Toggle between E\ **x**\ ploring mode and Recording mode.