# Lidar Obstacle Detection

## Summary
Step 1.
Voxel grid filtering is created to filter the cloud by only leaving a single point per voxel cube to lower the resolution of the point cloud.
Then,  a boxed region is defined to extract the region of interest. Filter point cloud on the roof of host vehicle.

Step 2. Segment the filtered cloud into two parts, road and obstacles. Use both PCL functions and self-built RANSAC.

Step 3. Cluster the obstacle cloud with euclidean clustering algorithms, construct KDTree, search K-NN points.

Step 4. Find bounding boxes for the clusters.

Step 5. Use the same processing pipeline on multiple pcd files to generate stream video.

## Result Video
![lidar](https://user-images.githubusercontent.com/25008320/112752501-aee44900-8fd3-11eb-9ab6-04e29cce6ab8.gif)


### Welcome to the Sensor Fusion course for self-driving cars.

In this course we will be talking about sensor fusion, whch is the process of taking data from multiple sensors and combining it to give us a better understanding of the world around us. we will mostly be focusing on two sensors, lidar, and radar. By the end we will be fusing the data from these two sensors to track multiple cars on the road, estimating their positions and speed.

**Lidar** sensing gives us high resolution data by sending out thousands of laser signals. These lasers bounce off objects, returning to the sensor where we can then determine how far away objects are by timing how long it takes for the signal to return. Also we can tell a little bit about the object that was hit by measuring the intesity of the returned signal. Each laser ray is in the infrared spectrum, and is sent out at many different angles, usually in a 360 degree range. While lidar sensors gives us very high accurate models for the world around us in 3D, they are currently very expensive, upwards of $60,000 for a standard unit.

**Radar** data is typically very sparse and in a limited range, however it can directly tell us how fast an object is moving in a certain direction. This ability makes radars a very pratical sensor for doing things like cruise control where its important to know how fast the car infront of you is traveling. Radar sensors are also very affordable and common now of days in newer cars.

**Sensor Fusion** by combing lidar's high resoultion imaging with radar's ability to measure velocity of objects we can get a better understanding of the sorrounding environment than we could using one of the sensors alone.


## Installation

### Linux Ubuntu 16

Install PCL, C++

The link here is very helpful, 
https://larrylisky.com/2014/03/03/installing-pcl-on-ubuntu/


