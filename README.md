# SFND 2D Feature Tracking

<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera course is to build a collision detection system - that's the overall goal for the Final Project. As a preparation for this, you will now build the feature tracking part and test various detector / descriptor combinations to see which ones perform best. This mid-term project consists of four parts:

* First, you will focus on loading images, setting up data structures and putting everything into a ring buffer to optimize memory load. 
* Then, you will integrate several keypoint detectors such as HARRIS, FAST, BRISK and SIFT and compare them with regard to number of keypoints and speed. 
* In the next part, you will then focus on descriptor extraction and matching using brute force and also the FLANN approach we discussed in the previous lesson. 
* In the last part, once the code framework is complete, you will test the various algorithms in different combinations and compare them with regard to some performance measures. 

See the classroom instruction and code comments for more details on each of these parts. Once you are finished with this project, the keypoint matching part will be set up and you can proceed to the next lesson, where the focus is on integrating Lidar points and on object detection using deep-learning. 

## Dependencies for Running Locally Windwos
* cmake >= 3.14.6
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* OpenCV >= 4.1.1
  * cmake -G "Visual Studio 16 2019" -a  Win64 -DCMAKE_WINDOWS_EXPORT_ALL_SYMBOLS=ON -DCMAKE_INSTALL_PREFIX=C:\pcl-ownBuild\install -DOPENCV_EXTRA_MODULES_PATH=C:/pcl-ownBuild/dep/opencv_contrib/modules  -DOPENCV_ENABLE_NONFREE=ON ..
  cmake --build . --clean-first --config Release --target INSTALL	

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Configure cmake -G "Visual Studio 16 2019" -a  Win64 -DCMAKE_WINDOWS_EXPORT_ALL_SYMBOLS=ON  -DOpenCV_DIR=C:\pcl-ownBuild\install\x64\vc16\lib  -DCMAKE_CXX_FLAGS=-I\ %include% ..
4 Compile cmake --build . --clean-first --config Release --target ALL_BUILD
5. Run it: `Release\2D_feature_tracking`.

MP.1 Data Buffer Optimization : Use Deque with push_back and pop_front
MP.2 Implmented the stuff as Shown an Previews sections
MP.3 Use a costem val cheak to remove keypoints outside the Region of Interest
MP.4 Implemented as shown in the lecture
MP.5 Implemented as shown in the lecture with the converer to float 
MP.6 Implemented as shown in the lecture
