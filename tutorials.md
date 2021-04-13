---
layout: default
---

# Content:
1 [How to run pople?](#1-How-to-run-pople?)  
   > 1.1 [Parallel calculation](#1.2-Parallel-calculation)  

2 [Input/output files](#2.-Input/output-files)      
 
## 1 How to run pople?
>> See [Installation](https://moldis-group.github.io/pople/installation.html) for installing the code. 
>> The input file is a python script (see examples below) which may be executed as 

```python inp.py > out &```

### 1.1 Parallel calculation
The number of processors and memory per core (as an option) have to be specified in the input file. In addition, the library variables for a parallel execution have to be set as follows.

```
  export OMP_NUM_THREADS=1
  export PATH=/apps/openmpi-3.0.0_install/bin:$PATH
  export LD_LIBRARY_PATH=/apps/openmpi-3.0.0_install/lib:$LD_LIBRARY_PATH
```


## 2 Input/output files
The code requires one input python script (say, inp.py) and generates three output files.
* Thermochemistry.out -- Contains a summary of results 
* ORCA_G4MP2.com -- All the input files entering orca calculations are appended 
* ORCA_G4MP2.out -- All the output files resulting from orca calculations are appended

>> NOTE: During multiple executions the outputs are appended.


### 2.1 Basic input
Following is the content of the input script (say 'inp.py') for calculating the standard enthalpy of the H_2 molecule.

```
import os
from pople import calculator as calc
from pople import au2ev

#=== Remove old files
os.system("rm -f ORCA.com ORCA.out Thermochemistry.out input.*")

geom = '''
0  1
H  0.0  0.0  0.0
H  0.0  0.0  0.7
'''

out = calc(code='orca', code_exe='/Library/Orca420/orca', method='g4mp2', xyz=geom)

H=out[2]

print(' Standard enthalpy (at 298.15 K) is ', H,' hartree')
```
