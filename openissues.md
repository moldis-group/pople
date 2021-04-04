---
layout: default
---
### 1. G4(MP2) calculation of heat-of-formation of phenyl radical 
Following B3LYP/6-31G(2df,p) geometry optimization and frequency calculations, the SCF calculations in the CCSD(T), MP2 and HF steps are failing. We recommend to converge the corresponding dication (i.e., charge=+2) of the same multiplicity and use the density to restart the SCF calculations for the neutral system. This can be done by including the following options at the end of the input file, pople.inp

```
  restart_cc  = true  
  restart_mp2 = true  
  restart_hf3 = true  
  restart_hf4 = true  
```

### 2. G4(MP2)-XP calculation of ionization energy of the diatomic molecule PO
G4(MP2)-XP (method_type = g4mp2-xp) uses  RI-B3LYP for geometry optimization with the GridX9 option. At this geometry, the SCF of this system fails to converge at the subsequent DLPNO-CCSD(T) calculations. While this requires further exploration, the geometry determined using GridX5 options seems to work. This requires the method used for geometry optimization in G4MP2-XP to be reset by including the following options at the end of the input file, pople.inp

```
  method_opt_freq = B3LYP/G Grid5 RIJCOSX def2/J GridX5 
```

### 3. G4(MP2)-XP calculation of ionization energy of the H atom
The cation of H is H+ with no electrons. When method_type is g4mp2, calculations for a zero-electron system is skipped and the energy is set to zero. This has not been enabled for method_type=g4mp2-xp. This requires some modification in the code where the DLPNO-CCSD(T) calculation is requested. Presently, a quick remedy is to include the following options at the end of the input file, pople.inp and to replace the DLPNO-CCSD(T) calculation by a CCSD(T) calculation. Alternatively, one can depend on a g4mp2 calculation for the IP of H atom.

```
 method_ccsdt = CCSD(T) RIJK def2/JK TightPNO 
```
