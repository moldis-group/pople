
# Content:
1. [Basic Input file structure (pople.inp)](#1.-Basic-Input-file-structure-(pople.inp))

### 1. Basic Input file structure (pople.inp)
The simplest input file requires 6 keywords and one or two geometry blocks (Cartesian coordinates in Angstrom). 
* When job_type is 'HF' (heat of formation) or 'AE' (atomization energy), one geometry is required.
* When job_type is 'IP' (ionization energy), 'EA' (electron affinity), 'PA' (proton affinity) or 'BE' (binding energy), two geometries are required. 
* Examples for each job_type are given below

The input file (pople.inp) can also take advanced options for fine-tuning the input for electronic structure calculations. See examples below.

>> NOTE: The keywords in the input should be in lower cases. The corresponding values can be in lower or upper cases.

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
### Basic input for heat of formation of H2O

>> NOTE: Any string followed by a hash ('#') will be treated as a comment and be ignored by the program.
>> The input file can have empty lines.

```
#=== Method and job ==================================================
method_type = g4mp2
job_type    = HF

#=== geometry ========================================================
geom_1
           3              # Number of atoms    
           0           1  # Charge       Multiplicity
 O        0.00000000     0.00000000     0.00000000
 H        0.96854000     0.00000000     0.00000000
 H       -0.22812000     0.00000000    -0.94129000

end_geom

#=== memory and processors ===========================================
maxcore_mb  = 1024       # RAM memory per core in megabytes, 1024 MB is 1 GB
nproc       = 1          # Number of CPU cores 

#=== Paths ===========================================================
openmpi_dir = /apps/openmpi-3.0.0_install/
orca_dir    = /apps/orca_4_1_2_linux_x86-64_shared_openmpi215/

```
