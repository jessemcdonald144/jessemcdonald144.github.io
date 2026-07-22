---
layout: inner
title: "IoT Traffic Sensor"
permalink: /projects/iot-traffic-sensor/
description: "Privacy-focused edge AI traffic monitoring using a Jetson Nano, YOLOv8, and LoRaWAN."
nav: false
---

# IoT Traffic Sensor

**Course:** Internet of Things  
**Semester:** Spring 2026

## Project Overview

This project is a privacy-focused traffic monitoring system that detects and classifies passing vehicles. Images are discarded after processing.

The final system was designed to:

- Count and classify cars, trucks, vans, and other vehicles
- Minimize network bandwidth by transmitting metadata instead of video
- Protect privacy through local image processing and immediate frame deletion

## System Design

The pipeline follows six steps:

1. Capture a frame with the CSI camera.
2. Run YOLOv8 inference on the Jetson Nano.
3. Identify and classify vehicles in the frame.
4. Aggregate vehicle counts locally.
5. Send the summarized data over LoRaWAN.
6. Delete the processed frame.

### Hardware Architecture

<figure style="margin-bottom: 40px;">
  <img src="/img/posts/iot/iot_hardware.png"
       alt="IoT traffic sensor hardware components and system layout"
       style="width: 100%; height: auto;">
  <figcaption><em>Figure 1. Hardware architecture showing the Jetson Nano, camera, LoRaWAN board, and power components.</em></figcaption>
</figure>

The prototype used:

- NVIDIA Jetson Nano
- Raspberry Pi CSI camera
- Feather M0 LoRaWAN board
- Grid-connected power supply
- Custom 3D-printed enclosure

### Mechanical Design

<figure style="margin-bottom: 40px;">
  <img src="/img/posts/iot/iot_case.png"
       alt="Custom 3D-printed enclosure for the IoT traffic sensor"
       style="width: 100%; height: auto;">
  <figcaption><em>Figure 2. Custom enclosure designed in Fusion 360 to organize and protect the hardware.</em></figcaption>
</figure>

## Deployment and Results

<figure style="margin-bottom: 40px;">
  <img src="/img/posts/iot/deploy.gif"
       alt="IoT traffic sensor operating during roadside deployment"
       style="width: 100%; height: auto;">
  <figcaption style="margin-top: 15px; text-align: center;"><em>Figure 3. Roadside deployment of the completed traffic-sensing prototype.</em></figcaption>
</figure>

<figure>
  <img src="/img/posts/iot/deploy_results.png"
       alt="YOLOv8 vehicle detection and classification results"
       style="width: 100%; height: auto;">
  <figcaption style="margin-top: 15px; text-align: center;"><em>Figure 4. Example YOLOv8 output showing vehicle detection and classification during testing.</em></figcaption>
</figure>

## Project Resources

<a href="https://github.com/jessemcdonald144/edge-vit-pipeline"
   target="_blank"
   rel="noopener noreferrer"
   class="btn btn-default btn-lg">
  <i class="fa fa-github fa-lg"></i>
  GitHub Repository
</a>

<a href="https://docs.google.com/presentation/d/1Neh7iUO9mIBXUF-v6fONAZ-haAOQD0Q9yqrP8UCiWfY/edit?usp=sharing"
   target="_blank"
   rel="noopener noreferrer"
   class="btn btn-default btn-lg">
  <i class="fa fa-file-powerpoint-o fa-lg"></i>
  Final Design Review
</a>
