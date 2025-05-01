# nmm-week4

Welcome to Classical hell! From this week we forget about electrons and embrace the simpler times when particles were particles and waves were waves. In other words, Molecular Dynamics based on classical equations of motion. This allows our models to reach larger scales of atomistic processes. Week 4 in particular is dedicated to all-atom simulations, the critical importance of MD force fields, and atomistic processes of relevance for nanomaterials.

## Assignment 1 - The Icebreaker

Let's use your first MD assignment to break the ice. Literally! In this assignment you will play with phase changes of water and how they depend on the chosen water model.

### Instructions

1a. start from ice 1h, tip3p model. Roughly find melting temperature. Compare to literature and explain experimental discrepancy.

1b. Switch to the more complex tip4p model. Roughly find melting temperature. Compare to literature and explain experimental discrepancy.

1c. optional: find the boiling points of the two models, compare to literature.

## Assignment 2 - Out of Flatland

Back to graphene, now much larger and without perfect periodic lattice conditions! In the real world, graphene is not an infinite 2D plane and graphene sheets tend to form crumpled structures (LINK TO PAPER). Let's see how these structures affect the energy and mechanical stresses of graphene flakes. Assignment and scripts inspired by and adapted from [Eric N. Hahn's tutorial](https://www.ericnhahn.com/tutorials/lammps-tutorials/crumpled-graphene).

### Instructions

2a. Check the simulation script crumplingSphere.in. Answer a few questions on the model implemented (you can also do this after running the simulation and visual inspection):
(i) what force field is used?
(ii) how many bonds are present in the graphene sheet created? Does it make sense?
(iii) what is the key command line used to deform the graphene sheet?

2b. Run the simulation and make a movie/a few snapshots of the process using Ovito for your report. Always start by visually inspecting your simulation! 
(i) Color particles by potential energy. What do you notice? (careful, this is sensitive to the boundary values you select for the coloring scheme)
(ii) Plot the potential energy and the radius of gyration of the system over time. Note that the first one is an output of the thermo command in the lammps output file, 
     while for the second one you need BeadSpring Analytics or any other post-processing tool of your choice. 

2c. Now modify the "fix indenter" line and try to make a cylindrical nanotube out of your initial sheet. 
    Report again your final structure and the variation in potential energy and radius of gyration. How does it compare to the previous simulation? 
    NOTE: No need to create a perfect nanotube, which would be very challenging and requires additional tricks to set up. But the closest structure to a perfect nanotube reported by the weekly deadline gets a non-grade-related prize!

2c. Instead of a "fix indenter", now use the "fix deform" command to perform uniaxial deformation of your graphene flake along the x (or y) axis. 
    Look at the LAMMPS documentation to implement it, and take care particularly of the "erate" and "remap" keywords. 
    Run the simulation again. What happens after a while? Discuss physically if it makes sense, both from an experimental point of view and within the framework of the model used.

## Assignment 3 - Go with the Flow

Transport and adsorption/absorption phenomena are of critical importance for nanomaterials, from batteries to functionalized surfaces. Let's play with them using what you are already familiar with: water and graphene! This assignment goes over the diffusion of water molecules in a graphene-bound nanochannel. Assignment adapted from [Simon Gravelle's original script](https://github.com/simongravelle/lammps-input-files/tree/main/inputs/water-in-graphene-slit).

### Instructions

3a. Which force field? C-O epsilon value? Is it appropriate? Differences with that of Assignment2? 
     Run the simulation, get msd overall and divided by groups. Also water density and velocity profiles. 
     
     Careful, big simulation. Use half a node (recommended), plan ahead.


3b. Repeat for different forces pushing water. Make a plot of all average msd as function of pushing force, discuss. Compare velocity profiles, discuss.
