---
title: "POPSTAR — Force Measurement Instrument"
excerpt: "Force-measurement instrument developed at NYU Tandon's Thermo-fluids Laboratory."
date: 2025-10-01
category: instrumentation
header:
  teaser: /assets/images/popstar-teaser.png
sidebar:
  - title: "Role"
    text: "Designer & builder"
  - title: "Affiliation"
    text: "NYU Tandon Thermo-fluids Lab"
---
POPSTAR is a thrust and drag measurement device designed as part of the instrumentation required for the Thermo-fluids laboratory at NYU Tandon. To characterize the [put-put boats](https://youtu.be/y9KV6c7MH7s?si=_YcqF1DF2VKHB9Lz) fully as thermal systems, it is critical to estimate how much power can a boat output. Additionally, the drag force is an important part of a boat's design process. Both of these magnitudes require measuring a force under different conditions: the first one requiring static flow, and the second one requiring a known relative fluid velocity. Also, the device allows for easy calibration by rotating the measuring arm to a horizontal position, where a known mass can be rested on the load cell end for taring. 

POPSTAR is an acronym for Put-put Observation Platform for Steam Testing and Resistance, which is also adequate given the colorful combinations that the assembled units have. The device was designed to be 3D printed with minimal supports and repaired easily using readily available additive manufacturing technology and materials. Parts are press-fit together, fastened using metric screws or glued in place.

The POPSTAR's main working principle is that of strain and electrical resistance. Strain gauges attached to the top and bottom of a load cell transduce the force exerted on the gauge into a (very small) change of resistance. A bridge then amplifies this signal into a readable change in electric potential that the microcontroller can read, log into a computer and send via I2C communication to the screen. This is the exact same principle that JPL uses in their rocket engine thrust test rigs. Only that this one is a bit smaller.

{% include figure image_path="/assets/images/engine_test.gif" alt="BlueOrigin rocket engine thrust test rig" caption="POPSTAR's big brother: a BlueOrigin rocket engine thrust test rig. *Credits: BlueOrigin Twitter*" %}
