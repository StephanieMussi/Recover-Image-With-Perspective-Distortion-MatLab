# Recover_Image_With_Perspective_Distortion_MatLab

The project aims to take the image of slanted view of a book, and compute the projective transformation to warp the image to a frontal view.  

Firstly, the image ["book.jpg"](https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/book.jpg) is read and displayed:  
```matlab
P = imread('book.jpg');
imshow(P);
```  

<img src = "https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/book.jpg" width = 350 height = 269>  
The image is a slanted view of a book of A4 dimensions, which is 210 mm x 297 mm.  

Then the coordinates of the four corners are obtained:  
```matlab
[X Y] = ginput(4)
```  

<img src = "https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/Figures/coordx.png" width = 130 height=140>

<img src = "https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/Figures/coordy.png" width = 130 height=140>  


The standard coordinates for corners of a image of A4 dimensions are:  
```matlab
x = [0, 0, 210, 210];
y = [0, 297, 297, 0];
```  

The algorithm of transformation is stated below:  

~  

<img src = "https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/Figures/algo.png" width = 744 height=733>  

~  

By applying the algorithm above, the resultant image is:  

<img src = "https://github.com/StephanieMussi/Recover_Image_With_Perspective_Distortion_MatLab/blob/main/Figures/book_A4.png" width = 239 height = 337>  
