OpenMP_Demos
==============

Samples containing OpenMP C code for parallel programming.  

**dotp.c** and **vadd.c** are traditional serial code for dot product and vector addition respectively.
The other files use variants of OpenMP #pragmas for parallelization.

Test results for my machine Intel Core-i7 3930k hexa-core @ 4.6Ghz:

##Vector Addition

kishan@kishan-vm ~/Desktop/OpenMP $ **./vadd**  
 1 thread(s) took 1.621685 seconds  

kishan@kishan-vm ~/Desktop/OpenMP $ **./vadd_OmpNaive**  
 1 thread(s) took 1.646165 seconds  
 2 thread(s) took 1.755742 seconds  
 3 thread(s) took 1.865191 seconds  
 4 thread(s) took 1.904279 seconds  
 5 thread(s) took 1.924284 seconds  
 6 thread(s) took 1.961957 seconds  
 
kishan@kishan-vm ~/Desktop/OpenMP $ **./vadd_OmpFor**  
 1 thread(s) took 1.573162 seconds  
 2 thread(s) took 1.373527 seconds  
 3 thread(s) took 1.359212 seconds  
 4 thread(s) took 1.392441 seconds  
 5 thread(s) took 1.388034 seconds  
 6 thread(s) took 1.401567 seconds  

Speed boost: **15.7%**

##Dot Product

kishan@kishan-vm ~/Desktop/OpenMP $ **./dotp**  
 1 thread(s) took 2.418260 seconds

kishan@kishan-vm ~/Desktop/OpenMP $ **./dotp_critical**  
 1 thread(s) took 2.418119 seconds  
 2 thread(s) took 1.248885 seconds  
 3 thread(s) took 0.864745 seconds  
 4 thread(s) took 0.678784 seconds  
 5 thread(s) took 0.571757 seconds  
 6 thread(s) took 0.610848 seconds  
 
kishan@kishan-vm ~/Desktop/OpenMP $ **./dotp_reduction**  
 1 thread(s) took 2.420208 seconds  
 2 thread(s) took 1.250492 seconds  
 3 thread(s) took 0.858941 seconds  
 4 thread(s) took 0.696310 seconds  
 5 thread(s) took 0.596546 seconds  
 6 thread(s) took 0.589709 seconds  

Speed boost: **410%**
