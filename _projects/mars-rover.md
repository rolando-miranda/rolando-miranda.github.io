---
title: "Autonomous Mars Rover (MuJoCo)"
excerpt: "Planning and control algorithm for soil-sample collection, tested in the MuJoCo physics simulator."
date: 2025-05-01
category: robotics
order: 3
header:
  teaser: /assets/images/rover_teaser.mp4
sidebar:
  - title: "Role"
    text: "Sole developer (coursework)"
  - title: "Timeframe"
    text: "Spring 2025"
  - title: "Tools"
    text: "MuJoCo · Python"
  - title: "Status"
    text: "Completed"
---

This project explored autonomous navigation for a miniaturized Sample Fetch Rover (mSFR), a lightweight rover concept proposed to support NASA's Mars Sample Return mission. The mSFR's role is to retrieve cached soil samples in Jezero Crater and return them to a lander, navigating mapped terrain with known obstacles along the way. I designed and implemented a full planning and control pipeline for this rover: a path planner to generate safe routes to each sample, and a controller to track that path through to completion.

I implemented an RRT*-based planner that generates sample-reaching paths while respecting a heading-change constraint between nodes, keeping the rover's steering within realistic limits. For control, I designed a Linear Quadratic Regulator (LQR) that minimizes a quadratic cost over torque and steering inputs, using a linearized model of the rover's dynamics re-derived at every timestep. I solved the optimization with the cvxpy library and validated the full system in the MuJoCo physics simulator, comparing the linearized control model against more realistic simulated dynamics.

The planner reached a 47% success rate generating valid paths under a ±30° heading tolerance, with performance improving as I relaxed the tolerance or increased the iteration budget, showing a clear, tunable tradeoff between planning reliability and compute cost. The LQR tracked single waypoints smoothly, converging in cost as the rover approached its target and correctly modulating speed based on the desired terminal velocity. Integrating the two systems surfaced a more advanced control challenge at higher speeds, giving me a precisely characterized problem, along with concrete next steps like penalizing steering rate-of-change in the cost function, to target in a future iteration. The project reinforced a workflow I want to carry into future robotics work: linearized control design, simulation-based validation, and integration testing to pinpoint exactly where a system needs refinement.
