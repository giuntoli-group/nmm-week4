# nmm-week4

Welcome to Classical hell! From this week we forget about electrons and embrace the simpler times when particles were particles and waves were waves. In other words, Molecular Dynamics based on classical equations of motion. This allows our models to reach larger scales of atomistic processes. Week 4 in particular is dedicated to all-atom simulations, the critical importance of MD force fields, and atomistic processes of relevance for nanomaterials.

## Assignment 1

Let's use your first MD assignment to break the ice. Literally! In this assignment you will play with phase changes of water and how they depend on the chosen water model.

### Instructions

1a. Setup and run the simulation in.tip3p_Water (TAKE AND TEST FROM HERE https://docs.lammps.org/Howto_tip3p.html). Varying temperature, determine the crystallization and boiling temperature of the model. Structurally characterize the solid, liquid, and gas phases with snapshots and standard metrics such as density, degree of crystallinity, or radial distribution functions.

1b. Switch to the more complex tip4p model (IN PRINCIPLE HERE https://docs.lammps.org/Howto_tip4p.html, TO TEST. DECIDE HOW MUCH TO GIVE AND HOW MUCH ASK THEM TO FIND). of water and repeat the assignment described in 1a.

1c. (optional, hard!) The water phase diagram has a critical triple point, where solid, liquid, and gas phases coexist! Try to determine it by also varying the pressure of your simulation. (NICE IDEA BUT TO BE TESTED, I HAVE NO IDEA IF IT CAN BE DONE!)

## Assignment 2

Back to graphene, now without perfect periodic lattice conditions! In the real world, graphene is not an infinite  2D plane and graphene sheets tend to form crumpled structures (LINK TO PAPER). Let's see how these structures affect the energy and mechanical stresses.

### Instructions

2a. Run the simulation in.grapheneCrumpling (ADAPT SCRIPT FROM https://www.ericnhahn.com/tutorials/lammps-tutorials/crumpled-graphene). Make a movie of the process and track over time potential energy, radius of gyration, and ... (CHECK PAPERS FOR INTERESTING METRICS). Repeat the simulation to test how these properties are affected by the size of the graphene sheet.

2b. Using the "region", "group", and "add force" commands, add an external force at two edges of your graphene sheets (EDGES MIGHT ALREADY BE DEFINED IN THE SCRIPT, MAYBE WE REMOVE THEM) so that the sheet gets pulled apart. Run the simulations with varying values of external forces. Calculate and report the potential energy of the system as a function of time, and separately the component due to bonded interactions. Visualize the process in Ovito coloring atoms by their stress/atom component.
The simulation should fail if you run it long enough. Explain why it happens, and briefly outline how you would fix it.

2c. (hard, optional) Fix it! Find a solution to complete the simulations of 2b without errors. (TEST OURSELVES/CHECK FOR REACTIVE FORCE FIELDS OR AT LEAST BOND BREAK)

## Assignment 3

Water transport (REPLICATE https://doi.org/10.1063/1.4996210) OR SURFACE ABSORPTION, WHATEVER WE MANAGE TO IMPLEMENT

### Instructions

3a. 

3b. 

## Assignment 4

Batteries: LET'S TRY TO IMPLEMENT THIS https://pubs.rsc.org/en/content/articlelanding/2021/cp/d0cp02851g

### Instructions

4a. 

4b. 
