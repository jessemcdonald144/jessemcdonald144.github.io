---
layout: inner
title: "IoT Traffic Sensor"
permalink: /projects/iot-traffic-sensor/
description: "Edge AI traffic monitoring using Jetson Nano, YOLOv8, and LoRaWAN."
image: /images/traffic_sensor/banner.jpg
nav: false
---

# IoT Traffic Sensor

**Course:** Internet of Things
**Semester:** Spring 2026

---

## Overview

This project developed an edge-based traffic monitoring system capable of
classifying passing vehicles while preserving privacy. Rather than streaming
video to the cloud, all computer vision processing occurs locally on an
NVIDIA Jetson Nano. Only aggregate traffic statistics are transmitted over
LoRaWAN, and captured video is deleted immediately after processing.

---

## Objectives

- Monitor traffic volume
- Classify vehicle types (cars, trucks, vans)
- Estimate environmental traffic loading
- Minimize bandwidth usage
- Preserve user privacy

---

## Hardware


![Component Layout](/img/posts/iot/iot_hardware.png)

- NVIDIA Jetson Nano
- Raspberry Pi CSI Camera
- Feather M0 LoRaWAN Board
- Grid Power Supply
- Custom 3D-printed enclosure

![3D Printed Enclosure](/img/posts/iot/iot_case.png)

---

## Software

- Python
- YOLOv8
- OpenCV
- LoRaWAN
- Fusion 360

---

## System Architecture

1. Capture images using the CSI camera.
2. Execute YOLOv8 inference locally.
3. Count and classify vehicles.
4. Aggregate metadata.
5. Transmit results over LoRaWAN.
6. Delete video frames after processing.

---

## Results

The system successfully:

- Classified multiple vehicle categories
- Operated entirely on edge hardware
- Reduced network bandwidth by transmitting only metadata
- Preserved privacy by eliminating stored video

---

## Skills Demonstrated

- Embedded Systems
- Computer Vision
- Edge AI
- Machine Learning
- Internet of Things
- LoRaWAN Networking
- Python Development
- CAD Design
- Fusion 360
- Rapid Prototyping

---

## Gallery

![Deployment](/img/posts/iot/deploy_2.gif)

![Detection Results](/img/posts/iot/deploy_results.png)
---

<h2>GitHub</h2>

<a href="https://github.com/jessemcdonald144/edge-vit-pipeline"
   target="_blank"
   rel="noopener noreferrer"
   class="github-button">
  View GitHub Repository
</a>

<style>
.github-button {
  display: inline-block;
  padding: 12px 20px;
  background-color: #24292e;
  color: white;
  text-decoration: none;
  font-weight: 600;
  border-radius: 6px;
  transition: opacity 0.2s ease, transform 0.2s ease;
}

.github-button:hover {
  color: white;
  opacity: 0.85;
  transform: translateY(-1px);
}
</style>