---
title: "Optimization of Daylit Space"
excerpt: "We apply a multi-objective genetic algorithm to optimize the daylight environment, develop a new formula to quantity the occupants' perception, and design a framework to compare the different shading strategies.<br/><img src='/images/Project/Project1/cover_photo.jpg'>"
collection: project
---

Background
======
Due to the growth of energy consumption, the tendency of global warming has been sped up. Building energy consumption occupied more than 20% of the energy consumption and lighting energy consumption has an about 15% of building energy consumption. In addition, some research had proven sunlight that has a positive impact on children and work efficiency. Therefore, it is important to obtain clean energy to supply the building lighting. However, excessive daylight also leads the glare for occupants. We tried to use a multi-objective genetic algorithm to balance between reducing glare and improving subjective satisfaction.

Method
======
The proposal process of this work contains three sections, which include daylight simulation, training of the artificial neural network, and comparison of shading devices.<center><br/><img src='/images/Project/Project1/ProposalPocess.png'><br/>Figure 1. The process used to optimize a shading device based on MOGA.</center>

**Daylight simulation**
<br/>First, daylight simulation is conducted to obtain the value of the objective function, which serves as the basis for optimization. The Ladybug and Honeybee platforms from the Grasshopper plugin in Rhino were used for the simulation. The daylight simulation engine was based on Radiance software.

**Objective function**
<br/>To minimize glare and maximize occupants’ visual satisfaction in a dynamic daylight environment, the objective function includes sGA and sDVA.


**Artificial Neural network (ANN)**
<br/>Artificial intelligence was an effective and feasible tool to generate the prediction model. Many researchers had applied the Artificial Neural network (ANN) in the field of daylighting simulation over the last few years and achieved good performance. <center><br/><img src='/images/Project/Project1/picture3.png'><br/>Figure 2. The studied library, plan of the studied area, virtual test points of DSV, DGP , and photos showing actual conditions.</center>

**Multi-objective genetic algorithm (MOGA)**
<br/>This study addressed a multi-objective problem with two objectives that change in opposite directions, so its solution was not unique. A solution that is not dominated by another is called a nondominated solution, and the group of nondominated solutions generated in the optimized algorithm is called a Pareto set, which can be obtained by the MOGA.

**Case Study**
<br/>Our method for optimizing and selecting a shading strategy was applied to a university library in Shanghai, China (W121.433°, N31.028°). We chose the west side of the top (fourth) floor of the studied region because it was exposed to very strong sunlight in the afternoon due to the very high glazing ratio (42.6%) in the western façade. The floor plan of the test region is provided in Figure 2, along with photos of existing conditions.

<br/>To remedy the poor existing window design, four shading strategies, namely, perforated aluminum sheet (PAS), vertical slats (Vs), serrated windows with southern orientation (Sw_S), and serrated windows with northern orientation (Sw_N), were selected for optimization and comparison. Figure 3 shows the four strategies and the corresponding design variables. Perforated aluminum sheet changes the window-to-wall ratio to prevent glare and at the same time changes the distribution of daylight. The number and size of the holes in the PAS are the key parameters of shading effectiveness. As a result, the design variables of the PAS are the number of holes in the vertical and horizontal columns and also the hole diameters. 

**Shading strategies**
<br/>To remedy the poor existing window design, four shading strategies, namely, perforated aluminum sheet (PAS), vertical slats (Vs), serrated windows with southern orientation (Sw_S), and serrated windows with northern orientation (Sw_N), were selected for optimization and comparison. Figure 3 shows the four strategies and the corresponding design variables. Perforated aluminum sheet changes the window-to-wall ratio to prevent glare and at the same time changes the distribution of daylight. The number and size of the holes in the PAS are the key parameters of shading effectiveness. As a result, the design variables of the PAS are the number of holes in the vertical and horizontal columns and also the hole diameters. 

When vertical slats are used, the angle of the slats can be adjusted to obstruct most daylight from directly entering the room. Lee et al. considered Vs to be the best shading device among vertical louvers, horizontal louvers, eggcrate louvers, overhangs, vertical slats, horizontal slats, and light shelves for improving UDI at the east and west orientations. The design variables of Vs are the number, width, and rotation angle of the slats.

Serrated windows transform the received sunlight from direct to diffuse by alternating the orientation of the windows. In this study, the Sw “changes” the façade orientation from west to south, to avoid the direct afternoon sunlight from the west while taking advantage of the diffuse sunlight from the south or north. To more accurately research the shading strategy, we separately set the opening surface in the opposite direction, namely, one was the serrated windows facing south (Sw_S) and the other one is the serrated windows facing north (Sw_N). The design parameters of the Sw are the rotation angle, extension length, and window opening ratio of the blocking surface.<center><br/><img src='/images/Project/Project1/shadingDevices.png'><br/>Figure 3. Four studied shading strategies and corresponding design parameters, where the serrated windows represent the different shading strategies of Sw_S and Sw_N.</center>