---
layout: default
---

# Content:
1 [How to run pople?](#1-How-to-run-pople?)  
   > 1.1 [Interactive mode](#1.1-Interactive-mode)  
   > 1.2 [Batch mode](#1.2-Batch-mode)  

2 [Sample input/output files](#2.-Example-input/output-files)  
   > 2.1 [Heat of formation of H2O](#2.1-Heat-of-formation-of-H2O)    
   > 2.2 [Atomization energy of H2O](#2.2-Atomization-energy-of-H2O)    
   > 2.3 [Ionization potential of H2O](#2.3-Ionization-potential-of-H2O)    
   > 2.4 [Electron affinity of HO](#2.4-Electron-affinity-of-HO)     
   > 2.5 [Proton energy of H2O](#2.5-Proton-energy-of-H2O)     
   > 2.6 [Binding energy of H2O dimer](#2.6-Binding-energy-of-H2O-dimer)    
 
## 1 How to run pople?
>> See [Installation](#https://moldis-group.github.io/pople/installation.html) for installing the code. 
>> Ensure that an input file (pople.inp) is present in the working directory (see examples below) a calculation can be 
performed either interactively on a python terminal or one can use a script.

### 1.1 Interactive mode
Interactive mode is typically recommded for small systems. Prepare pople.inp in the workding direct, open a python3 terminal and type the following lines
```
import pople
value=pople.run()
```

### 1.2 Batch mode
All the python commands can be included in a script, say run.py and the commands can be executed as python3 run.py

## 2 Sample input/output files
The code pople generates three output files. 
* Thermochemistry.out -- Contains a summary of results 
* ORCA_G4MP2.com -- All the input files entering orca calculations are appended 
* ORCA_G4MP2.out -- All the output files resulting from orca calculations are appended


### 2.1 Heat of formation of H2O

[H2O_HF.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/H2O_HF.tar.gz)

### 2.2 Atomization energy of H2O

[H2O_AE.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/H2O_AE.tar.gz)

### 2.3 Ionization potential of H2O

[H2O_IP.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/H2O_IP.tar.gz)

### 2.4 Electron affinity of HO

[HO_EA.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/HO_EA.tar.gz)

### 2.5 Proton energy of H2O

[H2O_PA.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/H2O_PA.tar.gz)

### 2.6 Binding energy of H2O dimer

[H2O_dimer_BE.tar.gz](#https://github.com/moldis-group/pople/blob/main/test/H2O_dimer_BE.tar.gz)
