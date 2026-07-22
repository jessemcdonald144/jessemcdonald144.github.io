---
layout: inner
title: "MEMS Gyroscope Design"
permalink: /projects/gyro/
description: "Designed and simulated a single-axis MEMS gyroscope in COMSOL Multiphysics, balancing sensitivity, resonant behavior, and fabrication constraints."
nav: false
---

# MEMS Gyroscope Design

**Course:** Microelectromechanical Systems (MEMS)  
**Semester:** Fall 2024

---

## Project Overview

This project focused on designing a manufacturable, single-axis MEMS gyroscope for angular-velocity sensing in a 4µm² area. I developed the device geometry and used COMSOL Multiphysics to determine its resonant behavior and refine the suspension system.

The sensor uses electrostatic actuation to drive a suspended proof mass. When the device rotates, the Coriolis effect produces motion in the perpendicular sense direction, which can be measured capacitively.

## Design and Simulation Process

1. Created the proof mass, suspension springs, anchors, and comb-drive structures.
2. Built the complete device model in COMSOL Multiphysics.
3. Performed eigenfrequency analysis to identify the drive and sense modes.
4. Adjusted spring and mass dimensions through iterative simulations.

---

## Final Device Layout

<figure style="margin-bottom: 40px;">
  <img src="/img/posts/mems/gyro2.png"
       alt="Final layout of the single-axis MEMS gyroscope"
       style="display:block; width:75%%; max-width:950px; height:auto; margin:0 auto;">
  <figcaption style="text-align:center; margin-top:10px;">
    <em>Figure 1. Final gyroscope layout showing the proof mass, suspension springs, anchors, and capacitive comb structures.</em>
  </figcaption>
</figure>

---

## Modal Analysis

<div class="row">
  <div class="6u 12u$(small)">
    <figure style="margin-bottom: 40px;">
      <img src="/img/posts/mems/gyro1.png"
           alt="COMSOL drive-mode simulation of the MEMS gyroscope"
           style="display:block; width:75%%; height:auto; margin:0 auto;">
      <figcaption style="text-align:center; margin-top:10px;">
        <em>Figure 2. Drive mode: the proof mass oscillates along the actuation axis.</em>
      </figcaption>
    </figure>
  </div>

  <div class="6u$ 12u$(small)">
    <figure style="margin-bottom: 40px;">
      <img src="/img/posts/mems/gyro0.png"
           alt="COMSOL sense-mode simulation of the MEMS gyroscope"
           style="display:block; width:75%%; height:auto; margin:0 auto;">
      <figcaption style="text-align:center; margin-top:10px;">
        <em>Figure 3. Sense mode: Coriolis-induced motion occurs perpendicular to the drive direction.</em>
      </figcaption>
    </figure>
  </div>
</div>