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

## Motivation
When we visit a beautiful building, we want to take pictures of it. However, there are always some details missing because you can only take limited pictures. What if you want to see a novel view of  building that you cannot see in your pictures?

The main objective of this project is to render novel view of buildings using pictures either taken by yourself or collected from internet. To achieve this, Feature Detection, Structure From Motion (SFM), Bundle Adjustment, and Neural Volume Rendering are used. While the three tasks look like traditional computer vision approaches, Data Science plays an important role in Neural Volume Rendering. Instead of constructing 3D mesh or point cloud, Neural Volume Rendering enables represting 3D model implicitly using differentiable deep learning models. This dramaticlly reduces the size of 3D models. For example, the [NeRF](https://www.matthewtancik.com/nerf) can generate high-detailed novel view of object using only 5MB model.
