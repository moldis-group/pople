---
layout: default
---

# Content:
1 [Basic input file](#1-Basic-input-file)  
   > 1.1 [Basic input file structure](#1.1-Basic-input-file-structure)  
   > 1.2 [Basic input keywords](#1.2-Basic-input-keywords)  
   > 1.3 [Basic input for heat of formation of H2O](#1.3-Basic-input-for-heat-of-formation-of-H2O)  
   > 1.4 [Basic input for ionization potential of H2O](#1.4-Basic-input-for-ionization-potential-of-H2O)

2 [Example input/output files](#2.-Example-input/output-files)
   > 2.1 [Heat of formation of H2O](#2.1-Heat-of-formation-of-H2O)  
   > 2.2 [Ionization potential of H2O](#2.2-Ionization-potential-of-H2O)
   
3 [More input options](#3-More-input-options)

4 [Advanced input options](#4-Advanced-input-options)
   

## 1 Basic input file
>> The input file must be named as pople.inp

### 1.1 Basic input file structure
The simplest input file requires 6 keywords and one or two geometry blocks (Cartesian coordinates in Angstrom). 
* When job_type is 'HF' (heat of formation) or 'AE' (atomization energy), one geometry is required.
* When job_type is 'IP' (ionization energy), 'EA' (electron affinity), 'PA' (proton affinity) or 'BE' (binding energy), two geometries are required. 
* Examples for each job_type are given below

The input file (pople.inp) can also take advanced options for fine-tuning the input for electronic structure calculations. See examples below.

>> NOTE: The keywords in the input should be in lower cases. The corresponding values can be in all-lower or all-upper cases.

```
method_type = ...
job_type    = ...
geom_1
...

end_geom
maxcore_mb  = ...
nproc       = ...
openmpi_dir = ...
orca_dir    = ...
```
### 1.2 Basic input keywords

```
method_type = ...
Options available are 
* g4mp2 (same as G4MP2)
* g4mp2-xp (same as G4MP2-XP)
```

```
job_type    = ...
Options available are 
* hf (same as HF), for heat of formation
* ae (same as AE), for atomization energy
* ip (same as IP), for ionization potential
* ea (same as EA), for electron affinity
* pa (same as PA), for proton affinity
* be (same as BE), for binding energy
```

>> Example for geometry blocks are provided in the following sections 1.3 and 1.4
```
geom_1
...

end_geom
```

```
maxcore_mb  = ...
* RAM memory per core in megabytes, 1024 stands for 1 GB. The value has to be an integer. 
* example: maxcore_mb  = 1024
```

```
nproc       = ...
* Number of CPU cores. The value has to be an integer. 
* example: nproc = 1
```

```
openmpi_dir = ...
* PATH for openmpi libraries
* example: openmpi_dir = /apps/openmpi-3.0.0_install/
```

```
orca_dir    = ...
* PATH where orca is installed
* example: orca_dir    = /apps/orca_4_1_2_linux_x86-64_shared_openmpi215/ 
```

### 1.3 Basic input for heat of formation of H2O

>> NOTE: Any string followed by a hash ('#') will be treated as a comment and be ignored by the program.
>> The input file can have empty lines.

```
#=== Method and job ==================================================
method_type = g4mp2
job_type    = HF

#=== Geometry ========================================================
geom_1  # The next line cannot be empty
           3              # Number of atoms    
           0           1  # Charge       Multiplicity
 O        0.00000000     0.00000000     0.00000000
 H        0.96854000     0.00000000     0.00000000
 H       -0.22812000     0.00000000    -0.94129000

end_geom

#=== Memory and processors ===========================================
maxcore_mb  = 1024       # RAM memory per core in megabytes, 1024 MB is 1 GB
nproc       = 1          # Number of CPU cores 

#=== Paths ===========================================================
openmpi_dir = /apps/openmpi-3.0.0_install/
orca_dir    = /apps/orca_4_1_2_linux_x86-64_shared_openmpi215/

```

### 1.4 Basic input for ionization potential of H2O
>> NOTE: As noted in [Basic input file](#1.-Basic-input-file)  job_type = IP requires two geometry blocks. The first is for the neutral system and the second is for the cation. Please provide appropriate charge and multiplicity.

```
#=== Method and job ==================================================
method_type = g4mp2
job_type    = IP

#=== Geometry ========================================================
geom_1  # H2O, neutral, the next line cannot be empty
           3                  
           0           1  
 O        0.00000000     0.00000000     0.00000000
 H        0.96854000     0.00000000     0.00000000
 H       -0.22812000     0.00000000    -0.94129000

end_geom

geom_2  # H2O, cation, the next line cannot be empty
           3                  
           1           2 
 O        0.00000000     0.00000000     0.00000000
 H        1.01249000     0.00000000     0.00000000
 H       -0.34159000     0.00000000    -0.95313000

end_geom

#=== Memory and processors ===========================================
maxcore_mb  = 1024       
nproc       = 1          

#=== Paths ===========================================================
openmpi_dir = /apps/openmpi-3.0.0_install/
orca_dir    = /apps/orca_4_1_2_linux_x86-64_shared_openmpi215/

```
