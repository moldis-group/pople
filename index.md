---
layout: default
---

## The Code
**Pople** is a toolkit written in Python to perform _ab initio_ thermochemistry calculations. The present version, [pople-1.0.1](https://github.com/moldis-group/Pople), supports G4(MP2) calculations using the [ORCA quantum chemistry program package](https://www.faccts.de/orca/) for all the electronic structure calculations. Pople enables customizing every step in a G4(MP2) calculation, facilitating users to explore effects various theories and basis sets can have on the speed and accuracy. G4(MP2)-XP is a variant based on DLPNO-CCSD(T), RI-MP2, RI-DFT and RI-HF approximations permitting thermochemistry calculations of molecules as large as buckminsterfullerene. 

* * *

## Calculations supported
1. Enthalpy of formation
2. Atomization energy 
3. Ionization Potential (vertical and adiabatic)
4. Electron Affinity (vertical and adiabatic)
5. Proton Affinity
6. Intermolecular Binding Energy

* * *

## Additional options
1. Calculations can also be performed in a _single point_ fashion with a user provided initial geometry and harmonic frequencies.
2. Empirical parameters such as reference standard enthalpies of atoms and higher-level correction (HLC) constants can be modified.
 
* * *

## Upcoming features
1. ccCA calculations
2. Entropy and Free Energy calculations
 
* * *
