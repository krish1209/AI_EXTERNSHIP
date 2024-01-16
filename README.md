# People Counting and Tracking System

This project uses a Single Shot Detector (SSD) with a MobileNet architecture to count and track people in real-time. It's designed to be scalable and ready for business use cases, such as monitoring foot traffic in stores, buildings, shopping malls, etc.

## Introduction

The primary aim of this project is to provide a robust and scalable solution for real-time people counting and tracking. The system can be integrated with different types of video streams, such as live video feeds from IP cameras or webcams. It also includes features for sending real-time alerts, automating tasks, and optimizing performance.

## Theory

### SSD Detector

We use a Single Shot Detector (SSD) with a MobileNet architecture. SSD is a fast object detection method that generates region proposals and detects objects in a single shot. MobileNet is a deep neural network designed to run on resource-constrained devices, making it ideal for real-time applications.

### Centroid Tracker

The Centroid Tracker is used to track individual objects across frames. It computes the centroid (center) of the bounding boxes of detected objects, assigns unique IDs to each object, and tracks these objects over a sequence of frames.

## Installation

Before running the program, make sure to install the required dependencies. You can find the list of dependencies in the `requirements.txt` file.

## Usage

To run the program, you need to specify the paths to the SSD model files (`detector/MobileNetSSD_deploy.prototxt` and `detector/MobileNetSSD_deploy.caffemodel`) and the input video file or device.

Example usage:

- Run inference on a test video file: bash python people_counter.py --prototxt detector/MobileNetSSD_deploy.prototxt --model detector/MobileNetSSD_deploy.caffemodel --input utils/data/tests/test_1.mp4


## Features

- Real-Time Alert: Send an email alert in real-time when the total number of people exceeds a certain threshold.
- Scheduler: Automatically schedule the software to run at specific times.
- Timer: Stop the software execution after a certain duration.
- Simple Log: Log the counting data at the end of the day.

## References

- SSD paper: https://arxiv.org/abs/1512.02325
- MobileNets paper: https://arxiv.org/abs/1704.04861
- Centroid tracker: https://www.pyimagesearch.com/2018/07/23/simple-object-tracking-with-opencv/

