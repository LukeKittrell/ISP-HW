ISP pipeline user manual

To use and operate this Python notebook is simple and only requires a few steps to work.

Steps
1. Identify where your image file is located in your directory
2. Make sure that the image file has access to the dcraw program (for Windows dcraw can be put in the \Windows file). If your image file doesn't have access to dcraw, then move it to a file that can access dcraw.
3. Once you have your correct file location run the following line in a terminal "dcraw -4 -d -v -w -T <Raw-file-location>. In the output you should see the following "Scaling with darkness <black>, saturation <white>, and
multipliers <r_scale> <g_scale> <b_scale> <g_scale>". Record the integer numbers for black, white, r scale, g scale, and b scale.
4. Place the corresponding recorded integers into their respective variable locations at the beginning of the notebook.
5. Delete the .tiff file that was created from the terminal command above.
6. Run the following line in your terminal to get a tiff file that will work with the notebook. "dcraw -4 -D -T <Raw-file-location>"
7. Locate where the .tiff file you created above is and plug it into the image variable under the "Python Initials" section.
8. You need to determine your image's Bayer pattern and place that into the Bayer pattern variable under the "Identifying the correct Bayer pattern" section.
9. From here, run each Python cell (giving enough time for the previous cell to complete) until you reach the section titled "Second white balancing picture". This will have gone through the entire ISP pipeline and saved a .png and .jpg  final image file to your computer.

Optional steps
1. You can change the desired mean intensity (range 0 to 1) when the image_brighted variable calls the brightness adjustment function in the "Brightness adjustment" section
2. In the "Compression" section you can change the quality parameter in the second imsave function call to change the quality of the compressed image.
3. In the "Manual white balancing" section, you can change the x and y variables to point to any patch on your image you want as the scale for white balancing.
