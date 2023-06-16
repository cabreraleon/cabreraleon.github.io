---
layout: post
title: Module 1 - Videogames
---

In one of my assigned discussion questions, I was prompted to discuss in depth one motion planning application. What type of motion planning algorithm is used? How is the algorithm modified to cater to the application? My response follows.

<br>

Motion planning is critical to developing high-quality, realistic graphic animation for video games. Gamers are less likely to reject video games where animated characters move in a realistic, natural path in a virtual plane with many obstacles. One main problem that motion planning can solve in graphic animation is when video game entities must move in groups. For example, in the Kingdom Hearts video games by Square Enix and Disney, the player-controlled character, Sora, navigates his path with two or more non-player controlled (NPC) characters, Donald and Goofy (shown below). All entities must find collision-free paths when traveling as a flock without deviating too far from each other or making unnatural movements like walking towards an enemy or moving in manners that aren't human or animal-like. This  can lead to characters getting stuck or walking through obstacles instead of around them, which I witnessed multiple times.

<br>

According to Overmars (2005),  path planning in video games is usually computed using a combination of grid-based A* techniques, local methods for obstacle avoidance, flocking for group motion, combinations of scripted motion, and waypoints. Probabilistic Roadmaps are used to create virtual videogame roadmaps and query the paths navigated by the animated character entities. The paper summarizes how in the pre-processing phase of the PRM, the roadmap computes all possible motions for the animated character entity and is represented by a graph in which the nodes correspond to an entity’s placements and the edges represent collision-free paths between those placements. During the game, the roadmap is used for answering path planning queries. Unfortunately, the PRM algorithm does not usually compute high quality roadmaps that can make multiple NPCs take long detours. 

<br>

![module1assignment](https://cabreraleon.github.io/images/fig5.png)
Figure 1. Kingdom Hearts Characters in Motion. Sora, Donald, Goofy, and Baymax are moving in a flock within the virtual free space without colliding into the  obstacles or each other.  In the roadmap at the top right corner, the flock of multiple characters is represented by the keychain icon, the free space is the blue area, and the obstacles are represented by white lines. (Source: Square Enix and Disney, 2019).

<br>

This motivated Overmars to propose a better way to create better roadmaps by creating nodes that lie far away from obstacles and then sampling near the Voroni diagram to increase the clearance in the configuration space, and then adding additional edges to create cycles in the roadmap graph to avoid long detours. Instead of only finding a straight line between two nodes that are collision free, their method also takes in circle arcs. Their roadmaps can be used in the query phase without the need for any post-processing. Basically, he still used PRM but they added his own techniques to the algorithm to create better roadmaps. The figure below illustrates his modified method.

![module1assignment](https://cabreraleon.github.io/images/fig6.png)
Figure 2. An example of a smooth roadmap completed in Overmars (2005)





