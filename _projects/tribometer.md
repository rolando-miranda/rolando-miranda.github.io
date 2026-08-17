---
title: "Tribometer Prototype (Pin-on-Disk / Block-on-Ring)"
excerpt: "Undergraduate capstone — desktop tribometer integrating mechanical design, FEA, mechatronic instrumentation, and materials testing."
date: 2023-04-01
category: mechanical-design
published: false
order: 4
header:
  teaser: /assets/images/tribometer-teaser.mp4
sidebar:
  - title: "Role"
    text: "Capstone team lead"
  - title: "Timeframe"
    text: "2022 – 2023"
  - title: "Tools"
    text: "SolidWorks · FEA · mechatronic instrumentation"
  - title: "Status"
    text: "Completed (BSc capstone)"
---

## What is tribometry?

Tribometry is the branch of material science that studies wear and friction between materials. The contact regimes in mechanical engineering are varied, and tribometric tests need to recreate the conditions that exist in modern day machinery. These tests try to optimize material selection for specific applications, predict part wear and tear and evaluate lubricant performance.

## Main design features 

This project consisted in the design of a low-cost tribometer capable of performing two different types of tests to evaluate wear and material performance between two test samples. The tests in question were Block on Ring and Pin on Disk, as described in ASTM G99-17 and ASTM G77- 17. The equipment makes use of a pivoting motor platform that positions the rotating sample axis between the two test positions while minimizing setup between tests. 
It also features a balanced, force sensing arm to measure friction force. To do this, a specific range of deformation /epsilon was required for the range of expected friction forces. Given is deformation range and selecting the material, Hooke’s law can be used to determine the required strain ranges and the arm geometry. 
$sigma=E*epsilon$

In an effort to make the equipment accessible for academic research, all sensors and actuators are controlled using Arduino and easily accessible parts from commonplace suppliers. Also, manufacturability and material availability were taken into account for OEM parts. 

This was the capstone project as a candidate for my Licenciate’s Degree in Mechanical Engineering, and was presented in January 2023. The full text is available [here](https://repositorio.sibdi.ucr.ac.cr/items/717c570e-2cc6-4a10-a6ee-f39ae8fad7c8/full). 
