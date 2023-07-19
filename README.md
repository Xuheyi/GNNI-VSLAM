# GNNI-VSLAM:An Improved Visual SLAM Algorithm Based on Graph neural network

## Introduction
Targeting conventional visual SLAM methods, which are prone to feature point extraction difficulties and feature mismatching when encounter sparse texture scenes or large viewing angle motion. we propose GNNI-VSLAM, the algorithm integrates feature extraction and matching map neural networks with the back-end of the [ORB-SLAM2] system to build an IGNN-VSLAM system with high-precision positioning and high-accuracy map building for mobile robots under sparse texture scenes or large viewing angle motion.

## Example
GNNI-VSLAM Real-time mapping with sparse texture sences and large viewing angle motion:

GNNI-VSLAM Real-time mapping with large viewing angle motion:

![image](https://github.com/Xuheyi/GNNI-VSLAM/blob/main/1.gif)

GNNI-VSLAM Real-time mapping with sparse texture and large viewing angle motion:

![image](https://github.com/Xuheyi/GNNI-VSLAM/blob/main/2.gif)

# Dependencies

## C++11 or C++0x Compiler
We use the new thread and chrono functionalities of C++11.

## Pytorch
We use [Pytorch](https://github.com/pytorch/pytorch) C++ api(libtorch) for deloying the GNNI-VSLAM. 
The libtorch can be built as follows:
```
git clone --recursive -b v1.0.1 https://github.com/pytorch/pytorch
cd pytorch && mkdir build && cd build
python ../tools/build_libtorch.py
```
The built libtorch library is located at ```pytorch/torch/lib/tmp_install/``` in default.

## Pangolin
We use [Pangolin](https://github.com/stevenlovegrove/Pangolin) for visualization and user interface. Dowload and install instructions can be found at: https://github.com/stevenlovegrove/Pangolin.

## OpenCV
We use [OpenCV](http://opencv.org) to manipulate images and features. Dowload and install instructions can be found at: http://opencv.org. **Required at leat 2.4.3. Tested with OpenCV 2.4.11 and OpenCV 3.2**.

## Eigen3
Required by g2o (see below). Download and install instructions can be found at: http://eigen.tuxfamily.org. **Required at least 3.1.0**.

## DBoW2 and g2o (Included in Thirdparty folder)
We use modified versions of the [DBoW2](https://github.com/dorian3d/DBoW2) library to perform place recognition and [g2o](https://github.com/RainerKuemmerle/g2o) library to perform non-linear optimizations. Both modified libraries (which are BSD) are included in the *Thirdparty* folder.

# Preparation
Clone the code
```
git clone https://github.com/Xuheyi/GNNI-VSLAM.git
```
Then build the project 
```
cd GNNI-VSLAM
./build.sh

```
