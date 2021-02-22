# **Finding Lane Lines on the Road**

<img src="examples/line-segments-example.jpg" width="480" alt="Combined Image" />

This repo is created for submitting Udacity's Self Driving Car Nanodegree "Finding Lane Lines on the Road" assignment.
This project consists of algorithms to detect lane lines in front of the vehicle.

Overview
---
Algorithm and pipeline is in [P1.ipynb](/P1.ipynb). Pipeline consists of 6 steps:

1. Grayscale Conversion: Image is transformed into grayscale to work with brightness values only
2. Blurring Image: Using Gaussian Filter, grayscale image is blurred to get rid of noise
3. Canny Edge Detection: Using Canny Detection, found edges on image
4. Masking: With masking a quadrangle area, edges are reduced to a region of interest
5. Hough Transform: With hough transform, edges are transformed into lines in image. Resulting lines used to detect left
   and right lane lines
6. Annotation: Image is annotated with new lines found through steps 1-6

The Project
---

## If you have already installed the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) you should be good to go!   If not, you should install the starter kit to get started on this project. ##

**Step 1:** Set up
the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) if you haven't
already.

**Step 2:** Open the code in a Jupyter Notebook

You will complete the project code in a Jupyter notebook. If you are unfamiliar with Jupyter Notebooks, check
out [Udacity's free course on Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111) to get
started.

Jupyter is an Ipython notebook where you can run blocks of code and see results interactively. All the code for this
project is contained in a Jupyter notebook. To start Jupyter in your browser, use terminal to navigate to your project
directory and then run the following command at the terminal prompt (be sure you've activated your Python 3 carnd-term1
environment as described in
the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) installation
instructions!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory. Click on the file called "P1.ipynb". Another
browser window will appear displaying the notebook. Follow the instructions in the notebook to complete the project.

**Step 3:** Complete the project and submit both the Ipython notebook and the project writeup

## How to write a README

A well written README file can enhance your project and portfolio. Develop your abilities to create professional README
files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).

