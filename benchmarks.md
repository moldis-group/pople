---
layout: default
---
# Content:
1 [G4(MP2) enthalpy of formation for the PPE1694 dataset](#1-g4(MP2)-enthalpy-of-formation-for-the-PPE1694-dataset)    
2 [G4(MP2)-XP enthalpy of formation for the PPE1694 dataset](#2-g4(MP2)-XP-enthalpy-of-formation-for-the-PPE1694-dataset)      
3 [G4(MP2)-XP enthalpy of formation for C60](#3-g4(MP2)-XP enthalpy of formation for C60)  
  
## 1 G4(MP2) enthalpy of formation for the PPE1694 dataset

[PPE1694_G4MP2.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/PPE1694_G4MP2.zip)

* * *

## 2 G4(MP2)-XP enthalpy of formation for the PPE1694 dataset

[PPE1694_G4MP2-XP.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/PPE1694_G4MP2-XP.zip)

Here is a screenshot of the output printed when running the python code enclosed in the zip

```
 $ python3.9 calc_hof.py | tee outfile

 #Mol.      Atm. E      Form. H        Exp. form. H [all in kcal/mol]
     1     22.2452     53.2421         51.6000
     2    136.7751    -80.6680        -80.7800
     3    258.0407    -28.2868        -26.4100
     4    225.3437     -0.2898          0.0000
     5     36.0511      0.8817          0.0000
     ...
     ...
     ...
  1690   2450.5240     11.1751         12.3000
  1691   2450.3301     11.5949         14.8000
  1692   2112.8919     10.1574         14.2000
  1693   1520.6502    195.0162        198.6000
  1694   1209.9533    -55.7556        -59.6000

```

* * *

## 3 G4(MP2)-XP enthalpy of formation for C60
The python code contains G4(MP2)-XP level geometry, harmonic frequencies, energies from CCSD(T), HF, and MP2 methods, and demonstrates how the atomization energy and standard formation enthalpy of buckminsterfullerene, C60 can be calculated.

[C60_enthalpy.py](https://github.com/moldis-group/pople/blob/main/benchmarks/C60_enthalpy.py)

After installing the pople code, running the above `C60_enthalpy.py` with python returns the following output

```
Atomization energy is              15.2943 hartree    
Atomization energy is            9597.3248 kcal/mol    

ZPVE is                           230.0659 kcal/mol    

             HOF_atoms(C)       HOF molecule  [all in kcal/mol]
             169.9800            600.4915
             170.0270            603.3115
             170.1100            608.2915
```

* * *


