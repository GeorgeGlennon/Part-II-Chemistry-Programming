# Part-II-Chemistry-Programming - Exercise 2
This program takes a set of gaussian output files, extracts bond lengths, angles and molecular energies for H2O or H2S. The program then plots surface energy plots for the selected molecule, and curve fits to the lowest energy points to calculate the symmetric strecth and bending frequencies.

# User input
The only user input required in the selection of H2O or H2S for analysis.

# File requirements
The relevant files can be obtained with this code:
<img width="452" alt="image" src="https://github.com/user-attachments/assets/27af74ef-8d21-481c-9d9f-97db1c106319" />


# Libraries 
There are a number of basic libraries required for this program, apart for these the program is self contained. Specifically:

matplotlib

numpy

os

curve_fit from scipy.optimize

The os library allows for interaction with the operating system running the code and for reading and manipulation of files stored on the system.


# Program output
The energy surface polts, energy minima conditions, optimal parameters for curve fitting, vibrational frequencies and plots showing the curve fits are all outputted.

Potential energy surface of H2O:
<img width="862" alt="image" src="https://github.com/user-attachments/assets/1e01da58-2f73-4fc6-9b00-99795359a49a" />

Poetntial energy surface of H2S:
![image](https://github.com/user-attachments/assets/cf2f57c8-bf32-4dd9-9f30-ba92c7a553ed)



