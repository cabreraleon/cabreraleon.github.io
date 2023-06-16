---
layout: post
title: The Adaptive Neighborhood Connector
---

For motion planning in heterogeneous environments and parallel machines, it can become infeasible for humans to hand-pick the best connector method for PRM variants at each step of a problem. 
In Heterogeneous Environments, different algorithm choices may apply for different regions
In Parallel Processing, subdivision is often used to increase parallelism so each region can be processed independently
Manually selecting a single connector across all problems can lead to poor performance overall. We need a way to automatically and adaptively select the best connector depending on the problem at hand and its input. This problem inspired Chinwe Ekenna, Sam Ade Jacobs, Shawna Thomas, Nancy M. Amato to develop the Adaptive Neighborhood Connector algorithm for robotic motion planning.


# Related Works

1. **Hybrid PRMs:**
Some works use more than 1 sampling strategy and adaptively learns which sampler to use over time. ANC works similarly but applies this methodology only in the connection phase

2. **Candidate Neighborhood Selection Methods**
    - k-Closest: returns k -closest neighbors to a node based on distance metric (k is small constant)
    Advantage: nodes have higher chance to be connectable by LP because the C-space volume occupied by the connector is smaller 
    - R-closest: returns all neighbors within a radius r of the node determined by distance metric
    + K-Closest,K-Rand: randomly selects k neighbors from k2 closest nodes where k2 = 3k)
    + R-Closest, K-Rand: randomly selects k-random neighbors from those within distance r
   -  Distance Metrics: Euclidean, Center of Mass, Swept Volume
   - Spatial Subdivision and Parallelism
