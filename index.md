---
layout: default
---

## The Code
**Pople** is an opensource toolkit written in Python to perform _ab initio_ thermochemistry calculations. The present version, [pople-21.4](https://github.com/moldis-group/Pople), supports G4(MP2) calculations using the [ORCA quantum chemistry program package](https://www.faccts.de/orca/) for all the electronic structure calculations. The releases will be semiannual using the year and month of the release as the version number. Pople enables customizing every step in a G4(MP2) calculation, facilitating users to explore effects various theories and basis sets can have on the speed and accuracy. G4(MP2)-XP is a variant based on DLPNO-CCSD(T), RI-MP2, RI-DFT and RI-HF approximations permitting thermochemistry calculations of molecules as large as buckminsterfullerene. 

The Pople project follows the computational chemistry software design principles of the [Psi4NumPy project](https://github.com/psi4/psi4numpy) and provides an interactive framework for thermochemistry calculations.

* * *

## Calculations supported
The input file is a programmable python script. This facilitates the user to design inputs to perform composite tasks. The tutorials provide example input/output files for the following job types: enthalpy of formation, atomization energy, ionization energy, electron affinity, proton affinity, intermolecular binding energy

Calculations can also be performed in a _single point_ fashion with a user provided initial geometry and harmonic frequencies. Further, empirical parameters such as reference standard enthalpies of atoms and higher-level correction (HLC) constants can be modified.
 
* * *


