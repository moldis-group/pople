---
layout: default
---

# Content:
1 [How to run pople?](#1-How-to-run-pople?)  
   > 1.1 [Interactive mode](#1.1-Interactive-mode)  
   > 1.2 [Batch mode](#1.2-Batch-mode)  

2 [Sample input/output files](#2.-Example-input/output-files)
   > 2.1 [Heat of formation of H2O](#2.1-Heat-of-formation-of-H2O)  
   > 2.2 [Ionization potential of H2O](#2.2-Ionization-potential-of-H2O)
 
## 1 How to run pople?
>> See [Installation](#https://moldis-group.github.io/pople/installation.html) for installing the code. 
>> Ensure that an input file (pople.inp) is present in the working directory (see examples below) a calculation can be 
performed either interactively on a python terminal or one can use a script.

### 1.1 Interactive mode
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
