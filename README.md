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

# Curve fit 
The lowest energy points on the potential energy surface are fit to the following equation:

<img width="207" alt="image" src="https://github.com/user-attachments/assets/9a62d0cd-0398-4e5a-8173-c96a40a24a43" />


# Program output
The energy surface polts, energy minima conditions, optimal parameters for curve fitting, vibrational frequencies and plots showing the curve fits are all outputted.

# H2O

![image](https://github.com/user-attachments/assets/9b1df75f-f9c5-471a-b211-555fc0c538cd)

![image](https://github.com/user-attachments/assets/2779c6ce-f77a-436f-966b-af9fa65507bb)

![image](https://github.com/user-attachments/assets/284194bd-164d-4670-abc8-403664765dda)


# H2S

![image](https://github.com/user-attachments/assets/cf2f57c8-bf32-4dd9-9f30-ba92c7a553ed)

![image](https://github.com/user-attachments/assets/7a275e90-f6a1-4787-8991-f499a517df01)

![image](https://github.com/user-attachments/assets/a8bf698a-1467-4e95-9c7a-41190f7685f3)




