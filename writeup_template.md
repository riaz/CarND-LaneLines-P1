# **Finding Lane Lines on the Road** 


### Setup

Runs Jupyter Notebook in a Docker container with `udacity/carnd-term1-starter-kit` image from ![Udacity][docker installation].

```
cd <project-directory>
docker run -it --rm -p 8888:8888 -v `pwd`:/src udacity/carnd-term1-starter-kit
```

---

**Finding Lane Lines on the Road**

The Project #1 for Udacity’s Self-Driving Car Nanodegree (SDCND) is about creating a pipeline that detects lane lines in images. 
We were previded with several image files, to test our pipeline and we have applied the same pipeline to a video example that was also provided to us, since videos are also streams of images. We made use of the helper functions to implement the pipeline which had code-snippets form the quiz that we have completed earlier. 

We make several improvements on the lane detection method and finish the project by making the system robust enough to work on examples that have curved roads and make the example work.

[//]: # (Image References)

![alt text][image0]

---

** My Pipeline **

My Pipeline consists of 6 stages:

1. Grayscale
2. Gaussian Blur
3. Canny Edge Detection
4. Region of Interest — Create Vertices
5. Hough Transform — Average Lines
6. Draw Lines

The screenshots for the pipeline was created using the following:

    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"gray.jpg"),gray)
    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"blur_gray.jpg"),blur_gray)
    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"edges.jpg"),edges)
    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"masked_edges.jpg"),masked_edges)
    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"line_image.jpg"),line_image)
    > cv2.imwrite(os.path.join(IMAGE_SAVE_PATH,"lines_image.jpg"),lines_image)
   

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

My selection of the vertices are hard-coded and 


[image0]: ./test_images/solidWhiteCurve.jpg "Original Image"
[image1]: ./test_images_output/report_hough_solidWhiteCurve.jpg "Hough Lines"
[image2]: ./test_images_output/annotated_solidWhiteCurve.jpg "Hough Lines on image"
