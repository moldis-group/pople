---
layout: default
---
# Content:   
[1. G4(MP2) enthalpy of formation for the PPE1694 dataset](#g4mp2_ppe)      
[2. G4(MP2)-XP enthalpy of formation for the PPE1694 dataset](#g4mp2xp_ppe)   
[3. G4(MP2) enthalpy of formation for 270 entries in the G3/05 dataset](#g4mp2_g305)      
[4. G4(MP2)-XP enthalpy of formation for 270 entries in the G3/05 dataset](#g4mp2xp_g305)  
[5. G4(MP2)-XP enthalpy of formation for C60](#g4mp2xp_C60)  
  
## <a name="g4mp2_ppe">1. G4MP2 enthalpy of formation for the PPE1694 dataset</a>

[PPE1694_G4MP2.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/PPE1694_G4MP2.zip)

The enclosed file `PPE1694_G4MP2.csv` contain geometries, frequencies and thermochemical energies of all 1694 molecules in the PPE1694 dataset calculated at the G4MP2 level. The file `ATOMS_G4MP2.csv` contains energies for the atoms using which atomization energy and standard formation enthalpy are calculated. Here is a screenshot of the output printed when running the python code enclosed in the zip. 

```
 $ python3.9 calc_hof.py | tee outfile

 #Mol.      Atm. E      Form. H        Exp. form. H [all in kcal/mol]
     1     22.1762     53.3112         51.6000
     2    136.5204    -80.4132        -80.7800
     3    257.4797    -27.7258        -26.4100
     4    225.0425      0.0114          0.0000
     5     35.6105      1.3222          0.0000
     ...
     ...
     ...
  1690   2449.2282     12.4709         12.3000
  1691   2449.0343     12.8907         14.8000
  1692   2111.7479     11.3013         14.2000
  1693   1519.7924    195.8740        198.6000
  1694   1208.4291    -54.2314        -59.6000
```

To print geometry and frequencies, please edit the following lines in `calc_hof.py`

```
  print_geom='false' # Set to 'true' for printing geometries in g4mp2_geom.xyz
  print_freq='false' # Set to 'true' for printing frequencies in g4mp2_freq.dat
```

* * *

## <a name="g4mp2xp_ppe">2. G4MP2-XP enthalpy of formation for the PPE1694 dataset</a>

[PPE1694_G4MP2-XP.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/PPE1694_G4MP2-XP.zip)

The enclosed file `PPE1694_G4MP2-XP.csv` contain geometries, frequencies and thermochemical energies of all 1694 molecules in the PPE1694 dataset calculated at the G4MP2-XP level. The file `ATOMS_G4MP2-XP.csv` contains energies for the atoms using which atomization energy and standard formation enthalpy are calculated. Here is a screenshot of the output printed when running the python code enclosed in the zip

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

To print geometry and frequencies, please edit the following lines in `calc_hof.py`

```
  print_geom='false' # Set to 'true' for printing geometries in g4mp2_geom.xyz
  print_freq='false' # Set to 'true' for printing frequencies in g4mp2_freq.dat
```

* * *

## <a name="g4mp2_g305">3. G4MP2 enthalpy of formation for 270 entries in the G3_05 dataset</a>

[Heat_G305_G4MP2.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/Heat_G305_G4MP2.zip)

* * *

## <a name="g4mp2xp_g305">4. G4MP2-XP enthalpy of formation for 270 entries in the G3_05 dataset</a>

[Heat_G305_G4MP2-XP.zip](https://github.com/moldis-group/pople/blob/main/benchmarks/Heat_G305_G4MP2-XP.zip)

* * *

## <a name="g4mp2xp_C60">5. G4MP2-XP enthalpy of formation for C60</a>

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


