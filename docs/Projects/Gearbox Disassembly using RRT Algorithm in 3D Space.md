---
id: Gearbox Disassembly using RRT Algorithm in 3D Space
aliases:
  - Gearbox Disassembly using RRT Algorithm in 3D Space
tags: []
---

# Gearbox Disassembly using RRT Algorithm in 3D Space


> Developed at: Worcester Polytechnic Institute

> Project date: February, 2023

> GitHub URL: [parth-20-07/Gearbox-Disassembly-using-RRT-Algorithm-in-3D-Space](https://github.com/parth-20-07/Gearbox-Disassembly-using-RRT-Algorithm-in-3D-Space)

## Brief Introduction on Project

The objective of this task is to disassemble a gearbox with no collisions using RRT Algorithm. We are using the gearbox called SM-465.

Restriction based Experimentation:

- Restricting the Planner to only 2 axes improves the speed to find the path.
- Restricting the domain of the new node search reduces the path planning time.
- Too small of a search domain satisfies the position requirement but fails the orientation requirement for motion.

Search Based Experimentation

- Setting the node search radius too small makes the path smooth but takes a lot of time.
- Setting the node search radius too big results in the shaft not being able to get out of the Gearbox due to collisions while motioning.

