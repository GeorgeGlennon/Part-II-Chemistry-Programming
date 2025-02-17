# Part-II-Chemistry-Programming Exercise 1
This program calculates the Huckel energies of specific SP2 polyene molecules by solving for the eigenvalues of the Huckel matrices generated within the program.
Specifically this program allows for energy calculations for a linear molecule of n atoms, a ring of n atoms or a platonic solid where n = 4,6,8,12,20 or 60.

# User input
There is a basic user interface that requires direct input form the user to specifc the type of polyene to be solved firstly and then the number of atoms in the ployene, there some safeguards to prevent the program form crashing if the user eneters an invalid input for example a letter when an integer was required.

# Libraries 
There are a number of basic libraries required for this program, apart for these the program is self contained. Specifically:

Counter from collections

Numpy

networkx

While numpy and collections are common libraries, networkx is less common and it is used for creating graphs of nodes and edges between nodes which create a network. There are several graphs contained within the library including those for the [platonic solids](https://networkx.org/documentation/stable/reference/generated/networkx.generators.small.icosahedral_graph.html). Using the 'to_numpy_array' fuction from the networkx library the graph of the platonic solid can be represented in matrix form where connections between nodes (or vertices in this case) are represeneted as a 1, these 1 values correspond to the overlap integral 'b' for adjacent atoms in the Huckel model. 

# Buckminsterfullerene problem
The buckminsterfullerene graph isn't available in networkx and so the tyhe matrix was constructed from the [graph of the truncated iscoahedron](https://en.wikipedia.org/wiki/Truncated_icosahedron), I decomposed this into 5 cyclic polyenes and hard-coded the links between the rings into the Huckel matrix. Lila Tazi provided some help with the hard-coding of the bridges between rings.

![image](https://github.com/user-attachments/assets/a0647916-6a3f-4aea-aa56-c9e2c4ce6e7e)


# Huckel model and its limitations

'a' and 'b' overlap integral parameters are pre defined as a = 0 and b = -1 in the program, but there is an option for changing this. These can be difficult to calculate which is a drawback of the Huckel model, additionally any overlap beyond 1 bond length is omitted, this will be small in comparison to 'b', but it may become important on a marcoscopic scale when looking at the structures of larger molecules. On the otherhand, the Huckel model is very amenable for computation as it only requires simple matrix diagonalisation which is a routine task.

# Program output
For the linear polyene the program will output n energies for the chain of n atoms in the units of 'a' and 'b', the ring and platonic solid will output the energies as well as their specificed degeneracies. For calculation of the degeneracies the matrix eigenvalues had to be rounded to 10 d.p. for comparison as there is some computational error beyond this point that would remove te degeneracy.

Linear polyene of n = 10 output:
<img width="862" alt="image" src="https://github.com/user-attachments/assets/1e01da58-2f73-4fc6-9b00-99795359a49a" />

Cyclic polyene of n = 10 output:

<img width="275" alt="image" src="https://github.com/user-attachments/assets/a07931b1-1bb2-4f57-b652-5dec9370c27d" />

Icosahedron output:

<img width="548" alt="image" src="https://github.com/user-attachments/assets/3fb6e4e4-93ba-4bb7-ad9b-8e6ab159a4cd" />


