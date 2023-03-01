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
The proposal process of this work contains three sections, which include daylight simulation, training of the artificial neural network, and comparison of shading devices.
<br/><img src='/images/Project/Project1/ProposalPocess.png'>"

**Daylight simulation**
First, daylight simulation is conducted to obtain the value of the objective function, which serves as the basis for optimization. The Ladybug and Honeybee platforms from the Grasshopper plugin in Rhino were used for the simulation. The daylight simulation engine was based on Radiance software.

**Objective function**
To minimize glare and maximize occupants’ visual satisfaction in a dynamic daylight environment, the objective function is set as:
{█(min⁡(sGA)@min⁡(sDVA) )┤  

where sGA is the spatial glare autonomy, and sDVA is spatial daylight vote autonomy. sGA was established by Jones [28], and it is about the percentage of test points that meet the defined minimum fraction of glare-free during daylight hours of a year. The sGA equation is as follows:
sGA = \frac{\sum_{i=1}^{N}GT\left(i\right)}{N},\ with\ GT\left(i\right)=1∶gti≥τtx0∶gti<τtx     

where {gt}_i is the quantity lower than the DGP threshold of sGA at point i, t_x represents the number of annual daytime hours, \tau the temporal fraction threshold. In this study, we set the DGP threshold to 0.35 and \tau to 95%, namely, sGA0.35/95%.

The sGA was the dynamic metric for assessing the glare discomfort of daylit space and was developed according to daylight glare probability (DGP). Therefore, the DGP threshold is important for the calculation of sGA. Table 3 shows the correlation between DGP and glare level. In addition, the DGP can be represented as the equation:

DGP=5.87\times{10}^{-5}E_v+9.18\times{10}^{-2}log\left(\sum_{i}^{n}\frac{L_{s,i}^2\omega_{s,i}}{E_v^{1.87}P_i^2}\right)+0.16 

where E_v the vertical illuminance (lux), L_s the luminance of the glare source (cd/m²), \omega_s the solid angle of the glare source, P the position index, and n the number of glare sources.

In objective function (1), sDVA is used to quantify people’s satisfaction with the dynamic daylight environment. It is reported as the ratio of test points that received a specific minimum fraction of satisfactory threshold during the daylight hours of a year. The sDVA equation is represented as:

sDVA = \frac{\sum_{i=1}^{N}DT\left(i\right)}{N},\ with\ DT\left(i\right)=1∶dti≥γty0∶dti<γty               

where {dt}_i is the amount of time lower than the daylight subjective vote (DSV) threshold of sDVA at point i, t_y represents the number of annual daytime hours, \gamma the temporal fraction threshold. For maintaining the satisfaction level, the temporal faction of the DSV threshold would refer to the daylight performance of the study case. In this study, we set the DSV threshold to 0.30 and \gamma to 80% which equates to the average daylight vote autonomy (DVA) in the original daylight environment of the study case, namely, sDVA0.30/80%. 

A formula was developed from the surveyed data to correlate the daylight subjective vote (DSV) with the horizontal illuminance level. Because the illuminance level increased much faster than the change in the occupants’ DSV, the x-axis was transformed logarithmically, as is commonly practiced in daylighting research. A quadratic function was used to correlate the DSV with the logarithmic illuminance (Eh, lux), as shown in Equation (5). The obtained equation was then used in the objective function to calculate the DSV with the simulated illuminance. 

DSV=0.003025\left[2.4098\ln{\left(E_h\right)}-10.233\right]^2-0.0405\left[2.4098\ln{\left(E_h\right)}-10.233\right]+0.380175 

**Artificial Neural network (ANN)**
Artificial intelligence was an effective and feasible tool to generate the prediction model.Many researches had applied the Artificial Neural network (ANN) in the field of daylighting simulation over the last few years and achieved good performance. 

**Multi-objective genetic algorithm (MOGA)**
This study addressed a multi-objective problem with two objectives that change in opposite directions, so its solution was not unique. A solution that is not dominated by another is called a nondominated solution, and the group of nondominated solutions generated in the optimized algorithm is called a Pareto set, which can be obtained by the MOGA.

**Shading strategies**
To remedy the poor existing window design, four shading strategies, namely, perforated aluminum sheet (PAS), vertical slats (Vs), serrated windows with southern orientation (Sw_S), and serrated windows with northern orientation (Sw_N), were selected for optimization and comparison. Figure 3 shows the four strategies and the corresponding design variables. Perforated aluminum sheet changes the window-to-wall ratio to prevent glare and at the same time changes the distribution of daylight. The number and size of the holes in the PAS are the key parameters of shading effectiveness. As a result, the design variables of the PAS are the number of holes in the vertical and horizontal columns and also the hole diameters. 

When vertical slats are used, the angle of the slats can be adjusted to obstruct most daylight from directly entering the room. Lee et al. considered Vs to be the best shading device among vertical louvers, horizontal louvers, eggcrate louvers, overhangs, vertical slats, horizontal slats, and light shelves for improving UDI at the east and west orientations. The design variables of Vs are the number, width, and rotation angle of the slats.

Serrated windows transform the received sunlight from direct to diffuse by alternating the orientation of the windows. In this study, the Sw “changes” the façade orientation from west to south, to avoid the direct afternoon sunlight from the west while taking advantage of the diffuse sunlight from the south or north. To more accurately research the shading strategy, we separately set the opening surface in the opposite direction, namely, one was the serrated windows facing south (Sw_S) and the other one is the serrated windows facing north (Sw_N). The design parameters of the Sw are the rotation angle, extension length, and window opening ratio of the blocking surface. 
<br/><img src='images/Project/Project1/shadingDevices.png'>"