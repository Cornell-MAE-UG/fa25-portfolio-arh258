---
layout: project
title: Thermodynamic Device Analysis
description: Breakdown of a Ossberger Crossflow G1078/20g (2 cell) —hydroturbine on Beebe/Fall Creek
technologies: [MATLAB]
image: /assets/images/hydrojpg.jpg
---


<h1><b>PROJECT OVERVIEW</b></h1>

This project was an assignment in my Thermodynamics class by which we applied our in class skills regarding device analysis to a real world instance of one of these devices. My group and I selected the Ossberger Crossflow G1078/20g (2 cell) —hydroturbine on Beebe/Fall Creek. I worked with James Larrabee, Annika Terezakis, and Andrew Nocily on this project; we did the whole thing entirely as a collective so our websites will essentially match.

<h2><b> IMAGES OF DEVICE AS A SYSTEM</b></h2>
The Hydroturbine in the collective cycle
![Shaded rendering of earlier version]({{ "/assets/images/overallsystem.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}

The hydroturbine isolated (useful for our analysis)
![Shaded rendering of earlier version]({{ "/assets/images/device.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}<br>



<h2><b> THERMODYNAMIC ANALYSIS</b></h2><br>
<b>Physical Description:</b><br> The plant uses two Ossberger cross-flow turbines: we chose to analyze the second unit listed on the Cornell Facilities page, named the “Crossflow G1078/20g (2 cell)”. In these types of system, water typically flows in from a body of water and passes through an inlet guides. These regulate flow rate and direct the water across the turbine’s blades twice, hence the “cross-flow” name, maximizing the amount of energy that can be harnessed. Water finally exits on the opposite side and is free to continue through the waterway. A benefit of crossflow turbines is that they operate at a variety of flows adequately and their efficiency remains relatively constant over a wide range of inputs, which is ideal for small river applications like this one where flow is far from constant under the variable weather conditions of Ithaca.<br>

<b>Mathematical:</b><br>
The best analysis for this setup is to model the cross-flow turbine as a control volume system operating at steady state, as the presence of running water makes a control model approximation unrealistic.<br>

Entropy: ![Shaded rendering of earlier version]({{ "/assets/images/entropy.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}

Due to limitations in the thermodynamics I have taken, I am unable to calculate the relative entropy change of the system, as that would take considerations of turbulent flow, friction between containing walls and particles, etc., that I am unable to do. For lack of a better process, I will stop with this equation here and return after later semesters for further, more detailed analysis than simply modeling the system as isentropic with no entropy generation.<br>

Energy: ![Shaded rendering of earlier version]({{ "/assets/images/energy.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}

For this model, it again makes sense to neglect heat transfer, as a turbine can be reasonably modeled as adiabatic without significantly affecting its operation. Assuming steady state as well, the energy term on the left can be neglected and mass terms can be combined. Due to limitations of current coursework, it also makes sense to have the enthalpy and velocity constant during the process, as it would be difficult to calculate specific values.<br>

This leaves power equal to the mass flow rate times the difference in specific potential energy. For a steady state system, mass flow rate can be found by multiplying volumetric creek flow by water’s density. For this part, I used USGS.gov’s automatic measurements of the discharge of Fall Creek to see how power output changes over the course of the year with different variable water flow rates.<br>

Final Work Rate Value: ![Shaded rendering of earlier version]({{ "/assets/images/workequation.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}<br>

System Interaction Diagram:

<b> MATLAB RESULTS </b><br>
USGS provides flow rate in cubic ft per second, for measurements taken every 3 hours and 15 minutes. <br>

In the code below, Andrew Nocily (groupmember) calculated the mass flow rate of the water and power output of the turbine. For lack of a better system, he labelled each measurement as an index of increasing number. The first data point was taken 12/18/24 at 7:30pm and continue until 12/18 at 3:45pm. Empty data points (blank spaces in the graph) appear where no data was unable to be taken–water was frozen.

    close all; % file setup

    % importing data from spreadsheet
    opts = detectImportOptions("water flow data fall creek.csv");
    opts.VariableNamesLine = 0;
    opts.VariableNames = ["Water", "Unit"];
    water_flow = readtable("water flow data fall creek.csv", opts);

    % data formatting
    wf = table2array(water_flow(:, "Water"));
    wf = flip(wf); % most recent data points were at top so I flipped

    wf = wf * 0.3048^3; % cfs to cms

    time = 1:2619; %index of times taken, every 3:15 hours:minutes

    % Discharge Plot
    figure;
    plot(time, wf)
    title("Fall Creek Discharge Over Time")
    xlabel("Index")
    ylabel("Volume Flow Rate [cubic meters per second]")

    % Power Calculations
    mf = wf * 1000; % mass flow rate
    dis_speed = 123.5 * 0.3048^3;
    power = mf * (9.81 * 35);
    power = power / 10^6;  % reduce orders of magnitude

    % Power Plot
    figure;
    plot(time, power)
    title("Power Produced Over Time")
    xlabel("Index")
    ylabel("Power [MW]")


Clearly, power output depends on the volumetric discharge of the river and has varying power outputs depending on the season and daily weather.

![Shaded rendering of earlier version]({{ "/assets/images/water.jpg" | relative_url }}){: .inline-image-r style="width: 500px"}

![Shaded rendering of earlier version]({{ "/assets/images/powerchart.jpg" | relative_url }}){: .inline-image-r style="width: 500px"} <br>
