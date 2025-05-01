# nmm-week4

Welcome to Classical hell! From this week we forget about electrons and embrace the simpler times when particles were particles and waves were waves. In other words, Molecular Dynamics (MD) based on classical equations of motion. This allows our models to reach larger scales of atomistic processes. We can also do crazy things like increasing temperature above 0K and pushing stuff! Week 4 in particular is dedicated to all-atom simulations, the critical importance of MD force fields, and atomistic processes of relevance for nanomaterials.

## Assignment 1 - The Icebreaker

Let's use your first MD assignment to break the ice. Literally! In this assignment you will play with phase changes of water and how they depend on the chosen water model and simulation setup.

### Instructions

1a. start from ice 1h, tip3p model. Roughly find melting temperature. Compare to literature and explain experimental discrepancy.

1b. Switch to the more complex tip4p model. Roughly find melting temperature. Compare to literature and explain experimental discrepancy.

1c. optional: find the boiling points of the two models, compare to literature.

## Assignment 2 - Out of Flatland

Back to graphene, now much larger and without perfect periodic lattice conditions! In the real world, graphene is not an infinite 2D plane and [graphene sheets tend to form twisted or crumpled structures](https://doi.org/10.1016/j.mattod.2015.10.002). While relevant for electronic properties, let's simply see how these crumpling affects the energy and mechanical stresses of a graphene sheet. 
Assignment and scripts inspired by and adapted from [Eric N. Hahn's tutorial](https://www.ericnhahn.com/tutorials/lammps-tutorials/crumpled-graphene).

### Instructions

2a. Check the simulation script crumplingSphere.in. Answer a few questions on the model implemented (you can also do this after running the simulation and visual inspection):

(i) what force field is used?

(ii) how many covalent bonds are present in the graphene sheet created? Does it make sense?

(iii) what is the key command line used to deform the graphene sheet?

2b. Run the simulation (the CH.airebo-m file is also needed) and make a movie/a few snapshots of the process using Ovito for your report. Always start by visually inspecting your simulation! 

(i) Color particles by potential energy. What do you notice? Careful: this is sensitive to the boundary values you select for the coloring scheme.

(ii) Plot the potential energy and the radius of gyration of the system over time. Note that the first one is an output of the thermo command in the LAMMPS output file, 
     while for the second one you need BeadSpring Analytics or any other post-processing tool of your choice. 

2c. Now modify the "fix indenter" line and try to make a cylindrical nanotube out of your initial sheet. 
    Report again your final structure and the variation in potential energy and radius of gyration. How does it compare to the previous simulation?     
    NOTE: No need to create a perfect nanotube, which would be very challenging and requires additional tricks to set up. But the closest structure to a perfect nanotube reported by the weekly deadline gets a non-grade-related prize!

2c. Instead of a "fix indenter", now use the "fix deform" command to perform uniaxial deformation of your graphene flake along the x (or y) axis. 
    Look at the LAMMPS documentation to implement it, and take care particularly of the "erate" and "remap" keywords. 
    Run the simulation again. What happens after a while? Briefly discuss if it makes sense physically, both from an experimental point of view and within the framework of the model used. 
    Pro tip: per/atom stress is saved in the trajectory file, so you can use it to color particles based on stress.

## Assignment 3 - Go with the Flow

Transport and adsorption/absorption phenomena are of critical importance for nanomaterials, from batteries to functionalized surfaces. Let's play with them using what you are already familiar with: water and graphene! This assignment goes over the diffusion of water molecules in a graphene-confined nanochannel. LAMMPS code adapted from [Simon Gravelle's original script](https://github.com/simongravelle/lammps-input-files/tree/main/inputs/water-in-graphene-slit).

### Instructions

3a. Look at the input files waterFlow.in, PARAM.lammps, and data.lammps and answer a few questions:

(i) what force fields are used to simulate water and graphene? How do they  compare to the ones used in the first two assignments?

(ii) what is the value of the interaction energy epsilon between oxygen and carbon atoms?

(iii) which command enforces the flow of water in the channel?

3b. Run the simulation. Note that it is quite large; it will not take too long (~10min) but plan the needed resources accordingly. Calculate a few properties from the trajectory: 

(i) the mean square displacement (MSD) of water molecules, both on average and also divided by layers along the z-axis. You can do that in Bead Spring Analytics by [ADD INSTRUCTIONS]. What is the physical origin of the difference across layers?

(ii) the layer-by-layer distribution of water molecules density and velocity profile. How does the velocity profile compare to what is expected for [macroscopic laminar flow](http://hyperphysics.phy-astr.gsu.edu/hbase/pfric.html)? 

3c (OPTIONAL). Repeat 3b for different values of the force pushing water. Compare the average MSDs and the velocity profiles with varying force values and discuss your results.
