.. _G4MP2-Thermo:

Thermochemistry.out
===================

.. currentmodule:: G4MP2

.. code-block:: text

    ==============================================
    |           G4MP2 THERMOCHEMISTRY            |
    ==============================================
     Starting time Thu Nov 19 16:58:26 IST 2020
     
     * Constants and conversion factors *
     
     h      =   6.6260700399999999E-34 J s
     kB     =   1.3806485199999999E-23 J K^-1
     Ry     =   1.0973731568507999E+07 m^-1
     e      =   1.6021764870000000E-19 C
     c      =   2.9979245800000000E+08 m s^-1
     N_avo  =   6.0221417899999999E+23 mol^-1
     
     au2ev  =   2.7211388291762535E+01
     au2kcm =   6.2750957099203276E+02
     au2kjm =   2.6255000450306652E+03
     au2cmi =   2.1947463137015997E+05
     
     * Parameterized for the following atoms  * 
        ____                                    
        |H |                                    
        --------    ---------------------       
        |Li| Be|    |B  |C  |N  |O  |F  |       
        |Na| Mg|    |Al |Si |P  |S  |Cl |       
        |K | Ca|    |Ga |Ge |As |Se |Br |       
        --------    ---------------------       
     
     Optimized atomic coordinates (Angstrom)
           C      0.00000024    -0.00000002     0.00000000
           H      1.07698196    -0.18012947    -0.00002129
           H     -0.52882274    -0.95534548     0.00013221
           H     -0.27411608     0.56763359    -0.89161936
           H     -0.27404603     0.56784158     0.89150844
     
     Unscaled harmonic wavenumbers (cm^-1)
            1323.51
            1323.52
            1323.52
            1541.17
            1541.17
            2998.34
            3110.48
            3110.49
            3110.50
     
     Scaling factor used:          0.9854
     
     * Geometry optimization/frequencies done in             151.62 s
     ** Elapsed time =             152.26 s
     
     * CCSD(T) done in               1.91 s
     ** Elapsed time =             154.18 s
     
     * MP2/L done in                 6.91 s
     ** Elapsed time =             161.11 s
     
     * HF/VTZ done in                3.18 s
     ** Elapsed time =             164.32 s
     
     * HF/VQZ done in               15.46 s
     ** Elapsed time =             179.87 s
     
               Temperature=     298.150000               Pressure=       1.000000
                    E(ZPE)=       0.044157             E(Thermal)=       0.047028
                       HLC=      -0.037888                     SO=       0.000000
                E(CCSD(T))=     -40.354687
                   DE(MP2)=      -0.074398                 DE(HF)=      -0.004870
                G4MP2(0 K)=     -40.427686           G4MP2 Energy=     -40.424814
            G4MP2 Enthalpy=     -40.423870      G4MP2 Free Energy=       0.000000
     
     * G4(MP2) done
     ** Elapsed time =             179.95 s
     
     * G4MP2 for reference atoms*
     
     * ATOM:   C
     
     * Geometry optimization skipped for atom
     
     * CCSD(T) done in               1.99 s
     ** Elapsed time =             182.08 s
     
     * MP2/L done in                 2.27 s
     ** Elapsed time =             184.46 s
     
     * HF/VTZ done in                2.63 s
     ** Elapsed time =             187.17 s
     
     * HF/VQZ done in                3.93 s
     ** Elapsed time =             192.22 s
     
               Temperature=     298.150000               Pressure=       1.000000
                    E(ZPE)=       0.000000             E(Thermal)=       0.001416
                       HLC=      -0.013971                     SO=      -0.000140
                E(CCSD(T))=     -37.751279
                   DE(MP2)=      -0.025410                 DE(HF)=      -0.003476
                G4MP2(0 K)=     -37.794277           G4MP2 Energy=     -37.792861
            G4MP2 Enthalpy=     -37.791917      G4MP2 Free Energy=       0.000000
     
     * G4(MP2) done
     ** Elapsed time =             192.27 s
     
     * ATOM:   H
     
     * Geometry optimization skipped for atom
     
     * CCSD(T) done in               2.12 s
     ** Elapsed time =             194.44 s
     
     * MP2/L done in                 1.49 s
     ** Elapsed time =             195.95 s
     
     * HF/VTZ done in                1.65 s
     ** Elapsed time =             197.63 s
     
     * HF/VQZ done in                1.58 s
     ** Elapsed time =             199.24 s
     
               Temperature=     298.150000               Pressure=       1.000000
                    E(ZPE)=       0.000000             E(Thermal)=       0.001416
                       HLC=      -0.002115                     SO=       0.000000
                E(CCSD(T))=      -0.498233
                   DE(MP2)=      -0.001585                 DE(HF)=      -0.000161
                G4MP2(0 K)=      -0.502094           G4MP2 Energy=      -0.500677
            G4MP2 Enthalpy=      -0.499733      G4MP2 Free Energy=       0.000000
     
     * G4(MP2) done
     ** Elapsed time =             199.26 s
     
     *---------* 
     * SUMMARY * 
     *---------* 
     
     * Atomization energy (Atoms - mol) =                0.62503407 Hartree
     * Atomization energy (Atoms - mol) =               17.00804473 eV
     * Atomization energy (Atoms - mol) =              392.21486014 kcal/mol
     * Atomization energy (Atoms - mol) =             1641.02697481 kj/mol
     * Atomization energy (Atoms - mol), NO HLC =              382.51544470 kcal/mol
     
     ** Elapsed time =             199.26 s
     
     *---------* 
     * SUMMARY * 
     *---------* 
     
     * Heat of formation =               -0.02806423 Hartree
     * Heat of formation =               -0.76366657 eV
     * Heat of formation =              -17.61057079 kcal/mol
     * Heat of formation =              -73.68262820 kj/mol
     * Heat of formation, NO HLC =               -7.91115535 kcal/mol
     
     ** Elapsed time =             199.26 s
     
     Final time Thu Nov 19 17:01:45 IST 2020
    ==============================================
