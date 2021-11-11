# BachelorThesis

Bachelor Thesis for my degree in Computer Science and Engineering in the University Carlos III of Madrid. The thesis is in Spanish as it's my native language.

The name topic of the thesis is about 3D mapping of environments using LIDAR sensors in drones with an autonomous navigation algorithm.

## Demos
Clicking on the first video showcases the navigation algotithm moving in the environment showing in the left what it can see. The second video visualizes an example 3D map.

[![Alt text](https://img.youtube.com/vi/rFUEEXAf83M/0.jpg)](https://www.youtube.com/watch?v=rFUEEXAf83M)
[![Alt text](https://img.youtube.com/vi/hA1wJa3V0BM/0.jpg)](https://www.youtube.com/watch?v=hA1wJa3V0BM)

## Summary of the work
The first part consists in a deep research work of many topics involved in the work: drone technology, LIDAR, navigation algorithms, 3D mapping, reinforcement learning...

The second part consists on the development of the tool responsible to generate and store a 3D map from the LIDAR data generated. The algorithm uses an specialized data structure called OcTree which is meant to represent 3D volume in the form of voxels in a very efficient manner. The map is capable of representing occupied, non-occupied and unknown volume.

A third part attempts to create an autonomous navigation algorithm for the exploration of the environment using reinforcement learning. This is the most technical part as it uses a custom environment and learning architecture:
* The perception of the algorithm is achieved using raytracing on the discovered map data to create an image without the need of additional sensors.
* The reset condition for training changes the map or the starting point to allow generalization in the learning.
* The reward function is made using principles of 'reward shaping'.
* The learning algorithm is PPO with a custom neural network policy.

Unfortunately, the achieved navigation algorithm is not nearly good enough to be practical.
