# Exercise 4 - Potential energy surface

# Required libraries:
-Numpy

-Tabulate

# Program expected functionality
This program takes an inputted potential energy function, that returns absoulte energy for a distance and a derivative of the energy at the inputted distance,
and a .xyz or .txt file that contains some random starting coordinates and outputs the minimised energy, a table of coordinates for the gemoetry of the energy minimum
and a .xyz file containing the minimum geometry.

# Notes when running the program
With this kind of geometry optiminsation we are dealing with a high dimensional potential energy surface (PES) that likely contains many local minimum, finding the global minimum 
isn't necessarily as easy as inputting a random strating geomtry and letting the program optiminse. It is advisable to try multiple random strarting geometries or to be 
judicious selecting a starting geometry. Energy should to compared to general formula for the global minimum energy of an N particle system.

# Avoiding local minima
This is not a trivial task and would require some form of minima hopping algorithm or the addition of stochastic motion to the point on the PES that we are porbing, i.e.
thermal fulctuations. Even with these there is still a risk of converging to one of the deeper local minima, if the modeled temperature is increased then the program 
is more lilely to eascape these local minima but it will never have the exact geometry of the global minimum as there will always be a fluctuation in its structure.

# Minimised structures

<img width="250" alt="image" src="https://github.com/user-attachments/assets/f53180a0-816c-4beb-a69d-372dcbc80b77" />
Minimum structure form the Lennard-Jones potential


<img width="276" alt="image" src="https://github.com/user-attachments/assets/66059153-765d-4d03-90ef-1b6861297f9e" />
Minimum structure from the Morse potential for re/sigma = 1.0


<img width="325" alt="image" src="https://github.com/user-attachments/assets/d9e139f1-150d-4376-92f7-09aa116a1a58" />
Minimum structure from the Morse potential for re/sigma = 1.0


<img width="215" alt="image" src="https://github.com/user-attachments/assets/cbce820b-00ba-4688-ae92-9755b186101e" />
An exampe of a local minimum that the program can converge to, this was from the Lennard_jones potential and had an energy of ~ -15.5 epsilon.




