---
layout: default
---

# Content:
[1. Running the code](#running)      
   >[1.1 Parallel calculation](#parallel)  
       
[2. Files](#files)       

[3. Simple calculation](#simple_calc)          

[4. Composite input](#comp_input)         

[5. Advanced calculations](#adv_calc)          
   >[5.1 Frozen geometry calculation](#frozen_geom)               
   >[5.2 Atomization energy](#atm_energy)          
   >[5.3 Enthalpy of formation](#form_enthalpy)               
   >[5.4 Multiple calculations](#multip)           
 
## <a name="running">1. Running the code</a>
>> See [Installation](https://moldis-group.github.io/pople/installation.html) for installing the code. 
>> The input file is a python script (see examples below) which may be executed as 

```python3 inp.py > out &```

### <a name="parallel">1.1 Parallel calculation</a>
The number of processors and memory per core (as an option) have to be specified in the input file. In addition, the library variables for a parallel execution have to be set as follows.

```
export OMP_NUM_THREADS=1
export PATH=/apps/openmpi-3.0.0_install/bin:$PATH
export LD_LIBRARY_PATH=/apps/openmpi-3.0.0_install/lib:$LD_LIBRARY_PATH
```

* * *

## <a name="files">2. Files</a>
The code requires one input python script (say, inp.py) and generates three output files.
* Thermochemistry.out -- Contains a summary of results 
* ORCA_G4MP2.com -- All the input files entering orca calculations are appended 
* ORCA_G4MP2.out -- All the output files resulting from orca calculations are appended

>> NOTE: During multiple executions the outputs are appended.

* * *

## <a name="simple_calc">3. Simple calculation</a>
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
exe='/home/Lib/ORCA_420/orca'
out = calc(code='orca', code_exe=exe, method='g4mp2', xyz=geom)

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
exe='/home/Lib/ORCA_420/orca'
out = calc(code='orca', code_exe=exe, method='g4mp2', xyz=geom)
```

The function 'calculator' returns the output as a list, which is assigned to the variable ```out```. The first three elements of ```out``` are internal energy at 0 Kelvin, internal energy at T (set to 298.5) Kelvin, and enthalpy at 298.15 K.

```
H=out[2]

print(' Standard enthalpy (at 298.15 K) is ', H,' hartree')
```

* * *

### <a name="comp_input">4. Composite input</a>
The test jobs `test_002_ionizationenergy_H2O`, `test_004_electronaffinity_Cl`, `test_005_protonaffinity_NH3`, and `test_006_bindingenergy_HFdimer` contain input/output files for composite calculations.

Following is the input for calculating the adiabatic ionization energy of the water molecule from `test_002_ionizationenergy_H2O`. The calculation returns zero-Kelvin internal energies, `U0`, of the neutral and cationic species. Ionization energy is calculated as `IP = U0_cation - U0_neutral`.

```
import os
from pople import calculator as calc
from pople import au2ev

#=== Remove old files
os.system("rm -f ORCA.com ORCA.out Thermochemistry.out input.*")

#=== Common inputs
exe='/home/Lib/ORCA_420/orca'

#=== neutral H2O
geom = '''
0  1
O      0.0         0.0      0.0
H      0.96854     0.0      0.0
H     -0.22812     0.0     -0.94129
'''

out = calc(code='orca', code_exe=exe, method='g4mp2', xyz=geom)
U0_neutral=out[0]

#=== cation H2O
geom = '''
+1  2
O      0.0         0.0      0.0
H      1.01249     0.0      0.0
H     -0.34159     0.0     -0.95313
'''

out = calc(code='orca', code_exe=exe, method='g4mp2', xyz=geom)
U0_cation=out[0]

print(' Ionization potential of H2O is ', (U0_cation-U0_neutral)*au2ev, ' eV')
```

This example shows how to use unit conversion factors coded up in the package. 
```
from pople import au2ev
...
print(' Ionization potential of H2O is ', (U0_cation-U0_neutral)*au2ev, ' eV')

```

Water molecule's IP calculated with the `method='g4mp2'` turns out to be `12.5908 eV`, which is in very good agreement with the experimental value `12.619 eV`.

* * *
  
## <a name="adv_calc">5. Advanced calculations</a>

### <a name="frozen_geom">5.1. Frozen geometry calculation</a>
 
The test job `test_003_enthalpy_H2_frozen_geom` shows how an optimized geometry and harmonic frequencies can be provided externally and a `g4mp2` enthalpy calculation can be performed in a single-point fashion. This requires the keyword `frozengeom` to be set to the value `'true'`, and harmonic frequencies (in cm^-1) are provided using a frequency block named here as `freq` and made as the argument to the keyword `freqcmi`.
 
```
geom = '''
0  1
H      0.00000000     0.00000000    -0.02139720
H      0.00000000     0.00000000     0.72139720
'''

freq='''
    4465.2000
'''

program='orca'
exe='/home/Lib/ORCA_420/orca'

out = calc(code=program, code_exe=exe, method='g4mp2', xyz=geom, frozengeom='true', freqcmi=freq)
```

### <a name="atm_energy">5.2. Atomization energy</a>
 
The test jobs `test_007_atomizationenergy_CH4` shows how to calculate atomization energy of CH4. Zero-Kelvin internal energy, `U0`, of the molecule and constitutent atoms are calculated, and atomization energy is determined as the reaction energy `Atm. Energy = U0_atoms - U0_molecule`. 
 
A unique list of the constitutent atoms and their multiplicities are collected using
```
from pople import getatoms, uniqatoms, getmultip

atoms = getatoms(geom)  # List of atoms
uniq = uniqatoms(atoms) # Unique atom data
N_ua = uniq["N_ua"]       # No. of unique atoms
ua   = uniq["uniq_sym"]   # unique atoms
ua_N = uniq["uan"]        # unique atom frequencies

multip=getmultip(ua)    # Multiplicities of unique atoms
```
 
Total internal energy of all the atoms is calculated using
```
exe='/home/Lib/ORCA_420/orca'
U0_atoms_total=0        # Sum of internal energy (at 0 K) of atoms
for i_ua in range(N_ua):

    print(' Atom ', ua[i_ua], ' with multiplicity ', multip[i_ua])

    #=== calculate for each unique atom
    geom = (f'''0  {multip[i_ua]} 
{ua[i_ua]}  0.0 0.0 0.0 ''')

    out = calc(code='orca', code_exe=exe, method='g4mp2', xyz=geom)
    U0=out[0]

    U0_atoms_total = U0_atoms_total + U0 * ua_N[i_ua]
```

G4MP2-level atomization energy of CH4 can be calculated as
```
print( ' Atomization energy of CH4 is ', (U0_atoms_total-U0_mol) * au2kcm, ' kcal/mol')
```
which results in a value of `392.2148` kcal/mol which is in good agreement with the experimental value `397.94` kcal/mol.

### <a name="form_enthalpy">5.3. Enthalpy of formation</a>
 
The test jobs `test_008_formationenthalpy_CH4` shows how to calculate the standard formation enthalpy of CH4 using previously determined atomization energy.
 
```
import os
from pople import au2kcm
from pople import getatoms, uniqatoms, getmultip
from pople import HOF_atoms, dH_atoms

#=== CH4 
geom = '''
 0  1
 C        0.00000000     0.00000000     0.00000000
 H        1.09336000     0.00000000     0.00000000
 H       -0.36445000     0.00000000    -1.03083000
 H       -0.36445000    -0.97188000     0.34361000
 H       -0.36445000     0.97188000     0.34361000
'''

#=== from test_007_atomizationenergy_CH4/Thermochemistry.out 
HTmol = -40.42387018
U0mol = -40.42768573

#=== from test_007_atomizationenergy_CH4/out
U0molAE = 392.2148180200836 / au2kcm


#=== Atoms
atoms = getatoms(geom)  # List of atoms

uniq = uniqatoms(atoms) # Unique atom data

N_ua = uniq["N_ua"]       # No. of unique atoms
ua   = uniq["uniq_sym"]   # unique atoms
ua_N = uniq["uan"]        # unique atom frequencies

multip=getmultip(ua)    # Multiplicities of unique atoms


#=== Enthalpy of formation
HT_form = HTmol - U0mol - U0molAE

for i_ua in range(N_ua):

   HOF_0K     = HOF_atoms(ua[i_ua])
   dH_298K_0K = dH_atoms(ua[i_ua])

   HT_form = HT_form + ua_N[i_ua] * ( HOF_0K - dH_298K_0K )

print( ' Standard formation enthalpy (at 298.15 K) of CH4 is ', HT_form * au2kcm, ' kcal/mol')
```
 
### <a name="multip">5.4. Multiple calculations</a>
 
The test job `test_009_methods_comparison_CH4` shows how to perform calculations with two methods using a for loop, compare the results in a table. 
 
The test job `test_010_methods_comparison_C6H6_parallel` presents similar results for the benzene molecule using 8 processors.

A comparison of the results (included as comments at the bottom of the inp.py files in both directories) shows that the accuracy of g4mp2-xp is marginally better compared to g4mp2. The speed in g4mp2-xp, due to DLPNO and RI approxations is noticeable for the larger molecule C6H6.

 
```
Method              Atm. energy (kcal/mol)    Form. enthalpy (kcal/mol)   Time (sec) 

CH4

g4mp2                           392.2148            -17.6105               122.4531
g4mp2-xp                        392.2910            -17.6868               191.8379
Exp.                            397.94              -17.90

C6H6

g4mp2                          1306.6164             18.8675              1264.3296
g4mp2-xp                       1305.8573             19.6262               796.0674
Exp.                                                 19.70
```

* * *
