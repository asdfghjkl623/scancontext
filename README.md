<!-- md preview: Show the rendered HTML markdown to the right of the current editor using ctrl-shift-m.-->

# Scan Context
- Scan Context is a global descriptor for LiDAR point cloud, which is proposed in this paper:

```
@INPROCEEDINGS { gkim-2018-iros,
  author = {Kim, Giseop and Kim, Ayoung},
  TITLE = { Scan Context: Egocentric Spatial Descriptor for Place Recognition within {3D} Point Cloud Map },
  BOOKTITLE = { Proceedings of the IEEE/RSJ International Conference on Intelligent Robots and Systems },
  YEAR = { 2018 },
  MONTH = { Oct. },
  ADDRESS = { Madrid }
}
```
- This point cloud descriptor is used for place retrieval problem such as place
recognition and long-term localization.


## What is Scan Context?

- Scan Context is a global descriptor for LiDAR point cloud, which is especially designed for a sparse and noisy point cloud acquired in outdoor environment.
- It encodes egocentric visible information as below:
<p align="center"><img src="example/basic/scmaking.gif" width=400></p>

- A user can vary the resolution of Scan Context for appropriate applications. Below is the example of Scan Contexts of various resolutions for the same point cloud.
<p align="center"><img src="example/basic/various_res.png" width=300></p>


## Structure of this repository
- Most of the codes are written in Matlab.
- A directory _matlab_ contains main functions including Scan Context generation and the distance function.
- A directory _example_ contains a full example code for a few applications. We provide a total 3 examples.
 1. _**basics**_ contains a literally basic codes such as generation and can be a start point to understand Scan Context.   
 2. _**place recognition**_ is the first example of our application. The example is conducted using KITTI sequence 00 and PlaceRecognizer.m is the main code. You can easily grasp the full pipeline of Scan Context-based place recognition via watching and following the PlaceRecognizer.m code.
 3. _**long-term localization**_ is the second example of our applicaiton. For the separation of mapping and localization, there are separate train and test steps. Main training and test codes are written in python and keras, only excluding data generation and performance evaluation codes (they are written in Matlab), and jupyter notebook of those python codes are provided. More details of our long-term localization pipeline is found in the below paper:
 ```
@ARTICLE{8633942, 
author={G. {Kim} and B. {Park} and A. {Kim}}, 
journal={IEEE Robotics and Automation Letters}, 
title={1-Day Learning, 1-Year Localization: Long-Term LiDAR Localization Using Scan Context Image}, 
year={2019}, 
volume={4}, 
number={2}, 
pages={1948-1955}, 
month={April},}
 ```
