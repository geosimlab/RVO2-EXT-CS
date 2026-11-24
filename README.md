# RVO2-EXT-CS

An extended C# implementation of the **RVO2** (Optimal Reciprocal Collision Avoidance) library for microscopic simulation of pedestrian and e-scooter interactions.

This codebase is based on the original C# port [snape/RVO2-CS](https://github.com/snape/RVO2-CS) (UNC Chapel Hill).

## Key Extensions

* **Field of View (FOV) Cone (`setFieldOfView`)**: Restricts agent neighbor perception to a forward viewing sector with a configurable apex offset (`backOffset`).
* **Asymmetric Responsibility (`setAgentResponsibility`)**: Replaces standard 50/50 reciprocal avoidance with weighted avoidance sharing between interacting agents.
* **Kinodynamic Acceleration Limits (`setAgentDynamics`)**: Adds longitudinal and lateral acceleration/deceleration constraints (`acceleration`, `deceleration`) to linear programming velocity selection.
* **Backward Motion Constraint (`setAgentNoBackwardConstraint`)**: Prevents agents from moving backward relative to their preferred heading.

## Research Context

Developed as part of the research project:  
***"Studying e-scooters’ safety based on spatially explicit knowledge of the urban road infrastructure and shared dockless e-scooters"***

## License

Licensed under the **Apache License, Version 2.0**, preserving the original licensing terms of RVO2-CS. See the `LICENSE` file and source file headers for details.
