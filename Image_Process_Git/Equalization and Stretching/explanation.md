Today is my first uploading in GitHub.
I'm so excited to start my activity. You'll see my progress!

I learned about Equalization and Histogram Stretching.
I think we need to know why they use these methods.


Before we know about them we need to know about "image contrast".
It's simply says that the difference between bright region and dark region.


![image](https://github.com/user-attachments/assets/bc5d7cd7-2fa5-4409-a5e8-210f2956aa50)


If we look at these 4 images. All left box have the same intensity but it seems a little difference because of the right box.
The same color can appear differntly depending on the brightness of adjacent colors, which can cause confusion in images where contrast is low.


If an image contains mostly similar pixel values, it becomes difficult to identify important features or details.
Among the ways to improve image quality, we will try to improve image contrast.


Implementation:
If we compare original image and processed image, we should compare histogram!

# Histogram Stretching

This method is often referred to as the histogram normalization technique.
It is a method of normalizing as much as the image pixel bit.


The calculation formula is as follows.


![image](https://github.com/user-attachments/assets/59908f4a-c6f9-4874-8f51-af995094ab29)

Let's compare original image and processed image.



![stretched](https://github.com/user-attachments/assets/40cc7514-8089-4c72-8b67-99b585187c75)


As the method was named, the histogram of the image has stretched.
I don't think it's working well.


# Equalization


This method converts the histogram to make the pixel value distribution more uniform.


Procedure 
1. Calcualte the histogram of the image to obtain the frequency of each pixel intensity value
2. Compute the cumulative frequency from the histogram values.
3. Normalize the cumulative frequencies.
4. Convert pixel values


More detailed explanations will be understood by searching or by looking at my code.


![equalization](https://github.com/user-attachments/assets/6d678497-e65c-45cf-886d-4aba604baa61)


This is the result!
It seems that the goal of improving image contrast has been reached.


These results clearly show the difference between the two methods.


Original image 
![image](https://github.com/user-attachments/assets/f2fc69bd-37b5-4586-a0e3-5d8aa1a10374)



Stretched_image
![image](https://github.com/user-attachments/assets/82d9dce0-6f73-4ab9-b1e1-98b90c2145e2)



Equalized_image
![image](https://github.com/user-attachments/assets/2ae6311e-71ff-48ea-a236-58a94297eec1)



We can make decision that the quality of this Equalized_image has been further improved. But it doesn't look natural.
After considering why this happens, I observed the histogram of the equalized image and noticed that the values in the histogram are spaced apart after the process. I believe this occurs because the values are not continuous, which makes the image appear unnatural to our eyes.








