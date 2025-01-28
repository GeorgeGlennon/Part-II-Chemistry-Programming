# Part-II-Chemistry-Programming
This program calculates the Huckel energies of specific SP2 polyene molecules by solving for the eigenvalues of the huckel matrices generated within the program.
Specifically this program allows for energy calculations for a linear molecule of n atoms, a ring of n atoms or a platonic solid where n = 4,6,8,12 or 20.

# User input
There is a basic user interface that requires direct input form the user to specifc the type of polyene to be solved firstly and then the number of atoms in the ployene, there some safeguards to prevent the program form crashing if the user eneters an invalid input for example a letter when an integer was required.

# Libraries 
There are a number of basic libraries required for this program, apart for these the program is self contained. Specifically:

Counter from collections

Numpy

networkx

While numpy and collections are common libraries, networkx is less common and it is used for creating graphs of nodes and edges between nodes which create a network. There are several graphs contained within the library including those for the [platonic solids](https://networkx.org/documentation/stable/reference/generated/networkx.generators.small.icosahedral_graph.html). Using the 'to_numpy_array' fuction from the networkx library the graph of the platonic solid can be represented in matrix form where connections between nodes (or vertices in this case) are represeneted as a 1, these 1 values correspond to the overlap integral 'b' for adjacent atoms in the huckel model.

# Huckel model and its limitations

'a' and 'b' overlap integral parameters are pre defined as a = 0 and b = -1 in the program, but there is an option for changing this. These can be difficult to calculate which is a drawback of the huckel model, additionally any overlap beyond 1 bond length is omitted, this will be small in comparison to 'b', but it may become important on a marcoscopic scale when looking at the structures of larger molecules. On the otherhand, the Huckel model is very amenable for computation as it only requires simple matrix diagonalisation which is a routine task.

# Program output
For the linear polyene the program will output n energies for the chain of n atoms in the units of 'a' and 'b', the ring and platonic solid will output the energies as well as their specificed degeneracies. For calculation of the degeneracies the matrix eigenvalues had to be rounded to 10 d.p. for comparison as there is some computational error beyond this point that would remove te degeneracy.
