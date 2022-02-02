# TDI Project - Novel View of Buildings Using Neural Volume Rendering of Pictures
Yu Zhao
yuzha0215@gmail.com

## Background
I am a PhD student in University of Illinois at Urbana-Champaign. My major is Agricultural and Biological Engineering. 
My research was about studying indoor air quality in human or animal buildings. 
More specifically, we capture tracer particle images by multiple cameras then perform 3D reconstruction to get their velocities.
To help my research, I took several data science and computer science classes in my university. 
So I am familar with data science, computer vision and programming. I have utilized data science to solve my [research problem](https://yuzhao0215.github.io/ds_portfolio/projects/project1.html).
And here is a link to a little [Heroku application](https://yuzhao0215.github.io/ds_portfolio/projects/project2.html) I made. 

I am interested in data science not only because it is helpful for research, but also because it can solve real world problems.
In fact, I think it might be more difficult to solve real problem because the data are less controled.
And for the topic of TDI project, I would like to do a project that is related to the 3D reconstruction and buildings. 

## Motivation and Objective
When we visit a beautiful building, we want to take pictures of it. However, there are always some details missing because you can only take limited pictures. What if you want to see a novel view of  building that you cannot see in your pictures? It would be nice if we can generate novel pictures from a new angle that cannot be seen in existing pictures.

<p align="center">
	<img width="380" height="200" src="./images/1.jpg">
</p>

Therefore, the goal of this project is to train a model using existing pictures either taken by yourself or collected from internet. To achieve this, Feature Detection, Structure From Motion (SFM), Bundle Adjustment, and Neural Volume Rendering are needed. Although the first three tasks are also very important, the focus of this project is the Neural Volume Rendering. Instead of constructing 3D mesh or point cloud, Neural Volume Rendering enables represting 3D model implicitly using differentiable deep learning models. This reduces the size of 3D models a lot. For example, the [NeRF](https://www.matthewtancik.com/nerf) can generate high-detailed novel view of object using only 5MB model.

## Data
The datasets such as those used in [Photo Tourism](http://phototour.cs.washington.edu/) can be used in this project. Some self taken pictures are also used for preliminary results.

## What have been done
1. In the exploratory stage, the objective is to show the feasibily of this project. First a data processing pipeline is built consisting of feature Detection, Structure from Motion, and Bundle Adjustment. These three tasks uses method provided [here](https://github.com/nghiaho12/SFM_example/blob/master/src/main.cpp). This pipeline finds the optimal camera parameters including angles of views and camera positions as shown in following figure. It can also generate sparse pointclouds for reference. 

<p align="center">
	<img width="380" height="250" src="./images/2.png">
</p>

This pipeline is necessary because for most self taken and online pictures, these parameters are unknown and thus need to be initialized and optimized. To test if this pipeline is correctly built, a set of self taken images of a building model is passed to it and the output camera parameters are used to construct point clouds. The result shows that the camera parameters can be correctly calculated. 

2. A basic volume rendering was trained to show the feasibily of generating novel views of existing 2D images. In this task, the images with optimized cameras parameters from the data processing pipeline were used as training data. A classic volume render is constructed using pytorch3D. The results shown that this model can generate novel view of building models.
Initial  
![Initial](./images/rendered_images/1.png)
Iterations 50
![Initial](./images/rendered_images/2.png)
Iteration 100
![Initial](./images/rendered_images/3.png)

