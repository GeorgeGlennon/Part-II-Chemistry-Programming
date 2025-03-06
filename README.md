# Part-II-Chemistry-Programming Exercise 3
This program simulates the folding of a protein in different concentrations of a denaturant and looks at how the concentrations in the Belousov–Zhabotinsky reaction evolve over time. Both methods use a samll timestep and incerement the respective concentrations over time.

# User input
There is no specific user input for this program, rates and starting concentrations can be changed by editing of the .txt files.

# File requirements
Two .txt files are needed for this program, the code in the program clones this github repo and so they should be successfully retrieved with the correct file paths when all the code is run:

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

# Optimisation

During this task I took a few steps to optimise the code, I pre-computed the exponentials as this saved a significant amount of time and turned out to be the majority of the computational time for each iterative loop for the protein folding. Numpy is written in C and it calls pre-compiled C functions, thus numpy is very fast compared to python and was used when possible. Using classes and functions sped the computational time up ~ 30%. Although numpy is fast for the reasons stated, I found that using numpy arrays as opposed to dictionaires were slower so dictionaires were used as they also allow for easier data management. Based on the thought of numpy being fast beacuse it is pre-compiled I found a library - numba - that pre-compiles the python loop that I am iterating over into machine level code, this proved unbelievably effective and reduced computational times by 3 orders of magnitude.

# Program output
The program outputs two graphs:

![image](https://github.com/user-attachments/assets/4d97ed33-0186-4193-a63c-0d7ba29eb2ee)

This shows how the how the equilibrium level of folding of a protein vaires with the concentration of a denaturant.

![image](https://github.com/user-attachments/assets/5c5fde90-1b2d-4bf5-a3cf-e52db8cc71b2)

This graph shows the evolving concentrations in the Belousov–Zhabotinsky reaction.


