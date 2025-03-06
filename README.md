# Part-II-Chemistry-Programming Exercise 3
This program simulates the folding of a protein in different concentrations of a denaturant and looks at how the concentrations in the Belousov–Zhabotinsky reaction evolve over time. Both methods use a samll timestep and incerement the respective concentrations over time.

# User input
There is no specific user input for this program, rates and starting concentrations can be changed by editing of the .txt files.

# File requirements
Two .txt files are needed for this program:

Oregonator.txt
Protein folding.txt

If the code is run in colab the files should be uploaded to the session storage, as this is how the file paths have been written.

# Libraries 
There are a four required libraries for this program, three of which are standard:

 numpy

 time

 matplotlib

There is a fourth non-standrad library also required:

 numba

Numba speeds up the code by compiling Python functions into highly optimized machine code using Just-In-Time (JIT) compilation, eliminating interpreter overhead and enabling fast, vectorized numerical operations. Numba has dramatic results, the oregonator took 1319 seconds to run initially, numba allows the same proces in around 1 second.

# Program output
The program outputs two graphs:
![image](https://github.com/user-attachments/assets/4d97ed33-0186-4193-a63c-0d7ba29eb2ee)
This shows how the how the equilibrium level of folding of a protein vaires with the concentration of a denaturant.

![image](https://github.com/user-attachments/assets/5c5fde90-1b2d-4bf5-a3cf-e52db8cc71b2)
This graph shows the evolving concentrations in the Belousov–Zhabotinsky reaction


