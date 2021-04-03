---
layout: default
---
### G4(MP2) calculation of phenyl radical
Following B3LYP/6-31G(2df,p) geometry optimization and frequency calculations, the SCF calculations in the CCSD(T), MP2 and HF steps are failing. We recommend to converge the corresponding dication (i.e., charge=+2) of the same multiplicity and use the density to restart the SCF calculations for the neutral system. This can be done by including the following options at the end of the input file, pople.inp


'''
 restart_cc  = false
 restart_mp2 = false
 restart_hf3 = false
 restart_hf4 = false
'''

