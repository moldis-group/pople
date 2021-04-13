---
layout: default
---

# Content:
1 [How to run pople?](#1-How-to-run-pople?)  
   > 1.1 [Parallel calculation](#1.2-Parallel-calculation)  

2 [Input/output files](#2.-Input/output-files) 
   > 2.1 [Basic input](#2.1-Basic-input)
   > 2.2 [Composite input] (#2.2-Composite-input)
 
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
from pople import calculator as calc

import os

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

Here is a more detailed explanation of the input.

Every calculation must import the basic function 'calculator' from the pople package.
```
from pople import calculator as calc
```

If the old output files are removed, new output will be appended to existing files. So, it is recommended to remove previous output files as follows
```
import os

os.system("rm -f ORCA.com ORCA.out Thermochemistry.out input.*")
```

Every calculation requires four essential input arguments. The input are processed by 'calculator' using arbitray keyword arguments ([\*\*kwargs](https://www.w3schools.com/python/gloss_python_function_arbitrary_keyword_arguments.asp)) 

The input depends on the four keywords ```code```, ```code_exe```, ```method```, and ```xyz```. For other possible keywords (and their arguments) that can be provided to 'calculator', see [Manual](https://moldis-group.github.io/pople/manual.html).

The geometry block collects the charge, multiplicity and Cartesian coodinates (in Angstroem) of the atom/molecule under consideration. The name of the block (here ```geom``` can be arbitrary. This name has to be made the argument to the keyword ```xyz```.

For performing calculations with orca one must set the ```code``` keyword to ```'orca'```. The path of the orca binary has to provided as the argument to the keyword ```code_exe```. The keyword ```method``` takes as argument the choice of theory, here set to ```'g4mp2'```.



```
geom = '''
0  1
H  0.0  0.0  0.0
H  0.0  0.0  0.7
'''

out = calc(code='orca', code_exe='/Library/Orca420/orca', method='g4mp2', xyz=geom)
```

The function 'calculator' returns the output as a list, which is assigned to the variable ```out```. The first three elements of ```out``` are internal energy at 0 Kelvin, internal energy at T (set to 298.5) Kelvin, and enthalpy at 298.15 K.

```
H=out[2]

print(' Standard enthalpy (at 298.15 K) is ', H,' hartree')
```

### 2.2 Composite input
Following is the input for calculating the adiabatic ionization energy of the water molecule. The calculation returns zero-Kelvin internal energies, $U_0$, of the neutral and cationic species. Ionization energy is calculated as `$P=U_0^{cation}-U_0^{neutral}$`.
