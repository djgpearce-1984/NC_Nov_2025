Unzip the Code_availabilty file which contains 5 files. 

The files with the prefix T_ are checkpoint files with suitable starting conditions for a simulation. 
The file simulate.cu contains the CUDA sourcecode to simulate the system. It does not rely on any external libraries other than CUDA. 
The file runcode.pl does a number of things. 
1. It will compile the sourcecode into a program named a.out.
2. It will write the simulation parameters into a file named input.dat. The current set of parameters in the runcode.pl file will generate suitable results.
3. It will run the program a.out which generates a number of output files.
4. It will run the Python file Fieldplotter.py which will plot a video of the output. The user can specify whether to plot the orientation field, order parameter, schlieren texture or vorticity field at the beginning of the Fieldplotter.py file.
   
