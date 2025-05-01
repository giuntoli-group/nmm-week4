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

2a. Run the simulation crumplingSphere.in. Questions on the script. Make a movie of the process. Make some snaphots coloring by stress, what can you see? Plot potential energy and Rg over time. 

2b. Change the "fix indenter" line and try to make nanotube. No need to be perfect, but the closest structure to a perfect nanotube gets a non-grade-related prize.

2c. Instead of an indenter, now use the fix deform command to perform a uniaxial deformation of graphene. Take care of the erate and remap options. What happens after a while? Discuss physically if it makes sense.

## Assignment 3 - Go with the Flow

Transport and adsorption/absorption phenomena are of critical importance for nanomaterials, from batteries to functionalized surfaces. Let's play with them using what you are already familiar with: water and graphene! This assignment goes over the diffusion of water molecules in a graphene-bound nanochannel. Credits to Simon Gravelle for the original script.

### Instructions

3a. Which force field? Is it appropriate? Differences with that of Assignment2? Run the simulation, get msd overall and divided by groups. Also water density and velocity profiles. Careful, big simulation. Use half a node (recommended), plan ahead.


3b. Repeat for different forces pushing water.
