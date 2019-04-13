
# Spatial domain filtering 
# We use this link when applying Spatial filters
https://github.com/machinelearninggod/Image-Processing-Algorithms

## Noise reduction filters



# Load the image 
#           we browse the image then convert it to grayscale


<img src = "/images/load.png" width = "50%">

# Adding  salt and pepper noise to the Image



<img src = "/images/noise.PNG" width = "50%">

# Apply filters on the noisy image

# 1.Box Filter
# we uset the width of the box filter equal 9
# The result 


<img src = "/images/BoxFilter.PNG" width = "50%">

# 2.Gaussian Filter 
# for σ = 0.3
# The result



<img src = "/images/gussianFilter.PNG" width = "50%">

# 3.Median (Non-linear) filter
# we use median filter 3x3
# The result


<img src = "/images/medianFilter.PNG" width = "50%">

# We have some problems in plotting in the mainwindow.ui so we plot using figures


<img src = "/images/LinesFigures.PNG" width = "50%">

# spatial domain filtering:

# 1-Prewitt : convolve image with Prewitt kernel in both directions

<img src = "/images/prewit.png" width = "50%">

# 2-sobel : convolve image with sobel kernel in both directions and calculate the magnitude to get the gradiant

<img src = "/images/sobel.png" width = "50%">

# 3-LAPLACIAN :convolve image with laplacian kernel

<img src = "/images/laplacian.png" width = "50%">

# 4-LOG : convolve laplacian kernel with gaussian kernel then convolve with image

## We use this link in applying LOG filter
http://homepages.inf.ed.ac.uk/rbf/HIPR2/log.htm

<img src = "/images/log.png" width = "50%">

# 5-DOG : convolve image with gaussian kernel twice with different std then subtract them
## We use this link while applying DOG filter
http://www.tjscientific.com/2017/01/31/using-python-and-opencv-to-create-a-difference-of-gaussian-filter/


<img src = "/images/dog.png" width = "50%">

# 6-SHARPENING:convolve image with sharpen kernel 
## We use this link when applying sharpening filter 
https://stackoverflow.com/questions/47377230/error-with-image-sharpening-in-python

<img src = "/images/sharping.png" width = "50%">

# Fourier Transform


## 1. first we extract value channel from the loaded image 

<img src = "/images/extractedValueChannel.png" width = "50%">

## 2. Then we apply FT but there is a problem in showing it on our GUI 

<img src = "/images/FT.PNG" width = "50%">

## 3. Then making shifted FT but there is a problem in showing it on our GUI


<img src = "/images/ShiftedFT.PNG" width = "50%">

## 4. we tried Shifted FT without log scale 

<img src = "/images/Without log.PNG" width = "50%">

## 5. we generate filres (low pass filter & high pass filter )  by using arrays of zeros and ones then apply Filter in Frequency Domain , we multipy the ideal LPF by the fourier spectrum of the image

### I. LPF REsult , it didn't work in gui but work outside it 

<img src = "/images/LPF.PNG" width = "50%">

### II.HPS Result, it didn't work in gui but work outside it

<img src = "/images/HPF.PNG" width = "50%">

# Hough Transform


# 1.Hough lines tranform
## we use this link to help us applying Hough lines
https://scikit-image.org/docs/dev/auto_examples/edges/plot_line_hough_transform.html

# first we convert the to grayscale
# The following steps are performed to detect lines in the image
# Step 1 : Initialize Accumulator
# Step 2: Detect Edges
# Step 3: Voting by Edge Pixels


# The result 


<img src = "/images/Lines.PNG" width = "50%">

## Hough circles 

## we have a help from our freind Omnia she gave us two useful links about hough circles 
1. https://www.codingame.com/playgrounds/38470/how-to-detect-circles-in-images?fbclid=IwAR0dhunhK6MLftiHfHJVEWTTOIL0MOr4NhWq2pBCnm5s2l0PnMCXNsAbBIc

2. https://github.com/PavanGJ/Circle-Hough-Transform?fbclid=IwAR0dhunhK6MLftiHfHJVEWTTOIL0MOr4NhWq2pBCnm5s2l0PnMCXNsAbBIc

## We make canny adge detector for the image 
## after lots of trying we choose specific parameters for circles and detection
    rmin = 20
    rmax = 25
    steps = 50
    threshold = 0.4



<img src = "/images/houghcircle.PNG" width = "50%">

## Histogram 

## we make an empty array and we count pixel value by making for loop
## then we plot it with  x (0:256)

<img src = "/images/inutHistogram.PNG" width = "50%">

# Histogram Equalization

## We make a cumulative function CDF , normalized cumulative sum to modify the intensity values of our original image. 
## we use a this link to make Equalization
https://hackernoon.com/histogram-equalization-in-python-from-scratch-ebb9c8aa3f23

<img src = "/images/outputHistogramEqualization.PNG" width = "50%">

<img src = "/images/HistogramEqualizatio.PNG" width = "50%">

# Matching histogram 

## We use this link while applying matching histogram
https://scikit-image.org/docs/dev/auto_examples/transform/plot_histogram_matching.html

# -get the set of  pixel values and their corresponding indices and counts

# - take the cumsum of the counts and normalize by the number of pixels to get the empirical cumulative distribution functions for the source and

# interpolate linearly to find the pixel values in the template image that correspond most closely to the quantiles in the source image

<img src = "/images/matching.png" width = "50%">


```python
:
```
