# Stereo Vision

Just like our eyes can give us a sense of how far some object is, algorithms can find the depth of an object in a frame by processing two images from a pair of stereo cameras. 

In this project, I use a dataset for stereo camera images to calculate the disparity and depth of an object in an image. Disparity is the horizontal displacement of the same point in an image in the two frames captured by the stereo camera (the left and right frame). Using this information, a depth map is calculated in which the pixels are color-coded depending on how close to the camera they are. 

Below is an example of a rough depth map using the semi-global matching algorithm. The pixels closer than a certain threshold are colored red, and those farther away are colored blue.

![Stereo](https://github.com/bad-engineer/stereo-vision/assets/74527254/b603ec9d-c377-45fc-9cc0-aa6daf57339d)

In this project, I combined object detection with depth estimation. I used the KITTI Dataset (http://www.cvlibs.net/datasets/kitti/) and YOLOv4 for object detection.

Below are the results of Yolov4 on a test image:

![result_yolo(1)](https://github.com/bad-engineer/stereo-vision/assets/74527254/5e6496b1-91ca-4f17-8ba2-09cd45afd2aa)

Applying depth calculation to the detected objects, we get an approximate distance from the camera:

![depth_res](https://github.com/bad-engineer/stereo-vision/assets/74527254/c161c9d7-9448-4ac1-91ec-aafeaf4f1ade)

### References

Jeremy Cohen's Course and Workshop on Stereo Vision and 3D Reconstruction (thinkautonomous.ai).
