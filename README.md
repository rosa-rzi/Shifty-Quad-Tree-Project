# Shifty-Quad-Tree-Project
> Programming Language: C++

> Testing: GDB, Valgrind

> IDE: Visual Studio

---
About
---
This project is inspired by an artist who recreates classic portraits with a blocky effect. This is achieved by creating functions that compute statistics, such as variance and average, and recursively splitting the image. 

Input             |  Output
:-------------------------:|:-------------------------:
![](https://github.com/rosa-rzi/Shifty-Quad-Tree-Project/blob/3bb7ae824eb2758e61c76968d1cb2401d2827727/images/Screen%20Shot%202021-05-18%20at%203.22.17%20PM.png)  | ![](https://github.com/rosa-rzi/Shifty-Quad-Tree-Project/blob/3bb7ae824eb2758e61c76968d1cb2401d2827727/images/Screen%20Shot%202021-05-18%20at%203.22.24%20PM.png)




---
Implementation Strategy
---
The image is partitioned into two or four children using at most one vertical and at most one vertical line. The variability of all children is measured for each partition and the split that minimizes the maximum variability among children is the one used to partition the image. The most optimal split is found in O(wh) time. We continue to split the image until the variability is at most a prescribed *tolerance* which then the pixel is colored using it's average pixel color.

Here is an animation of the partitioning (leaves of the shifty-quadtree):
<p align="center">
  <img width="175" height="175" src="https://github.com/rosa-rzi/Shifty-Quad-Tree-Project/blob/2841c3a198f6c8b2ba845cae4987e9eb4559082a/images/pacman.gif">
</p>

#Acknowledgment
This project is a programming assignment for UBC's Data Algortihms and Structures class offered in 2020W2. My partner, Ishraq Mostaf, and I received a grade of 100%
