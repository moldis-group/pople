---
layout: default
---

# Content:
1 [How to run pople?](#1-How-to-run-pople?)  
   > 1.1 [Parallel calculation](#1.2-Parallel-calculation)  

2 [Sample input/output files](#2.-Example-input/output-files)  
   > 2.1 [Heat of formation of H2O](#2.1-Heat-of-formation-of-H2O)    
   > 2.2 [Atomization energy of H2O](#2.2-Atomization-energy-of-H2O)    
   > 2.3 [Ionization potential of H2O](#2.3-Ionization-potential-of-H2O)    
   > 2.4 [Electron affinity of HO](#2.4-Electron-affinity-of-HO)     
   > 2.5 [Proton energy of H2O](#2.5-Proton-energy-of-H2O)     
   > 2.6 [Binding energy of H2O dimer](#2.6-Binding-energy-of-H2O-dimer)    
 
## 1 How to run pople?
>> See [Installation](https://moldis-group.github.io/pople/installation.html) for installing the code. 
>> The input file is a python script (see examples below) when is executed with python3.

### 1.1 Parallel calculation
The number of processors and memory per core (in MB) has to be specified in the input file. In addition, the library variables for a parallel execution have to be set, for example as follows.

  export OMP_NUM_THREADS=1
  export PATH=/apps/openmpi-3.0.0_install/bin:$PATH
  export LD_LIBRARY_PATH=/apps/openmpi-3.0.0_install/lib:$LD_LIBRARY_PATH



## 2 Sample input/output files
The code pople generates three output files. 
* Thermochemistry.out -- Contains a summary of results 
* ORCA_G4MP2.com -- All the input files entering orca calculations are appended 
* ORCA_G4MP2.out -- All the output files resulting from orca calculations are appended


### 2.1 Heat of formation of H2O

[H2O_HF.tar.gz](https://github.com/moldis-group/pople/blob/main/test/H2O_HF.tar.gz)

### 2.2 Atomization energy of H2O

[H2O_AE.tar.gz](https://github.com/moldis-group/pople/blob/main/test/H2O_AE.tar.gz)

### 2.3 Ionization potential of H2O

[H2O_IP.tar.gz](https://github.com/moldis-group/pople/blob/main/test/H2O_IP.tar.gz)

### 2.4 Electron affinity of HO

[HO_EA.tar.gz](https://github.com/moldis-group/pople/blob/main/test/HO_EA.tar.gz)

### 2.5 Proton energy of H2O

[H2O_PA.tar.gz](https://github.com/moldis-group/pople/blob/main/test/H2O_PA.tar.gz)

### 2.6 Binding energy of H2O dimer

[H2O_dimer_BE.tar.gz](https://github.com/moldis-group/pople/blob/main/test/H2O_dimer_BE.tar.gz)
