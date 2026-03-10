Recreating figures from the manuscript.

Data to generate the figures from the main text and supplementary information are stored in files Source_Data_Main_Text.zip and Source_Data_Supplementary_Information.zip, respectively. 
Each file contains a folder for each figure in the respective part of the manuscript. 
The folders contain the raw data to recreate each figure as presented in the manuscript. All data is stored as tab delineated text files. 
The Python file gen_figs.py contained within each folder can generate all plots with associated formatting from the raw data. 

Running simulations of active nematics. 

Unzip the NC_Nov_2025.zip file which contains 5 files. 

The files with the prefix T_ are checkpoint files with suitable starting conditions for a simulation. 
The file simulate.cu contains the CUDA sourcecode to simulate the system. It does not rely on any external libraries other than CUDA. 
The file runcode.pl does a number of things. 
1. It will compile the sourcecode into a program named a.out.
2. It will write the simulation parameters into a file named input.dat. The current set of parameters in the runcode.pl file will generate suitable results.
3. It will run the program a.out which generates a number of output files.
4. It will run the Python file Fieldplotter.py which will plot a video of the output. The user can specify whether to plot the orientation field, order parameter, schlieren texture or vorticity field at the beginning of the Fieldplotter.py file.
   
