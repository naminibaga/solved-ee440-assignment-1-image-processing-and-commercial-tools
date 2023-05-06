Download Link: https://assignmentchef.com/product/solved-ee440-assignment-1-image-processing-and-commercial-tools
<br>
Image processing and commercial tools




<ol start="2">

 <li>Capture a digital color image of yourself and enlarge it by a factor of 2.5 in both horizontal and vertical dimensions using an image editing tool. Put the original and enlarged images in your report.</li>

 <li>Adjust <strong>jpg</strong> (e.g. brightness, contrast …) until you find it most pleasant. Put the adjusted image in your report.</li>

</ol>




<strong><em>HINT:</em></strong> You could use any software you have (e.g. Adobe Photoshop, Paint/Photos in Windows).




<ul>

 <li>MATLAB basics: image I/O and data types.

  <ol start="4">

   <li>Load the Lena image <strong>bmp</strong>, using imread(), and show it using imshow().</li>

   <li>Get the type of the loaded image data (Use MATLAB function class()), and get the maximum and the minimum data values for this image (Use MATLAB function max() and min()).</li>

   <li>Convert the data to the “double” type (use MATLAB function double()), can you show the double-typed image using imshow() ?</li>

   <li>If not, given an image which has been converted to the “double” type, how do you show the image?</li>

  </ol></li>

</ul>

<strong><em> </em></strong>

<strong><em>HINT:</em></strong> MATLAB has an image value range for the default uint8 type in [0 255]. For imshow(), if the data type is double, it should be in the range [0 1]. Double type data can be converted to uint8 data, or data can be normalized to be in [0 1] for imshow().




<ul>

 <li>Matlab basics: Matlab commands.</li>

</ul>




Write a Matlab script to do the following.




<ol start="2">

 <li>Read <strong>tif</strong> and its associated colormap into variables named “X” and “map”.</li>

</ol>

Use X and “map” to convert the image to a 256-level grayscale image Y.

<ol>

 <li>Rotate Y 45 degrees clockwise to generate image Z.</li>

 <li>Submit images Y and Z, and the script you wrote.</li>

</ol>




<strong><em>HINT:</em></strong> Use the Matlab commands: [X,map]=imread( ‘1_2.tif’, ‘tif’ ) , imshow(X, map) , ind2gray, imrotate.




<strong><em><u>Note: Write your own Matlab codes for the following problems.</u></em></strong>




<ul>

 <li>Image Resolution.</li>

</ul>




<ol start="3">

 <li>Reduce the resolution of <strong>asc</strong> by a factor of 4 in both horizontal and vertical</li>

</ol>

dimensions (e.g., if the original image is 400 by 400, then result shall be 100 by 100) to create a decimated image using two different methods:




<strong><em>HINT: </em></strong>To read in an “.asc”, use X=load(‘<strong>1_3.asc</strong>’). For the double type, ‘imshow’ only works for images with values between 0 and 1. To display the .asc image, you may use imshow(X/256).




<ol>

 <li>Keep one pixel out of every 4×4 pixel area. Display the resulting image Y1. <strong><em>HINT:</em></strong> This can be done with only one line of code. You do not need to use for loops to accomplish this. Consider what the command A=B(1:3:20, 1:3:30) does to an image B.</li>

 <li>Replace every 4×4 pixel area in <strong>asc</strong> by the average value of the pixel values in that region. Display the resulting image Y2.</li>

</ol>




<ol>

 <li>Enlarge Image Y1 by a factor of 4 in both horizontal and vertical dimensions (e.g., from 100 by 100 to 400 by 400) using:</li>

</ol>




<ol>

 <li>Pixel repeating. (Since each pixel is blown up to a 4×4 block, the image looks</li>

</ol>

“blocky”.)  ii. Bilinear interpolation (do not use <em>interp2, use your own code</em>).  iii. Keep the resulting images from (b.i) and (b.ii) the same size as <strong>1_3.asc</strong> and compare the images.




<strong><em>HINT: </em></strong>Use <em>A=a </em>to generate a matrix <em>A </em>with all entries equal to <em>a</em>.