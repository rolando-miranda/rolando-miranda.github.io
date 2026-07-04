---
title: "Peristaltic Pump with Closed Loop Flow Control"
excerpt: "STM32-based, closed-loop-capable peristaltic pump."
date: 2025-11-01
category: mechatronics
published: true
order: 4
header:
  teaser: /assets/images/pump-teaser.png
sidebar:
  - title: "Role"
    text: "Sole developer (coursework)"
  - title: "Timeframe"
    text: "Fall 2025 — in progress"
  - title: "Tools"
    text: "STM32 · C · SolidWorks · 3D printing"
  - title: "Status"
    text: "In progress"
---

A closed-loop peristaltic pump controller: a stepper-driven peristaltic pump holds a reservoir at a target level using proportional control on a capacitive level sensor. The same principle drives the infusion pumps that deliver drugs to patients, which is what drew me to the project.

## What is a peristaltic pump?

A peristaltic pump is a type of positive displacement pump that uses rollers and a flexible tube to act on a fluid. Positive displacement pumps have design advantages that make them preferable to conventional centrifugal pumps in certain applications. One advantage is that flow rate is linearly dependent on motor input speed. Positive displacement pumps can also work against much higher pressure differentials and still generate flow in those conditions, compared to centrifugal pumps.

## The build

Mechanical and enclosure: the system integrates a peristaltic pump driven by a stepper motor, and tubing. I designed and 3D printed a custom enclosure that houses the screen, keypad, motor driver, and microcontroller, with mounting holes to fasten the pump directly to the body. Designing for assembly this way kept the wiring contained and made the unit easy to handle and iterate on.

Electronics: an STM32 microcontroller, a stepper driver, and a capacitive level sensor. The design handles two voltage domains, a low voltage for the logic and a higher voltage to drive the motor.

Firmware and interface: a proportional control loop written in C. The capacitive sensor reading sets the error against the target level, and the controller modulates pump speed to close it. A screen and keypad let the user set the target level.

{% include figure image_path="/assets/images/pump-teaser.png" alt="Pump" caption="3D render of the fully assembled peristaltic pump. Credits: Gemini" %}

## Design control choice

I chose proportional control deliberately. The flow rate was small relative to the reservoir volume, and the target level did not require tight precision, so proportional control was the right fit rather than reaching for a more complex controller. Matching the control approach to the actual demands of the problem mattered more than maximizing sophistication.

## What I learned

The most demanding part was implementing PWM on the STM32 in C. Coming from an Arduino background, working directly with duty cycle and frequency to drive a stepper motor is a different level of engagement with the hardware, and getting it right forced me to understand what the microcontroller was actually doing underneath the abstractions I was used to.

## Current state and next steps

The system successfully holds the reservoir at the setpoint, correcting in both directions whether the reservoir is overfilled or liquid is removed. A next step is a fully controllable interface with flow rate, volume dispensing, and timer settings, enabling low-cost, precise flow dispensing built from 3D printed parts and easy-to-find components.
