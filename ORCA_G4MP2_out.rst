.. _G4MP2-out:

ORCA_G4MP2.out
==============

.. currentmodule:: G4MP2

.. code-block:: text
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: Geometry Optimization
              ===> : Switching off AutoStart
                     For restart on a previous wavefunction, please use MOREAD
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> !   B3LYP/G Grid7 Printbasis  TightOpt  Freq
            |  2> * xyz   0  1
            |  3> C     0.00000000     0.00000000     0.00000000
            |  4> H     1.09336000     0.00000000     0.00000000
            |  5> H    -0.36445000     0.00000000    -1.03083000
            |  6> H    -0.36445000    -0.97188000     0.34361000
            |  7> H    -0.36445000     0.97188000     0.34361000
            |  8> *
            |  9> %MaxCore    64000
            | 10> %scf
            | 11>   MaxIter 500
            | 12>   Convergence VeryTight
            | 13> end
            | 14> %pal nprocs     1
            | 15> end
            | 16> %method
            | 17>   IntAcc 7.0
            | 18> end
            | 19> %geom
            | 20>   Calc_Hess true
            | 21>   Recalc_Hess        5
            | 22> end
            | 23> %freq  Temp  273.15, 298.15
            | 24> end
            | 25> %basis
            | 26>      NewGTO   C
            | 27>      S  6
            | 28>      1            3047.52488000               0.00183474
            | 29>      2             457.36951800               0.01403732
            | 30>      3             103.94868500               0.06884262
            | 31>      4              29.21015530               0.23218444
            | 32>      5               9.28666296               0.46794135
            | 33>      6               3.16392696               0.36231199
            | 34>      S  3
            | 35>      1               7.86827235              -0.11933242
            | 36>      2               1.88128854              -0.16085415
            | 37>      3               0.54424926               1.14345644
            | 38>      P  3
            | 39>      1               7.86827235               0.06899907
            | 40>      2               1.88128854               0.31642396
            | 41>      3               0.54424926               0.74430829
            | 42>      S  1
            | 43>      1               0.16871448               1.00000000
            | 44>      P  1
            | 45>      1               0.16871448               1.00000000
            | 46>      D  1
            | 47>      1               1.60000000               1.00000000
            | 48>      D  1
            | 49>      1               0.40000000               1.00000000
            | 50>      F  1
            | 51>      1               0.80000000               1.00000000
            | 52>      end
            | 53> end
            | 54> %basis
            | 55>      NewGTO   H
            | 56>      S  3
            | 57>      1              18.73113696               0.03349460
            | 58>      2               2.82539437               0.23472695
            | 59>      3               0.64012169               0.81375733
            | 60>      S  1
            | 61>      1               0.16127776               1.00000000
            | 62>      P  1
            | 63>      1               1.10000000               1.00000000
            | 64>      end
            | 65> end
            | 66> 
            | 67>                          ****END OF INPUT****
            ================================================================================
            
                                   *****************************
                                   * Geometry Optimization Run *
                                   *****************************
            
            Geometry optimization settings:
            Update method            Update   .... BFGS
            Choice of coordinates    CoordSys .... Z-matrix Internals
            Initial Hessian          InHess   .... Almoef's Model
            
            Convergence Tolerances:
            Energy Change            TolE     ....  1.0000e-06 Eh
            Max. Gradient            TolMAXG  ....  1.0000e-04 Eh/bohr
            RMS Gradient             TolRMSG  ....  3.0000e-05 Eh/bohr
            Max. Displacement        TolMAXD  ....  1.0000e-03 bohr
            RMS Displacement         TolRMSD  ....  6.0000e-04 bohr
            Strict Convergence                ....  False
            ------------------------------------------------------------------------------
                                    ORCA OPTIMIZATION COORDINATE SETUP
            ------------------------------------------------------------------------------
            
            The optimization will be done in new redundant internal coordinates
            Making redundant internal coordinates   ...  (new redundants) done
            Evaluating the initial hessian          ...  (Is done on the fly) done
            Evaluating the coordinates              ...  done
            Calculating the B-matrix                .... done
            Calculating the G-matrix                .... done
            Diagonalizing the G-matrix              .... done
            The first mode is                       ....    1
            The number of degrees of freedom        ....    9
            
                -----------------------------------------------------------------
                                Redundant Internal Coordinates
            
            
                -----------------------------------------------------------------
                     Definition                    Initial Value    d2E/dq (diagonal element)
                -----------------------------------------------------------------
                  1. B(H   1,C   0)                  1.0934         0.000000   
                  2. B(H   2,C   0)                  1.0934         0.000000   
                  3. B(H   3,C   0)                  1.0934         0.000000   
                  4. B(H   4,C   0)                  1.0934         0.000000   
                  5. A(H   1,C   0,H   3)          109.4710         0.000000   
                  6. A(H   2,C   0,H   3)          100.6720         0.000000   
                  7. A(H   1,C   0,H   4)          109.4710         0.000000   
                  8. A(H   2,C   0,H   4)          100.6720         0.000000   
                  9. A(H   3,C   0,H   4)          125.4683         0.000000   
                 10. A(H   1,C   0,H   2)          109.4711         0.000000   
                -----------------------------------------------------------------
            
            Number of atoms                         .... 5
            Number of degrees of freedom            .... 10
            
                     *************************************************************
                     *                GEOMETRY OPTIMIZATION CYCLE   1            *
                     *************************************************************
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000    0.000000    0.000000
              H      1.093360    0.000000    0.000000
              H     -0.364450    0.000000   -1.030830
              H     -0.364450   -0.971880    0.343610
              H     -0.364450    0.971880    0.343610
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000    0.000000    0.000000
               1 H     1.0000    0     1.008    2.066151    0.000000    0.000000
               2 H     1.0000    0     1.008   -0.688711    0.000000   -1.947986
               3 H     1.0000    0     1.008   -0.688711   -1.836587    0.649329
               4 H     1.0000    0     1.008   -0.688711    1.836587    0.649329
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.093360000000     0.00000000     0.00000000
             H      1   2   0     1.093359177672   109.47105060     0.00000000
             H      1   2   3     1.093362871603   109.47098216   109.47114364
             H      1   2   3     1.093362871603   109.47098216   250.52885636
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.066150965784     0.00000000     0.00000000
             H      1   2   0     2.066149411810   109.47105060     0.00000000
             H      1   2   3     2.066156392327   109.47098216   109.47114364
             H      1   2   3     2.066156392327   109.47098216   250.52885636
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 10s4p2d1f contracted to 3s2p2d1f pattern {631/31/11/1}
             Group   2 Type H   : 4s1p contracted to 2s1p pattern {31/1}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      18.7311369600      0.0334946000
               2       2.8253943700      0.2347269502
               3       0.6401216900      0.8137573307
             S 1 
               1       0.1612777600      1.0000000000
             P 1 
               1       1.1000000000      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    3047.5248800000      0.0018347400
               2     457.3695180000      0.0140373200
               3     103.9486850000      0.0688426199
               4      29.2101553000      0.2321844397
               5       9.2866629600      0.4679413494
               6       3.1639269600      0.3623119895
             S 3 
               1       7.8682723500     -0.1193324197
               2       1.8812885400     -0.1608541495
               3       0.5442492600      1.1434564368
             P 3 
               1       7.8682723500      0.0689990700
               2       1.8812885400      0.3164239600
               3       0.5442492600      0.7443082900
             S 1 
               1       0.1687144800      1.0000000000
             P 1 
               1       0.1687144800      1.0000000000
             D 1 
               1       1.6000000000      1.0000000000
             D 1 
               1       0.4000000000      1.0000000000
             F 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   37
             # of primitive gaussian functions       ...   67
             # of contracted shells                  ...   20
             # of contracted basis functions         ...   46
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Density Functional     Method          .... DFT(GTOs)
             Exchange Functional    Exchange        .... B88
               X-Alpha parameter    XAlpha          ....  0.666667
               Becke's b parameter  XBeta           ....  0.004200
             Correlation Functional Correlation     .... LYP
             LDA part of GGA corr.  LDAOpt          .... VWN-3
             Gradients option       PostSCFGGA      .... off
             Hybrid DFT is turned on
               Fraction HF Exchange ScalHFX         ....  0.200000
               Scaling of DF-GGA-X  ScalDFX         ....  0.720000
               Scaling of DF-GGA-C  ScalDFC         ....  0.810000
               Scaling of DF-LDA-C  ScalLDAC        ....  1.000000
               Perturbative correction              ....  0.000000
               Density functional embedding theory  .... OFF
               NL short-range parameter             ....  4.800000
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....   46
             Nuclear Repulsion      ENuc            ....     13.4059055337 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.533e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-770
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ... 134918 (   0.0 sec)
            # of grid points (after weights+screening)   ... 130961 (   0.1 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    3.5 sec
            Reduced shell lists constructed in    3.7 sec
            
            Total number of grid points                  ...   130961
            Total number of batches                      ...     2049
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...    26192
            Average number of shells per batch           ...    16.42 (82.10%)
            Average number of basis functions per batch  ...    37.29 (81.07%)
            Average number of large shells per batch     ...    15.21 (92.63%)
            Average number of large basis fcns per batch ...    34.44 (92.35%)
            Maximum spatial batch extension              ...  19.51, 16.67, 19.77 au
            Average spatial batch extension              ...   1.78,  1.70,  1.76 au
            
            Time for grid setup =    3.826 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.4 sec)
              promolecular density results
                 # of electrons  =      9.998041761
                 EX              =     -6.306106352
                 EC              =     -0.288501622
                 EX+EC           =     -6.594607974
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   4.3 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.4367198750   0.000000000000 0.06861182  0.00363062  0.2079733 0.7000
              1    -40.4735518774  -0.036832002366 0.04666408  0.00269945  0.1073215 0.7000
                                           ***Turning on DIIS***
              2    -40.4884553168  -0.014903439400 0.07170398  0.00448563  0.0396585 0.0000
              3    -40.5080755086  -0.019620191809 0.03030419  0.00173585  0.0596812 0.0000
              4    -40.5145279895  -0.006452480932 0.00797704  0.00056767  0.0149627 0.0000
              5    -40.5149640407  -0.000436051162 0.00275842  0.00019070  0.0036255 0.0000
                                  *** Initiating the SOSCF procedure ***
                                       *** Shutting down DIIS ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              6    -40.51499374  -0.0000297010  0.000359  0.000359  0.001323  0.000091
                           *** Restarting incremental Fock matrix formation ***
              7    -40.51499592  -0.0000021771  0.000035  0.000044  0.000091  0.000005
              8    -40.51499592   0.0000000004  0.000030  0.000027  0.000052  0.000003
                              ***Gradient check signals convergence***
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   9 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.51499593 Eh           -1102.46909 eV
            
            Components:
            Nuclear Repulsion  :           13.40590553 Eh             364.79324 eV
            Electronic Energy  :          -53.92090146 Eh           -1467.26232 eV
            One Electron Energy:          -79.78719486 Eh           -2171.11995 eV
            Two Electron Energy:           25.86629340 Eh             703.85763 eV
            
            Virial components:
            Potential Energy   :          -80.66654449 Eh           -2195.04827 eV
            Kinetic Energy     :           40.15154856 Eh            1092.57918 eV
            Virial Ratio       :            2.00905189
            
            
            DFT components:
            N(Alpha)           :        5.000000014630 electrons
            N(Beta)            :        5.000000014630 electrons
            N(Total)           :       10.000000029259 electrons
            E(X)               :       -5.205795031346 Eh       
            E(C)               :       -0.387448953370 Eh       
            E(XC)              :       -5.593243984716 Eh       
            DFET-embed. en.    :        0.000000000000 Eh       
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -9.9318e-09  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    6.3075e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    5.9331e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    3.9633e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    7.5250e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -10.164821      -276.5988 
               1   2.0000      -0.691245       -18.8097 
               2   2.0000      -0.411077       -11.1860 
               3   2.0000      -0.391454       -10.6520 
               4   2.0000      -0.356752        -9.7077 
               5   0.0000       0.114965         3.1283 
               6   0.0000       0.157139         4.2760 
               7   0.0000       0.178437         4.8555 
               8   0.0000       0.186484         5.0745 
               9   0.0000       0.499817        13.6007 
              10   0.0000       0.511852        13.9282 
              11   0.0000       0.525296        14.2940 
              12   0.0000       0.728035        19.8108 
              13   0.0000       0.754144        20.5213 
              14   0.0000       0.757241        20.6056 
              15   0.0000       0.760142        20.6845 
              16   0.0000       0.777522        21.1574 
              17   0.0000       0.916359        24.9354 
              18   0.0000       1.125244        30.6194 
              19   0.0000       1.539786        41.8997 
              20   0.0000       1.684479        45.8370 
              21   0.0000       1.700663        46.2774 
              22   0.0000       1.962882        53.4127 
              23   0.0000       1.988429        54.1079 
              24   0.0000       2.082860        56.6775 
              25   0.0000       2.319413        63.1144 
              26   0.0000       2.445215        66.5377 
              27   0.0000       2.524732        68.7014 
              28   0.0000       2.700880        73.4947 
              29   0.0000       2.869979        78.0961 
              30   0.0000       2.902010        78.9677 
              31   0.0000       2.954491        80.3958 
              32   0.0000       3.130118        85.1748 
              33   0.0000       3.151730        85.7629 
              34   0.0000       3.538503        96.2876 
              35   0.0000       3.661629        99.6380 
              36   0.0000       3.797269       103.3290 
              37   0.0000       3.886158       105.7477 
              38   0.0000       3.911985       106.4505 
              39   0.0000       4.019197       109.3679 
              40   0.0000       4.150704       112.9464 
              41   0.0000       4.252124       115.7062 
              42   0.0000       4.286331       116.6370 
              43   0.0000       4.638667       126.2245 
              44   0.0000       4.727923       128.6533 
              45   0.0000       4.823300       131.2487 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.526131
               1 H :    0.129746
               2 H :    0.128223
               3 H :    0.134081
               4 H :    0.134081
            Sum of atomic charges:    0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.289953  s :     3.289953
                  pz      :     1.093498  p :     3.200243
                  px      :     1.061451
                  py      :     1.045294
                  dz2     :     0.011811  d :     0.033820
                  dxz     :     0.003282
                  dyz     :     0.002505
                  dx2y2   :     0.011981
                  dxy     :     0.004240
                  f0      :     0.000250  f :     0.002116
                  f+1     :     0.000649
                  f-1     :     0.000208
                  f+2     :     0.000231
                  f-2     :    -0.000003
                  f+3     :     0.000618
                  f-3     :     0.000163
              1 H s       :     0.858683  s :     0.858683
                  pz      :     0.002581  p :     0.011571
                  px      :     0.006704
                  py      :     0.002286
              2 H s       :     0.859877  s :     0.859877
                  pz      :     0.006244  p :     0.011900
                  px      :     0.002895
                  py      :     0.002761
              3 H s       :     0.854170  s :     0.854170
                  pz      :     0.003140  p :     0.011749
                  px      :     0.002790
                  py      :     0.005819
              4 H s       :     0.854170  s :     0.854170
                  pz      :     0.003140  p :     0.011749
                  px      :     0.002790
                  py      :     0.005819
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :   -0.448080
               1 H :    0.109606
               2 H :    0.112018
               3 H :    0.113228
               4 H :    0.113228
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     2.939466  s :     2.939466
                  pz      :     1.154648  p :     3.381282
                  px      :     1.122420
                  py      :     1.104215
                  dz2     :     0.034618  d :     0.114625
                  dxz     :     0.010798
                  dyz     :     0.012148
                  dx2y2   :     0.042476
                  dxy     :     0.014585
                  f0      :     0.002043  f :     0.012707
                  f+1     :     0.003516
                  f-1     :     0.000726
                  f+2     :     0.001001
                  f-2     :     0.001220
                  f+3     :     0.003222
                  f-3     :     0.000979
              1 H s       :     0.849175  s :     0.849175
                  pz      :     0.008804  p :     0.041219
                  px      :     0.024681
                  py      :     0.007734
              2 H s       :     0.846295  s :     0.846295
                  pz      :     0.022788  p :     0.041686
                  px      :     0.010167
                  py      :     0.008732
              3 H s       :     0.844994  s :     0.844994
                  pz      :     0.010788  p :     0.041778
                  px      :     0.009914
                  py      :     0.021077
              4 H s       :     0.844994  s :     0.844994
                  pz      :     0.010788  p :     0.041778
                  px      :     0.009914
                  py      :     0.021077
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.5261     6.0000    -0.5261     3.8943     3.8943     0.0000
              1 H      0.8703     1.0000     0.1297     0.9555     0.9555    -0.0000
              2 H      0.8718     1.0000     0.1282     0.9485     0.9485    -0.0000
              3 H      0.8659     1.0000     0.1341     0.9561     0.9561    -0.0000
              4 H      0.8659     1.0000     0.1341     0.9561     0.9561     0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9744 B(  0-C ,  2-H ) :   0.9734 B(  0-C ,  3-H ) :   0.9732 
            B(  0-C ,  4-H ) :   0.9732 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 10 sec 
            
            Total time                  ....      10.464 sec
            Sum of individual times     ....      10.225 sec  ( 97.7%)
            
            Fock matrix formation       ....       5.902 sec  ( 56.4%)
              XC integration            ....       4.651 sec  ( 78.8% of F)
                Basis function eval.    ....       1.854 sec  ( 39.9% of XC)
                Density eval.           ....       0.742 sec  ( 15.9% of XC)
                XC-Functional eval.     ....       0.888 sec  ( 19.1% of XC)
                XC-Potential eval.      ....       0.868 sec  ( 18.7% of XC)
            Diagonalization             ....       0.003 sec  (  0.0%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.0%)
            Initial guess               ....       0.492 sec  (  4.7%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.0%)
            SOSCF solution              ....       0.001 sec  (  0.0%)
            Grid generation             ....       3.826 sec  ( 36.6%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.514995928288
            -------------------------   --------------------
            
            ------------------------------------------------------------------------------
                                     ORCA SCF GRADIENT CALCULATION
            ------------------------------------------------------------------------------
            
            Gradient of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type      ... RKS
            Hartree-Fock exchange scaling    ...    0.200
            Number of operators              ...    1
            Number of atoms                  ...    5
            Basis set dimensions             ...   46
            Integral neglect threshold       ... 1.0e-12
            Integral primitive cutoff        ... 1.0e-14
            
            Nuclear repulsion gradient       ... done
            One Electron Gradient            ... done
            Pre-screening matrix             ... done
            Starting the two electron gradient:
            Two electron gradient done
            Exchange-correlation gradient    ... done
            
            ------------------
            CARTESIAN GRADIENT
            ------------------
            
               1   C   :   -0.002116421    0.000000000    0.028333837
               2   H   :    0.001218322   -0.000000000    0.000945144
               3   H   :   -0.008291045    0.000000000    0.008614106
               4   H   :    0.004594572   -0.011222606   -0.018946544
               5   H   :    0.004594572    0.011222606   -0.018946544
            
            Difference to translation invariance:
                       :   -0.0000000000    0.0000000000    0.0000000000
            
            Norm of the cartesian gradient     ...    0.0443245353
            RMS gradient                       ...    0.0114445458
            MAX gradient                       ...    0.0283338373
            
            -------
            TIMINGS
            -------
            
            Total SCF gradient time            ...        2.148 sec
            
            One electron gradient       ....       0.005 sec  (  0.2%)
            Prescreening matrices       ....       0.019 sec  (  0.9%)
            Two electron gradient       ....       0.164 sec  (  7.7%)
            XC gradient                 ....       1.846 sec  ( 85.9%)
            
            -------------------------------------------------------------------------------
                                           ORCA SCF HESSIAN
            -------------------------------------------------------------------------------
            
            Hessian of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type                      ... RKS
            Hartree-Fock exchange scaling                    ...    0.200
            Number of operators                              ...    1
            Number of atoms                                  ...    5
            Basis set dimensions                             ...   46
            Integral neglect threshold                       ... 1.0e-12
            Integral primitive cutoff                        ... 1.0e-14
            
            Setting up DFT Hessian calculations              ... 
            Electron density on the grid                     ... found on disk
            Building xc-kernel on the grid                   ... done   (      0.2 sec)
                                                                 done   (      0.2 sec)
            
            Nuclear repulsion Hessian                        ... done   (      0.0 sec)
            
            ----------------------------------------------
            Forming right-hand sides of CP-SCF equations     ...
            ----------------------------------------------
            One electron integral derivatives                ... done   (      0.1 sec)
            Transforming the overlap derivative matrices     ... done   (      0.0 sec)
            Making the Q(x) pseudodensities                  ... done   (      0.0 sec)
            Adding the E*S(x)*S(y) terms to the Hessian      ... done   (      0.0 sec)
            Calculating energy weighted overlap derivatives  ... done   (      0.0 sec)
            Two electron integral derivatives                ... done   (      0.4 sec)
            Exchange-correlation integral derivatives        ... done   (      8.9 sec)
            tr(F(y)Q(x)) contribution to the Hessian         ... done   (      0.0 sec)
            Response fock operator R(S(x))                   ... done   (      0.2 sec)
            XC Response fock operator R(S(x))                ... done   (      3.1 sec)
            tr(F(y)S(x)) contribution to the Hessian         ... done   (      0.0 sec)
            Transforming and finalizing RHSs                 ... done   (      0.0 sec)
            
            ----------------------------------------------
            Solving the CP-SCF equations                     ...
            ----------------------------------------------
                 CP-SCF ITERATION   0: 
                 CP-SCF ITERATION   1:      0.000160709290
                 CP-SCF ITERATION   2:      0.000004644793
                 CP-SCF ITERATION   3:      0.000000040964
                 CP-SCF ITERATION   4:      0.000000000906
            
                                                             ... done   (     17.2 sec)
            Forming perturbed density Hessian contributions  ... done   (      0.0 sec)
            Making the perturbed densities                   ... done   (      0.0 sec)
            2nd integral derivative contribs                 ... done   (      1.6 sec)
            Exchange-correlation Hessian                     ... done   (     12.6 sec)
            Dipol derivatives                                ... done   (      0.1 sec)
            
            Total SCF Hessian time: 0 days 0 hours 0 min 44 sec 
            
            Writing the Hessian file to the disk             ... done
            
            
            Maximum memory used throughout the entire calculation: 150.9 MB
            
            -----------------------
            VIBRATIONAL FREQUENCIES
            -----------------------
            
            Scaling factor for frequencies =  1.000000000  (already applied!)
            
               0:         0.00 cm**-1
               1:         0.00 cm**-1
               2:         0.00 cm**-1
               3:         0.00 cm**-1
               4:         0.00 cm**-1
               5:         0.00 cm**-1
               6:      1242.43 cm**-1
               7:      1329.48 cm**-1
               8:      1403.71 cm**-1
               9:      1530.62 cm**-1
              10:      1590.11 cm**-1
              11:      3028.59 cm**-1
              12:      3086.82 cm**-1
              13:      3149.18 cm**-1
              14:      3186.90 cm**-1
            
            
            ------------
            NORMAL MODES
            ------------
            
            These modes are the Cartesian displacements weighted by the diagonal matrix
            M(i,i)=1/sqrt(m[i]) where m[i] is the mass of the displaced atom
            Thus, these vectors are normalized but *not* orthogonal
            
                              0          1          2          3          4          5    
                  0       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  1       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  2       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  3       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  4       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  5       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  6       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  7       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  8       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  9       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 10       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 11       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 12       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 13       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 14       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                              6          7          8          9         10         11    
                  0      -0.017743  -0.121818   0.000000  -0.013834  -0.000000   0.002301
                  1       0.000000  -0.000000  -0.118487  -0.000000   0.007467   0.000000
                  2      -0.129614   0.019465  -0.000000   0.008397  -0.000000  -0.017441
                  3      -0.009551  -0.088712   0.000000  -0.012047  -0.000000   0.459980
                  4      -0.000000   0.000000   0.664415   0.000000   0.458993  -0.000000
                  5       0.531192  -0.087103   0.000000  -0.528348   0.000000  -0.009606
                  6      -0.098642   0.415949  -0.000000   0.578088  -0.000000  -0.056553
                  7       0.000000   0.000000   0.538454  -0.000000  -0.577862  -0.000000
                  8      -0.052926  -0.148629   0.000000  -0.180188   0.000000  -0.213845
                  9       0.159809   0.562153  -0.233588  -0.200598  -0.360925  -0.215421
                 10       0.185285  -0.266629   0.104494   0.209983   0.014946  -0.525964
                 11       0.533085   0.001897   0.248613   0.304240  -0.311741   0.215638
                 12       0.159809   0.562153   0.233588  -0.200598   0.360925  -0.215421
                 13      -0.185285   0.266629   0.104494  -0.209983   0.014946   0.525964
                 14       0.533085   0.001897  -0.248613   0.304240   0.311741   0.215638
                              12         13         14    
                  0       0.023868  -0.088769   0.000000
                  1       0.000000  -0.000000  -0.098144
                  2      -0.078127  -0.024487  -0.000000
                  3      -0.365297   0.806127  -0.000000
                  4      -0.000000   0.000000  -0.023959
                  5      -0.012146  -0.000338   0.000000
                  6       0.279956   0.140633   0.000000
                  7       0.000000   0.000000  -0.040254
                  8       0.791988   0.475820   0.000000
                  9      -0.099531   0.055492   0.237237
                 10      -0.247880   0.190351   0.616830
                 11       0.075548  -0.091849  -0.239429
                 12      -0.099531   0.055492  -0.237237
                 13       0.247880  -0.190351   0.616830
                 14       0.075548  -0.091849   0.239429
            
            
            -----------
            IR SPECTRUM
            -----------
            
             Mode    freq (cm**-1)   T**2         TX         TY         TZ
            -------------------------------------------------------------------
               6:      1242.43   23.195574  (  0.998033  -0.000000   4.711635)
               7:      1329.48   10.178689  (  3.183742   0.000000  -0.206096)
               8:      1403.71    7.142375  ( -0.000000   2.672522   0.000000)
               9:      1530.62    0.125959  (  0.352585   0.000000  -0.040523)
              10:      1590.11    0.110492  ( -0.000000  -0.332403  -0.000000)
              11:      3028.59    0.800277  (  0.021102  -0.000000  -0.894333)
              12:      3086.82   30.450845  (  0.887506   0.000000  -5.446391)
              13:      3149.18   24.247128  ( -4.507913   0.000000  -1.981376)
              14:      3186.90   11.012046  ( -0.000000  -3.318440   0.000000)
            
            The first frequency considered to be a vibration is 6
            The total number of vibrations considered is 9
            
            
            --------------------------
            THERMOCHEMISTRY AT 273.15K
            --------------------------
            
            Temperature         ... 273.15 K
            Pressure            ... 1.00 atm
            Total Mass          ... 16.04 AMU
            
            Throughout the following assumptions are being made:
              (1) The electronic state is orbitally nondegenerate
              (2) There are no thermally accessible electronically excited states
              (3) Hindered rotations indicated by low frequency modes are not
                  treated as such but are treated as vibrations and this may
                  cause some error
              (4) All equations used are the standard statistical mechanics
                  equations for an ideal gas
              (5) All vibrations are strictly harmonic
            
            freq.    1242.43  E(vib)   ...       0.01 
            freq.    1329.48  E(vib)   ...       0.00 
            freq.    1403.71  E(vib)   ...       0.00 
            freq.    1530.62  E(vib)   ...       0.00 
            freq.    1590.11  E(vib)   ...       0.00 
            freq.    3028.59  E(vib)   ...       0.00 
            freq.    3086.82  E(vib)   ...       0.00 
            freq.    3149.18  E(vib)   ...       0.00 
            freq.    3186.90  E(vib)   ...       0.00 
            
            ------------
            INNER ENERGY
            ------------
            
            The inner energy is: U= E(el) + E(ZPE) + E(vib) + E(rot) + E(trans)
                E(el)   - is the total energy from the electronic structure calculation
                          = E(kin-el) + E(nuc-el) + E(el-el) + E(nuc-nuc)
                E(ZPE)  - the the zero temperature vibrational energy from the frequency calculation
                E(vib)  - the the finite temperature correction to E(ZPE) due to population
                          of excited vibrational states
                E(rot)  - is the rotational thermal energy
                E(trans)- is the translational thermal energy
            
            Summary of contributions to the inner energy U:
            Electronic energy                ...    -40.51499593 Eh
            Zero point energy                ...      0.04453325 Eh      27.94 kcal/mol
            Thermal vibrational correction   ...      0.00002148 Eh       0.01 kcal/mol
            Thermal rotational correction    ...      0.00129752 Eh       0.81 kcal/mol
            Thermal translational correction ...      0.00129752 Eh       0.81 kcal/mol
            -----------------------------------------------------------------------
            Total thermal energy                    -40.46784616 Eh
            
            
            Summary of corrections to the electronic energy:
            (perhaps to be used in another calculation)
            Total thermal correction                  0.00261651 Eh       1.64 kcal/mol
            Non-thermal (ZPE) correction              0.04453325 Eh      27.94 kcal/mol
            -----------------------------------------------------------------------
            Total correction                          0.04714977 Eh      29.59 kcal/mol
            
            
            --------
            ENTHALPY
            --------
            
            The enthalpy is H = U + kB*T
                            kB is Boltzmann's constant
            Total free energy                 ...    -40.46784616 Eh 
            Thermal Enthalpy correction       ...      0.00086504 Eh       0.54 kcal/mol
            -----------------------------------------------------------------------
            Total Enthalpy                    ...    -40.46698113 Eh
            
            
            Note: Rotational entropy computed according to Herzberg 
            Infrared and Raman Spectra, Chapter V,1, Van Nostrand Reinhold, 1945 
            Point Group:  Cs, Symmetry Number:   1  
            Rotational constants in cm-1:     5.796357     5.334011     4.740168 
            
            Vibrational entropy computed according to the QRRHO of S. Grimme
            Chem.Eur.J. 2012 18 9955
            
            
            -------
            ENTROPY
            -------
            
            The entropy contributions are T*S = T*(S(el)+S(vib)+S(rot)+S(trans))
                 S(el)   - electronic entropy
                 S(vib)  - vibrational entropy
                 S(rot)  - rotational entropy
                 S(trans)- translational entropy
            The entropies will be listed as mutliplied by the temperature to get
            units of energy
            
            Electronic entropy                ...      0.00000000 Eh      0.00 kcal/mol
            Vibrational entropy               ...      0.00002452 Eh      0.02 kcal/mol
            Rotational entropy                ...      0.00644261 Eh      4.04 kcal/mol
            Translational entropy             ...      0.01472517 Eh      9.24 kcal/mol
            -----------------------------------------------------------------------
            Final entropy term                ...      0.02119231 Eh     13.30 kcal/mol
            
            In case the symmetry of your molecule has not been determined correctly
            or in case you have a reason to use a different symmetry number we print 
            out the resulting rotational entropy values for sn=1,12 :
             --------------------------------------------------------
            |  sn= 1 | S(rot)=       0.00644261 Eh      4.04 kcal/mol|
            |  sn= 2 | S(rot)=       0.00584303 Eh      3.67 kcal/mol|
            |  sn= 3 | S(rot)=       0.00549230 Eh      3.45 kcal/mol|
            |  sn= 4 | S(rot)=       0.00524345 Eh      3.29 kcal/mol|
            |  sn= 5 | S(rot)=       0.00505043 Eh      3.17 kcal/mol|
            |  sn= 6 | S(rot)=       0.00489272 Eh      3.07 kcal/mol|
            |  sn= 7 | S(rot)=       0.00475938 Eh      2.99 kcal/mol|
            |  sn= 8 | S(rot)=       0.00464387 Eh      2.91 kcal/mol|
            |  sn= 9 | S(rot)=       0.00454199 Eh      2.85 kcal/mol|
            |  sn=10 | S(rot)=       0.00445085 Eh      2.79 kcal/mol|
            |  sn=11 | S(rot)=       0.00436841 Eh      2.74 kcal/mol|
            |  sn=12 | S(rot)=       0.00429314 Eh      2.69 kcal/mol|
             --------------------------------------------------------
            
            
            -------------------
            GIBBS FREE ENERGY
            -------------------
            
            The Gibbs free energy is G = H - T*S
            
            Total enthalpy                    ...    -40.46698113 Eh 
            Total entropy correction          ...     -0.02119231 Eh    -13.30 kcal/mol
            -----------------------------------------------------------------------
            Final Gibbs free energy         ...    -40.48817344 Eh
            
            For completeness - the Gibbs free energy minus the electronic energy
            G-E(el)                           ...      0.02682249 Eh     16.83 kcal/mol
            
            
            The first frequency considered to be a vibration is 6
            The total number of vibrations considered is 9
            
            
            --------------------------
            THERMOCHEMISTRY AT 298.15K
            --------------------------
            
            Temperature         ... 298.15 K
            Pressure            ... 1.00 atm
            Total Mass          ... 16.04 AMU
            
            Throughout the following assumptions are being made:
              (1) The electronic state is orbitally nondegenerate
              (2) There are no thermally accessible electronically excited states
              (3) Hindered rotations indicated by low frequency modes are not
                  treated as such but are treated as vibrations and this may
                  cause some error
              (4) All equations used are the standard statistical mechanics
                  equations for an ideal gas
              (5) All vibrations are strictly harmonic
            
            freq.    1242.43  E(vib)   ...       0.01 
            freq.    1329.48  E(vib)   ...       0.01 
            freq.    1403.71  E(vib)   ...       0.00 
            freq.    1530.62  E(vib)   ...       0.00 
            freq.    1590.11  E(vib)   ...       0.00 
            freq.    3028.59  E(vib)   ...       0.00 
            freq.    3086.82  E(vib)   ...       0.00 
            freq.    3149.18  E(vib)   ...       0.00 
            freq.    3186.90  E(vib)   ...       0.00 
            
            ------------
            INNER ENERGY
            ------------
            
            The inner energy is: U= E(el) + E(ZPE) + E(vib) + E(rot) + E(trans)
                E(el)   - is the total energy from the electronic structure calculation
                          = E(kin-el) + E(nuc-el) + E(el-el) + E(nuc-nuc)
                E(ZPE)  - the the zero temperature vibrational energy from the frequency calculation
                E(vib)  - the the finite temperature correction to E(ZPE) due to population
                          of excited vibrational states
                E(rot)  - is the rotational thermal energy
                E(trans)- is the translational thermal energy
            
            Summary of contributions to the inner energy U:
            Electronic energy                ...    -40.51499593 Eh
            Zero point energy                ...      0.04453325 Eh      27.94 kcal/mol
            Thermal vibrational correction   ...      0.00003909 Eh       0.02 kcal/mol
            Thermal rotational correction    ...      0.00141627 Eh       0.89 kcal/mol
            Thermal translational correction ...      0.00141627 Eh       0.89 kcal/mol
            -----------------------------------------------------------------------
            Total thermal energy                    -40.46759104 Eh
            
            
            Summary of corrections to the electronic energy:
            (perhaps to be used in another calculation)
            Total thermal correction                  0.00287164 Eh       1.80 kcal/mol
            Non-thermal (ZPE) correction              0.04453325 Eh      27.94 kcal/mol
            -----------------------------------------------------------------------
            Total correction                          0.04740489 Eh      29.75 kcal/mol
            
            
            --------
            ENTHALPY
            --------
            
            The enthalpy is H = U + kB*T
                            kB is Boltzmann's constant
            Total free energy                 ...    -40.46759104 Eh 
            Thermal Enthalpy correction       ...      0.00094421 Eh       0.59 kcal/mol
            -----------------------------------------------------------------------
            Total Enthalpy                    ...    -40.46664683 Eh
            
            
            Note: Rotational entropy computed according to Herzberg 
            Infrared and Raman Spectra, Chapter V,1, Van Nostrand Reinhold, 1945 
            Point Group:  Cs, Symmetry Number:   1  
            Rotational constants in cm-1:     5.796357     5.334011     4.740168 
            
            Vibrational entropy computed according to the QRRHO of S. Grimme
            Chem.Eur.J. 2012 18 9955
            
            
            -------
            ENTROPY
            -------
            
            The entropy contributions are T*S = T*(S(el)+S(vib)+S(rot)+S(trans))
                 S(el)   - electronic entropy
                 S(vib)  - vibrational entropy
                 S(rot)  - rotational entropy
                 S(trans)- translational entropy
            The entropies will be listed as mutliplied by the temperature to get
            units of energy
            
            Electronic entropy                ...      0.00000000 Eh      0.00 kcal/mol
            Vibrational entropy               ...      0.00004511 Eh      0.03 kcal/mol
            Rotational entropy                ...      0.00715630 Eh      4.49 kcal/mol
            Translational entropy             ...      0.01627961 Eh     10.22 kcal/mol
            -----------------------------------------------------------------------
            Final entropy term                ...      0.02348103 Eh     14.73 kcal/mol
            
            In case the symmetry of your molecule has not been determined correctly
            or in case you have a reason to use a different symmetry number we print 
            out the resulting rotational entropy values for sn=1,12 :
             --------------------------------------------------------
            |  sn= 1 | S(rot)=       0.00715630 Eh      4.49 kcal/mol|
            |  sn= 2 | S(rot)=       0.00650185 Eh      4.08 kcal/mol|
            |  sn= 3 | S(rot)=       0.00611901 Eh      3.84 kcal/mol|
            |  sn= 4 | S(rot)=       0.00584739 Eh      3.67 kcal/mol|
            |  sn= 5 | S(rot)=       0.00563670 Eh      3.54 kcal/mol|
            |  sn= 6 | S(rot)=       0.00546456 Eh      3.43 kcal/mol|
            |  sn= 7 | S(rot)=       0.00531901 Eh      3.34 kcal/mol|
            |  sn= 8 | S(rot)=       0.00519293 Eh      3.26 kcal/mol|
            |  sn= 9 | S(rot)=       0.00508173 Eh      3.19 kcal/mol|
            |  sn=10 | S(rot)=       0.00498225 Eh      3.13 kcal/mol|
            |  sn=11 | S(rot)=       0.00489226 Eh      3.07 kcal/mol|
            |  sn=12 | S(rot)=       0.00481010 Eh      3.02 kcal/mol|
             --------------------------------------------------------
            
            
            -------------------
            GIBBS FREE ENERGY
            -------------------
            
            The Gibbs free energy is G = H - T*S
            
            Total enthalpy                    ...    -40.46664683 Eh 
            Total entropy correction          ...     -0.02348103 Eh    -14.73 kcal/mol
            -----------------------------------------------------------------------
            Final Gibbs free energy         ...    -40.49012786 Eh
            
            For completeness - the Gibbs free energy minus the electronic energy
            G-E(el)                           ...      0.02486807 Eh     15.60 kcal/mol
            
            Actual Hessian File stored as input.001.hess
            ------------------------------------------------------------------------------
                                     ORCA GEOMETRY RELAXATION STEP
            ------------------------------------------------------------------------------
            
            Reading the OPT-File                    .... done
            Getting information on internals        .... done
            Copying old internal coords+grads       .... done
            Making the new internal coordinates     .... (new redundants).... done
            Validating the new internal coordinates .... (new redundants).... done
            Calculating the B-matrix                .... done
            Calculating the G,G- and P matrices     .... done
            Transforming gradient to internals      .... done
            Projecting the internal gradient        .... done
            Number of atoms                         ....   5
            Number of internal coordinates          ....  10
            Current Energy                          ....   -40.514995928 Eh
            Current gradient norm                   ....     0.044324535 Eh/bohr
            Maximum allowed component of the step   ....  0.300
            Current trust radius                    ....  0.300
            Evaluating the initial hessian          ....  (read) 
            (Reading Exact Hessian)...  
            InHessName: input.hess	The file <input.hess> is opened as a .hess file
            done
            done
            Diagonalizing the Hessian               .... done
            Dimension of the hessian                .... 10
            Lowest eigenvalues of the non projected Hessian:
             -0.000000006  0.102302547  0.113919098  0.131019128  0.134199401
            done
            Projecting the Hessian                  .... done
            Forming the augmented Hessian           .... done
            Diagonalizing the augmented Hessian     .... done
            Last element of RFO vector              ....  0.950059734
            Lowest eigenvalues of augmented Hessian:
             -0.015071046  0.106104356  0.113919098  0.133861242  0.134199401
            Length of the computed step             ....  0.328472090
            Warning: the length of the step is outside the trust region - taking restricted step instead
            The input lambda is                     ....    -0.015071
               iter:   1  x=   -0.026375  g=    1.582960 f(x)=     0.017894
               iter:   2  x=   -0.028015  g=    1.241545 f(x)=     0.002035
               iter:   3  x=   -0.028043  g=    1.200573 f(x)=     0.000034
               iter:   4  x=   -0.028043  g=    1.199884 f(x)=     0.000000
               iter:   5  x=   -0.028043  g=    1.199884 f(x)=     0.000000
            The output lambda is                    ....    -0.028043 (5 iterations)
            The final length of the internal step   ....  0.300000000
            Converting the step to cartesian space:
             Initial RMS(Int)=    0.0948683298
            Transforming coordinates:
             Iter   0:  RMS(Cart)=    0.0875690952 RMS(Int)=    0.0978129636
             Iter   1:  RMS(Cart)=    0.0076944452 RMS(Int)=    0.0105501657
             Iter   2:  RMS(Cart)=    0.0008692207 RMS(Int)=    0.0009226300
             Iter   3:  RMS(Cart)=    0.0001100784 RMS(Int)=    0.0001528208
             Iter   4:  RMS(Cart)=    0.0000143271 RMS(Int)=    0.0000159781
             Iter   5:  RMS(Cart)=    0.0000015545 RMS(Int)=    0.0000021043
             Iter   6:  RMS(Cart)=    0.0000002310 RMS(Int)=    0.0000002766
             Iter   7:  RMS(Cart)=    0.0000000225 RMS(Int)=    0.0000000281
            done
            Storing new coordinates                 .... done
            
                                            .--------------------.
                      ----------------------|Geometry convergence|-------------------------
                      Item                value                   Tolerance       Converged
                      ---------------------------------------------------------------------
                      RMS gradient        0.0147667323            0.0000300000      NO
                      MAX gradient        0.0329512766            0.0001000000      NO
                      RMS step            0.0948683298            0.0006000000      NO
                      MAX step            0.2304518319            0.0010000000      NO
                      ........................................................
                      Max(Bonds)      0.0072      Max(Angles)   13.20
                      Max(Dihed)        0.00      Max(Improp)    0.00
                      ---------------------------------------------------------------------
            
            The optimization has not yet converged - more geometry cycles are needed
            
            
                ---------------------------------------------------------------------------
                                     Redundant Internal Coordinates
                                        (Angstroem and degrees)
            
                    Definition                    Value    dE/dq     Step     New-Value
                ----------------------------------------------------------------------------
                 1. B(H   1,C   0)                1.0934  0.001218 -0.0013    1.0920   
                 2. B(H   2,C   0)                1.0934 -0.005358 -0.0019    1.0915   
                 3. B(H   3,C   0)                1.0934  0.002490 -0.0072    1.0861   
                 4. B(H   4,C   0)                1.0934  0.002490 -0.0072    1.0861   
                 5. A(H   1,C   0,H   3)          109.47  0.000977    0.31    109.78   
                 6. A(H   2,C   0,H   3)          100.67 -0.022842    7.73    108.40   
                 7. A(H   1,C   0,H   4)          109.47  0.000977    0.31    109.78   
                 8. A(H   2,C   0,H   4)          100.67 -0.022842    7.73    108.40   
                 9. A(H   3,C   0,H   4)          125.47  0.032951  -13.20    112.26   
                10. A(H   1,C   0,H   2)          109.47  0.002604    0.18    109.65   
                ----------------------------------------------------------------------------
            
                     *************************************************************
                     *                GEOMETRY OPTIMIZATION CYCLE   2            *
                     *************************************************************
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C     -0.001082    0.000000   -0.057915
              H      1.090271   -0.000000   -0.019047
              H     -0.327848    0.000000   -1.099357
              H     -0.380665   -0.900359    0.416355
              H     -0.380665    0.900359    0.416355
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011   -0.002045    0.000000   -0.109444
               1 H     1.0000    0     1.008    2.060313   -0.000000   -0.035993
               2 H     1.0000    0     1.008   -0.619543    0.000000   -2.077484
               3 H     1.0000    0     1.008   -0.719353   -1.701431    0.786796
               4 H     1.0000    0     1.008   -0.719353    1.701431    0.786796
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.092044883016     0.00000000     0.00000000
             H      1   2   0     1.091502150293   109.45967833     0.00000000
             H      1   2   3     1.086121828292   109.49478610   118.43238173
             H      1   2   3     1.086121826108   109.49479065   241.56761555
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063665754851     0.00000000     0.00000000
             H      1   2   0     2.062640138640   109.45967833     0.00000000
             H      1   2   3     2.052472803545   109.49478610   118.43238173
             H      1   2   3     2.052472799418   109.49479065   241.56761555
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.517e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-770
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ... 134918 (   0.1 sec)
            # of grid points (after weights+screening)   ... 130860 (   0.1 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    4.0 sec
            Reduced shell lists constructed in    4.3 sec
            
            Total number of grid points                  ...   130860
            Total number of batches                      ...     2047
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...    26172
            Average number of shells per batch           ...    16.41 (82.06%)
            Average number of basis functions per batch  ...    37.28 (81.04%)
            Average number of large shells per batch     ...    15.25 (92.91%)
            Average number of large basis fcns per batch ...    34.52 (92.60%)
            Maximum spatial batch extension              ...  19.46, 17.31, 17.99 au
            Average spatial batch extension              ...   1.78,  1.73,  1.75 au
            
            Time for grid setup =    4.413 sec
            
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.5211338163   0.000000000000 0.00476549  0.00030735  0.0192279 0.7000
                                  *** Initiating the SOSCF procedure ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              1    -40.52161450  -0.0004806856  0.002872  0.002872  0.013669  0.000890
                           *** Restarting incremental Fock matrix formation ***
              2    -40.52277993  -0.0011654324  0.002371  0.002628  0.003565  0.000220
              3    -40.52279734  -0.0000174030  0.001080  0.001042  0.002207  0.000103
              4    -40.52280805  -0.0000107081  0.000257  0.000308  0.000375  0.000027
              5    -40.52280849  -0.0000004450  0.000120  0.000104  0.000108  0.000009
              6    -40.52280866  -0.0000001707  0.000004  0.000005  0.000009  0.000000
              7    -40.52280866  -0.0000000002  0.000001  0.000000  0.000001  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   8 CYCLES          *
                           *****************************************************
            
            Total Energy       :          -40.52280866 Eh           -1102.68168 eV
              Last Energy change         ...   -2.3519e-12  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    9.5695e-08  Tolerance :   1.0000e-08
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            Total SCF time: 0 days 0 hours 0 min 10 sec 
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.522808661344
            -------------------------   --------------------
            
            ------------------------------------------------------------------------------
                                     ORCA SCF GRADIENT CALCULATION
            ------------------------------------------------------------------------------
            
            Gradient of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type      ... RKS
            Hartree-Fock exchange scaling    ...    0.200
            Number of operators              ...    1
            Number of atoms                  ...    5
            Basis set dimensions             ...   46
            Integral neglect threshold       ... 1.0e-12
            Integral primitive cutoff        ... 1.0e-14
            
            Nuclear repulsion gradient       ... done
            One Electron Gradient            ... done
            Pre-screening matrix             ... done
            Starting the two electron gradient:
            Two electron gradient done
            Exchange-correlation gradient    ... done
            
            ------------------
            CARTESIAN GRADIENT
            ------------------
            
               1   C   :   -0.002807095    0.000000006    0.007124954
               2   H   :    0.000033502   -0.000000004    0.000207340
               3   H   :   -0.001172149    0.000000000    0.001588546
               4   H   :    0.001972873    0.001075403   -0.004460419
               5   H   :    0.001972869   -0.001075404   -0.004460420
            
            Difference to translation invariance:
                       :    0.0000000000   -0.0000000000   -0.0000000000
            
            Norm of the cartesian gradient     ...    0.0106053943
            RMS gradient                       ...    0.0027383010
            MAX gradient                       ...    0.0071249539
            
            -------
            TIMINGS
            -------
            
            Total SCF gradient time            ...        2.134 sec
            
            One electron gradient       ....       0.005 sec  (  0.2%)
            Prescreening matrices       ....       0.018 sec  (  0.9%)
            Two electron gradient       ....       0.165 sec  (  7.7%)
            XC gradient                 ....       1.831 sec  ( 85.8%)
            ------------------------------------------------------------------------------
                                     ORCA GEOMETRY RELAXATION STEP
            ------------------------------------------------------------------------------
            
            Reading the OPT-File                    .... done
            Getting information on internals        .... done
            Copying old internal coords+grads       .... done
            Making the new internal coordinates     .... (new redundants).... done
            Validating the new internal coordinates .... (new redundants).... done
            Calculating the B-matrix                .... done
            Calculating the G,G- and P matrices     .... done
            Transforming gradient to internals      .... done
            Projecting the internal gradient        .... done
            Number of atoms                         ....   5
            Number of internal coordinates          ....  10
            Current Energy                          ....   -40.522808661 Eh
            Current gradient norm                   ....     0.010605394 Eh/bohr
            Maximum allowed component of the step   ....  0.300
            Current trust radius                    ....  0.300
            Updating the Hessian (BFGS)             .... done
            Forming the augmented Hessian           .... done
            Diagonalizing the augmented Hessian     .... done
            Last element of RFO vector              ....  0.998424860
            Lowest eigenvalues of augmented Hessian:
             -0.000438909  0.104088024  0.113919606  0.133042212  0.134198879
            Length of the computed step             ....  0.056193769
            The final length of the internal step   ....  0.056193769
            Converting the step to cartesian space:
             Initial RMS(Int)=    0.0177700300
            Transforming coordinates:
             Iter   0:  RMS(Cart)=    0.0148313941 RMS(Int)=    0.0177688369
             Iter   1:  RMS(Cart)=    0.0002416954 RMS(Int)=    0.0002915018
             Iter   2:  RMS(Cart)=    0.0000037224 RMS(Int)=    0.0000047141
             Iter   3:  RMS(Cart)=    0.0000001246 RMS(Int)=    0.0000001438
             Iter   4:  RMS(Cart)=    0.0000000019 RMS(Int)=    0.0000000026
            done
            Storing new coordinates                 .... done
            
                                            .--------------------.
                      ----------------------|Geometry convergence|-------------------------
                      Item                value                   Tolerance       Converged
                      ---------------------------------------------------------------------
                      Energy change      -0.0078127331            0.0000010000      NO
                      RMS gradient        0.0026899552            0.0000300000      NO
                      MAX gradient        0.0053531373            0.0001000000      NO
                      RMS step            0.0177700300            0.0006000000      NO
                      MAX step            0.0455361114            0.0010000000      NO
                      ........................................................
                      Max(Bonds)      0.0057      Max(Angles)    2.61
                      Max(Dihed)        0.00      Max(Improp)    0.00
                      ---------------------------------------------------------------------
            
            The optimization has not yet converged - more geometry cycles are needed
            
            
                ---------------------------------------------------------------------------
                                     Redundant Internal Coordinates
                                        (Angstroem and degrees)
            
                    Definition                    Value    dE/dq     Step     New-Value
                ----------------------------------------------------------------------------
                 1. B(H   1,C   0)                1.0920  0.000041 -0.0003    1.0917   
                 2. B(H   2,C   0)                1.0915 -0.001165  0.0004    1.0919   
                 3. B(H   3,C   0)                1.0861 -0.003529  0.0057    1.0919   
                 4. B(H   4,C   0)                1.0861 -0.003529  0.0057    1.0919   
                 5. A(H   1,C   0,H   3)          109.49 -0.000009    0.20    109.70   
                 6. A(H   2,C   0,H   3)          108.18 -0.002938    1.16    109.34   
                 7. A(H   1,C   0,H   4)          109.49 -0.000009    0.20    109.70   
                 8. A(H   2,C   0,H   4)          108.18 -0.002938    1.16    109.34   
                 9. A(H   3,C   0,H   4)          111.99  0.005353   -2.61    109.38   
                10. A(H   1,C   0,H   2)          109.46  0.000417    0.14    109.60   
                ----------------------------------------------------------------------------
            
                     *************************************************************
                     *                GEOMETRY OPTIMIZATION CYCLE   3            *
                     *************************************************************
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.001705    0.000000   -0.068317
              H      1.092496   -0.000000   -0.023824
              H     -0.321706    0.000000   -1.111188
              H     -0.386242   -0.890767    0.429860
              H     -0.386242    0.890767    0.429860
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.003222    0.000000   -0.129101
               1 H     1.0000    0     1.008    2.064518   -0.000000   -0.045021
               2 H     1.0000    0     1.008   -0.607936    0.000000   -2.099841
               3 H     1.0000    0     1.008   -0.729892   -1.683305    0.812317
               4 H     1.0000    0     1.008   -0.729892    1.683305    0.812317
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091697873237     0.00000000     0.00000000
             H      1   2   0     1.091867587306   109.56528672     0.00000000
             H      1   2   3     1.091855421027   109.65886038   119.96572125
             H      1   2   3     1.091855415610   109.65887521   240.03427187
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063010001403     0.00000000     0.00000000
             H      1   2   0     2.063330714513   109.56528672     0.00000000
             H      1   2   3     2.063307723578   109.65886038   119.96572125
             H      1   2   3     2.063307713342   109.65887521   240.03427187
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.530e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-770
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ... 134918 (   0.0 sec)
            # of grid points (after weights+screening)   ... 130875 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    3.6 sec
            Reduced shell lists constructed in    3.9 sec
            
            Total number of grid points                  ...   130875
            Total number of batches                      ...     2048
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...    26175
            Average number of shells per batch           ...    16.43 (82.13%)
            Average number of basis functions per batch  ...    37.29 (81.07%)
            Average number of large shells per batch     ...    15.22 (92.65%)
            Average number of large basis fcns per batch ...    34.49 (92.47%)
            Maximum spatial batch extension              ...  19.58, 17.31, 18.86 au
            Average spatial batch extension              ...   1.79,  1.73,  1.76 au
            
            Time for grid setup =    4.041 sec
            
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
                                  *** Initiating the SOSCF procedure ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              0    -40.52296575 -40.5229657502  0.002813  0.002813  0.003524  0.000207
                           *** Restarting incremental Fock matrix formation ***
              1    -40.52302420  -0.0000584463  0.000663  0.000741  0.001557  0.000084
              2    -40.52302740  -0.0000032037  0.000292  0.000398  0.000906  0.000038
              3    -40.52302812  -0.0000007174  0.000183  0.000176  0.000315  0.000015
              4    -40.52302827  -0.0000001573  0.000013  0.000013  0.000011  0.000001
              5    -40.52302828  -0.0000000009  0.000004  0.000003  0.000003  0.000000
                              ***Gradient check signals convergence***
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   6 CYCLES          *
                           *****************************************************
            
            Total Energy       :          -40.52302828 Eh           -1102.68766 eV
              Last Energy change         ...   -1.3801e-10  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    6.6289e-07  Tolerance :   1.0000e-08
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            Total SCF time: 0 days 0 hours 0 min 10 sec 
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.523028275886
            -------------------------   --------------------
            
            ------------------------------------------------------------------------------
                                     ORCA SCF GRADIENT CALCULATION
            ------------------------------------------------------------------------------
            
            Gradient of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type      ... RKS
            Hartree-Fock exchange scaling    ...    0.200
            Number of operators              ...    1
            Number of atoms                  ...    5
            Basis set dimensions             ...   46
            Integral neglect threshold       ... 1.0e-12
            Integral primitive cutoff        ... 1.0e-14
            
            Nuclear repulsion gradient       ... done
            One Electron Gradient            ... done
            Pre-screening matrix             ... done
            Starting the two electron gradient:
            Two electron gradient done
            Exchange-correlation gradient    ... done
            
            ------------------
            CARTESIAN GRADIENT
            ------------------
            
               1   C   :    0.000813407    0.000000014    0.000182902
               2   H   :   -0.000009419   -0.000000014   -0.000099467
               3   H   :   -0.000219108    0.000000002    0.000199363
               4   H   :   -0.000292432    0.000162047   -0.000141396
               5   H   :   -0.000292448   -0.000162050   -0.000141402
            
            Difference to translation invariance:
                       :    0.0000000000   -0.0000000000    0.0000000000
            
            Norm of the cartesian gradient     ...    0.0010277983
            RMS gradient                       ...    0.0002653764
            MAX gradient                       ...    0.0008134069
            
            -------
            TIMINGS
            -------
            
            Total SCF gradient time            ...        2.185 sec
            
            One electron gradient       ....       0.005 sec  (  0.2%)
            Prescreening matrices       ....       0.021 sec  (  1.0%)
            Two electron gradient       ....       0.189 sec  (  8.6%)
            XC gradient                 ....       1.820 sec  ( 83.3%)
            ------------------------------------------------------------------------------
                                     ORCA GEOMETRY RELAXATION STEP
            ------------------------------------------------------------------------------
            
            Reading the OPT-File                    .... done
            Getting information on internals        .... done
            Copying old internal coords+grads       .... done
            Making the new internal coordinates     .... (new redundants).... done
            Validating the new internal coordinates .... (new redundants).... done
            Calculating the B-matrix                .... done
            Calculating the G,G- and P matrices     .... done
            Transforming gradient to internals      .... done
            Projecting the internal gradient        .... done
            Number of atoms                         ....   5
            Number of internal coordinates          ....  10
            Current Energy                          ....   -40.523028276 Eh
            Current gradient norm                   ....     0.001027798 Eh/bohr
            Maximum allowed component of the step   ....  0.300
            Current trust radius                    ....  0.300
            Updating the Hessian (BFGS)             .... done
            Forming the augmented Hessian           .... done
            Diagonalizing the augmented Hessian     .... done
            Last element of RFO vector              ....  0.999975372
            Lowest eigenvalues of augmented Hessian:
             -0.000005877  0.113919606  0.114962320  0.124868829  0.134198879
            Length of the computed step             ....  0.007018439
            The final length of the internal step   ....  0.007018439
            Converting the step to cartesian space:
             Initial RMS(Int)=    0.0022194254
            Transforming coordinates:
             Iter   0:  RMS(Cart)=    0.0017749308 RMS(Int)=    0.0022148892
             Iter   1:  RMS(Cart)=    0.0000039411 RMS(Int)=    0.0000057352
             Iter   2:  RMS(Cart)=    0.0000000107 RMS(Int)=    0.0000000143
            done
            Storing new coordinates                 .... done
            
                                            .--------------------.
                      ----------------------|Geometry convergence|-------------------------
                      Item                value                   Tolerance       Converged
                      ---------------------------------------------------------------------
                      Energy change      -0.0002196145            0.0000010000      NO
                      RMS gradient        0.0002692785            0.0000300000      NO
                      MAX gradient        0.0003990074            0.0001000000      NO
                      RMS step            0.0022194254            0.0006000000      NO
                      MAX step            0.0032018153            0.0010000000      NO
                      ........................................................
                      Max(Bonds)      0.0002      Max(Angles)    0.18
                      Max(Dihed)        0.00      Max(Improp)    0.00
                      ---------------------------------------------------------------------
            
            The optimization has not yet converged - more geometry cycles are needed
            
            
                ---------------------------------------------------------------------------
                                     Redundant Internal Coordinates
                                        (Angstroem and degrees)
            
                    Definition                    Value    dE/dq     Step     New-Value
                ----------------------------------------------------------------------------
                 1. B(H   1,C   0)                1.0917 -0.000013  0.0002    1.0919   
                 2. B(H   2,C   0)                1.0919 -0.000126  0.0000    1.0919   
                 3. B(H   3,C   0)                1.0919 -0.000093  0.0002    1.0920   
                 4. B(H   4,C   0)                1.0919 -0.000093  0.0002    1.0920   
                 5. A(H   1,C   0,H   3)          109.66  0.000399   -0.18    109.48   
                 6. A(H   2,C   0,H   3)          109.30 -0.000357    0.17    109.47   
                 7. A(H   1,C   0,H   4)          109.66  0.000399   -0.18    109.48   
                 8. A(H   2,C   0,H   4)          109.30 -0.000357    0.17    109.47   
                 9. A(H   3,C   0,H   4)          109.34 -0.000284    0.16    109.50   
                10. A(H   1,C   0,H   2)          109.57  0.000194   -0.10    109.47   
                ----------------------------------------------------------------------------
            
                     *************************************************************
                     *                GEOMETRY OPTIMIZATION CYCLE   4            *
                     *************************************************************
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C     -0.000030    0.000000   -0.068687
              H      1.090973   -0.000000   -0.023458
              H     -0.320906   -0.000000   -1.112360
              H     -0.385013   -0.891749    0.430447
              H     -0.385013    0.891749    0.430447
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011   -0.000057    0.000000   -0.129799
               1 H     1.0000    0     1.008    2.061639   -0.000000   -0.044329
               2 H     1.0000    0     1.008   -0.606424   -0.000000   -2.102056
               3 H     1.0000    0     1.008   -0.727569   -1.685161    0.813427
               4 H     1.0000    0     1.008   -0.727569    1.685161    0.813427
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091940044245     0.00000000     0.00000000
             H      1   2   0     1.091885945655   109.46386902     0.00000000
             H      1   2   3     1.092044990486   109.46915128   119.99037167
             H      1   2   3     1.092044987334   109.46915251   240.00962481
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063467638285     0.00000000     0.00000000
             H      1   2   0     2.063365406765   109.46386902     0.00000000
             H      1   2   3     2.063665957940   109.46915128   119.99037167
             H      1   2   3     2.063665951982   109.46915251   240.00962481
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.531e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-770
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ... 134918 (   0.0 sec)
            # of grid points (after weights+screening)   ... 130872 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    3.4 sec
            Reduced shell lists constructed in    3.7 sec
            
            Total number of grid points                  ...   130872
            Total number of batches                      ...     2048
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...    26174
            Average number of shells per batch           ...    16.43 (82.13%)
            Average number of basis functions per batch  ...    37.30 (81.09%)
            Average number of large shells per batch     ...    15.22 (92.66%)
            Average number of large basis fcns per batch ...    34.47 (92.42%)
            Maximum spatial batch extension              ...  19.45, 17.31, 18.86 au
            Average spatial batch extension              ...   1.78,  1.73,  1.76 au
            
            Time for grid setup =    3.934 sec
            
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
                                  *** Initiating the SOSCF procedure ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              0    -40.52303005 -40.5230300516  0.000350  0.000350  0.000356  0.000026
                           *** Restarting incremental Fock matrix formation ***
              1    -40.52303107  -0.0000010229  0.000080  0.000089  0.000098  0.000008
              2    -40.52303112  -0.0000000502  0.000018  0.000030  0.000073  0.000003
              3    -40.52303113  -0.0000000017  0.000016  0.000014  0.000030  0.000001
              4    -40.52303113  -0.0000000021  0.000002  0.000002  0.000002  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   5 CYCLES          *
                           *****************************************************
            
            Total Energy       :          -40.52303113 Eh           -1102.68774 eV
              Last Energy change         ...   -2.4272e-11  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    8.9348e-07  Tolerance :   1.0000e-08
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            Total SCF time: 0 days 0 hours 0 min 8 sec 
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.523031128574
            -------------------------   --------------------
            
            ------------------------------------------------------------------------------
                                     ORCA SCF GRADIENT CALCULATION
            ------------------------------------------------------------------------------
            
            Gradient of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type      ... RKS
            Hartree-Fock exchange scaling    ...    0.200
            Number of operators              ...    1
            Number of atoms                  ...    5
            Basis set dimensions             ...   46
            Integral neglect threshold       ... 1.0e-12
            Integral primitive cutoff        ... 1.0e-14
            
            Nuclear repulsion gradient       ... done
            One Electron Gradient            ... done
            Pre-screening matrix             ... done
            Starting the two electron gradient:
            Two electron gradient done
            Exchange-correlation gradient    ... done
            
            ------------------
            CARTESIAN GRADIENT
            ------------------
            
               1   C   :    0.000016233    0.000000004   -0.000061786
               2   H   :   -0.000003060   -0.000000001   -0.000007549
               3   H   :    0.000016822   -0.000000002    0.000035736
               4   H   :   -0.000014997   -0.000073402    0.000016799
               5   H   :   -0.000014997    0.000073401    0.000016800
            
            Difference to translation invariance:
                       :    0.0000000000   -0.0000000000   -0.0000000000
            
            Norm of the cartesian gradient     ...    0.0001322769
            RMS gradient                       ...    0.0000341537
            MAX gradient                       ...    0.0000734019
            
            -------
            TIMINGS
            -------
            
            Total SCF gradient time            ...        2.357 sec
            
            One electron gradient       ....       0.005 sec  (  0.2%)
            Prescreening matrices       ....       0.019 sec  (  0.8%)
            Two electron gradient       ....       0.286 sec  ( 12.1%)
            XC gradient                 ....       1.886 sec  ( 80.0%)
            ------------------------------------------------------------------------------
                                     ORCA GEOMETRY RELAXATION STEP
            ------------------------------------------------------------------------------
            
            Reading the OPT-File                    .... done
            Getting information on internals        .... done
            Copying old internal coords+grads       .... done
            Making the new internal coordinates     .... (new redundants).... done
            Validating the new internal coordinates .... (new redundants).... done
            Calculating the B-matrix                .... done
            Calculating the G,G- and P matrices     .... done
            Transforming gradient to internals      .... done
            Projecting the internal gradient        .... done
            Number of atoms                         ....   5
            Number of internal coordinates          ....  10
            Current Energy                          ....   -40.523031129 Eh
            Current gradient norm                   ....     0.000132277 Eh/bohr
            Maximum allowed component of the step   ....  0.300
            Current trust radius                    ....  0.300
            Updating the Hessian (BFGS)             .... done
            Forming the augmented Hessian           .... done
            Diagonalizing the augmented Hessian     .... done
            Last element of RFO vector              ....  0.999999892
            Lowest eigenvalues of augmented Hessian:
             -0.000000051  0.113919606  0.119505570  0.122485369  0.134198879
            Length of the computed step             ....  0.000463968
            The final length of the internal step   ....  0.000463968
            Converting the step to cartesian space:
             Initial RMS(Int)=    0.0001467195
            Transforming coordinates:
             Iter   0:  RMS(Cart)=    0.0001403290 RMS(Int)=    0.0001465872
             Iter   1:  RMS(Cart)=    0.0000000100 RMS(Int)=    0.0000000140
            done
            Storing new coordinates                 .... done
            
                                            .--------------------.
                      ----------------------|Geometry convergence|-------------------------
                      Item                value                   Tolerance       Converged
                      ---------------------------------------------------------------------
                      Energy change      -0.0000028527            0.0000010000      NO
                      RMS gradient        0.0000382164            0.0000300000      NO
                      MAX gradient        0.0000729043            0.0001000000      YES
                      RMS step            0.0001467195            0.0006000000      YES
                      MAX step            0.0003065357            0.0010000000      YES
                      ........................................................
                      Max(Bonds)      0.0001      Max(Angles)    0.02
                      Max(Dihed)        0.00      Max(Improp)    0.00
                      ---------------------------------------------------------------------
            
                   The step convergence is overachieved with 
                   reasonable convergence on the gradient
                   Convergence will therefore be signaled now
            
            
                                ***********************HURRAY********************
                                ***        THE OPTIMIZATION HAS CONVERGED     ***
                                *************************************************
            
            
                ---------------------------------------------------------------------------
                                     Redundant Internal Coordinates
            
                                      --- Optimized Parameters ---  
                                        (Angstroem and degrees)
            
                    Definition                    OldVal   dE/dq     Step     FinalVal
                ----------------------------------------------------------------------------
                 1. B(H   1,C   0)                1.0919 -0.000003  0.0000    1.0919   
                 2. B(H   2,C   0)                1.0919 -0.000039  0.0001    1.0919   
                 3. B(H   3,C   0)                1.0920  0.000073 -0.0001    1.0919   
                 4. B(H   4,C   0)                1.0920  0.000073 -0.0001    1.0919   
                 5. A(H   1,C   0,H   3)          109.47 -0.000004    0.00    109.47   
                 6. A(H   2,C   0,H   3)          109.47 -0.000008    0.00    109.47   
                 7. A(H   1,C   0,H   4)          109.47 -0.000004    0.00    109.47   
                 8. A(H   2,C   0,H   4)          109.47 -0.000008    0.00    109.47   
                 9. A(H   3,C   0,H   4)          109.49  0.000044   -0.02    109.47   
                10. A(H   1,C   0,H   2)          109.46 -0.000019    0.01    109.47   
                ----------------------------------------------------------------------------
                             *******************************************************
                             *** FINAL ENERGY EVALUATION AT THE STATIONARY POINT ***
                             ***               (AFTER    4 CYCLES)               ***
                             *******************************************************
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000003    0.000000   -0.068722
              H      1.091004   -0.000000   -0.023418
              H     -0.320952   -0.000000   -1.112430
              H     -0.385022   -0.891564    0.430480
              H     -0.385022    0.891564    0.430480
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000005    0.000000   -0.129866
               1 H     1.0000    0     1.008    2.061699   -0.000000   -0.044253
               2 H     1.0000    0     1.008   -0.606512   -0.000000   -2.102188
               3 H     1.0000    0     1.008   -0.727586   -1.684812    0.813489
               4 H     1.0000    0     1.008   -0.727586    1.684812    0.813489
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091941497635     0.00000000     0.00000000
             H      1   2   0     1.091942628556   109.47127220     0.00000000
             H      1   2   3     1.091939901594   109.47132124   120.00008188
             H      1   2   3     1.091939901421   109.47132127   239.99991794
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063470384794     0.00000000     0.00000000
             H      1   2   0     2.063472521925   109.47127220     0.00000000
             H      1   2   3     2.063467368713   109.47132124   120.00008188
             H      1   2   3     2.063467368386   109.47132127   239.99991794
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 10s4p2d1f contracted to 3s2p2d1f pattern {631/31/11/1}
             Group   2 Type H   : 4s1p contracted to 2s1p pattern {31/1}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      18.7311369600      0.0334946000
               2       2.8253943700      0.2347269502
               3       0.6401216900      0.8137573307
             S 1 
               1       0.1612777600      1.0000000000
             P 1 
               1       1.1000000000      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    3047.5248800000      0.0018347400
               2     457.3695180000      0.0140373200
               3     103.9486850000      0.0688426199
               4      29.2101553000      0.2321844397
               5       9.2866629600      0.4679413494
               6       3.1639269600      0.3623119895
             S 3 
               1       7.8682723500     -0.1193324197
               2       1.8812885400     -0.1608541495
               3       0.5442492600      1.1434564368
             P 3 
               1       7.8682723500      0.0689990700
               2       1.8812885400      0.3164239600
               3       0.5442492600      0.7443082900
             S 1 
               1       0.1687144800      1.0000000000
             P 1 
               1       0.1687144800      1.0000000000
             D 1 
               1       1.6000000000      1.0000000000
             D 1 
               1       0.4000000000      1.0000000000
             F 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   37
             # of primitive gaussian functions       ...   67
             # of contracted shells                  ...   20
             # of contracted basis functions         ...   46
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Density Functional     Method          .... DFT(GTOs)
             Exchange Functional    Exchange        .... B88
               X-Alpha parameter    XAlpha          ....  0.666667
               Becke's b parameter  XBeta           ....  0.004200
             Correlation Functional Correlation     .... LYP
             LDA part of GGA corr.  LDAOpt          .... VWN-3
             Gradients option       PostSCFGGA      .... off
             Hybrid DFT is turned on
               Fraction HF Exchange ScalHFX         ....  0.200000
               Scaling of DF-GGA-X  ScalDFX         ....  0.720000
               Scaling of DF-GGA-C  ScalDFC         ....  0.810000
               Scaling of DF-LDA-C  ScalLDAC        ....  1.000000
               Perturbative correction              ....  0.000000
               Density functional embedding theory  .... OFF
               NL short-range parameter             ....  4.800000
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....   46
             Nuclear Repulsion      ENuc            ....     13.4115070799 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.530e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            ---------------------
            INITIAL GUESS: MOREAD
            ---------------------
            Guess MOs are being read from file: input.gbw
            Input Geometry matches current geometry (good)
            Input basis set matches current basis set (good)
            MOs were renormalized
            MOs were reorthogonalized (Cholesky)
                                  ------------------
                                  INITIAL GUESS DONE (   0.0 sec)
                                  ------------------
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-770
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ... 134918 (   0.0 sec)
            # of grid points (after weights+screening)   ... 130872 (   0.1 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    3.5 sec
            Reduced shell lists constructed in    3.7 sec
            
            Total number of grid points                  ...   130872
            Total number of batches                      ...     2049
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...    26174
            Average number of shells per batch           ...    16.42 (82.12%)
            Average number of basis functions per batch  ...    37.30 (81.08%)
            Average number of large shells per batch     ...    15.22 (92.66%)
            Average number of large basis fcns per batch ...    34.46 (92.41%)
            Maximum spatial batch extension              ...  19.53, 17.31, 18.86 au
            Average spatial batch extension              ...   1.79,  1.74,  1.77 au
            
            Time for grid setup =    3.877 sec
            
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
                                  *** Initiating the SOSCF procedure ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              0    -40.52303115 -40.5230311483  0.000023  0.000023  0.000023  0.000002
                           *** Restarting incremental Fock matrix formation ***
              1    -40.52303115  -0.0000000049  0.000007  0.000010  0.000014  0.000001
              2    -40.52303115  -0.0000000002  0.000004  0.000004  0.000007  0.000000
              3    -40.52303115  -0.0000000002  0.000001  0.000001  0.000001  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   4 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.52303115 Eh           -1102.68774 eV
            
            Components:
            Nuclear Repulsion  :           13.41150708 Eh             364.94566 eV
            Electronic Energy  :          -53.93453823 Eh           -1467.63340 eV
            One Electron Energy:          -79.80862921 Eh           -2171.70321 eV
            Two Electron Energy:           25.87409097 Eh             704.06981 eV
            
            Virial components:
            Potential Energy   :          -80.68058655 Eh           -2195.43037 eV
            Kinetic Energy     :           40.15755540 Eh            1092.74264 eV
            Virial Ratio       :            2.00910105
            
            
            DFT components:
            N(Alpha)           :        5.000000006721 electrons
            N(Beta)            :        5.000000006721 electrons
            N(Total)           :       10.000000013443 electrons
            E(X)               :       -5.208629179371 Eh       
            E(C)               :       -0.387468478262 Eh       
            E(XC)              :       -5.596097657633 Eh       
            DFET-embed. en.    :        0.000000000000 Eh       
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -3.2898e-12  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    2.9590e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    2.2287e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    3.8516e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    2.9030e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -10.164302      -276.5847 
               1   2.0000      -0.689777       -18.7698 
               2   2.0000      -0.387714       -10.5502 
               3   2.0000      -0.387713       -10.5502 
               4   2.0000      -0.387713       -10.5502 
               5   0.0000       0.118158         3.2152 
               6   0.0000       0.176397         4.8000 
               7   0.0000       0.176398         4.8000 
               8   0.0000       0.176398         4.8000 
               9   0.0000       0.508217        13.8293 
              10   0.0000       0.508218        13.8293 
              11   0.0000       0.508218        13.8293 
              12   0.0000       0.755885        20.5687 
              13   0.0000       0.755886        20.5687 
              14   0.0000       0.755886        20.5687 
              15   0.0000       0.764139        20.7933 
              16   0.0000       0.764139        20.7933 
              17   0.0000       0.894712        24.3464 
              18   0.0000       1.109753        30.1979 
              19   0.0000       1.690321        45.9960 
              20   0.0000       1.690323        45.9960 
              21   0.0000       1.690325        45.9961 
              22   0.0000       1.955998        53.2254 
              23   0.0000       1.955998        53.2254 
              24   0.0000       1.955999        53.2254 
              25   0.0000       2.418214        65.8029 
              26   0.0000       2.418214        65.8029 
              27   0.0000       2.418217        65.8030 
              28   0.0000       2.859195        77.8027 
              29   0.0000       2.859197        77.8027 
              30   0.0000       2.859198        77.8027 
              31   0.0000       3.022656        82.2507 
              32   0.0000       3.022659        82.2507 
              33   0.0000       3.107355        84.5554 
              34   0.0000       3.713114       101.0390 
              35   0.0000       3.713117       101.0390 
              36   0.0000       3.713118       101.0391 
              37   0.0000       3.945278       107.3565 
              38   0.0000       3.945280       107.3565 
              39   0.0000       3.945280       107.3565 
              40   0.0000       4.152205       112.9872 
              41   0.0000       4.241942       115.4291 
              42   0.0000       4.241942       115.4291 
              43   0.0000       4.734773       128.8397 
              44   0.0000       4.734775       128.8398 
              45   0.0000       4.734780       128.8399 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.517270
               1 H :    0.129318
               2 H :    0.129318
               3 H :    0.129317
               4 H :    0.129317
            Sum of atomic charges:   -0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.293470  s :     3.293470
                  pz      :     1.063289  p :     3.189865
                  px      :     1.063288
                  py      :     1.063288
                  dz2     :     0.008618  d :     0.032081
                  dxz     :     0.003191
                  dyz     :     0.006705
                  dx2y2   :     0.009578
                  dxy     :     0.003989
                  f0      :     0.000495  f :     0.001854
                  f+1     :     0.000354
                  f-1     :     0.000000
                  f+2     :     0.000228
                  f-2     :     0.000169
                  f+3     :     0.000585
                  f-3     :     0.000023
              1 H s       :     0.859167  s :     0.859167
                  pz      :     0.002414  p :     0.011515
                  px      :     0.006695
                  py      :     0.002406
              2 H s       :     0.859167  s :     0.859167
                  pz      :     0.006331  p :     0.011515
                  px      :     0.002778
                  py      :     0.002406
              3 H s       :     0.859167  s :     0.859167
                  pz      :     0.003304  p :     0.011515
                  px      :     0.002941
                  py      :     0.005271
              4 H s       :     0.859167  s :     0.859167
                  pz      :     0.003304  p :     0.011515
                  px      :     0.002941
                  py      :     0.005271
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :   -0.438158
               1 H :    0.109540
               2 H :    0.109540
               3 H :    0.109539
               4 H :    0.109539
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     2.938793  s :     2.938793
                  pz      :     1.124282  p :     3.372845
                  px      :     1.124282
                  py      :     1.124282
                  dz2     :     0.030694  d :     0.114253
                  dxz     :     0.011364
                  dyz     :     0.023879
                  dx2y2   :     0.034110
                  dxy     :     0.014205
                  f0      :     0.002346  f :     0.012267
                  f+1     :     0.002495
                  f-1     :     0.000005
                  f+2     :     0.001523
                  f-2     :     0.002520
                  f+3     :     0.003029
                  f-3     :     0.000348
              1 H s       :     0.849217  s :     0.849217
                  pz      :     0.008286  p :     0.041243
                  px      :     0.024700
                  py      :     0.008257
              2 H s       :     0.849217  s :     0.849217
                  pz      :     0.023305  p :     0.041243
                  px      :     0.009680
                  py      :     0.008257
              3 H s       :     0.849218  s :     0.849218
                  pz      :     0.011700  p :     0.041243
                  px      :     0.010305
                  py      :     0.019238
              4 H s       :     0.849218  s :     0.849218
                  pz      :     0.011700  p :     0.041243
                  px      :     0.010305
                  py      :     0.019238
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.5173     6.0000    -0.5173     3.8969     3.8969     0.0000
              1 H      0.8707     1.0000     0.1293     0.9551     0.9551    -0.0000
              2 H      0.8707     1.0000     0.1293     0.9551     0.9551    -0.0000
              3 H      0.8707     1.0000     0.1293     0.9551     0.9551    -0.0000
              4 H      0.8707     1.0000     0.1293     0.9551     0.9551    -0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9742 B(  0-C ,  2-H ) :   0.9742 B(  0-C ,  3-H ) :   0.9742 
            B(  0-C ,  4-H ) :   0.9742 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 8 sec 
            
            Total time                  ....       8.111 sec
            Sum of individual times     ....       7.821 sec  ( 96.4%)
            
            Fock matrix formation       ....       3.940 sec  ( 48.6%)
              XC integration            ....       3.135 sec  ( 79.6% of F)
                Basis function eval.    ....       1.356 sec  ( 43.2% of XC)
                Density eval.           ....       0.488 sec  ( 15.6% of XC)
                XC-Functional eval.     ....       0.593 sec  ( 18.9% of XC)
                XC-Potential eval.      ....       0.460 sec  ( 14.7% of XC)
            Diagonalization             ....       0.000 sec  (  0.0%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.0%)
            Initial guess               ....       0.001 sec  (  0.0%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.000 sec  (  0.0%)
            SOSCF solution              ....       0.001 sec  (  0.0%)
            Grid generation             ....       3.877 sec  ( 47.8%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.523031153574
            -------------------------   --------------------
            
                                            *** OPTIMIZATION RUN DONE ***
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000005,  0.000000 -0.129866)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000      -0.00000
            Nuclear contribution   :     -0.00000      -0.00000      -0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000       0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00001
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078689 157685.033219 157684.479617 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000    -0.000002     0.000000 
            x,y,z [Debye]:     0.000000    -0.000006     0.000000 
            
             
            
            -------------------------------------------------------------------------------
                                           ORCA SCF HESSIAN
            -------------------------------------------------------------------------------
            
            Hessian of the Kohn-Sham DFT energy:
            Kohn-Sham wavefunction type                      ... RKS
            Hartree-Fock exchange scaling                    ...    0.200
            Number of operators                              ...    1
            Number of atoms                                  ...    5
            Basis set dimensions                             ...   46
            Integral neglect threshold                       ... 1.0e-12
            Integral primitive cutoff                        ... 1.0e-14
            
            Setting up DFT Hessian calculations              ... 
            Electron density on the grid                     ... found on disk
            Building xc-kernel on the grid                   ... done   (      0.2 sec)
                                                                 done   (      0.2 sec)
            
            Nuclear repulsion Hessian                        ... done   (      0.0 sec)
            
            ----------------------------------------------
            Forming right-hand sides of CP-SCF equations     ...
            ----------------------------------------------
            One electron integral derivatives                ... done   (      0.1 sec)
            Transforming the overlap derivative matrices     ... done   (      0.0 sec)
            Making the Q(x) pseudodensities                  ... done   (      0.0 sec)
            Adding the E*S(x)*S(y) terms to the Hessian      ... done   (      0.0 sec)
            Calculating energy weighted overlap derivatives  ... done   (      0.0 sec)
            Two electron integral derivatives                ... done   (      0.3 sec)
            Exchange-correlation integral derivatives        ... done   (      8.7 sec)
            tr(F(y)Q(x)) contribution to the Hessian         ... done   (      0.0 sec)
            Response fock operator R(S(x))                   ... done   (      0.2 sec)
            XC Response fock operator R(S(x))                ... done   (      2.6 sec)
            tr(F(y)S(x)) contribution to the Hessian         ... done   (      0.0 sec)
            Transforming and finalizing RHSs                 ... done   (      0.0 sec)
            
            ----------------------------------------------
            Solving the CP-SCF equations                     ...
            ----------------------------------------------
                 CP-SCF ITERATION   0: 
                 CP-SCF ITERATION   1:      0.000142789189
                 CP-SCF ITERATION   2:      0.000003959512
                 CP-SCF ITERATION   3:      0.000000009928
                 CP-SCF ITERATION   4:      0.000000000055
            
                                                             ... done   (     16.9 sec)
            Forming perturbed density Hessian contributions  ... done   (      0.0 sec)
            Making the perturbed densities                   ... done   (      0.0 sec)
            2nd integral derivative contribs                 ... done   (      1.5 sec)
            Exchange-correlation Hessian                     ... done   (     13.7 sec)
            Dipol derivatives                                ... done   (      0.1 sec)
            
            Total SCF Hessian time: 0 days 0 hours 0 min 44 sec 
            
            Writing the Hessian file to the disk             ... done
            
            
            Maximum memory used throughout the entire calculation: 150.9 MB
            
            -----------------------
            VIBRATIONAL FREQUENCIES
            -----------------------
            
            Scaling factor for frequencies =  1.000000000  (already applied!)
            
               0:         0.00 cm**-1
               1:         0.00 cm**-1
               2:         0.00 cm**-1
               3:         0.00 cm**-1
               4:         0.00 cm**-1
               5:         0.00 cm**-1
               6:      1343.12 cm**-1
               7:      1343.13 cm**-1
               8:      1343.13 cm**-1
               9:      1564.00 cm**-1
              10:      1564.00 cm**-1
              11:      3042.76 cm**-1
              12:      3156.57 cm**-1
              13:      3156.58 cm**-1
              14:      3156.59 cm**-1
            
            
            ------------
            NORMAL MODES
            ------------
            
            These modes are the Cartesian displacements weighted by the diagonal matrix
            M(i,i)=1/sqrt(m[i]) where m[i] is the mass of the displaced atom
            Thus, these vectors are normalized but *not* orthogonal
            
                              0          1          2          3          4          5    
                  0       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  1       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  2       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  3       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  4       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  5       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  6       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  7       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  8       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                  9       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 10       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 11       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 12       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 13       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                 14       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
                              6          7          8          9         10         11    
                  0       0.094434   0.081873   0.000015   0.000000  -0.000000   0.000002
                  1      -0.000004   0.000026  -0.124984  -0.000000  -0.000000  -0.000000
                  2       0.081873  -0.094435  -0.000022  -0.000000   0.000001  -0.000007
                  3       0.086970   0.037246   0.000005  -0.000009   0.020745  -0.499591
                  4       0.000017  -0.000127   0.604133  -0.499996  -0.000214   0.000000
                  5      -0.373178   0.474441   0.000110   0.000214  -0.499573  -0.020748
                  6      -0.283082  -0.504008  -0.000098  -0.000205   0.477915   0.146984
                  7       0.000017  -0.000127   0.604127   0.500002   0.000214   0.000000
                  8       0.168079   0.104394   0.000017   0.000063  -0.146965   0.477971
                  9      -0.464575  -0.254362  -0.200259   0.396026  -0.249159   0.176289
                 10      -0.018767   0.327268   0.140575  -0.000124   0.288674   0.408214
                 11      -0.385229   0.273153   0.259658   0.305228   0.323396  -0.228567
                 12      -0.464563  -0.254446   0.200178  -0.395813  -0.249499   0.176289
                 13       0.018775  -0.327327   0.140436   0.000124  -0.288674  -0.408214
                 14      -0.385244   0.273262  -0.259522  -0.305505   0.323134  -0.228567
                              12         13         14    
                  0      -0.050749  -0.076724  -0.000007
                  1       0.000002  -0.000010   0.091989
                  2      -0.076724   0.050749   0.000007
                  3       0.505170   0.697398   0.000066
                  4       0.000000  -0.000002   0.019904
                  5       0.004832   0.040630   0.000004
                  6       0.237666  -0.089722  -0.000015
                  7       0.000000  -0.000002   0.019904
                  8       0.791971  -0.226799  -0.000042
                  9      -0.069071   0.153300  -0.253853
                 10      -0.134514   0.393423  -0.567914
                 11       0.058715  -0.209304   0.329131
                 12      -0.069060   0.153244   0.253890
                 13       0.134489  -0.393298  -0.568007
                 14       0.058700  -0.209231  -0.329180
            
            
            -----------
            IR SPECTRUM
            -----------
            
             Mode    freq (cm**-1)   T**2         TX         TY         TZ
            -------------------------------------------------------------------
               6:      1343.12   10.824683  ( -2.485937   0.000092  -2.155180)
               7:      1343.13   10.824153  ( -2.155211  -0.000691   2.485803)
               8:      1343.13   10.823459  ( -0.000383   3.289903   0.000583)
               9:      1564.00    0.000000  (  0.000000   0.000064  -0.000000)
              10:      1564.00    0.000000  ( -0.000091   0.000000   0.000206)
              11:      3042.76    0.000000  (  0.000151  -0.000000  -0.000413)
              12:      3156.57   21.725960  ( -2.571467   0.000103  -3.887611)
              13:      3156.58   21.725551  ( -3.887601  -0.000513   2.571403)
              14:      3156.59   21.724866  ( -0.000371   4.660994   0.000369)
            
            The first frequency considered to be a vibration is 6
            The total number of vibrations considered is 9
            
            
            --------------------------
            THERMOCHEMISTRY AT 273.15K
            --------------------------
            
            Temperature         ... 273.15 K
            Pressure            ... 1.00 atm
            Total Mass          ... 16.04 AMU
            
            Throughout the following assumptions are being made:
              (1) The electronic state is orbitally nondegenerate
              (2) There are no thermally accessible electronically excited states
              (3) Hindered rotations indicated by low frequency modes are not
                  treated as such but are treated as vibrations and this may
                  cause some error
              (4) All equations used are the standard statistical mechanics
                  equations for an ideal gas
              (5) All vibrations are strictly harmonic
            
            freq.    1343.12  E(vib)   ...       0.00 
            freq.    1343.13  E(vib)   ...       0.00 
            freq.    1343.13  E(vib)   ...       0.00 
            freq.    1564.00  E(vib)   ...       0.00 
            freq.    1564.00  E(vib)   ...       0.00 
            freq.    3042.76  E(vib)   ...       0.00 
            freq.    3156.57  E(vib)   ...       0.00 
            freq.    3156.58  E(vib)   ...       0.00 
            freq.    3156.59  E(vib)   ...       0.00 
            
            ------------
            INNER ENERGY
            ------------
            
            The inner energy is: U= E(el) + E(ZPE) + E(vib) + E(rot) + E(trans)
                E(el)   - is the total energy from the electronic structure calculation
                          = E(kin-el) + E(nuc-el) + E(el-el) + E(nuc-nuc)
                E(ZPE)  - the the zero temperature vibrational energy from the frequency calculation
                E(vib)  - the the finite temperature correction to E(ZPE) due to population
                          of excited vibrational states
                E(rot)  - is the rotational thermal energy
                E(trans)- is the translational thermal energy
            
            Summary of contributions to the inner energy U:
            Electronic energy                ...    -40.52303115 Eh
            Zero point energy                ...      0.04481131 Eh      28.12 kcal/mol
            Thermal vibrational correction   ...      0.00001933 Eh       0.01 kcal/mol
            Thermal rotational correction    ...      0.00129752 Eh       0.81 kcal/mol
            Thermal translational correction ...      0.00129752 Eh       0.81 kcal/mol
            -----------------------------------------------------------------------
            Total thermal energy                    -40.47560549 Eh
            
            
            Summary of corrections to the electronic energy:
            (perhaps to be used in another calculation)
            Total thermal correction                  0.00261436 Eh       1.64 kcal/mol
            Non-thermal (ZPE) correction              0.04481131 Eh      28.12 kcal/mol
            -----------------------------------------------------------------------
            Total correction                          0.04742567 Eh      29.76 kcal/mol
            
            
            --------
            ENTHALPY
            --------
            
            The enthalpy is H = U + kB*T
                            kB is Boltzmann's constant
            Total free energy                 ...    -40.47560549 Eh 
            Thermal Enthalpy correction       ...      0.00086504 Eh       0.54 kcal/mol
            -----------------------------------------------------------------------
            Total Enthalpy                    ...    -40.47474045 Eh
            
            
            Note: Rotational entropy computed according to Herzberg 
            Infrared and Raman Spectra, Chapter V,1, Van Nostrand Reinhold, 1945 
            Point Group:  Cs, Symmetry Number:   1  
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            
            Vibrational entropy computed according to the QRRHO of S. Grimme
            Chem.Eur.J. 2012 18 9955
            
            
            -------
            ENTROPY
            -------
            
            The entropy contributions are T*S = T*(S(el)+S(vib)+S(rot)+S(trans))
                 S(el)   - electronic entropy
                 S(vib)  - vibrational entropy
                 S(rot)  - rotational entropy
                 S(trans)- translational entropy
            The entropies will be listed as mutliplied by the temperature to get
            units of energy
            
            Electronic entropy                ...      0.00000000 Eh      0.00 kcal/mol
            Vibrational entropy               ...      0.00002199 Eh      0.01 kcal/mol
            Rotational entropy                ...      0.00644570 Eh      4.04 kcal/mol
            Translational entropy             ...      0.01472517 Eh      9.24 kcal/mol
            -----------------------------------------------------------------------
            Final entropy term                ...      0.02119286 Eh     13.30 kcal/mol
            
            In case the symmetry of your molecule has not been determined correctly
            or in case you have a reason to use a different symmetry number we print 
            out the resulting rotational entropy values for sn=1,12 :
             --------------------------------------------------------
            |  sn= 1 | S(rot)=       0.00644570 Eh      4.04 kcal/mol|
            |  sn= 2 | S(rot)=       0.00584612 Eh      3.67 kcal/mol|
            |  sn= 3 | S(rot)=       0.00549538 Eh      3.45 kcal/mol|
            |  sn= 4 | S(rot)=       0.00524654 Eh      3.29 kcal/mol|
            |  sn= 5 | S(rot)=       0.00505351 Eh      3.17 kcal/mol|
            |  sn= 6 | S(rot)=       0.00489580 Eh      3.07 kcal/mol|
            |  sn= 7 | S(rot)=       0.00476246 Eh      2.99 kcal/mol|
            |  sn= 8 | S(rot)=       0.00464696 Eh      2.92 kcal/mol|
            |  sn= 9 | S(rot)=       0.00454507 Eh      2.85 kcal/mol|
            |  sn=10 | S(rot)=       0.00445393 Eh      2.79 kcal/mol|
            |  sn=11 | S(rot)=       0.00437149 Eh      2.74 kcal/mol|
            |  sn=12 | S(rot)=       0.00429622 Eh      2.70 kcal/mol|
             --------------------------------------------------------
            
            
            -------------------
            GIBBS FREE ENERGY
            -------------------
            
            The Gibbs free energy is G = H - T*S
            
            Total enthalpy                    ...    -40.47474045 Eh 
            Total entropy correction          ...     -0.02119286 Eh    -13.30 kcal/mol
            -----------------------------------------------------------------------
            Final Gibbs free energy         ...    -40.49593331 Eh
            
            For completeness - the Gibbs free energy minus the electronic energy
            G-E(el)                           ...      0.02709785 Eh     17.00 kcal/mol
            
            
            The first frequency considered to be a vibration is 6
            The total number of vibrations considered is 9
            
            
            --------------------------
            THERMOCHEMISTRY AT 298.15K
            --------------------------
            
            Temperature         ... 298.15 K
            Pressure            ... 1.00 atm
            Total Mass          ... 16.04 AMU
            
            Throughout the following assumptions are being made:
              (1) The electronic state is orbitally nondegenerate
              (2) There are no thermally accessible electronically excited states
              (3) Hindered rotations indicated by low frequency modes are not
                  treated as such but are treated as vibrations and this may
                  cause some error
              (4) All equations used are the standard statistical mechanics
                  equations for an ideal gas
              (5) All vibrations are strictly harmonic
            
            freq.    1343.12  E(vib)   ...       0.01 
            freq.    1343.13  E(vib)   ...       0.01 
            freq.    1343.13  E(vib)   ...       0.01 
            freq.    1564.00  E(vib)   ...       0.00 
            freq.    1564.00  E(vib)   ...       0.00 
            freq.    3042.76  E(vib)   ...       0.00 
            freq.    3156.57  E(vib)   ...       0.00 
            freq.    3156.58  E(vib)   ...       0.00 
            freq.    3156.59  E(vib)   ...       0.00 
            
            ------------
            INNER ENERGY
            ------------
            
            The inner energy is: U= E(el) + E(ZPE) + E(vib) + E(rot) + E(trans)
                E(el)   - is the total energy from the electronic structure calculation
                          = E(kin-el) + E(nuc-el) + E(el-el) + E(nuc-nuc)
                E(ZPE)  - the the zero temperature vibrational energy from the frequency calculation
                E(vib)  - the the finite temperature correction to E(ZPE) due to population
                          of excited vibrational states
                E(rot)  - is the rotational thermal energy
                E(trans)- is the translational thermal energy
            
            Summary of contributions to the inner energy U:
            Electronic energy                ...    -40.52303115 Eh
            Zero point energy                ...      0.04481131 Eh      28.12 kcal/mol
            Thermal vibrational correction   ...      0.00003570 Eh       0.02 kcal/mol
            Thermal rotational correction    ...      0.00141627 Eh       0.89 kcal/mol
            Thermal translational correction ...      0.00141627 Eh       0.89 kcal/mol
            -----------------------------------------------------------------------
            Total thermal energy                    -40.47535160 Eh
            
            
            Summary of corrections to the electronic energy:
            (perhaps to be used in another calculation)
            Total thermal correction                  0.00286825 Eh       1.80 kcal/mol
            Non-thermal (ZPE) correction              0.04481131 Eh      28.12 kcal/mol
            -----------------------------------------------------------------------
            Total correction                          0.04767955 Eh      29.92 kcal/mol
            
            
            --------
            ENTHALPY
            --------
            
            The enthalpy is H = U + kB*T
                            kB is Boltzmann's constant
            Total free energy                 ...    -40.47535160 Eh 
            Thermal Enthalpy correction       ...      0.00094421 Eh       0.59 kcal/mol
            -----------------------------------------------------------------------
            Total Enthalpy                    ...    -40.47440739 Eh
            
            
            Note: Rotational entropy computed according to Herzberg 
            Infrared and Raman Spectra, Chapter V,1, Van Nostrand Reinhold, 1945 
            Point Group:  Cs, Symmetry Number:   1  
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            
            Vibrational entropy computed according to the QRRHO of S. Grimme
            Chem.Eur.J. 2012 18 9955
            
            
            -------
            ENTROPY
            -------
            
            The entropy contributions are T*S = T*(S(el)+S(vib)+S(rot)+S(trans))
                 S(el)   - electronic entropy
                 S(vib)  - vibrational entropy
                 S(rot)  - rotational entropy
                 S(trans)- translational entropy
            The entropies will be listed as mutliplied by the temperature to get
            units of energy
            
            Electronic entropy                ...      0.00000000 Eh      0.00 kcal/mol
            Vibrational entropy               ...      0.00004106 Eh      0.03 kcal/mol
            Rotational entropy                ...      0.00715967 Eh      4.49 kcal/mol
            Translational entropy             ...      0.01627961 Eh     10.22 kcal/mol
            -----------------------------------------------------------------------
            Final entropy term                ...      0.02348033 Eh     14.73 kcal/mol
            
            In case the symmetry of your molecule has not been determined correctly
            or in case you have a reason to use a different symmetry number we print 
            out the resulting rotational entropy values for sn=1,12 :
             --------------------------------------------------------
            |  sn= 1 | S(rot)=       0.00715967 Eh      4.49 kcal/mol|
            |  sn= 2 | S(rot)=       0.00650521 Eh      4.08 kcal/mol|
            |  sn= 3 | S(rot)=       0.00612238 Eh      3.84 kcal/mol|
            |  sn= 4 | S(rot)=       0.00585075 Eh      3.67 kcal/mol|
            |  sn= 5 | S(rot)=       0.00564007 Eh      3.54 kcal/mol|
            |  sn= 6 | S(rot)=       0.00546792 Eh      3.43 kcal/mol|
            |  sn= 7 | S(rot)=       0.00532238 Eh      3.34 kcal/mol|
            |  sn= 8 | S(rot)=       0.00519630 Eh      3.26 kcal/mol|
            |  sn= 9 | S(rot)=       0.00508509 Eh      3.19 kcal/mol|
            |  sn=10 | S(rot)=       0.00498561 Eh      3.13 kcal/mol|
            |  sn=11 | S(rot)=       0.00489562 Eh      3.07 kcal/mol|
            |  sn=12 | S(rot)=       0.00481347 Eh      3.02 kcal/mol|
             --------------------------------------------------------
            
            
            -------------------
            GIBBS FREE ENERGY
            -------------------
            
            The Gibbs free energy is G = H - T*S
            
            Total enthalpy                    ...    -40.47440739 Eh 
            Total entropy correction          ...     -0.02348033 Eh    -14.73 kcal/mol
            -----------------------------------------------------------------------
            Final Gibbs free energy         ...    -40.49788772 Eh
            
            For completeness - the Gibbs free energy minus the electronic energy
            G-E(el)                           ...      0.02514343 Eh     15.78 kcal/mol
            
            
            Timings for individual modules:
            
            Sum of individual times         ...      148.912 sec (=   2.482 min)
            GTO integral calculation        ...        1.481 sec (=   0.025 min)   1.0 %
            SCF iterations                  ...       48.596 sec (=   0.810 min)  32.6 %
            SCF Gradient evaluation         ...        8.915 sec (=   0.149 min)   6.0 %
            Geometry relaxation             ...        0.330 sec (=   0.006 min)   0.2 %
            Analytical frequency calculation...       89.589 sec (=   1.493 min)  60.2 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 2 minutes 31 seconds 547 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: MDCI localization with Augmented Hessian Foster-Boys
              ===> : Switching off randomization!
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! CCSD(T) Printbasis
            |  2> * xyz   0  1
            |  3> C     0.00000024    -0.00000002     0.00000000
            |  4> H     1.07698196    -0.18012947    -0.00002129
            |  5> H    -0.52882274    -0.95534548     0.00013221
            |  6> H    -0.27411608     0.56763359    -0.89161936
            |  7> H    -0.27404603     0.56784158     0.89150844
            |  8> *
            |  9> %MaxCore    64000
            | 10> %scf
            | 11>   MaxIter 500
            | 12>   Convergence VeryTight
            | 13> end
            | 14> %pal nprocs     1
            | 15> end
            | 16> %method
            | 17>   IntAcc 7.0
            | 18>   NewNCore C     2 end
            | 19>   NewNCore H     0 end
            | 20> end
            | 21> %basis
            | 22>      NewGTO   C
            | 23>      S  6
            | 24>      1            3047.52488000               0.00183474
            | 25>      2             457.36951800               0.01403732
            | 26>      3             103.94868500               0.06884262
            | 27>      4              29.21015530               0.23218444
            | 28>      5               9.28666296               0.46794135
            | 29>      6               3.16392696               0.36231199
            | 30>      S  3
            | 31>      1               7.86827235              -0.11933242
            | 32>      2               1.88128854              -0.16085415
            | 33>      3               0.54424926               1.14345644
            | 34>      P  3
            | 35>      1               7.86827235               0.06899907
            | 36>      2               1.88128854               0.31642396
            | 37>      3               0.54424926               0.74430829
            | 38>      S  1
            | 39>      1               0.16871448               1.00000000
            | 40>      P  1
            | 41>      1               0.16871448               1.00000000
            | 42>      D  1
            | 43>      1               0.80000000               1.00000000
            | 44>      end
            | 45> end
            | 46> %basis
            | 47>      NewGTO   H
            | 48>      S  3
            | 49>      1              18.73113696               0.03349460
            | 50>      2               2.82539437               0.23472695
            | 51>      3               0.64012169               0.81375733
            | 52>      S  1
            | 53>      1               0.16127776               1.00000000
            | 54>      end
            | 55> end
            | 56> 
            | 57>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000   -0.000000    0.000000
              H      1.076982   -0.180129   -0.000021
              H     -0.528823   -0.955345    0.000132
              H     -0.274116    0.567634   -0.891619
              H     -0.274046    0.567842    0.891508
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000   -0.000000    0.000000
               1 H     1.0000    0     1.008    2.035201   -0.340395   -0.000040
               2 H     1.0000    0     1.008   -0.999330   -1.805341    0.000250
               3 H     1.0000    0     1.008   -0.518004    1.072672   -1.684916
               4 H     1.0000    0     1.008   -0.517872    1.073065    1.684707
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091941502291     0.00000000     0.00000000
             H      1   2   0     1.091942631093   109.47127198     0.00000000
             H      1   2   3     1.091939904582   109.47132155   239.99991800
             H      1   2   3     1.091939897331   109.47132094   120.00008173
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063470393592     0.00000000     0.00000000
             H      1   2   0     2.063472526719   109.47127198     0.00000000
             H      1   2   3     2.063467374360   109.47132155   239.99991800
             H      1   2   3     2.063467360657   109.47132094   120.00008173
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 10s4p1d contracted to 3s2p1d pattern {631/31/1}
             Group   2 Type H   : 4s contracted to 2s pattern {31}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      18.7311369600      0.0334946000
               2       2.8253943700      0.2347269502
               3       0.6401216900      0.8137573307
             S 1 
               1       0.1612777600      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    3047.5248800000      0.0018347400
               2     457.3695180000      0.0140373200
               3     103.9486850000      0.0688426199
               4      29.2101553000      0.2321844397
               5       9.2866629600      0.4679413494
               6       3.1639269600      0.3623119895
             S 3 
               1       7.8682723500     -0.1193324197
               2       1.8812885400     -0.1608541495
               3       0.5442492600      1.1434564368
             P 3 
               1       7.8682723500      0.0689990700
               2       1.8812885400      0.3164239600
               3       0.5442492600      0.7443082900
             S 1 
               1       0.1687144800      1.0000000000
             P 1 
               1       0.1687144800      1.0000000000
             D 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   31
             # of primitive gaussian functions       ...   43
             # of contracted shells                  ...   14
             # of contracted basis functions         ...   22
             Highest angular momentum                ...    2
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....   22
             Nuclear Repulsion      ENuc            ....     13.4115070612 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 2.065e-02
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...  10952 (   0.0 sec)
            # of grid points (after weights+screening)   ...  10744 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...    10744
            Total number of batches                      ...      171
            Average number of points per batch           ...       62
            Average number of grid points per atom       ...     2149
            Average number of shells per batch           ...    12.78 (91.32%)
            Average number of basis functions per batch  ...    20.08 (91.25%)
            Average number of large shells per batch     ...    12.22 (95.59%)
            Average number of large basis fcns per batch ...    19.33 (96.26%)
            Maximum spatial batch extension              ...  32.44, 25.14, 18.36 au
            Average spatial batch extension              ...   4.15,  3.91,  3.48 au
            
            Time for grid setup =    0.047 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.2 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.0914409560   0.000000000000 0.06156782  0.00611892  0.2363943 0.7000
              1    -40.1291602316  -0.037719275580 0.04649479  0.00483308  0.1531768 0.7000
                                           ***Turning on DIIS***
              2    -40.1515679006  -0.022407668979 0.09698773  0.01050030  0.0900653 0.0000
              3    -40.0664839246   0.085083975941 0.02359165  0.00265218  0.0384304 0.0000
              4    -40.1797772411  -0.113293316518 0.00426664  0.00052246  0.0045056 0.0000
                                  *** Initiating the SOSCF procedure ***
                                       *** Shutting down DIIS ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              5    -40.19259043  -0.0128131894  0.000785  0.000785  0.001096  0.000183
                           *** Restarting incremental Fock matrix formation ***
              6    -40.19465509  -0.0020646596  0.000186  0.000157  0.000377  0.000066
              7    -40.19465550  -0.0000004132  0.000063  0.000110  0.000187  0.000034
              8    -40.19465555  -0.0000000487  0.000013  0.000010  0.000037  0.000003
              9    -40.19465555  -0.0000000012  0.000003  0.000002  0.000004  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  10 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.19465555 Eh           -1093.75218 eV
            
            Components:
            Nuclear Repulsion  :           13.41150706 Eh             364.94566 eV
            Electronic Energy  :          -53.60616261 Eh           -1458.69784 eV
            One Electron Energy:          -79.65556803 Eh           -2167.53820 eV
            Two Electron Energy:           26.04940541 Eh             708.84036 eV
            
            Virial components:
            Potential Energy   :          -80.40383503 Eh           -2187.89958 eV
            Kinetic Energy     :           40.20917947 Eh            1094.14740 eV
            Virial Ratio       :            1.99963879
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -4.6931e-11  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    8.7202e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    6.1698e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    2.0467e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    1.3381e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -11.204806      -304.8983 
               1   2.0000      -0.941250       -25.6127 
               2   2.0000      -0.544108       -14.8059 
               3   2.0000      -0.544107       -14.8059 
               4   2.0000      -0.544107       -14.8059 
               5   0.0000       0.255552         6.9539 
               6   0.0000       0.325493         8.8571 
               7   0.0000       0.325494         8.8571 
               8   0.0000       0.325494         8.8571 
               9   0.0000       0.731194        19.8968 
              10   0.0000       0.731195        19.8968 
              11   0.0000       0.731196        19.8968 
              12   0.0000       1.177042        32.0289 
              13   0.0000       1.177043        32.0290 
              14   0.0000       1.177044        32.0290 
              15   0.0000       1.240606        33.7586 
              16   0.0000       1.327985        36.1363 
              17   0.0000       1.942105        52.8474 
              18   0.0000       1.942105        52.8474 
              19   0.0000       2.579596        70.1944 
              20   0.0000       2.579598        70.1944 
              21   0.0000       2.579600        70.1945 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.675353
               1 H :    0.168838
               2 H :    0.168838
               3 H :    0.168838
               4 H :    0.168838
            Sum of atomic charges:   -0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.368106  s :     3.368106
                  pz      :     1.088498  p :     3.265493
                  px      :     1.088498
                  py      :     1.088498
                  dz2     :     0.010438  d :     0.041754
                  dxz     :     0.002631
                  dyz     :     0.011287
                  dx2y2   :     0.009880
                  dxy     :     0.007518
              1 H s       :     0.831162  s :     0.831162
              2 H s       :     0.831162  s :     0.831162
              3 H s       :     0.831162  s :     0.831162
              4 H s       :     0.831162  s :     0.831162
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :   -0.514581
               1 H :    0.128645
               2 H :    0.128645
               3 H :    0.128645
               4 H :    0.128645
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     3.018697  s :     3.018697
                  pz      :     1.144994  p :     3.434979
                  px      :     1.144993
                  py      :     1.144993
                  dz2     :     0.015226  d :     0.060905
                  dxz     :     0.003837
                  dyz     :     0.016464
                  dx2y2   :     0.014411
                  dxy     :     0.010966
              1 H s       :     0.871355  s :     0.871355
              2 H s       :     0.871355  s :     0.871355
              3 H s       :     0.871355  s :     0.871355
              4 H s       :     0.871355  s :     0.871355
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.6754     6.0000    -0.6754     3.8340     3.8340    -0.0000
              1 H      0.8312     1.0000     0.1688     0.9307     0.9307    -0.0000
              2 H      0.8312     1.0000     0.1688     0.9307     0.9307    -0.0000
              3 H      0.8312     1.0000     0.1688     0.9307     0.9307    -0.0000
              4 H      0.8312     1.0000     0.1688     0.9307     0.9307    -0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9585 B(  0-C ,  2-H ) :   0.9585 B(  0-C ,  3-H ) :   0.9585 
            B(  0-C ,  4-H ) :   0.9585 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.158 sec
            Sum of individual times     ....       0.989 sec  ( 85.4%)
            
            Fock matrix formation       ....       0.824 sec  ( 71.2%)
            Diagonalization             ....       0.001 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.000 sec  (  0.0%)
            Initial guess               ....       0.114 sec  (  9.9%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.000 sec  (  0.0%)
            SOSCF solution              ....       0.001 sec  (  0.1%)
            
            
            ------------------------------------------------------------------------------- 
                                          ORCA-MATRIX DRIVEN CI                            
            ------------------------------------------------------------------------------- 
            
            --------------------------------
            AUTOMATIC CHOICE OF INCORE LEVEL
            --------------------------------
            
            Memory available                           ...  32000.00 MB
            Memory needed for S+T                      ...      0.07 MB
            Memory needed for J+K                      ...      0.13 MB
            Memory needed for DIIS                     ...      0.93 MB
            Memory needed for 3-ext                    ...      0.15 MB
            Memory needed for 4-ext                    ...      0.34 MB
            Memory needed for triples                  ...      0.19 MB
             -> Final InCoreLevel    ... 5
             -> check shows that triples correction can be computed
            
            
            Wavefunction type
            -----------------
            Correlation treatment                      ...      CCSD     
            Single excitations                         ... ON
            Orbital optimization                       ... OFF
            Calculation of Z vector                    ... OFF
            Calculation of Brueckner orbitals          ... OFF
            Perturbative triple excitations            ... ON
            Calculation of F12 correction              ... OFF
            Frozen core treatment                      ... chemical core (2 el)
            Reference Wavefunction                     ... RHF
              Internal Orbitals:     1 ...    4 (  4 MO's/  8 electrons)
              Virtual  Orbitals:     5 ...   21 ( 17 MO's              )
            Number of AO's                             ...     22
            Number of electrons                        ...     10
            Number of correlated electrons             ...      8
            
            Algorithmic settings
            --------------------
            Integral transformation                    ... AO direct full transformation
            K(C) Formation                             ... FULL-MO TRAFO
            Maximum number of iterations               ...        50
            Convergence tolerance (max. residuum)      ... 2.500e-05
            Level shift for amplitude update           ... 2.000e-01
            Maximum number of DIIS vectors             ...         7
            DIIS turned on at iteration                ...         0
            Damping before turning on DIIS             ...     0.500
            Damping after turning on DIIS              ...     0.000
            Pair specific amplitude update             ... OFF
            Natural orbital iterations                 ... OFF
            Perturbative natural orbital generation    ... OFF
            Printlevel                                 ... 2
            
            Memory handling:
            ----------------
            Maximum memory for working arrays          ...  32000 MB
            Data storage in matrix containers          ... UNCOMPRESSED
            Data type for integral storage             ... DOUBLE
            In-Core Storage of quantities:
               Amplitudes+Sigma Vector      ... YES
               J+K operators                ... YES
               DIIS vectors                 ... YES
               3-external integrals         ... YES
               4-external integrals         ... YES
            
            
            Initializing the integral package          ... done
            Warning: reference  - re-canonicalizations have been set to INT 1 VIRT 1
            
            --------------------------
            CLOSED-SHELL FOCK OPERATOR
            --------------------------
            
            <ss|ss>:         2211 b            0 skpd (  0.0%)    0.001 s ( 0.001 ms/b)
            <ss|sp>:         1452 b            0 skpd (  0.0%)    0.003 s ( 0.002 ms/b)
            <ss|sd>:          726 b            0 skpd (  0.0%)    0.001 s ( 0.001 ms/b)
            <ss|pp>:          198 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <ss|pd>:          132 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <ss|dd>:           66 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <sp|sp>:          253 b            0 skpd (  0.0%)    0.001 s ( 0.002 ms/b)
            <sp|sd>:          242 b            0 skpd (  0.0%)    0.001 s ( 0.002 ms/b)
            <sp|pp>:           66 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <sp|pd>:           44 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <sp|dd>:           22 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <sd|sd>:           66 b            0 skpd (  0.0%)    0.000 s ( 0.003 ms/b)
            <sd|pp>:           33 b            0 skpd (  0.0%)    0.000 s ( 0.005 ms/b)
            <sd|pd>:           22 b            0 skpd (  0.0%)    0.000 s ( 0.006 ms/b)
            <sd|dd>:           11 b            0 skpd (  0.0%)    0.000 s ( 0.007 ms/b)
            <pp|pp>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.011 ms/b)
            <pp|pd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.010 ms/b)
            <pp|dd>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.012 ms/b)
            <pd|pd>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.018 ms/b)
            <pd|dd>:            2 b            0 skpd (  0.0%)    0.000 s ( 0.024 ms/b)
            <dd|dd>:            1 b            0 skpd (  0.0%)    0.000 s ( 0.066 ms/b)
            Recanonicalizing the internal orbitals
            Recanonicalizing the virtual orbitals
            Time needed for Fock operator              ...            0.009 sec
            Reference energy                           ...    -40.194655553
            
            ------------------------------
            PARTIAL COULOMB TRANSFORMATION
            ------------------------------
            
            Transformation type                        ... one-operator
            Dimension of the basis                     ...   22
            Number of internal MOs                     ...   21 (1-21)
            Pair cutoff                                ... 0.000e+00 Eh
            Number of AO pairs included in the trafo   ...  253
            Total Number of distinct AO pairs          ...  253
            Memory devoted for trafo                   ... 32000.0 MB 
            Max. Number of MO pairs treated together   ... 16578276      
            Max. Number of MOs treated per batch       ... 753558      
            Number Format for Storage                  ... Double (8 Byte)
            AO-integral source                         ... DIRECT
            Integral package used                      ... LIBINT
            
            Starting integral evaluation:
            <ss|**>:         6930 b        0 skpd     0.008 s (  0.001 ms/b)
            <sp|**>:         2310 b        0 skpd     0.005 s (  0.002 ms/b)
            <sd|**>:         1155 b        0 skpd     0.002 s (  0.002 ms/b)
            <pp|**>:          315 b        0 skpd     0.001 s (  0.003 ms/b)
            <pd|**>:          210 b        0 skpd     0.001 s (  0.004 ms/b)
            <dd|**>:          105 b        0 skpd     0.000 s (  0.004 ms/b)
            Closing buffer AOJ ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer AOJ 
                ... done with AO integral generation
            Number of MO pairs included in the trafo   ...  231
                ... Now sorting integrals
            IBATCH = 1 of  1
            Closing buffer JAO ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer JAO 
            TOTAL TIME for half transformation         ...     0.019 sec
            AO-integral generation                     ...     0.015 sec
            Half transformation                        ...     0.002 sec
            J-integral sorting                         ...     0.001 sec
            
            -------------------------- SECOND HALF TRANSFORMATION -------------------------
            Formation of (pq|rs)                       ... ok (     0.002 sec)
            Integral sorting                           ... ok (     0.001 sec)
            
            ------------------
            CLOSED SHELL GUESS
            ------------------
            
            Initial guess performed in     0.000 sec
            E(0)                                       ...    -40.194655553
            E(MP2)                                     ...     -0.136592541
            Initial E(tot)                             ...    -40.331248094
            <T|T>                                      ...      0.045558946
            Number of pairs included                   ... 10
            Total number of pairs                      ... 10
            
            ------------------------------------------------
                              RHF COUPLED CLUSTER ITERATIONS
            ------------------------------------------------
            
            Number of amplitudes to be optimized       ... 2958
            
            Iter       E(tot)           E(Corr)          Delta-E          Residual     Time
              0    -40.331248094     -0.136592541      0.000000000      0.012532777    0.00
                                       *** Turning on DIIS ***
              1    -40.345045609     -0.150390056     -0.013797515      0.005452597    0.01
              2    -40.351196173     -0.156540619     -0.006150563      0.001417579    0.01
              3    -40.351869497     -0.157213944     -0.000673324      0.000391348    0.01
              4    -40.351973254     -0.157317701     -0.000103757      0.000098357    0.01
              5    -40.351984534     -0.157328981     -0.000011280      0.000027752    0.01
              6    -40.351985221     -0.157329668     -0.000000687      0.000005491    0.01
                           --- The Coupled-Cluster iterations have converged ---
            
            ----------------------
            COUPLED CLUSTER ENERGY
            ----------------------
            
            E(0)                                       ...    -40.194655553
            E(CORR)                                    ...     -0.157329668
            E(TOT)                                     ...    -40.351985221
            Singles Norm <S|S>**1/2                    ...      0.020407778  
            T1 diagnostic                              ...      0.007215239  
            
            ------------------
            LARGEST AMPLITUDES
            ------------------
               4->  6   4->  6       0.044038
               3->  7   3->  7       0.041231
               2->  8   2->  8       0.032624
               4-> 12   4-> 12       0.031450
               3-> 13   3-> 13       0.029376
               4-> 11   4-> 11       0.028494
               3->  9   3->  9       0.027633
               4->  6   4-> 12       0.027022
               4-> 12   4->  6       0.027022
               3-> 13   3->  7       0.025331
               3->  7   3-> 13       0.025331
               2-> 10   2-> 10       0.023805
               2-> 14   2-> 14       0.023470
               2->  8   2-> 14       0.020581
               2-> 14   2->  8       0.020581
               4->  6   1->  5       0.018260
            
            
                    !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! 
                    !  Warning: Densities are linearized densities !                         !
                    !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! 
            
            Trace of internal density part =     -0.127840319
            Trace of external density part =      0.127840319
            ----------------------
            RHF TRIPLES CORRECTION (Algorithm 1)
            ----------------------
            
            Multiplier for the singles contribution    ...      1.000000000
            
            10% done
            20% done
            30% done
            40% done
            50% done
            60% done
            70% done
            80% done
            90% done
            
            Triples Correction (T)                     ...     -0.002701939
            Scaling of triples based on CCSD energies (Peterson et al. Molecular Physics 113, 1551 (2015))
            E(T*) = f*E(T) where f = E(F12-CCSD)/E(CCSD) 
            f = CCSD (with F12)/ CCSD (without F12)    ...      1.000000000
            Scaled triples correction (T)              ...     -0.002701939
            
            Final correlation energy                   ...     -0.160031607
            E(CCSD)                                    ...    -40.351985221
            E(CCSD(T))                                 ...    -40.354687161
            
            NORM  =      1.064336637 sqrt=     1.031666922
            W(HF) =      0.939552361
            ------------------------------------------------------------------------------
                                       ORCA POPULATION ANALYSIS
            ------------------------------------------------------------------------------
            Input electron density              ... input.mdcip
            BaseName (.gbw .S,...)              ... input
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.665597
               1 H :    0.166399
               2 H :    0.166399
               3 H :    0.166399
               4 H :    0.166399
            Sum of atomic charges:   -0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.328336  s :     3.328336
                  pz      :     1.095066  p :     3.285197
                  px      :     1.095066
                  py      :     1.095065
                  dz2     :     0.012086  d :     0.052063
                  dxz     :     0.005829
                  dyz     :     0.012766
                  dx2y2   :     0.011638
                  dxy     :     0.009745
              1 H s       :     0.833601  s :     0.833601
              2 H s       :     0.833601  s :     0.833601
              3 H s       :     0.833601  s :     0.833601
              4 H s       :     0.833601  s :     0.833601
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :   -0.547677
               1 H :    0.136919
               2 H :    0.136919
               3 H :    0.136919
               4 H :    0.136919
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     3.014849  s :     3.014849
                  pz      :     1.152833  p :     3.458498
                  px      :     1.152832
                  py      :     1.152832
                  dz2     :     0.017652  d :     0.074330
                  dxz     :     0.007232
                  dyz     :     0.018785
                  dx2y2   :     0.016906
                  dxy     :     0.013754
              1 H s       :     0.863081  s :     0.863081
              2 H s       :     0.863081  s :     0.863081
              3 H s       :     0.863081  s :     0.863081
              4 H s       :     0.863081  s :     0.863081
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.6656     6.0000    -0.6656     3.9580     3.6625     0.2956
              1 H      0.8336     1.0000     0.1664     0.9391     0.8874     0.0517
              2 H      0.8336     1.0000     0.1664     0.9391     0.8874     0.0517
              3 H      0.8336     1.0000     0.1664     0.9391     0.8874     0.0517
              4 H      0.8336     1.0000     0.1664     0.9391     0.8874     0.0517
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9156 B(  0-C ,  2-H ) :   0.9156 B(  0-C ,  3-H ) :   0.9156 
            B(  0-C ,  4-H ) :   0.9156 
            
            
            
            ------------------------------------------------------------------------------- 
                                                 TIMINGS                                   
            ------------------------------------------------------------------------------- 
            
            
            Total execution time                   ...        0.195 sec
            
            Fock Matrix Formation                  ...        0.009 sec (  4.8%)
            Initial Guess                          ...        0.000 sec (  0.0%)
            DIIS Solver                            ...        0.001 sec (  0.4%)
            State Vector Update                    ...        0.000 sec (  0.0%)
            Sigma-vector construction              ...        0.063 sec ( 32.2%)
              <D|H|D>(2-ext)                       ...        0.002 sec (  3.5% of sigma)
              <D|H|D>(4-ext)                       ...        0.002 sec (  3.6% of sigma)
              <D|H|D>(4-ext-corr)                  ...        0.002 sec (  2.7% of sigma)
              <S|H|D>(3-ext)                       ...        0.001 sec (  2.1% of sigma)
              Fock-dressing                        ...        0.049 sec ( 77.5% of sigma)
              (ij|ab),(ia|jb)-dressing             ...        0.003 sec (  4.9% of sigma)
            Total Time for computing (T)           ...        0.003 sec (  1.4% of ALL)
            
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.354687160506
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = (-0.000000, -0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000       0.00000
            Nuclear contribution   :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078381 157685.032765 157684.479059 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000001     0.000001     0.000000 
            x,y,z [Debye]:     0.000001     0.000003     0.000000 
            
             
            
                                       *** MDCI DENSITY ***
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.mdcip
            The origin for moment calculation is the CENTER OF MASS  = (-0.000000, -0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000       0.00000
            Nuclear contribution   :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078381 157685.032765 157684.479059 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000001     0.000001     0.000000 
            x,y,z [Debye]:     0.000002     0.000003     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        1.635 sec (=   0.027 min)
            GTO integral calculation        ...        0.224 sec (=   0.004 min)  13.7 %
            SCF iterations                  ...        1.183 sec (=   0.020 min)  72.3 %
            MDCI module                     ...        0.228 sec (=   0.004 min)  14.0 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 1 seconds 847 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: No MP2 level density has been requested!
                     To caclulate MP2 level properties use
                     %mp2 Density relaxed end
                     or
                     %mp2 Density unrelaxed end
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! MP2 Printbasis
            |  2> * xyz   0  1
            |  3> C     0.00000024    -0.00000002     0.00000000
            |  4> H     1.07698196    -0.18012947    -0.00002129
            |  5> H    -0.52882274    -0.95534548     0.00013221
            |  6> H    -0.27411608     0.56763359    -0.89161936
            |  7> H    -0.27404603     0.56784158     0.89150844
            |  8> *
            |  9> %MaxCore    64000
            | 10> %scf
            | 11>   MaxIter 500
            | 12>   Convergence VeryTight
            | 13> end
            | 14> %pal nprocs     1
            | 15> end
            | 16> %method
            | 17>   IntAcc 7.0
            | 18>   NewNCore C     2 end
            | 19>   NewNCore H     0 end
            | 20> end
            | 21> %basis
            | 22>      NewGTO   C
            | 23>      S  6
            | 24>      1            4563.24000000               0.00196665
            | 25>      2             682.02400000               0.01523060
            | 26>      3             154.97300000               0.07612691
            | 27>      4              44.45530000               0.26080103
            | 28>      5              13.02900000               0.61646208
            | 29>      6               1.82773000               0.22100603
            | 30>      S  3
            | 31>      1              20.96420000               0.11466008
            | 32>      2               4.80331000               0.91999965
            | 33>      3               1.45933000              -0.00303068
            | 34>      P  3
            | 35>      1              20.96420000               0.04024869
            | 36>      2               4.80331000               0.23759396
            | 37>      3               1.45933000               0.81585385
            | 38>      S  1
            | 39>      1               0.48345600               1.00000000
            | 40>      P  1
            | 41>      1               0.48345600               1.00000000
            | 42>      S  1
            | 43>      1               0.14558500               1.00000000
            | 44>      P  1
            | 45>      1               0.14558500               1.00000000
            | 46>      S  1
            | 47>      1               0.04380000               1.00000000
            | 48>      P  1
            | 49>      1               0.04380000               1.00000000
            | 50>      D  1
            | 51>      1               2.50400000               1.00000000
            | 52>      D  1
            | 53>      1               0.62600000               1.00000000
            | 54>      D  1
            | 55>      1               0.15650000               1.00000000
            | 56>      F  1
            | 57>      1               0.80000000               1.00000000
            | 58>      end
            | 59> end
            | 60> %basis
            | 61>      NewGTO   H
            | 62>      S  3
            | 63>      1              33.86500000               0.02549381
            | 64>      2               5.09479000               0.19037311
            | 65>      3               1.15879000               0.85216149
            | 66>      S  1
            | 67>      1               0.32584000               1.00000000
            | 68>      S  1
            | 69>      1               0.10274100               1.00000000
            | 70>      S  1
            | 71>      1               0.03600000               1.00000000
            | 72>      P  1
            | 73>      1               1.50000000               1.00000000
            | 74>      P  1
            | 75>      1               0.37500000               1.00000000
            | 76>      end
            | 77> end
            | 78> 
            | 79>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000   -0.000000    0.000000
              H      1.076982   -0.180129   -0.000021
              H     -0.528823   -0.955345    0.000132
              H     -0.274116    0.567634   -0.891619
              H     -0.274046    0.567842    0.891508
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000   -0.000000    0.000000
               1 H     1.0000    0     1.008    2.035201   -0.340395   -0.000040
               2 H     1.0000    0     1.008   -0.999330   -1.805341    0.000250
               3 H     1.0000    0     1.008   -0.518004    1.072672   -1.684916
               4 H     1.0000    0     1.008   -0.517872    1.073065    1.684707
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091941502291     0.00000000     0.00000000
             H      1   2   0     1.091942631093   109.47127198     0.00000000
             H      1   2   3     1.091939904582   109.47132155   239.99991800
             H      1   2   3     1.091939897331   109.47132094   120.00008173
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063470393592     0.00000000     0.00000000
             H      1   2   0     2.063472526719   109.47127198     0.00000000
             H      1   2   3     2.063467374360   109.47132155   239.99991800
             H      1   2   3     2.063467360657   109.47132094   120.00008173
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 12s6p3d1f contracted to 5s4p3d1f pattern {63111/3111/111/1}
             Group   2 Type H   : 6s2p contracted to 4s2p pattern {3111/11}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      33.8650000000      0.0254938099
               2       5.0947900000      0.1903731093
               3       1.1587900000      0.8521614869
             S 1 
               1       0.3258400000      1.0000000000
             S 1 
               1       0.1027410000      1.0000000000
             S 1 
               1       0.0360000000      1.0000000000
             P 1 
               1       1.5000000000      1.0000000000
             P 1 
               1       0.3750000000      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    4563.2400000000      0.0019666500
               2     682.0240000000      0.0152306000
               3     154.9730000000      0.0761269100
               4      44.4553000000      0.2608010300
               5      13.0290000000      0.6164620800
               6       1.8277300000      0.2210060300
             S 3 
               1      20.9642000000      0.1146600796
               2       4.8033100000      0.9199996470
               3       1.4593300000     -0.0030306800
             P 3 
               1      20.9642000000      0.0402486900
               2       4.8033100000      0.2375939599
               3       1.4593300000      0.8158538497
             S 1 
               1       0.4834560000      1.0000000000
             P 1 
               1       0.4834560000      1.0000000000
             S 1 
               1       0.1455850000      1.0000000000
             P 1 
               1       0.1455850000      1.0000000000
             S 1 
               1       0.0438000000      1.0000000000
             P 1 
               1       0.0438000000      1.0000000000
             D 1 
               1       2.5040000000      1.0000000000
             D 1 
               1       0.6260000000      1.0000000000
             D 1 
               1       0.1565000000      1.0000000000
             F 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   54
             # of primitive gaussian functions       ...  100
             # of contracted shells                  ...   37
             # of contracted basis functions         ...   79
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....   79
             Nuclear Repulsion      ENuc            ....     13.4115070612 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.178e-03
            Time for diagonalization                   ...    0.002 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.001 sec
            Total time needed                          ...    0.003 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...  10952 (   0.0 sec)
            # of grid points (after weights+screening)   ...  10744 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.1 sec
            
            Total number of grid points                  ...    10744
            Total number of batches                      ...      171
            Average number of points per batch           ...       62
            Average number of grid points per atom       ...     2149
            Average number of shells per batch           ...    33.82 (91.40%)
            Average number of basis functions per batch  ...    71.30 (90.25%)
            Average number of large shells per batch     ...    31.89 (94.29%)
            Average number of large basis fcns per batch ...    67.16 (94.19%)
            Maximum spatial batch extension              ...  32.44, 25.14, 18.36 au
            Average spatial batch extension              ...   4.15,  3.91,  3.48 au
            
            Time for grid setup =    0.060 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.2 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.0987467310   0.000000000000 0.06498054  0.00133440  0.3081349 0.7000
              1    -40.1400281124  -0.041281381327 0.04440478  0.00098643  0.1968168 0.7000
                                           ***Turning on DIIS***
              2    -40.1645581544  -0.024530042016 0.02540761  0.00060922  0.1152236 0.7000
              3    -40.3444510236  -0.179892869167 0.03057615  0.00100922  0.0657479 0.0000
              4    -40.1856184148   0.158832608773 0.00930506  0.00018013  0.0107469 0.0000
                                  *** Initiating the SOSCF procedure ***
                                       *** Shutting down DIIS ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              5    -40.20885531  -0.0232368903  0.001671  0.001671  0.002200  0.000071
                           *** Restarting incremental Fock matrix formation ***
              6    -40.21212916  -0.0032738573  0.000489  0.000527  0.000491  0.000035
              7    -40.21213314  -0.0000039739  0.000171  0.000275  0.000348  0.000021
              8    -40.21213372  -0.0000005841  0.000038  0.000025  0.000097  0.000002
              9    -40.21213373  -0.0000000116  0.000008  0.000004  0.000012  0.000000
             10    -40.21213373  -0.0000000007  0.000001  0.000001  0.000002  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  11 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.21213373 Eh           -1094.22779 eV
            
            Components:
            Nuclear Repulsion  :           13.41150706 Eh             364.94566 eV
            Electronic Energy  :          -53.62364079 Eh           -1459.17345 eV
            One Electron Energy:          -79.68506471 Eh           -2168.34085 eV
            Two Electron Energy:           26.06142392 Eh             709.16740 eV
            
            Virial components:
            Potential Energy   :          -80.36401923 Eh           -2186.81614 eV
            Kinetic Energy     :           40.15188550 Eh            1092.58835 eV
            Virial Ratio       :            2.00150051
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -8.5549e-12  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    6.0047e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    2.2171e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    1.7925e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    1.5824e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -11.206965      -304.9570 
               1   2.0000      -0.941585       -25.6218 
               2   2.0000      -0.544186       -14.8081 
               3   2.0000      -0.544186       -14.8081 
               4   2.0000      -0.544186       -14.8080 
               5   0.0000       0.041824         1.1381 
               6   0.0000       0.076983         2.0948 
               7   0.0000       0.076983         2.0948 
               8   0.0000       0.076983         2.0948 
               9   0.0000       0.149798         4.0762 
              10   0.0000       0.149798         4.0762 
              11   0.0000       0.149798         4.0762 
              12   0.0000       0.189136         5.1467 
              13   0.0000       0.299624         8.1532 
              14   0.0000       0.299624         8.1532 
              15   0.0000       0.299624         8.1532 
              16   0.0000       0.364056         9.9065 
              17   0.0000       0.409128        11.1329 
              18   0.0000       0.409129        11.1330 
              19   0.0000       0.465198        12.6587 
              20   0.0000       0.465198        12.6587 
              21   0.0000       0.465198        12.6587 
              22   0.0000       0.797152        21.6916 
              23   0.0000       0.797152        21.6916 
              24   0.0000       0.797152        21.6916 
              25   0.0000       0.830490        22.5988 
              26   0.0000       0.854841        23.2614 
              27   0.0000       0.854841        23.2614 
              28   0.0000       0.854841        23.2614 
              29   0.0000       0.865378        23.5481 
              30   0.0000       1.057761        28.7832 
              31   0.0000       1.057762        28.7832 
              32   0.0000       1.057763        28.7832 
              33   0.0000       1.170002        31.8374 
              34   0.0000       1.170002        31.8374 
              35   0.0000       1.334257        36.3070 
              36   0.0000       1.334257        36.3070 
              37   0.0000       1.334257        36.3070 
              38   0.0000       1.523597        41.4592 
              39   0.0000       1.523598        41.4592 
              40   0.0000       1.523599        41.4592 
              41   0.0000       1.821310        49.5604 
              42   0.0000       2.209874        60.1337 
              43   0.0000       2.209876        60.1338 
              44   0.0000       2.259364        61.4804 
              45   0.0000       2.259365        61.4804 
              46   0.0000       2.259366        61.4805 
              47   0.0000       2.734754        74.4164 
              48   0.0000       2.967758        80.7568 
              49   0.0000       2.967759        80.7568 
              50   0.0000       2.967759        80.7568 
              51   0.0000       3.268914        88.9517 
              52   0.0000       3.268915        88.9517 
              53   0.0000       3.268915        88.9517 
              54   0.0000       3.682362       100.2022 
              55   0.0000       3.682362       100.2022 
              56   0.0000       3.682363       100.2022 
              57   0.0000       3.894354       105.9708 
              58   0.0000       3.894358       105.9709 
              59   0.0000       3.894360       105.9709 
              60   0.0000       4.317672       117.4898 
              61   0.0000       4.524537       123.1189 
              62   0.0000       4.524537       123.1189 
              63   0.0000       4.524539       123.1190 
              64   0.0000       4.560338       124.0931 
              65   0.0000       4.560339       124.0931 
              66   0.0000       4.792112       130.4000 
              67   0.0000       4.792115       130.4001 
              68   0.0000       4.792117       130.4001 
              69   0.0000       5.253712       142.9608 
              70   0.0000       6.156484       167.5264 
              71   0.0000       6.156489       167.5266 
              72   0.0000       6.156497       167.5268 
              73   0.0000       7.645282       208.0387 
              74   0.0000       7.645283       208.0387 
              75   0.0000       8.278356       225.2655 
              76   0.0000       8.278360       225.2656 
              77   0.0000       8.278362       225.2657 
              78   0.0000      25.454264       692.6457 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.431482
               1 H :    0.107870
               2 H :    0.107870
               3 H :    0.107871
               4 H :    0.107871
            Sum of atomic charges:    0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.143248  s :     3.143248
                  pz      :     1.070062  p :     3.210184
                  px      :     1.070061
                  py      :     1.070061
                  dz2     :     0.018863  d :     0.075451
                  dxz     :     0.004754
                  dyz     :     0.020397
                  dx2y2   :     0.017853
                  dxy     :     0.013585
                  f0      :     0.000016  f :     0.002600
                  f+1     :     0.000407
                  f-1     :     0.001055
                  f+2     :     0.000090
                  f-2     :     0.000143
                  f+3     :     0.000811
                  f-3     :     0.000078
              1 H s       :     0.857538  s :     0.857538
                  pz      :     0.007838  p :     0.034592
                  px      :     0.018614
                  py      :     0.008139
              2 H s       :     0.857538  s :     0.857538
                  pz      :     0.007838  p :     0.034592
                  px      :     0.010436
                  py      :     0.016318
              3 H s       :     0.857537  s :     0.857537
                  pz      :     0.015224  p :     0.034592
                  px      :     0.008536
                  py      :     0.010832
              4 H s       :     0.857537  s :     0.857537
                  pz      :     0.015222  p :     0.034592
                  px      :     0.008536
                  py      :     0.010834
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :    0.017812
               1 H :   -0.004453
               2 H :   -0.004452
               3 H :   -0.004453
               4 H :   -0.004453
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     2.651680  s :     2.651680
                  pz      :     1.041291  p :     3.123872
                  px      :     1.041290
                  py      :     1.041290
                  dz2     :     0.048195  d :     0.192780
                  dxz     :     0.012146
                  dyz     :     0.052114
                  dx2y2   :     0.045615
                  dxy     :     0.034710
                  f0      :     0.000168  f :     0.013856
                  f+1     :     0.002715
                  f-1     :     0.004179
                  f+2     :     0.000976
                  f-2     :     0.001547
                  f+3     :     0.003685
                  f-3     :     0.000586
              1 H s       :     0.850068  s :     0.850068
                  pz      :     0.040160  p :     0.154385
                  px      :     0.073142
                  py      :     0.041083
              2 H s       :     0.850067  s :     0.850067
                  pz      :     0.040160  p :     0.154385
                  px      :     0.048112
                  py      :     0.066113
              3 H s       :     0.850068  s :     0.850068
                  pz      :     0.062766  p :     0.154386
                  px      :     0.042297
                  py      :     0.049323
              4 H s       :     0.850068  s :     0.850068
                  pz      :     0.062761  p :     0.154386
                  px      :     0.042296
                  py      :     0.049329
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.4315     6.0000    -0.4315     3.9508     3.9508     0.0000
              1 H      0.8921     1.0000     0.1079     0.9946     0.9946     0.0000
              2 H      0.8921     1.0000     0.1079     0.9946     0.9946     0.0000
              3 H      0.8921     1.0000     0.1079     0.9946     0.9946     0.0000
              4 H      0.8921     1.0000     0.1079     0.9946     0.9946     0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9877 B(  0-C ,  2-H ) :   0.9877 B(  0-C ,  3-H ) :   0.9877 
            B(  0-C ,  4-H ) :   0.9877 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 5 sec 
            
            Total time                  ....       5.377 sec
            Sum of individual times     ....       5.211 sec  ( 96.9%)
            
            Fock matrix formation       ....       5.006 sec  ( 93.1%)
            Diagonalization             ....       0.009 sec  (  0.2%)
            Density matrix formation    ....       0.001 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.0%)
            Initial guess               ....       0.126 sec  (  2.3%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.006 sec  (  0.1%)
            SOSCF solution              ....       0.003 sec  (  0.1%)
            
            ------------------------------------------------------------------------------
                                            ORCA  MP2 
            ------------------------------------------------------------------------------
            
            Freezing NCore=2 chemical core electrons
            
            ----------
            MP2 ENERGY (disk based algorithm)
            ----------
            
            Dimension of the basis                    ...   79
            Memory devoted to MP2                     ... 64000 MB   
            Data format for buffers                   ... DOUBLE
            Compression type for matrix containers    ... UNCOMPRESSED
            
            -------------------------------
            PARTIAL EXCHANGE TRANSFORMATION
            -------------------------------
            
            Transformation type                        ... one-operator
            Generation of integrals (i,mue|j,nue)      ... ON
            Generation of integrals (mue,kappa|nue,tau)... OFF
            Generation of integrals (i,mue|a,nue)      ... OFF
            Dimension of the basis                     ...   79
            Number of internal MOs                     ...    4 (   1-   4)
            Pair cutoff                                ... 1.000e-14 Eh
            Number of AO pairs in the trafo            ... 3160
            Total Number of distinct AO pairs          ... 3160
            Memory devoted for trafo                   ... 64000.0 MB 
            Max. Number of MO pairs treated together   ... 1344112      
            Number Format for Storage                  ... Double (8 Byte)
            Integral package used                      ... LIBINT
            
            Starting integral evaluation:
                ... done with AO integral generation
            Closing buffer AOK     ( 0.00 GB; CompressionRatio= 0.62)
            Collecting buffer AOK 
            Number of MO pairs included in the trafo   ...   10
            ------------------------
            SORTING OF (i,mue|j,nue)
            ------------------------
            
            IBATCH = 1 of  1
            Closing buffer KAO     ( 0.00 GB; CompressionRatio= 1.00)
            Collecting buffer KAO 
            N(AO-Batches) Done                         ...    962407 
            N(AO-Batches) Skipped                      ...         0 
            N(IJ)-pairs Skipped                        ...         0 
            TOTAL TIME for half transformation         ...     0.993 sec
            AO-integral generation                     ...     0.915 sec
            Half transformation                        ...     0.040 sec
            K-integral sorting                         ...     0.005 sec
            
            Finished integral transformation - now doing MP2 part
            
            OPERATOR COMBINATION   0   0: ij=(  1..  4,  1..  4)
              Internal MO   3
            -----------------------------------------------
             MP2 CORRELATION ENERGY   :     -0.193512430 Eh
            -----------------------------------------------
            
            
            -------
            TIMINGS
            -------
            Total time                :    1.071 sec
            Integral trafo            :    0.994 sec ( 92.8%)
            K(i,j)                    :    0.001 sec (  0.1%)
            T(i,j)                    :    0.000 sec (  0.0%)
            
            ---------------------------------------
            MP2 TOTAL ENERGY:      -40.405646162 Eh
            ---------------------------------------
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.405646162405
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
            
              WARNING: The energy has been calculated at the MP2 level but the densities
                       used in the property calculations are still SCF densities
                       MP2 response densities have not been calculated 
                       use %mp2 Density relaxed end
                       or  %mp2 Density unrelaxed end
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = (-0.000000, -0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000       0.00000
            Nuclear contribution   :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078381 157685.032765 157684.479059 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000001     0.000001     0.000000 
            x,y,z [Debye]:     0.000001     0.000003     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        6.717 sec (=   0.112 min)
            GTO integral calculation        ...        0.213 sec (=   0.004 min)   3.2 %
            SCF iterations                  ...        5.400 sec (=   0.090 min)  80.4 %
            MP2 module                      ...        1.103 sec (=   0.018 min)  16.4 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 6 seconds 867 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  1
            |  3> C     0.00000024    -0.00000002     0.00000000
            |  4> H     1.07698196    -0.18012947    -0.00002129
            |  5> H    -0.52882274    -0.95534548     0.00013221
            |  6> H    -0.27411608     0.56763359    -0.89161936
            |  7> H    -0.27404603     0.56784158     0.89150844
            |  8> *
            |  9> %MaxCore    64000
            | 10> %scf
            | 11>   MaxIter 500
            | 12>   Convergence VeryTight
            | 13> end
            | 14> %pal nprocs     1
            | 15> end
            | 16> %method
            | 17>   IntAcc 7.0
            | 18> end
            | 19> %basis
            | 20>      NewGTO   C
            | 21>      S  7
            | 22>      1            8236.00000000               0.00054198
            | 23>      2            1235.00000000               0.00419287
            | 24>      3             280.80000000               0.02152216
            | 25>      4              79.27000000               0.08353432
            | 26>      5              25.59000000               0.23958285
            | 27>      6               8.99700000               0.44285284
            | 28>      7               3.31900000               0.35179956
            | 29>      S  6
            | 30>      1             280.80000000              -0.00005949
            | 31>      2              79.27000000              -0.00114816
            | 32>      3              25.59000000              -0.01001914
            | 33>      4               8.99700000              -0.06121949
            | 34>      5               3.31900000              -0.17326985
            | 35>      6               0.36430000               1.07291519
            | 36>      S  1
            | 37>      1               0.90590000               1.00000000
            | 38>      S  1
            | 39>      1               0.12850000               1.00000000
            | 40>      S  1
            | 41>      1               0.04402000               1.00000000
            | 42>      P  3
            | 43>      1              18.71000000               0.03942639
            | 44>      2               4.13300000               0.24408898
            | 45>      3               1.20000000               0.81549201
            | 46>      P  1
            | 47>      1               0.38270000               1.00000000
            | 48>      P  1
            | 49>      1               0.12090000               1.00000000
            | 50>      P  1
            | 51>      1               0.03569000               1.00000000
            | 52>      D  1
            | 53>      1               1.09700000               1.00000000
            | 54>      D  1
            | 55>      1               0.31800000               1.00000000
            | 56>      F  1
            | 57>      1               0.76100000               1.00000000
            | 58>      end
            | 59> end
            | 60> %basis
            | 61>      NewGTO   H
            | 62>      S  3
            | 63>      1              33.87000000               0.02549486
            | 64>      2               5.09500000               0.19036277
            | 65>      3               1.15900000               0.85216202
            | 66>      S  1
            | 67>      1               0.32580000               1.00000000
            | 68>      S  1
            | 69>      1               0.10270000               1.00000000
            | 70>      P  1
            | 71>      1               0.72700000               1.00000000
            | 72>      end
            | 73> end
            | 74> 
            | 75>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000   -0.000000    0.000000
              H      1.076982   -0.180129   -0.000021
              H     -0.528823   -0.955345    0.000132
              H     -0.274116    0.567634   -0.891619
              H     -0.274046    0.567842    0.891508
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000   -0.000000    0.000000
               1 H     1.0000    0     1.008    2.035201   -0.340395   -0.000040
               2 H     1.0000    0     1.008   -0.999330   -1.805341    0.000250
               3 H     1.0000    0     1.008   -0.518004    1.072672   -1.684916
               4 H     1.0000    0     1.008   -0.517872    1.073065    1.684707
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091941502291     0.00000000     0.00000000
             H      1   2   0     1.091942631093   109.47127198     0.00000000
             H      1   2   3     1.091939904582   109.47132155   239.99991800
             H      1   2   3     1.091939897331   109.47132094   120.00008173
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063470393592     0.00000000     0.00000000
             H      1   2   0     2.063472526719   109.47127198     0.00000000
             H      1   2   3     2.063467374360   109.47132155   239.99991800
             H      1   2   3     2.063467360657   109.47132094   120.00008173
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 16s6p2d1f contracted to 5s4p2d1f pattern {76111/3111/11/1}
             Group   2 Type H   : 5s1p contracted to 3s1p pattern {311/1}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      33.8700000000      0.0254948600
               2       5.0950000000      0.1903627700
               3       1.1590000000      0.8521620200
             S 1 
               1       0.3258000000      1.0000000000
             S 1 
               1       0.1027000000      1.0000000000
             P 1 
               1       0.7270000000      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 7 
               1    8236.0000000000      0.0005419800
               2    1235.0000000000      0.0041928700
               3     280.8000000000      0.0215221600
               4      79.2700000000      0.0835343202
               5      25.5900000000      0.2395828505
               6       8.9970000000      0.4428528409
               7       3.3190000000      0.3517995607
             S 6 
               1     280.8000000000     -0.0000594900
               2      79.2700000000     -0.0011481600
               3      25.5900000000     -0.0100191400
               4       8.9970000000     -0.0612194901
               5       3.3190000000     -0.1732698502
               6       0.3643000000      1.0729151911
             S 1 
               1       0.9059000000      1.0000000000
             S 1 
               1       0.1285000000      1.0000000000
             S 1 
               1       0.0440200000      1.0000000000
             P 3 
               1      18.7100000000      0.0394263901
               2       4.1330000000      0.2440889805
               3       1.2000000000      0.8154920116
             P 1 
               1       0.3827000000      1.0000000000
             P 1 
               1       0.1209000000      1.0000000000
             P 1 
               1       0.0356900000      1.0000000000
             D 1 
               1       1.0970000000      1.0000000000
             D 1 
               1       0.3180000000      1.0000000000
             F 1 
               1       0.7610000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   49
             # of primitive gaussian functions       ...   83
             # of contracted shells                  ...   28
             # of contracted basis functions         ...   58
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    7
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....   58
             Nuclear Repulsion      ENuc            ....     13.4115070612 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 5.519e-03
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...  10952 (   0.0 sec)
            # of grid points (after weights+screening)   ...  10744 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...    10744
            Total number of batches                      ...      171
            Average number of points per batch           ...       62
            Average number of grid points per atom       ...     2149
            Average number of shells per batch           ...    25.64 (91.57%)
            Average number of basis functions per batch  ...    53.00 (91.38%)
            Average number of large shells per batch     ...    24.23 (94.49%)
            Average number of large basis fcns per batch ...    50.35 (95.01%)
            Maximum spatial batch extension              ...  32.44, 25.14, 18.36 au
            Average spatial batch extension              ...   4.15,  3.91,  3.48 au
            
            Time for grid setup =    0.053 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.2 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.0984328447   0.000000000000 0.02975277  0.00152276  0.2888580 0.7000
              1    -40.1392852658  -0.040852421125 0.02161044  0.00118331  0.1854130 0.7000
                                           ***Turning on DIIS***
              2    -40.1636275535  -0.024342287721 0.01323124  0.00076854  0.1085910 0.7000
              3    -40.3398971783  -0.176269624807 0.02719844  0.00149723  0.0701293 0.0000
              4    -40.1832558389   0.156641339464 0.00570478  0.00024297  0.0109143 0.0000
                                  *** Initiating the SOSCF procedure ***
                                       *** Shutting down DIIS ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              5    -40.20763819  -0.0243823526  0.001419  0.001419  0.001793  0.000125
                           *** Restarting incremental Fock matrix formation ***
              6    -40.21100054  -0.0033623466  0.000434  0.000432  0.000623  0.000057
              7    -40.21100422  -0.0000036810  0.000153  0.000303  0.000373  0.000035
              8    -40.21100476  -0.0000005395  0.000039  0.000022  0.000047  0.000002
              9    -40.21100477  -0.0000000099  0.000007  0.000005  0.000006  0.000000
             10    -40.21100477  -0.0000000007  0.000001  0.000001  0.000002  0.000000
                             **** Energy Check signals convergence ****
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  11 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.21100477 Eh           -1094.19707 eV
            
            Components:
            Nuclear Repulsion  :           13.41150706 Eh             364.94566 eV
            Electronic Energy  :          -53.62251183 Eh           -1459.14273 eV
            One Electron Energy:          -79.67811955 Eh           -2168.15186 eV
            Two Electron Energy:           26.05560772 Eh             709.00913 eV
            
            Virial components:
            Potential Energy   :          -80.34495745 Eh           -2186.29744 eV
            Kinetic Energy     :           40.13395268 Eh            1092.10037 eV
            Virial Ratio       :            2.00191987
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -4.2277e-12  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    4.0518e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    1.9667e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    1.9230e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    1.9724e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -11.209070      -305.0143 
               1   2.0000      -0.941820       -25.6282 
               2   2.0000      -0.544188       -14.8081 
               3   2.0000      -0.544187       -14.8081 
               4   2.0000      -0.544187       -14.8081 
               5   0.0000       0.074099         2.0163 
               6   0.0000       0.090185         2.4540 
               7   0.0000       0.090185         2.4540 
               8   0.0000       0.090185         2.4540 
               9   0.0000       0.257941         7.0189 
              10   0.0000       0.257941         7.0189 
              11   0.0000       0.257941         7.0189 
              12   0.0000       0.309171         8.4130 
              13   0.0000       0.461663        12.5625 
              14   0.0000       0.461663        12.5625 
              15   0.0000       0.461663        12.5625 
              16   0.0000       0.719020        19.5655 
              17   0.0000       0.719021        19.5655 
              18   0.0000       0.719021        19.5656 
              19   0.0000       0.762234        20.7414 
              20   0.0000       0.785838        21.3837 
              21   0.0000       0.785839        21.3838 
              22   0.0000       0.932446        25.3731 
              23   0.0000       1.172479        31.9048 
              24   0.0000       1.172479        31.9048 
              25   0.0000       1.172479        31.9048 
              26   0.0000       1.683528        45.8111 
              27   0.0000       1.683528        45.8111 
              28   0.0000       1.683530        45.8112 
              29   0.0000       2.015973        54.8574 
              30   0.0000       2.015973        54.8574 
              31   0.0000       2.015975        54.8575 
              32   0.0000       2.401236        65.3409 
              33   0.0000       2.401236        65.3410 
              34   0.0000       2.401237        65.3410 
              35   0.0000       2.409958        65.5783 
              36   0.0000       2.548001        69.3346 
              37   0.0000       2.548004        69.3347 
              38   0.0000       2.636389        71.7398 
              39   0.0000       2.636389        71.7398 
              40   0.0000       2.636390        71.7398 
              41   0.0000       2.887239        78.5658 
              42   0.0000       2.928300        79.6831 
              43   0.0000       2.928303        79.6832 
              44   0.0000       2.928305        79.6832 
              45   0.0000       3.315760        90.2264 
              46   0.0000       3.315760        90.2264 
              47   0.0000       3.640951        99.0753 
              48   0.0000       3.640953        99.0754 
              49   0.0000       3.640954        99.0754 
              50   0.0000       3.805951       103.5652 
              51   0.0000       3.805952       103.5652 
              52   0.0000       3.805954       103.5653 
              53   0.0000       4.256609       115.8282 
              54   0.0000       4.793715       130.4436 
              55   0.0000       4.793718       130.4437 
              56   0.0000       4.793724       130.4439 
              57   0.0000       9.675752       263.2906 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.455970
               1 H :    0.113992
               2 H :    0.113992
               3 H :    0.113992
               4 H :    0.113992
            Sum of atomic charges:    0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.267653  s :     3.267653
                  pz      :     1.045059  p :     3.135177
                  px      :     1.045059
                  py      :     1.045059
                  dz2     :     0.012245  d :     0.048979
                  dxz     :     0.003086
                  dyz     :     0.013241
                  dx2y2   :     0.011589
                  dxy     :     0.008819
                  f0      :     0.000013  f :     0.004161
                  f+1     :     0.000577
                  f-1     :     0.001884
                  f+2     :     0.000077
                  f-2     :     0.000122
                  f+3     :     0.001385
                  f-3     :     0.000102
              1 H s       :     0.864352  s :     0.864352
                  pz      :     0.004367  p :     0.021655
                  px      :     0.012688
                  py      :     0.004600
              2 H s       :     0.864353  s :     0.864353
                  pz      :     0.004367  p :     0.021655
                  px      :     0.006373
                  py      :     0.010915
              3 H s       :     0.864352  s :     0.864352
                  pz      :     0.010070  p :     0.021655
                  px      :     0.004906
                  py      :     0.006679
              4 H s       :     0.864352  s :     0.864352
                  pz      :     0.010069  p :     0.021655
                  px      :     0.004906
                  py      :     0.006680
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :   -0.338056
               1 H :    0.084514
               2 H :    0.084514
               3 H :    0.084514
               4 H :    0.084514
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     2.886048  s :     2.886048
                  pz      :     1.098444  p :     3.295329
                  px      :     1.098443
                  py      :     1.098443
                  dz2     :     0.035946  d :     0.143785
                  dxz     :     0.009059
                  dyz     :     0.038870
                  dx2y2   :     0.034022
                  dxy     :     0.025889
                  f0      :     0.000184  f :     0.012894
                  f+1     :     0.002705
                  f-1     :     0.003420
                  f+2     :     0.001069
                  f-2     :     0.001695
                  f+3     :     0.003221
                  f-3     :     0.000601
              1 H s       :     0.845956  s :     0.845956
                  pz      :     0.015081  p :     0.069530
                  px      :     0.038708
                  py      :     0.015742
              2 H s       :     0.845956  s :     0.845956
                  pz      :     0.015081  p :     0.069530
                  px      :     0.020777
                  py      :     0.033672
              3 H s       :     0.845956  s :     0.845956
                  pz      :     0.031275  p :     0.069530
                  px      :     0.016611
                  py      :     0.021644
              4 H s       :     0.845956  s :     0.845956
                  pz      :     0.031271  p :     0.069530
                  px      :     0.016611
                  py      :     0.021649
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.4560     6.0000    -0.4560     3.9146     3.9146    -0.0000
              1 H      0.8860     1.0000     0.1140     0.9707     0.9707     0.0000
              2 H      0.8860     1.0000     0.1140     0.9707     0.9707     0.0000
              3 H      0.8860     1.0000     0.1140     0.9707     0.9707     0.0000
              4 H      0.8860     1.0000     0.1140     0.9707     0.9707     0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9787 B(  0-C ,  2-H ) :   0.9787 B(  0-C ,  3-H ) :   0.9787 
            B(  0-C ,  4-H ) :   0.9787 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 2 sec 
            
            Total time                  ....       2.690 sec
            Sum of individual times     ....       2.519 sec  ( 93.7%)
            
            Fock matrix formation       ....       2.340 sec  ( 87.0%)
            Diagonalization             ....       0.003 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.1%)
            Initial guess               ....       0.117 sec  (  4.4%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.0%)
            SOSCF solution              ....       0.002 sec  (  0.1%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.211004769099
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = (-0.000000, -0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000      -0.00000
            Nuclear contribution   :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078381 157685.032765 157684.479059 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000001     0.000001     0.000000 
            x,y,z [Debye]:     0.000001     0.000003     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        2.952 sec (=   0.049 min)
            GTO integral calculation        ...        0.226 sec (=   0.004 min)   7.7 %
            SCF iterations                  ...        2.725 sec (=   0.045 min)  92.3 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 3 seconds 120 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  1
            |  3> C     0.00000024    -0.00000002     0.00000000
            |  4> H     1.07698196    -0.18012947    -0.00002129
            |  5> H    -0.52882274    -0.95534548     0.00013221
            |  6> H    -0.27411608     0.56763359    -0.89161936
            |  7> H    -0.27404603     0.56784158     0.89150844
            |  8> *
            |  9> %MaxCore    64000
            | 10> %scf
            | 11>   MaxIter 500
            | 12>   Convergence VeryTight
            | 13> end
            | 14> %pal nprocs     1
            | 15> end
            | 16> %method
            | 17>   IntAcc 7.0
            | 18> end
            | 19> %basis
            | 20>      NewGTO   C
            | 21>      S  8
            | 22>      1           33980.00000000               0.00014681
            | 23>      2            5089.00000000               0.00111646
            | 24>      3            1157.00000000               0.00589089
            | 25>      4             326.60000000               0.02421726
            | 26>      5             106.10000000               0.08317164
            | 27>      6              38.11000000               0.22056848
            | 28>      7              14.75000000               0.42873150
            | 29>      8               6.03500000               0.36436142
            | 30>      S  7
            | 31>      1            5089.00000000              -0.00001002
            | 32>      2             326.60000000              -0.00043659
            | 33>      3             106.10000000              -0.00193231
            | 34>      4              38.11000000              -0.02148395
            | 35>      5              14.75000000              -0.09030917
            | 36>      6               6.03500000              -0.41879151
            | 37>      7               2.53000000              -0.53180191
            | 38>      S  1
            | 39>      1               0.73550000               1.00000000
            | 40>      S  1
            | 41>      1               0.29050000               1.00000000
            | 42>      S  1
            | 43>      1               0.11110000               1.00000000
            | 44>      S  1
            | 45>      1               0.04145000               1.00000000
            | 46>      P  3
            | 47>      1              34.51000000               0.03168786
            | 48>      2               7.91500000               0.21289431
            | 49>      3               2.36800000               0.83958675
            | 50>      P  1
            | 51>      1               0.81320000               1.00000000
            | 52>      P  1
            | 53>      1               0.28900000               1.00000000
            | 54>      P  1
            | 55>      1               0.10070000               1.00000000
            | 56>      P  1
            | 57>      1               0.03218000               1.00000000
            | 58>      D  1
            | 59>      1               1.84800000               1.00000000
            | 60>      D  1
            | 61>      1               0.64900000               1.00000000
            | 62>      D  1
            | 63>      1               0.22800000               1.00000000
            | 64>      F  1
            | 65>      1               1.41900000               1.00000000
            | 66>      F  1
            | 67>      1               0.48500000               1.00000000
            | 68>      G  1
            | 69>      1               1.01100000               1.00000000
            | 70>      end
            | 71> end
            | 72> %basis
            | 73>      NewGTO   H
            | 74>      S  3
            | 75>      1              82.64000000               0.02295076
            | 76>      2              12.41000000               0.17554012
            | 77>      3               2.82400000               0.86470355
            | 78>      S  1
            | 79>      1               0.79770000               1.00000000
            | 80>      S  1
            | 81>      1               0.25810000               1.00000000
            | 82>      S  1
            | 83>      1               0.08989000               1.00000000
            | 84>      P  1
            | 85>      1               1.40700000               1.00000000
            | 86>      P  1
            | 87>      1               0.38800000               1.00000000
            | 88>      D  1
            | 89>      1               1.05700000               1.00000000
            | 90>      end
            | 91> end
            | 92> 
            | 93>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000   -0.000000    0.000000
              H      1.076982   -0.180129   -0.000021
              H     -0.528823   -0.955345    0.000132
              H     -0.274116    0.567634   -0.891619
              H     -0.274046    0.567842    0.891508
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000   -0.000000    0.000000
               1 H     1.0000    0     1.008    2.035201   -0.340395   -0.000040
               2 H     1.0000    0     1.008   -0.999330   -1.805341    0.000250
               3 H     1.0000    0     1.008   -0.518004    1.072672   -1.684916
               4 H     1.0000    0     1.008   -0.517872    1.073065    1.684707
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     1.091941502291     0.00000000     0.00000000
             H      1   2   0     1.091942631093   109.47127198     0.00000000
             H      1   2   3     1.091939904582   109.47132155   239.99991800
             H      1   2   3     1.091939897331   109.47132094   120.00008173
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
             H      1   0   0     2.063470393592     0.00000000     0.00000000
             H      1   2   0     2.063472526719   109.47127198     0.00000000
             H      1   2   3     2.063467374360   109.47132155   239.99991800
             H      1   2   3     2.063467360657   109.47132094   120.00008173
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 2 groups of distinct atoms
            
             Group   1 Type C   : 19s7p3d2f1g contracted to 6s5p3d2f1g pattern {871111/31111/111/11/1}
             Group   2 Type H   : 6s2p1d contracted to 4s2p1d pattern {3111/11/1}
            
            Atom   0C    basis set group =>   1
            Atom   1H    basis set group =>   2
            Atom   2H    basis set group =>   2
            Atom   3H    basis set group =>   2
            Atom   4H    basis set group =>   2
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      82.6400000000      0.0229507600
               2      12.4100000000      0.1755401198
               3       2.8240000000      0.8647035489
             S 1 
               1       0.7977000000      1.0000000000
             S 1 
               1       0.2581000000      1.0000000000
             S 1 
               1       0.0898900000      1.0000000000
             P 1 
               1       1.4070000000      1.0000000000
             P 1 
               1       0.3880000000      1.0000000000
             D 1 
               1       1.0570000000      1.0000000000
              end;
            
             # Basis set for element : C 
             NewGTO C 
             S 8 
               1   33980.0000000000      0.0001468100
               2    5089.0000000000      0.0011164600
               3    1157.0000000000      0.0058908900
               4     326.6000000000      0.0242172599
               5     106.1000000000      0.0831716395
               6      38.1100000000      0.2205684788
               7      14.7500000000      0.4287314976
               8       6.0350000000      0.3643614179
             S 7 
               1    5089.0000000000     -0.0000100200
               2     326.6000000000     -0.0004365900
               3     106.1000000000     -0.0019323100
               4      38.1100000000     -0.0214839499
               5      14.7500000000     -0.0903091694
               6       6.0350000000     -0.4187915074
               7       2.5300000000     -0.5318019067
             S 1 
               1       0.7355000000      1.0000000000
             S 1 
               1       0.2905000000      1.0000000000
             S 1 
               1       0.1111000000      1.0000000000
             S 1 
               1       0.0414500000      1.0000000000
             P 3 
               1      34.5100000000      0.0316878600
               2       7.9150000000      0.2128943097
               3       2.3680000000      0.8395867487
             P 1 
               1       0.8132000000      1.0000000000
             P 1 
               1       0.2890000000      1.0000000000
             P 1 
               1       0.1007000000      1.0000000000
             P 1 
               1       0.0321800000      1.0000000000
             D 1 
               1       1.8480000000      1.0000000000
             D 1 
               1       0.6490000000      1.0000000000
             D 1 
               1       0.2280000000      1.0000000000
             F 1 
               1       1.4190000000      1.0000000000
             F 1 
               1       0.4850000000      1.0000000000
             G 1 
               1       1.0110000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   68
             # of primitive gaussian functions       ...  146
             # of contracted shells                  ...   45
             # of contracted basis functions         ...  119
             Highest angular momentum                ...    4
             Maximum contraction depth               ...    8
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... RHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    1
             Number of Electrons    NEL             ....   10
             Basis Dimension        Dim             ....  119
             Nuclear Repulsion      ENuc            ....     13.4115070612 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... on
               Start iteration      SOSCFMaxIt      ....   150
               Startup grad/error   SOSCFStart      ....  0.003300
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             Orbital Gradient       TolG            ....  2.000e-06
             Orbital Rotation angle TolX            ....  2.000e-06
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 3.110e-04
            Time for diagonalization                   ...    0.003 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.002 sec
            Total time needed                          ...    0.005 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...  10952 (   0.0 sec)
            # of grid points (after weights+screening)   ...  10744 (   0.0 sec)
            nearest neighbour list constructed           ...    0.0 sec
            Grid point re-assignment to atoms done       ...    0.0 sec
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.1 sec
            
            Total number of grid points                  ...    10744
            Total number of batches                      ...      171
            Average number of points per batch           ...       62
            Average number of grid points per atom       ...     2149
            Average number of shells per batch           ...    39.40 (87.55%)
            Average number of basis functions per batch  ...   104.72 (88.00%)
            Average number of large shells per batch     ...    36.08 (91.57%)
            Average number of large basis fcns per batch ...    97.48 (93.09%)
            Maximum spatial batch extension              ...  32.44, 25.14, 18.36 au
            Average spatial batch extension              ...   4.15,  3.91,  3.48 au
            
            Time for grid setup =    0.086 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.1 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.3 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -40.1010279498   0.000000000000 0.02536851  0.00070296  0.3063194 0.7000
              1    -40.1427193779  -0.041691428142 0.02029105  0.00055931  0.1943386 0.7000
                                           ***Turning on DIIS***
              2    -40.1675389510  -0.024819573104 0.01493044  0.00037021  0.1148586 0.7000
              3    -40.3481688989  -0.180629947858 0.03774430  0.00076101  0.0763818 0.0000
              4    -40.1905893075   0.157579591364 0.00361270  0.00009918  0.0101516 0.0000
                                  *** Initiating the SOSCF procedure ***
                                       *** Shutting down DIIS ***
                                  *** Re-Reading the Fockian *** 
                                  *** Removing any level shift *** 
            ITER      Energy       Delta-E        Grad      Rot      Max-DP    RMS-DP
              5    -40.21326520  -0.0226758959  0.001211  0.001211  0.001839  0.000056
                           *** Restarting incremental Fock matrix formation ***
              6    -40.21582335  -0.0025581480  0.000418  0.000459  0.000709  0.000028
              7    -40.21582742  -0.0000040717  0.000144  0.000296  0.000475  0.000017
              8    -40.21582803  -0.0000006074  0.000026  0.000018  0.000033  0.000001
              9    -40.21582804  -0.0000000080  0.000006  0.000006  0.000005  0.000000
                              ***Gradient check signals convergence***
                          ***Rediagonalizing the Fockian in SOSCF/NRSCF***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  10 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -40.21582804 Eh           -1094.32832 eV
            
            Components:
            Nuclear Repulsion  :           13.41150706 Eh             364.94566 eV
            Electronic Energy  :          -53.62733510 Eh           -1459.27398 eV
            One Electron Energy:          -79.69161380 Eh           -2168.51906 eV
            Two Electron Energy:           26.06427870 Eh             709.24508 eV
            
            Virial components:
            Potential Energy   :          -80.36845888 Eh           -2186.93695 eV
            Kinetic Energy     :           40.15263084 Eh            1092.60863 eV
            Virial Ratio       :            2.00157392
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -7.6371e-10  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    2.0422e-06  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    4.2367e-08  Tolerance :   1.0000e-09
              Last Orbital Gradient      ...    4.6038e-07  Tolerance :   2.0000e-06
              Last Orbital Rotation      ...    6.8569e-07  Tolerance :   2.0000e-06
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
            
              NO   OCC          E(Eh)            E(eV) 
               0   2.0000     -11.207392      -304.9686 
               1   2.0000      -0.941499       -25.6195 
               2   2.0000      -0.544212       -14.8088 
               3   2.0000      -0.544212       -14.8088 
               4   2.0000      -0.544211       -14.8087 
               5   0.0000       0.064398         1.7524 
               6   0.0000       0.078256         2.1295 
               7   0.0000       0.078256         2.1295 
               8   0.0000       0.078256         2.1295 
               9   0.0000       0.228982         6.2309 
              10   0.0000       0.228982         6.2309 
              11   0.0000       0.228982         6.2309 
              12   0.0000       0.267625         7.2824 
              13   0.0000       0.367172         9.9913 
              14   0.0000       0.367172         9.9913 
              15   0.0000       0.367173         9.9913 
              16   0.0000       0.572657        15.5828 
              17   0.0000       0.572657        15.5828 
              18   0.0000       0.573677        15.6105 
              19   0.0000       0.586820        15.9682 
              20   0.0000       0.586821        15.9682 
              21   0.0000       0.586821        15.9682 
              22   0.0000       0.727113        19.7857 
              23   0.0000       0.844052        22.9678 
              24   0.0000       0.844052        22.9678 
              25   0.0000       0.844052        22.9678 
              26   0.0000       1.039460        28.2851 
              27   0.0000       1.039460        28.2851 
              28   0.0000       1.039461        28.2852 
              29   0.0000       1.234622        33.5958 
              30   0.0000       1.234623        33.5958 
              31   0.0000       1.234624        33.5958 
              32   0.0000       1.417449        38.5707 
              33   0.0000       1.549512        42.1644 
              34   0.0000       1.549513        42.1644 
              35   0.0000       1.606348        43.7110 
              36   0.0000       1.606349        43.7110 
              37   0.0000       1.606349        43.7110 
              38   0.0000       1.651062        44.9277 
              39   0.0000       1.651062        44.9277 
              40   0.0000       1.651064        44.9277 
              41   0.0000       1.789637        48.6985 
              42   0.0000       1.907875        51.9159 
              43   0.0000       1.907877        51.9160 
              44   0.0000       1.907877        51.9160 
              45   0.0000       2.098124        57.0929 
              46   0.0000       2.098124        57.0929 
              47   0.0000       2.267610        61.7048 
              48   0.0000       2.267611        61.7048 
              49   0.0000       2.267611        61.7048 
              50   0.0000       2.324547        63.2541 
              51   0.0000       2.384382        64.8823 
              52   0.0000       2.384383        64.8824 
              53   0.0000       2.384383        64.8824 
              54   0.0000       3.157283        85.9140 
              55   0.0000       3.157284        85.9141 
              56   0.0000       3.157288        85.9142 
              57   0.0000       3.421126        93.0936 
              58   0.0000       3.611455        98.2727 
              59   0.0000       3.611456        98.2727 
              60   0.0000       3.611458        98.2728 
              61   0.0000       3.654712        99.4498 
              62   0.0000       3.654713        99.4498 
              63   0.0000       4.069703       110.7422 
              64   0.0000       4.069703       110.7422 
              65   0.0000       4.069705       110.7423 
              66   0.0000       4.254663       115.7753 
              67   0.0000       4.254664       115.7753 
              68   0.0000       4.254666       115.7754 
              69   0.0000       4.359486       118.6276 
              70   0.0000       4.359487       118.6277 
              71   0.0000       4.425648       120.4280 
              72   0.0000       4.472590       121.7054 
              73   0.0000       4.472593       121.7054 
              74   0.0000       4.472595       121.7055 
              75   0.0000       4.590086       124.9026 
              76   0.0000       4.590088       124.9026 
              77   0.0000       4.590088       124.9027 
              78   0.0000       4.753553       129.3508 
              79   0.0000       4.753556       129.3508 
              80   0.0000       4.753558       129.3509 
              81   0.0000       4.860010       132.2476 
              82   0.0000       4.860010       132.2476 
              83   0.0000       4.860011       132.2476 
              84   0.0000       5.064959       137.8245 
              85   0.0000       5.424259       147.6016 
              86   0.0000       5.424263       147.6017 
              87   0.0000       5.424265       147.6018 
              88   0.0000       5.553880       151.1288 
              89   0.0000       5.553883       151.1288 
              90   0.0000       5.939929       161.6337 
              91   0.0000       5.939930       161.6337 
              92   0.0000       5.939930       161.6337 
              93   0.0000       6.303507       171.5272 
              94   0.0000       6.303508       171.5272 
              95   0.0000       6.421832       174.7469 
              96   0.0000       6.421833       174.7470 
              97   0.0000       6.421833       174.7470 
              98   0.0000       6.592964       179.4037 
              99   0.0000       7.077230       192.5812 
             100   0.0000       7.077233       192.5813 
             101   0.0000       7.083791       192.7598 
             102   0.0000       7.083793       192.7598 
             103   0.0000       7.083794       192.7598 
             104   0.0000       7.627222       207.5472 
             105   0.0000       7.627222       207.5473 
             106   0.0000       7.627224       207.5473 
             107   0.0000       7.679135       208.9599 
             108   0.0000       7.679138       208.9600 
             109   0.0000       7.679143       208.9601 
             110   0.0000       7.998616       217.6534 
             111   0.0000       7.998624       217.6536 
             112   0.0000       7.998626       217.6537 
             113   0.0000       8.010167       217.9677 
             114   0.0000       9.899189       269.3706 
             115   0.0000      10.332878       281.1719 
             116   0.0000      10.332885       281.1721 
             117   0.0000      10.332891       281.1723 
             118   0.0000      23.623908       642.8392 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            -----------------------
            MULLIKEN ATOMIC CHARGES
            -----------------------
               0 C :   -0.358474
               1 H :    0.089619
               2 H :    0.089619
               3 H :    0.089618
               4 H :    0.089618
            Sum of atomic charges:    0.0000000
            
            --------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES
            --------------------------------
              0 C s       :     3.223889  s :     3.223889
                  pz      :     1.023099  p :     3.069297
                  px      :     1.023099
                  py      :     1.023099
                  dz2     :     0.015122  d :     0.060489
                  dxz     :     0.003811
                  dyz     :     0.016352
                  dx2y2   :     0.014313
                  dxy     :     0.010891
                  f0      :     0.000015  f :     0.004227
                  f+1     :     0.000595
                  f-1     :     0.001889
                  f+2     :     0.000087
                  f-2     :     0.000138
                  f+3     :     0.001396
                  f-3     :     0.000106
                  g0      :     0.000053  g :     0.000571
                  g+1     :     0.000023
                  g-1     :     0.000100
                  g+2     :     0.000097
                  g-2     :     0.000102
                  g+3     :     0.000033
                  g-3     :     0.000002
                  g+4     :     0.000070
                  g-4     :     0.000091
              1 H s       :     0.878588  s :     0.878588
                  pz      :     0.007594  p :     0.029767
                  px      :     0.014389
                  py      :     0.007784
                  dz2     :     0.000223  d :     0.002027
                  dxz     :     0.000537
                  dyz     :     0.000037
                  dx2y2   :     0.000634
                  dxy     :     0.000595
              2 H s       :     0.878588  s :     0.878588
                  pz      :     0.007594  p :     0.029767
                  px      :     0.009232
                  py      :     0.012941
                  dz2     :     0.000223  d :     0.002027
                  dxz     :     0.000093
                  dyz     :     0.000482
                  dx2y2   :     0.000619
                  dxy     :     0.000611
              3 H s       :     0.878588  s :     0.878588
                  pz      :     0.012251  p :     0.029767
                  px      :     0.008034
                  py      :     0.009481
                  dz2     :     0.000625  d :     0.002027
                  dxz     :     0.000395
                  dyz     :     0.000603
                  dx2y2   :     0.000211
                  dxy     :     0.000193
              4 H s       :     0.878588  s :     0.878588
                  pz      :     0.012250  p :     0.029767
                  px      :     0.008034
                  py      :     0.009483
                  dz2     :     0.000624  d :     0.002027
                  dxz     :     0.000395
                  dyz     :     0.000603
                  dx2y2   :     0.000211
                  dxy     :     0.000193
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            ----------------------
            LOEWDIN ATOMIC CHARGES
            ----------------------
               0 C :    0.023868
               1 H :   -0.005967
               2 H :   -0.005966
               3 H :   -0.005968
               4 H :   -0.005968
            
            -------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES
            -------------------------------
              0 C s       :     2.698785  s :     2.698785
                  pz      :     1.013102  p :     3.039303
                  px      :     1.013101
                  py      :     1.013101
                  dz2     :     0.052041  d :     0.208166
                  dxz     :     0.013115
                  dyz     :     0.056274
                  dx2y2   :     0.049256
                  dxy     :     0.037480
                  f0      :     0.000406  f :     0.029271
                  f+1     :     0.006059
                  f-1     :     0.007975
                  f+2     :     0.002354
                  f-2     :     0.003731
                  f+3     :     0.007407
                  f-3     :     0.001339
                  g0      :     0.000032  g :     0.000606
                  g+1     :     0.000007
                  g-1     :     0.000030
                  g+2     :     0.000152
                  g-2     :     0.000225
                  g+3     :     0.000010
                  g-3     :     0.000001
                  g+4     :     0.000027
                  g-4     :     0.000124
              1 H s       :     0.832640  s :     0.832640
                  pz      :     0.040116  p :     0.148221
                  px      :     0.067232
                  py      :     0.040874
                  dz2     :     0.001829  d :     0.025105
                  dxz     :     0.008427
                  dyz     :     0.000577
                  dx2y2   :     0.005473
                  dxy     :     0.008799
              2 H s       :     0.832640  s :     0.832640
                  pz      :     0.040116  p :     0.148221
                  px      :     0.046653
                  py      :     0.061452
                  dz2     :     0.001829  d :     0.025105
                  dxz     :     0.001466
                  dyz     :     0.007537
                  dx2y2   :     0.008282
                  dxy     :     0.005990
              3 H s       :     0.832640  s :     0.832640
                  pz      :     0.058701  p :     0.148222
                  px      :     0.041872
                  py      :     0.047648
                  dz2     :     0.008115  d :     0.025106
                  dxz     :     0.005365
                  dyz     :     0.005848
                  dx2y2   :     0.003092
                  dxy     :     0.002686
              4 H s       :     0.832640  s :     0.832640
                  pz      :     0.058697  p :     0.148222
                  px      :     0.041872
                  py      :     0.047654
                  dz2     :     0.008115  d :     0.025106
                  dxz     :     0.005363
                  dyz     :     0.005847
                  dx2y2   :     0.003093
                  dxy     :     0.002687
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.3585     6.0000    -0.3585     3.9441     3.9441     0.0000
              1 H      0.9104     1.0000     0.0896     0.9899     0.9899     0.0000
              2 H      0.9104     1.0000     0.0896     0.9899     0.9899    -0.0000
              3 H      0.9104     1.0000     0.0896     0.9899     0.9899    -0.0000
              4 H      0.9104     1.0000     0.0896     0.9899     0.9899     0.0000
            
              Mayer bond orders larger than 0.100000
            B(  0-C ,  1-H ) :   0.9860 B(  0-C ,  2-H ) :   0.9860 B(  0-C ,  3-H ) :   0.9860 
            B(  0-C ,  4-H ) :   0.9860 
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 14 sec 
            
            Total time                  ....      14.955 sec
            Sum of individual times     ....      14.726 sec  ( 98.5%)
            
            Fock matrix formation       ....      14.430 sec  ( 96.5%)
            Diagonalization             ....       0.016 sec  (  0.1%)
            Density matrix formation    ....       0.001 sec  (  0.0%)
            Population analysis         ....       0.004 sec  (  0.0%)
            Initial guess               ....       0.177 sec  (  1.2%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.006 sec  (  0.0%)
            SOSCF solution              ....       0.007 sec  (  0.0%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -40.215828039203
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = (-0.000000, -0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000       0.00000
            Nuclear contribution   :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     5.259808     5.259807     5.259788 
            Rotational constants in MHz : 157685.078381 157685.032765 157684.479059 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000     0.000001     0.000000 
            x,y,z [Debye]:     0.000001     0.000003     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...       15.266 sec (=   0.254 min)
            GTO integral calculation        ...        0.289 sec (=   0.005 min)   1.9 %
            SCF iterations                  ...       14.977 sec (=   0.250 min)  98.1 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 15 seconds 415 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            WARNING: MDCI localization with Augmented Hessian Foster-Boys
              ===> : Switching off randomization!
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! CCSD(T) Printbasis
            |  2> * xyz   0  3
            |  3> C     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14>   NewNCore C     2 end
            | 15>   NewNCore H     0 end
            | 16> end
            | 17> %basis
            | 18>      NewGTO   C
            | 19>      S  6
            | 20>      1            3047.52488000               0.00183474
            | 21>      2             457.36951800               0.01403732
            | 22>      3             103.94868500               0.06884262
            | 23>      4              29.21015530               0.23218444
            | 24>      5               9.28666296               0.46794135
            | 25>      6               3.16392696               0.36231199
            | 26>      S  3
            | 27>      1               7.86827235              -0.11933242
            | 28>      2               1.88128854              -0.16085415
            | 29>      3               0.54424926               1.14345644
            | 30>      P  3
            | 31>      1               7.86827235               0.06899907
            | 32>      2               1.88128854               0.31642396
            | 33>      3               0.54424926               0.74430829
            | 34>      S  1
            | 35>      1               0.16871448               1.00000000
            | 36>      P  1
            | 37>      1               0.16871448               1.00000000
            | 38>      D  1
            | 39>      1               0.80000000               1.00000000
            | 40>      end
            | 41> end
            | 42> 
            | 43>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type C   : 10s4p1d contracted to 3s2p1d pattern {631/31/1}
            
            Atom   0C    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    3047.5248800000      0.0018347400
               2     457.3695180000      0.0140373200
               3     103.9486850000      0.0688426199
               4      29.2101553000      0.2321844397
               5       9.2866629600      0.4679413494
               6       3.1639269600      0.3623119895
             S 3 
               1       7.8682723500     -0.1193324197
               2       1.8812885400     -0.1608541495
               3       0.5442492600      1.1434564368
             P 3 
               1       7.8682723500      0.0689990700
               2       1.8812885400      0.3164239600
               3       0.5442492600      0.7443082900
             S 1 
               1       0.1687144800      1.0000000000
             P 1 
               1       0.1687144800      1.0000000000
             D 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   15
             # of primitive gaussian functions       ...   27
             # of contracted shells                  ...    6
             # of contracted basis functions         ...   14
             Highest angular momentum                ...    2
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    3
             Number of Electrons    NEL             ....    6
             Basis Dimension        Dim             ....   14
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.869e-01
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   3592 (   0.0 sec)
            # of grid points (after weights+screening)   ...   3592 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     3592
            Total number of batches                      ...       57
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     3592
            Average number of shells per batch           ...     5.28 (87.93%)
            Average number of basis functions per batch  ...    12.52 (89.41%)
            Average number of large shells per batch     ...     5.00 (94.77%)
            Average number of large basis fcns per batch ...    11.86 (94.77%)
            Maximum spatial batch extension              ...  32.44, 31.96, 31.96 au
            Average spatial batch extension              ...   8.49,  7.32,  7.29 au
            
            Time for grid setup =    0.017 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -37.6735754210   0.000000000000 0.01104721  0.00112100  0.0660696 0.7000
              1    -37.6752865647  -0.001711143700 0.00969647  0.00098784  0.0471530 0.7000
                                           ***Turning on DIIS***
              2    -37.6766292087  -0.001342643964 0.02504675  0.00259048  0.0333430 0.0000
              3    -37.6779680277  -0.001338818962 0.01139526  0.00087809  0.0033720 0.0000
              4    -37.6784643207  -0.000496292995 0.00938006  0.00070083  0.0018490 0.0000
              5    -37.6796789102  -0.001214589585 0.00310507  0.00023131  0.0005110 0.0000
              6    -37.6806149230  -0.000936012729 0.00018474  0.00001805  0.0000267 0.0000
              7    -37.6805988385   0.000016084446 0.00007451  0.00000656  0.0000091 0.0000
              8    -37.6805786216   0.000020216889 0.00000662  0.00000056  0.0000008 0.0000
              9    -37.6805767497   0.000001871971 0.00000037  0.00000003  0.0000000 0.0000
                                        ***DIIS convergence achieved***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  10 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -37.68057666 Eh           -1025.34062 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :          -37.68057666 Eh           -1025.34062 eV
            One Electron Energy:          -50.48084904 Eh           -1373.65374 eV
            Two Electron Energy:           12.80027238 Eh             348.31312 eV
            
            Virial components:
            Potential Energy   :          -75.38356908 Eh           -2051.29120 eV
            Kinetic Energy     :           37.70299242 Eh            1025.95058 eV
            Virial Ratio       :            1.99940546
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...    9.2872e-08  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    1.4405e-08  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    1.2545e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.6281e-09  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     2.004711
            Ideal value S*(S+1) for S=1.0   :     2.000000
            Deviation                       :     0.004711
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.336039      -308.4693 
               1   1.0000      -0.819963       -22.3123 
               2   1.0000      -0.429209       -11.6794 
               3   1.0000      -0.429209       -11.6794 
               4   0.0000       0.054983         1.4962 
               5   0.0000       0.707576        19.2541 
               6   0.0000       0.707576        19.2541 
               7   0.0000       0.761399        20.7187 
               8   0.0000       0.787635        21.4326 
               9   0.0000       1.902095        51.7586 
              10   0.0000       1.902095        51.7586 
              11   0.0000       1.934488        52.6401 
              12   0.0000       1.934488        52.6401 
              13   0.0000       1.946953        52.9793 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.290960      -307.2426 
               1   1.0000      -0.574924       -15.6445 
               2   0.0000       0.098737         2.6868 
               3   0.0000       0.157842         4.2951 
               4   0.0000       0.157842         4.2951 
               5   0.0000       0.818574        22.2745 
               6   0.0000       0.835024        22.7222 
               7   0.0000       0.871296        23.7092 
               8   0.0000       0.871296        23.7092 
               9   0.0000       2.024597        55.0921 
              10   0.0000       2.041032        55.5393 
              11   0.0000       2.041032        55.5393 
              12   0.0000       2.095301        57.0160 
              13   0.0000       2.095301        57.0160 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 C :    0.000000    2.000000
            Sum of atomic charges         :    0.0000000
            Sum of atomic spin populations:    2.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 C s       :     3.998659  s :     3.998659
                  pz      :     0.053814  p :     2.000000
                  px      :     0.994152
                  py      :     0.952033
                  dz2     :     0.001134  d :     0.001341
                  dxz     :     0.000022
                  dyz     :     0.000183
                  dx2y2   :     0.000002
                  dxy     :     0.000001
            
            SPIN
              0 C s       :    -0.000108  s :    -0.000108
                  pz      :     0.053814  p :     2.000000
                  px      :     0.994152
                  py      :     0.952033
                  dz2     :     0.000091  d :     0.000108
                  dxz     :     0.000002
                  dyz     :     0.000015
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 C :    0.000000    2.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 C s       :     3.998659  s :     3.998659
                  pz      :     0.053814  p :     2.000000
                  px      :     0.994152
                  py      :     0.952033
                  dz2     :     0.001134  d :     0.001341
                  dxz     :     0.000022
                  dyz     :     0.000183
                  dx2y2   :     0.000002
                  dxy     :     0.000001
            
            SPIN
              0 C s       :    -0.000108  s :    -0.000108
                  pz      :     0.053814  p :     2.000000
                  px      :     0.994152
                  py      :     0.952033
                  dz2     :     0.000091  d :     0.000108
                  dxz     :     0.000002
                  dyz     :     0.000015
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.0000     6.0000     0.0000     2.0094     0.0000     2.0094
            
              Mayer bond orders larger than 0.100000
            
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.025 sec
            Sum of individual times     ....       0.857 sec  ( 83.7%)
            
            Fock matrix formation       ....       0.740 sec  ( 72.2%)
            Diagonalization             ....       0.001 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.1%)
            Initial guess               ....       0.097 sec  (  9.5%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.1%)
            
            
            ------------------------------------------------------------------------------- 
                                          ORCA-MATRIX DRIVEN CI                            
            ------------------------------------------------------------------------------- 
            
            --------------------------------
            AUTOMATIC CHOICE OF INCORE LEVEL
            --------------------------------
            
            Memory available                           ...  32000.00 MB
            Memory needed for S+T                      ...      0.01 MB
            Memory needed for J+K                      ...      0.03 MB
            Memory needed for DIIS                     ...      0.19 MB
            Memory needed for 3-ext                    ...      0.02 MB
            Memory needed for 4-ext                    ...      0.04 MB
            Memory needed for triples                  ...      0.04 MB
             -> Final InCoreLevel    ... 5
             -> check shows that triples correction can be computed
            
            
            Wavefunction type
            -----------------
            Correlation treatment                      ...      CCSD     
            Single excitations                         ... ON
            Orbital optimization                       ... OFF
            Calculation of Z vector                    ... OFF
            Calculation of Brueckner orbitals          ... OFF
            Perturbative triple excitations            ... ON
            Calculation of F12 correction              ... OFF
            Frozen core treatment                      ... chemical core (2 el)
            Reference Wavefunction                     ... UHF
              Alpha-MOs occ    :     1 ...    3 (  3 MO's/  3 electrons)
              Beta-MOs occ     :     1 ...    1 (  1 MO's/  1 electrons)
              Alpha-MOs virt   :     4 ...   13 ( 10 MO's              )
              Beta-MOs virt    :     2 ...   13 ( 12 MO's              )
            Number of AO's                             ...     14
            Number of electrons                        ...      6
            Number of correlated electrons             ...      4
            
            Algorithmic settings
            --------------------
            Integral transformation                    ... AO direct full transformation
            K(C) Formation                             ... FULL-MO TRAFO
            Maximum number of iterations               ...        50
            Convergence tolerance (max. residuum)      ... 2.500e-05
            Level shift for amplitude update           ... 2.000e-01
            Maximum number of DIIS vectors             ...         7
            DIIS turned on at iteration                ...         0
            Damping before turning on DIIS             ...     0.500
            Damping after turning on DIIS              ...     0.000
            Pair specific amplitude update             ... OFF
            Natural orbital iterations                 ... OFF
            Perturbative natural orbital generation    ... OFF
            Printlevel                                 ... 2
            
            Memory handling:
            ----------------
            Maximum memory for working arrays          ...  32000 MB
            Data storage in matrix containers          ... UNCOMPRESSED
            Data type for integral storage             ... DOUBLE
            In-Core Storage of quantities:
               Amplitudes+Sigma Vector      ... YES
               J+K operators                ... YES
               DIIS vectors                 ... YES
               3-external integrals         ... YES
               4-external integrals         ... YES
            
            
            Initializing the integral package          ... done
            Warning: reference  - re-canonicalizations have been set to INT 1 VIRT 1
            
            --------------------------
            UNRESTRICTED FOCK OPERATOR
            --------------------------
            
            <ss|ss>:           21 b            0 skpd (  0.0%)    0.000 s ( 0.005 ms/b)
            <ss|sp>:           36 b            0 skpd (  0.0%)    0.000 s ( 0.006 ms/b)
            <ss|sd>:           18 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <ss|pp>:           18 b            0 skpd (  0.0%)    0.000 s ( 0.005 ms/b)
            <ss|pd>:           12 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <ss|dd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <sp|sp>:           21 b            0 skpd (  0.0%)    0.000 s ( 0.005 ms/b)
            <sp|sd>:           18 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <sp|pp>:           18 b            0 skpd (  0.0%)    0.000 s ( 0.007 ms/b)
            <sp|pd>:           12 b            0 skpd (  0.0%)    0.000 s ( 0.007 ms/b)
            <sp|dd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.007 ms/b)
            <sd|sd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.006 ms/b)
            <sd|pp>:            9 b            0 skpd (  0.0%)    0.000 s ( 0.007 ms/b)
            <sd|pd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.010 ms/b)
            <sd|dd>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.014 ms/b)
            <pp|pp>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.012 ms/b)
            <pp|pd>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.014 ms/b)
            <pp|dd>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.015 ms/b)
            <pd|pd>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.022 ms/b)
            <pd|dd>:            2 b            0 skpd (  0.0%)    0.000 s ( 0.033 ms/b)
            <dd|dd>:            1 b            0 skpd (  0.0%)    0.000 s ( 0.072 ms/b)
            Recanonicalizing the internal orbitals
            Recanonicalizing the virtual orbitals
            Time needed for Fock operator              ...            0.002 sec
            Reference energy                           ...    -37.680576656
            Warning: for UHF the TrafoType has to be JK
            Warning: for UHF the K(C)-option cannot be MO but must be AOX
            
            -------------------------------
            PARTIAL EXCHANGE TRANSFORMATION
            -------------------------------
            
            Transformation type                        ... two-operators
            Generation of integrals (i,mue|j,nue)      ... ON
            Generation of integrals (mue,kappa|nue,tau)... ON
            Generation of integrals (i,mue|a,nue)      ... ON
            Dimension of the basis                     ...   14
            Number of internal alpha-MOs               ...    3 (   1-   3)
            Number of internal beta-MOs                ...    1 (   1-   1)
            Number of external alpha-MOs               ...   10 (   4-  13)
            Number of external beta-MOs                ...   12 (   2-  13)
            Pair cutoff                                ... 0.000e+00 Eh
            Number of AO pairs in the trafo            ...  105
            Total Number of distinct AO pairs          ...  105
            Memory devoted for trafo                   ... 32000.0 MB 
            Max. Number of MO pairs treated together   ... 21399510      
            Number Format for Storage                  ... Double (8 Byte)
            Integral package used                      ... LIBINT
            
            Starting integral evaluation:
                ... done with AO integral generation
            Closing buffer AOK[aa] ( 0.00 GB; CompressionRatio= 0.86)
            Closing buffer AOK[bb] ( 0.00 GB; CompressionRatio= 0.40)
            Closing buffer AOK[ab] ( 0.00 GB; CompressionRatio= 0.67)
            Closing buffer AOK[ba] ( 0.00 GB; CompressionRatio= 0.67)
            Collecting buffer AOK 
            Closing buffer IAAO1[aa] ( 0.00 GB; CompressionRatio= 0.95)
            Closing buffer IAAO1[bb] ( 0.00 GB; CompressionRatio= 0.89)
            Closing buffer IAAO1[ab] ( 0.00 GB; CompressionRatio= 0.96)
            Closing buffer IAAO1[ba] ( 0.00 GB; CompressionRatio= 0.87)
            Closing buffer IAAO2[aa] ( 0.00 GB; CompressionRatio= 0.95)
            Closing buffer IAAO2[bb] ( 0.00 GB; CompressionRatio= 0.89)
            Closing buffer IAAO2[ab] ( 0.00 GB; CompressionRatio= 0.96)
            Closing buffer IAAO2[ba] ( 0.00 GB; CompressionRatio= 0.87)
            Collecting buffer IAAO 
            Closing buffer PRQS    ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer PRQS 
            Number of alpha/alpha MO pairs in trafo    ...    6
            Number of beta /beta  MO pairs in trafo    ...    1
            Number of alpha/ beta MO pairs in trafo    ...    3
            ------------------------
            SORTING OF (i,mue|j,nue)
            ------------------------
            
            SORTING OF ALPHA/ALPHA PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[aa] ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer KAO 
            SORTING OF BETA /BETA  PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[bb] ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer KAO 
            SORTING OF ALPHA/BETA  PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[ab] ( 0.00 GB; CompressionRatio= 0.992405063291)
            Collecting buffer KAO[ab] 
            ------------------------
            SORTING OF (i,mue|a,nue)
            ------------------------
            
            Number of alpha/alpha (i,a) pairs in trafo  ...   30
            Number of beta /beta  (i,a) pairs in trafo  ...   12
            Number of alpha/ beta (i,a) pairs in trafo  ...   36
            Number of beta /alpha (i,a) pairs in trafo  ...   10
            Setting up the alpha/alpha list             ... done
            Setting up the beta /beta  list             ... done
            Setting up the alpha/beta  list             ... done
            Setting up the beta /alpha list             ... done
                ... Now sorting (i,mue|a,nue)integrals
                ... Integrals (i,b|a,c) will be made on the fly
            SORTING OF ALPHA/ALPHA PAIRS
            IBATCH = 1 of  1
            Closing buffer IPAQ[aa]  0.00 GB; CompressionRatio= 1.00)
            SORTING OF BETA /BETA  PAIRS
            IBATCH = 1 of  1
            Closing buffer IPAQ[bb]( 0.00 GB; CompressionRatio= 1.00)
            SORTING OF ALPHA/BETA  PAIRS (NMatSort_ab=36)
            IBATCH = 1 of  1
            Closing buffer IPAQ[ab]( 0.00 GB; CompressionRatio= 1.00)
            SORTING OF BETA/ALPHA  PAIRS
            IBATCH = 1 of  1
            Closing buffer IPAQ[ba]( 0.00 GB; CompressionRatio= 1.00)
            N(AO-Batches) Done                         ...       756 
            N(AO-Batches) Skipped                      ...         0 
            N(IJ)-pairs Skipped                        ...         0 
            TOTAL TIME for half transformation         ...     0.008 sec
            AO-integral generation                     ...     0.003 sec
            Half transformation                        ...     0.002 sec
            K-integral sorting                         ...     0.001 sec
            
            ------------------------------
            PARTIAL COULOMB TRANSFORMATION
            ------------------------------
            
            Transformation type                        ... two-operators
            Dimension of the basis                     ...   14
            Number of internal alpha-MOs               ...    3 (1-3)
            Number of internal beta-MOs                ...    1 (1-1)
            Pair cutoff                                ... 0.000e+00 Eh
            Number of AO pairs included in the trafo   ...  105
            Total Number of distinct AO pairs          ...  105
            Memory devoted for trafo                   ... 32000.0 MB 
            Max. Number of MO pairs treated together   ... 39945752      
            Max. Number of MOs treated per batch       ... 2853268      
            Number Format for Storage                  ... Double (8 Byte)
            AO-integral source                         ... DIRECT
            Integral package used                      ... LIBINT
            
            Starting integral evaluation:
            <ss|**>:          126 b        0 skpd     0.001 s (  0.005 ms/b)
            <sp|**>:          126 b        0 skpd     0.001 s (  0.005 ms/b)
            <sd|**>:           63 b        0 skpd     0.000 s (  0.005 ms/b)
            <pp|**>:           63 b        0 skpd     0.000 s (  0.007 ms/b)
            <pd|**>:           42 b        0 skpd     0.000 s (  0.009 ms/b)
            <dd|**>:           21 b        0 skpd     0.000 s (  0.010 ms/b)
            Closing buffer AOJ[aa] ( 0.00 GB; CompressionRatio= 0.80)
            Closing buffer AOJ[bb] ( 0.00 GB; CompressionRatio= 0.40)
            Collecting buffer AOJ 
                ... done with AO integral generation
            Number of Alpha-MO pairs included          ...    6
            Number of Beta-MO pairs included           ...    1
                ... Now sorting integrals
            SORTING ALPHA/ALPHA PAIRS
            IBATCH = 1 of  1
            Closing buffer JAO[aa] ( 0.00 GB; CompressionRatio= 0.99)
            SORTING BETA/BETA PAIRS
            IBATCH = 1 of  1
            Closing buffer JAO[bb] ( 0.00 GB; CompressionRatio= 0.99)
            Collecting buffer JAO 
            TOTAL TIME for half transformation         ...     0.003 sec
            AO-integral generation                     ...     0.002 sec
            Half transformation                        ...     0.001 sec
            J-integral sorting                         ...     0.000 sec
            
            -------------------------- SECOND HALF TRANSFORMATION -------------------------
            Formation of (ij|kl),(ij|ka), (ij|ab)      ... ok (     0.000 sec)
            Formation of (ik|jl),(ik|ja), (ia|jb)      ... ok (     0.000 sec)
            
            
            -----------------------
            SPIN UNRESTRICTED GUESS
            -----------------------
            
            Entering MDCI_UHF_Guess, Tailored=0
            Spin-components of the MP2 energy:
            EMP2(aa)=     -0.009007794
            EMP2(bb)=      0.000000000
            EMP2(ab)=     -0.041855969
            
            Initial guess performed in     0.000 sec
            E(0)                                       ...    -37.680576656
            E(MP2)                                     ...     -0.050863763
            Initial E(tot)                             ...    -37.731440419
            <T|T>                                      ...      0.018678736
            Number of pairs included                   ... 6
            
            ------------------------------------------------
                              UHF COUPLED CLUSTER ITERATIONS
            ------------------------------------------------
            
            Number of amplitudes to be optimized       ...          531
            
            Iter       E(tot)           E(Corr)          Delta-E          Residual     Time      <S|S>**1/2
              0    -37.731440419     -0.050863763      0.000000000      0.045754340    0.00      0.000000002
                                       *** Turning on DIIS ***
              1    -37.743068020     -0.062491364     -0.011627602      0.025744304    0.00      0.005385004
              2    -37.749101997     -0.068525341     -0.006033976      0.009321309    0.00      0.009764389
              3    -37.750219457     -0.069642801     -0.001117461      0.001262902    0.00      0.011337650
              4    -37.750370462     -0.069793806     -0.000151004      0.000083669    0.00      0.011338001
              5    -37.750347977     -0.069771321      0.000022485      0.000034679    0.00      0.011318254
              6    -37.750360825     -0.069784169     -0.000012848      0.000012615    0.00      0.011325541
                           --- The Coupled-Cluster iterations have converged ---
            
            ----------------------
            COUPLED CLUSTER ENERGY
            ----------------------
            
            E(0)                                       ...    -37.680576656
            E(CORR)                                    ...     -0.069784169
            E(TOT)                                     ...    -37.750360825
            Singles norm <S|S>**1/2                    ...      0.011325541 ( 0.007735133, 0.003590408)  
            T1 diagnostic                              ...      0.005662771                              
            
            ------------------
            LARGEST AMPLITUDES
            ------------------
               1a->  4a   1b->  2b       0.127363
               3a->  6a   2a->  5a       0.042512
               3a->  5a   2a->  6a       0.042512
               1a->  4a   1b->  5b       0.041082
               1a->  8a   1b->  2b       0.038292
               3a-> 10a   1b->  4b       0.034194
               2a->  9a   1b->  4b       0.034194
               3a->  9a   1b->  3b       0.034194
               2a-> 10a   1b->  3b       0.034194
               3a->  6a   1b->  6b       0.033100
               2a->  5a   1b->  6b       0.033100
               2a-> 12a   1b->  2b       0.031119
               3a-> 11a   1b->  2b       0.031119
               1a->  7a   1b->  6b       0.029026
               3a->  9a   2a-> 10a       0.023887
               3a-> 10a   2a->  9a       0.023887
            
            ----------------------
            UHF TRIPLES CORRECTION (Algorithm 1)
            ----------------------
            
            Multiplier for the singles contribution    ...      1.000000000
            
            SPIN-CASE Alpha-Alpha-Alpha:
            10% done
            20% done
            30% done
            40% done
            50% done
            60% done
            70% done
            80% done
            90% done
            
            
            SPIN-CASE Beta-Beta-Beta:
            
            SPIN-CASE Alpha-Alpha-Beta:
            10% done
            20% done
            30% done
            40% done
            50% done
            60% done
            70% done
            80% done
            90% done
            
            
            SPIN-CASE Beta-Beta-Alpha:
            
            Triples Correction (T)                     ...     -0.000918656
                alpha-alpha-alpha ... -0.000011840 (  1.3%)
                alpha-alpha-beta  ... -0.000906816 ( 98.7%)
                alpha-beta -beta  ...  0.000000000 ( -0.0%)
                beta -beta -beta  ...  0.000000000 ( -0.0%)
            Scaling of triples based on CCSD energies (Peterson et al. Molecular Physics 113, 1551 (2015))
            E(T*) = f*E(T) where f = E(F12-CCSD)/E(CCSD) 
            f = CCSD (with F12)/ CCSD (without F12)    ...      1.000000000
            Scaled triples correction (T)              ...     -0.000918656
            
            Final correlation energy                   ...     -0.070702825
            E(CCSD)                                    ...    -37.750360825
            E(CCSD(T))                                 ...    -37.751279481
            
            
            
                    !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! 
                    !  Warning: Densities are linearized densities                           !
                    !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! 
            
            NORM  =      1.042002708 sqrt=     1.020785339
            W(HF) =      0.959690404
            ------------------------------------------------------------------------------
                                       ORCA POPULATION ANALYSIS
            ------------------------------------------------------------------------------
            Input electron density              ... input.mdcip
            Input spin density                  ... input.mdcir
            BaseName (.gbw .S,...)              ... input
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            ------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN DENSITIES
            ------------------------------------------
               0 C :   -0.000000    2.000000
            Sum of atomic charges       :   -0.0000000
            Sum of atomic spin densities:    2.0000000
            
            ---------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN DENSITIES
            ---------------------------------------------------
            CHARGE
              0 C s       :     3.944252  s :     3.944252
                  pz      :     0.095279  p :     2.040195
                  px      :     0.992553
                  py      :     0.952363
                  dz2     :     0.002377  d :     0.015554
                  dxz     :     0.002783
                  dyz     :     0.002731
                  dx2y2   :     0.003831
                  dxy     :     0.003831
            
            SPIN
              0 C s       :     0.013081  s :     0.013081
                  pz      :     0.051989  p :     1.977152
                  px      :     0.983442
                  py      :     0.941721
                  dz2     :     0.000631  d :     0.009767
                  dxz     :     0.001324
                  dyz     :     0.001235
                  dx2y2   :     0.003288
                  dxy     :     0.003288
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -----------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN DENSITIES
            -----------------------------------------
               0 C :    0.000000    2.000000
            
            --------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN DENSITIES
            --------------------------------------------------
            CHARGE
              0 C s       :     3.944252  s :     3.944252
                  pz      :     0.095279  p :     2.040195
                  px      :     0.992553
                  py      :     0.952363
                  dz2     :     0.002377  d :     0.015554
                  dxz     :     0.002783
                  dyz     :     0.002731
                  dx2y2   :     0.003831
                  dxy     :     0.003831
            
            SPIN
              0 C s       :     0.013081  s :     0.013081
                  pz      :     0.051989  p :     1.977152
                  px      :     0.983442
                  py      :     0.941721
                  dz2     :     0.000631  d :     0.009767
                  dxz     :     0.001324
                  dyz     :     0.001235
                  dx2y2   :     0.003288
                  dxy     :     0.003288
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.0000     6.0000    -0.0000     2.2742     0.0000     2.2742
            
            
            
            
            
            ------------------------------------------------------------------------------- 
                                                 TIMINGS                                   
            ------------------------------------------------------------------------------- 
            
            
            Total execution time                   ...        0.128 sec
            
            Fock Matrix Formation                  ...        0.002 sec (  1.9%)
            Initial Guess                          ...        0.000 sec (  0.0%)
            DIIS Solver                            ...        0.001 sec (  0.4%)
            State Vector Update                    ...        0.000 sec (  0.0%)
            Sigma-vector construction              ...        0.015 sec ( 11.9%)
              <D|H|D>(4-ext)                       ...        0.002 sec ( 15.0% of sigma)
              Fock-dressing                        ...        0.009 sec ( 58.6% of sigma)
              (ij|ab),(ia|jb)-dressing             ...        0.001 sec (  9.8% of sigma)
            Total Time for computing (T)           ...        0.001 sec (  0.7% of ALL)
            
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -37.751279480924
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000      -0.00000      -0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000      -0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000    -0.000000    -0.000000 
            x,y,z [Debye]:     0.000000    -0.000000    -0.000000 
            
             
            
                                       *** MDCI DENSITY ***
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.mdcip
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000      -0.00000      -0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000      -0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000    -0.000000    -0.000000 
            x,y,z [Debye]:     0.000000    -0.000000    -0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        1.458 sec (=   0.024 min)
            GTO integral calculation        ...        0.244 sec (=   0.004 min)  16.7 %
            SCF iterations                  ...        1.050 sec (=   0.017 min)  72.0 %
            MDCI module                     ...        0.165 sec (=   0.003 min)  11.3 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 1 seconds 680 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            WARNING: No MP2 level density has been requested!
                     To caclulate MP2 level properties use
                     %mp2 Density relaxed end
                     or
                     %mp2 Density unrelaxed end
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! MP2 Printbasis
            |  2> * xyz   0  3
            |  3> C     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14>   NewNCore C     2 end
            | 15>   NewNCore H     0 end
            | 16> end
            | 17> %basis
            | 18>      NewGTO   C
            | 19>      S  6
            | 20>      1            4563.24000000               0.00196665
            | 21>      2             682.02400000               0.01523060
            | 22>      3             154.97300000               0.07612691
            | 23>      4              44.45530000               0.26080103
            | 24>      5              13.02900000               0.61646208
            | 25>      6               1.82773000               0.22100603
            | 26>      S  3
            | 27>      1              20.96420000               0.11466008
            | 28>      2               4.80331000               0.91999965
            | 29>      3               1.45933000              -0.00303068
            | 30>      P  3
            | 31>      1              20.96420000               0.04024869
            | 32>      2               4.80331000               0.23759396
            | 33>      3               1.45933000               0.81585385
            | 34>      S  1
            | 35>      1               0.48345600               1.00000000
            | 36>      P  1
            | 37>      1               0.48345600               1.00000000
            | 38>      S  1
            | 39>      1               0.14558500               1.00000000
            | 40>      P  1
            | 41>      1               0.14558500               1.00000000
            | 42>      S  1
            | 43>      1               0.04380000               1.00000000
            | 44>      P  1
            | 45>      1               0.04380000               1.00000000
            | 46>      D  1
            | 47>      1               2.50400000               1.00000000
            | 48>      D  1
            | 49>      1               0.62600000               1.00000000
            | 50>      D  1
            | 51>      1               0.15650000               1.00000000
            | 52>      F  1
            | 53>      1               0.80000000               1.00000000
            | 54>      end
            | 55> end
            | 56> 
            | 57>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type C   : 12s6p3d1f contracted to 5s4p3d1f pattern {63111/3111/111/1}
            
            Atom   0C    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : C 
             NewGTO C 
             S 6 
               1    4563.2400000000      0.0019666500
               2     682.0240000000      0.0152306000
               3     154.9730000000      0.0761269100
               4      44.4553000000      0.2608010300
               5      13.0290000000      0.6164620800
               6       1.8277300000      0.2210060300
             S 3 
               1      20.9642000000      0.1146600796
               2       4.8033100000      0.9199996470
               3       1.4593300000     -0.0030306800
             P 3 
               1      20.9642000000      0.0402486900
               2       4.8033100000      0.2375939599
               3       1.4593300000      0.8158538497
             S 1 
               1       0.4834560000      1.0000000000
             P 1 
               1       0.4834560000      1.0000000000
             S 1 
               1       0.1455850000      1.0000000000
             P 1 
               1       0.1455850000      1.0000000000
             S 1 
               1       0.0438000000      1.0000000000
             P 1 
               1       0.0438000000      1.0000000000
             D 1 
               1       2.5040000000      1.0000000000
             D 1 
               1       0.6260000000      1.0000000000
             D 1 
               1       0.1565000000      1.0000000000
             F 1 
               1       0.8000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   22
             # of primitive gaussian functions       ...   52
             # of contracted shells                  ...   13
             # of contracted basis functions         ...   39
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    6
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    3
             Number of Electrons    NEL             ....    6
             Basis Dimension        Dim             ....   39
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 7.696e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   3592 (   0.0 sec)
            # of grid points (after weights+screening)   ...   3592 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     3592
            Total number of batches                      ...       57
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     3592
            Average number of shells per batch           ...    11.43 (87.93%)
            Average number of basis functions per batch  ...    34.29 (87.93%)
            Average number of large shells per batch     ...    10.98 (96.08%)
            Average number of large basis fcns per batch ...    32.88 (95.88%)
            Maximum spatial batch extension              ...  32.44, 31.96, 31.96 au
            Average spatial batch extension              ...   8.49,  7.32,  7.29 au
            
            Time for grid setup =    0.017 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -37.6744098605   0.000000000000 0.01317135  0.00050842  0.1361695 0.7000
              1    -37.6780457133  -0.003635852811 0.01135596  0.00044752  0.0961910 0.7000
                                           ***Turning on DIIS***
              2    -37.6809976306  -0.002951917313 0.02832507  0.00117065  0.0676212 0.0000
              3    -37.6841490314  -0.003151400758 0.01608851  0.00045527  0.0081016 0.0000
              4    -37.6871658468  -0.003016815453 0.01162010  0.00031753  0.0044819 0.0000
              5    -37.6870114135   0.000154433294 0.00653544  0.00017374  0.0019814 0.0000
              6    -37.6889927085  -0.001981294970 0.00192096  0.00006714  0.0006733 0.0000
              7    -37.6902639769  -0.001271268373 0.00046136  0.00001298  0.0000881 0.0000
              8    -37.6902683184  -0.000004341573 0.00009846  0.00000317  0.0000182 0.0000
              9    -37.6902534185   0.000014899896 0.00000667  0.00000025  0.0000026 0.0000
             10    -37.6902524638   0.000000954735 0.00000112  0.00000004  0.0000004 0.0000
             11    -37.6902525085  -0.000000044739 0.00000017  0.00000001  0.0000000 0.0000
                                        ***DIIS convergence achieved***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  12 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -37.69025252 Eh           -1025.60391 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :          -37.69025252 Eh           -1025.60391 eV
            One Electron Energy:          -50.44138410 Eh           -1372.57984 eV
            Two Electron Energy:           12.75113157 Eh             346.97593 eV
            
            Virial components:
            Potential Energy   :          -75.38601099 Eh           -2051.35765 eV
            Kinetic Energy     :           37.69575847 Eh            1025.75374 eV
            Virial Ratio       :            1.99985394
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -1.5158e-08  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    1.1268e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    3.3734e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.6300e-08  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     2.010207
            Ideal value S*(S+1) for S=1.0   :     2.000000
            Deviation                       :     0.010207
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.346345      -308.7497 
               1   1.0000      -0.829818       -22.5805 
               2   1.0000      -0.439312       -11.9543 
               3   1.0000      -0.439312       -11.9543 
               4   0.0000       0.018519         0.5039 
               5   0.0000       0.098775         2.6878 
               6   0.0000       0.121690         3.3113 
               7   0.0000       0.121690         3.3113 
               8   0.0000       0.154181         4.1955 
               9   0.0000       0.449984        12.2447 
              10   0.0000       0.449984        12.2447 
              11   0.0000       0.455672        12.3995 
              12   0.0000       0.455672        12.3995 
              13   0.0000       0.458353        12.4724 
              14   0.0000       0.675468        18.3804 
              15   0.0000       0.675468        18.3804 
              16   0.0000       0.731695        19.9104 
              17   0.0000       0.801897        21.8207 
              18   0.0000       1.781170        48.4681 
              19   0.0000       1.781170        48.4681 
              20   0.0000       1.800253        48.9874 
              21   0.0000       1.800253        48.9874 
              22   0.0000       1.807612        49.1876 
              23   0.0000       3.008255        81.8588 
              24   0.0000       3.008255        81.8588 
              25   0.0000       3.034559        82.5745 
              26   0.0000       3.074184        83.6528 
              27   0.0000       3.075280        83.6826 
              28   0.0000       3.075280        83.6826 
              29   0.0000       3.080544        83.8259 
              30   0.0000       3.080544        83.8259 
              31   0.0000       3.089940        84.0815 
              32   0.0000       3.089940        84.0815 
              33   0.0000       7.323979       199.2956 
              34   0.0000       7.325864       199.3469 
              35   0.0000       7.325864       199.3469 
              36   0.0000       7.331704       199.5058 
              37   0.0000       7.331704       199.5058 
              38   0.0000      24.315132       661.6484 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.300030      -307.4894 
               1   1.0000      -0.584305       -15.8997 
               2   0.0000       0.040970         1.1148 
               3   0.0000       0.071296         1.9401 
               4   0.0000       0.071296         1.9401 
               5   0.0000       0.111839         3.0433 
               6   0.0000       0.172547         4.6952 
               7   0.0000       0.211251         5.7484 
               8   0.0000       0.211251         5.7484 
               9   0.0000       0.476540        12.9673 
              10   0.0000       0.482712        13.1353 
              11   0.0000       0.482712        13.1353 
              12   0.0000       0.502207        13.6657 
              13   0.0000       0.502207        13.6657 
              14   0.0000       0.757200        20.6045 
              15   0.0000       0.804426        21.8895 
              16   0.0000       0.804426        21.8895 
              17   0.0000       0.868333        23.6285 
              18   0.0000       1.868034        50.8318 
              19   0.0000       1.882531        51.2263 
              20   0.0000       1.882531        51.2263 
              21   0.0000       1.930687        52.5367 
              22   0.0000       1.930687        52.5367 
              23   0.0000       3.054488        83.1168 
              24   0.0000       3.103447        84.4491 
              25   0.0000       3.103447        84.4491 
              26   0.0000       3.119649        84.8900 
              27   0.0000       3.134010        85.2807 
              28   0.0000       3.134010        85.2807 
              29   0.0000       3.143883        85.5494 
              30   0.0000       3.143883        85.5494 
              31   0.0000       3.182191        86.5918 
              32   0.0000       3.182191        86.5918 
              33   0.0000       7.368990       200.5204 
              34   0.0000       7.385116       200.9592 
              35   0.0000       7.385116       200.9592 
              36   0.0000       7.434117       202.2926 
              37   0.0000       7.434117       202.2926 
              38   0.0000      24.347101       662.5183 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 C :   -0.000000    2.000000
            Sum of atomic charges         :   -0.0000000
            Sum of atomic spin populations:    2.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 C s       :     3.997017  s :     3.997017
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000746  d :     0.002983
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.002238
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000001
                  f-3     :     0.000000
            
            SPIN
              0 C s       :    -0.000258  s :    -0.000258
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000065  d :     0.000258
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000194
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000001
                  f-3     :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 C :   -0.000000    2.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 C s       :     3.997017  s :     3.997017
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000746  d :     0.002983
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.002238
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000001
                  f-3     :     0.000000
            
            SPIN
              0 C s       :    -0.000258  s :    -0.000258
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000065  d :     0.000258
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000194
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000001
                  f-3     :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.0000     6.0000    -0.0000     2.0204     0.0000     2.0204
            
              Mayer bond orders larger than 0.100000
            
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.610 sec
            Sum of individual times     ....       1.451 sec  ( 90.1%)
            
            Fock matrix formation       ....       1.334 sec  ( 82.9%)
            Diagonalization             ....       0.006 sec  (  0.4%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.0%)
            Initial guess               ....       0.090 sec  (  5.6%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.003 sec  (  0.2%)
            
            ------------------------------------------------------------------------------
                                            ORCA  MP2 
            ------------------------------------------------------------------------------
            
            Freezing NCore=2 chemical core electrons
            
            ----------
            MP2 ENERGY (disk based algorithm)
            ----------
            
            Dimension of the basis                    ...   39
            Memory devoted to MP2                     ... 64000 MB   
            Data format for buffers                   ... DOUBLE
            Compression type for matrix containers    ... UNCOMPRESSED
            
            -------------------------------
            PARTIAL EXCHANGE TRANSFORMATION
            -------------------------------
            
            Transformation type                        ... two-operators
            Generation of integrals (i,mue|j,nue)      ... ON
            Generation of integrals (mue,kappa|nue,tau)... OFF
            Generation of integrals (i,mue|a,nue)      ... OFF
            Dimension of the basis                     ...   39
            Number of internal alpha-MOs               ...    3 (   1-   3)
            Number of internal beta-MOs                ...    1 (   1-   1)
            Pair cutoff                                ... 1.000e-14 Eh
            Number of AO pairs in the trafo            ...  780
            Total Number of distinct AO pairs          ...  780
            Memory devoted for trafo                   ... 64000.0 MB 
            Max. Number of MO pairs treated together   ... 5515192      
            Number Format for Storage                  ... Double (8 Byte)
            Integral package used                      ... LIBINT
            
            Starting integral evaluation:
                ... done with AO integral generation
            Closing buffer AOK[aa] ( 0.00 GB; CompressionRatio= 0.99)
            Closing buffer AOK[bb] ( 0.00 GB; CompressionRatio= 0.28)
            Closing buffer AOK[ab] ( 0.00 GB; CompressionRatio= 0.47)
            Closing buffer AOK[ba] ( 0.00 GB; CompressionRatio= 0.68)
            Collecting buffer AOK 
            Number of alpha/alpha MO pairs in trafo    ...    6
            Number of beta /beta  MO pairs in trafo    ...    1
            Number of alpha/ beta MO pairs in trafo    ...    3
            ------------------------
            SORTING OF (i,mue|j,nue)
            ------------------------
            
            SORTING OF ALPHA/ALPHA PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[aa] ( 0.00 GB; CompressionRatio= 1.00)
            Collecting buffer KAO 
            SORTING OF BETA /BETA  PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[bb] ( 0.00 GB; CompressionRatio= 1.00)
            Collecting buffer KAO 
            SORTING OF ALPHA/BETA  PAIRS
            IBATCH = 1 of  1
            Closing buffer KAO[ab] ( 0.00 GB; CompressionRatio= 0.999014778325)
            Collecting buffer KAO[ab] 
            N(AO-Batches) Done                         ...     15379 
            N(AO-Batches) Skipped                      ...         0 
            N(IJ)-pairs Skipped                        ...         0 
            TOTAL TIME for half transformation         ...     0.074 sec
            AO-integral generation                     ...     0.055 sec
            Half transformation                        ...     0.014 sec
            K-integral sorting                         ...     0.003 sec
            
            Finished integral transformation - now doing MP2 part
            
            OPERATOR COMBINATION   0   0: ij=(  1..  3,  1..  3)
              Internal MO   3
            OPERATOR COMBINATION   0   1: ij=(  1..  3,  1..  1)
              Internal MO   3
            OPERATOR COMBINATION   1   1: ij=(  1..  1,  1..  1)
            
            Correlation energy components
             E2 and T2 for alpha/alpha pairs :     -0.012666454 Eh 
             E2 and T2 for beta/beta   pairs :      0.000000000 Eh 
             E2 and T2 for alpha/beta  pairs :     -0.053931829 Eh 
            
            -----------------------------------------------
             MP2 CORRELATION ENERGY   :     -0.066598283 Eh
            -----------------------------------------------
            
            
            -------
            TIMINGS
            -------
            Total time                :    0.151 sec
            Integral trafo            :    0.074 sec ( 49.2%)
            K(i,j)                    :    0.000 sec (  0.1%)
            T(i,j)                    :    0.000 sec (  0.0%)
            
            ---------------------------------------
            MP2 TOTAL ENERGY:      -37.756850807 Eh
            ---------------------------------------
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -37.756850806708
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
            
              WARNING: The energy has been calculated at the MP2 level but the densities
                       used in the property calculations are still SCF densities
                       MP2 response densities have not been calculated 
                       use %mp2 Density relaxed end
                       or  %mp2 Density unrelaxed end
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:     -0.00000      -0.00000      -0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000      -0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :    -0.000000    -0.000000    -0.000000 
            x,y,z [Debye]:    -0.000000    -0.000000    -0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        2.055 sec (=   0.034 min)
            GTO integral calculation        ...        0.239 sec (=   0.004 min)  11.6 %
            SCF iterations                  ...        1.635 sec (=   0.027 min)  79.6 %
            MP2 module                      ...        0.181 sec (=   0.003 min)   8.8 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 2 seconds 223 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  3
            |  3> C     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14> end
            | 15> %basis
            | 16>      NewGTO   C
            | 17>      S  7
            | 18>      1            8236.00000000               0.00054198
            | 19>      2            1235.00000000               0.00419287
            | 20>      3             280.80000000               0.02152216
            | 21>      4              79.27000000               0.08353432
            | 22>      5              25.59000000               0.23958285
            | 23>      6               8.99700000               0.44285284
            | 24>      7               3.31900000               0.35179956
            | 25>      S  6
            | 26>      1             280.80000000              -0.00005949
            | 27>      2              79.27000000              -0.00114816
            | 28>      3              25.59000000              -0.01001914
            | 29>      4               8.99700000              -0.06121949
            | 30>      5               3.31900000              -0.17326985
            | 31>      6               0.36430000               1.07291519
            | 32>      S  1
            | 33>      1               0.90590000               1.00000000
            | 34>      S  1
            | 35>      1               0.12850000               1.00000000
            | 36>      S  1
            | 37>      1               0.04402000               1.00000000
            | 38>      P  3
            | 39>      1              18.71000000               0.03942639
            | 40>      2               4.13300000               0.24408898
            | 41>      3               1.20000000               0.81549201
            | 42>      P  1
            | 43>      1               0.38270000               1.00000000
            | 44>      P  1
            | 45>      1               0.12090000               1.00000000
            | 46>      P  1
            | 47>      1               0.03569000               1.00000000
            | 48>      D  1
            | 49>      1               1.09700000               1.00000000
            | 50>      D  1
            | 51>      1               0.31800000               1.00000000
            | 52>      F  1
            | 53>      1               0.76100000               1.00000000
            | 54>      end
            | 55> end
            | 56> 
            | 57>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type C   : 16s6p2d1f contracted to 5s4p2d1f pattern {76111/3111/11/1}
            
            Atom   0C    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : C 
             NewGTO C 
             S 7 
               1    8236.0000000000      0.0005419800
               2    1235.0000000000      0.0041928700
               3     280.8000000000      0.0215221600
               4      79.2700000000      0.0835343202
               5      25.5900000000      0.2395828505
               6       8.9970000000      0.4428528409
               7       3.3190000000      0.3517995607
             S 6 
               1     280.8000000000     -0.0000594900
               2      79.2700000000     -0.0011481600
               3      25.5900000000     -0.0100191400
               4       8.9970000000     -0.0612194901
               5       3.3190000000     -0.1732698502
               6       0.3643000000      1.0729151911
             S 1 
               1       0.9059000000      1.0000000000
             S 1 
               1       0.1285000000      1.0000000000
             S 1 
               1       0.0440200000      1.0000000000
             P 3 
               1      18.7100000000      0.0394263901
               2       4.1330000000      0.2440889805
               3       1.2000000000      0.8154920116
             P 1 
               1       0.3827000000      1.0000000000
             P 1 
               1       0.1209000000      1.0000000000
             P 1 
               1       0.0356900000      1.0000000000
             D 1 
               1       1.0970000000      1.0000000000
             D 1 
               1       0.3180000000      1.0000000000
             F 1 
               1       0.7610000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   25
             # of primitive gaussian functions       ...   51
             # of contracted shells                  ...   12
             # of contracted basis functions         ...   34
             Highest angular momentum                ...    3
             Maximum contraction depth               ...    7
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    3
             Number of Electrons    NEL             ....    6
             Basis Dimension        Dim             ....   34
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 2.982e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   3592 (   0.0 sec)
            # of grid points (after weights+screening)   ...   3592 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     3592
            Total number of batches                      ...       57
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     3592
            Average number of shells per batch           ...    10.83 (90.23%)
            Average number of basis functions per batch  ...    30.79 (90.57%)
            Average number of large shells per batch     ...    10.26 (94.75%)
            Average number of large basis fcns per batch ...    29.05 (94.34%)
            Maximum spatial batch extension              ...  32.44, 31.96, 31.96 au
            Average spatial batch extension              ...   8.49,  7.32,  7.29 au
            
            Time for grid setup =    0.030 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -37.6745379218   0.000000000000 0.01133670  0.00065217  0.1634017 0.7000
              1    -37.6785740817  -0.004036159840 0.01014066  0.00056770  0.1167852 0.7000
                                           ***Turning on DIIS***
              2    -37.6818138241  -0.003239742447 0.02740787  0.00148178  0.0827826 0.0000
              3    -37.6842382438  -0.002424419711 0.00875820  0.00045053  0.0088751 0.0000
              4    -37.6889536630  -0.004715419181 0.00759405  0.00030428  0.0040865 0.0000
              5    -37.6886356471   0.000318015946 0.00435910  0.00016028  0.0018045 0.0000
              6    -37.6904711169  -0.001835469776 0.00143636  0.00006455  0.0006379 0.0000
              7    -37.6917604947  -0.001289377858 0.00033319  0.00001187  0.0000903 0.0000
              8    -37.6917841307  -0.000023636008 0.00007650  0.00000290  0.0000193 0.0000
              9    -37.6917626237   0.000021507026 0.00000370  0.00000017  0.0000018 0.0000
             10    -37.6917619146   0.000000709096 0.00000066  0.00000003  0.0000003 0.0000
             11    -37.6917620575  -0.000000142892 0.00000016  0.00000001  0.0000000 0.0000
             12    -37.6917620835  -0.000000026002 0.00000010  0.00000000  0.0000000 0.0000
                                        ***DIIS convergence achieved***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  13 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -37.69176206 Eh           -1025.64499 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :          -37.69176206 Eh           -1025.64499 eV
            One Electron Energy:          -50.44486003 Eh           -1372.67443 eV
            Two Electron Energy:           12.75309797 Eh             347.02944 eV
            
            Virial components:
            Potential Energy   :          -75.37574593 Eh           -2051.07832 eV
            Kinetic Energy     :           37.68398386 Eh            1025.43333 eV
            Virial Ratio       :            2.00020641
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...    2.0516e-08  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    1.0098e-08  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    3.6409e-10  Tolerance :   1.0000e-09
              Last DIIS Error            ...    4.1693e-09  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     2.009852
            Ideal value S*(S+1) for S=1.0   :     2.000000
            Deviation                       :     0.009852
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.346369      -308.7504 
               1   1.0000      -0.829485       -22.5714 
               2   1.0000      -0.438705       -11.9378 
               3   1.0000      -0.438705       -11.9378 
               4   0.0000       0.017377         0.4728 
               5   0.0000       0.094556         2.5730 
               6   0.0000       0.096380         2.6226 
               7   0.0000       0.096380         2.6226 
               8   0.0000       0.124043         3.3754 
               9   0.0000       0.529782        14.4161 
              10   0.0000       0.529782        14.4161 
              11   0.0000       0.583066        15.8660 
              12   0.0000       0.724991        19.7280 
              13   0.0000       0.819324        22.2949 
              14   0.0000       0.819324        22.2949 
              15   0.0000       0.837976        22.8025 
              16   0.0000       0.837976        22.8025 
              17   0.0000       0.846195        23.0261 
              18   0.0000       2.336562        63.5811 
              19   0.0000       2.336562        63.5811 
              20   0.0000       2.372319        64.5541 
              21   0.0000       2.932621        79.8007 
              22   0.0000       2.934507        79.8520 
              23   0.0000       2.934507        79.8520 
              24   0.0000       2.940139        80.0052 
              25   0.0000       2.940139        80.0052 
              26   0.0000       2.949373        80.2565 
              27   0.0000       2.949373        80.2565 
              28   0.0000       3.228701        87.8574 
              29   0.0000       3.228701        87.8574 
              30   0.0000       3.237695        88.1022 
              31   0.0000       3.237695        88.1022 
              32   0.0000       3.241025        88.1928 
              33   0.0000       4.626670       125.8981 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.301362      -307.5257 
               1   1.0000      -0.584039       -15.8925 
               2   0.0000       0.038019         1.0346 
               3   0.0000       0.062972         1.7135 
               4   0.0000       0.062972         1.7135 
               5   0.0000       0.106533         2.8989 
               6   0.0000       0.141548         3.8517 
               7   0.0000       0.180278         4.9056 
               8   0.0000       0.180278         4.9056 
               9   0.0000       0.606817        16.5123 
              10   0.0000       0.650728        17.7072 
              11   0.0000       0.650728        17.7072 
              12   0.0000       0.783398        21.3173 
              13   0.0000       0.888862        24.1872 
              14   0.0000       0.898870        24.4595 
              15   0.0000       0.898870        24.4595 
              16   0.0000       0.934440        25.4274 
              17   0.0000       0.934440        25.4274 
              18   0.0000       2.397486        65.2389 
              19   0.0000       2.452687        66.7410 
              20   0.0000       2.452687        66.7410 
              21   0.0000       2.973204        80.9050 
              22   0.0000       2.980394        81.1007 
              23   0.0000       2.980394        81.1007 
              24   0.0000       3.002210        81.6943 
              25   0.0000       3.002210        81.6943 
              26   0.0000       3.039898        82.7198 
              27   0.0000       3.039898        82.7198 
              28   0.0000       3.301115        89.8279 
              29   0.0000       3.317506        90.2739 
              30   0.0000       3.317506        90.2739 
              31   0.0000       3.369768        91.6960 
              32   0.0000       3.369768        91.6960 
              33   0.0000       4.683420       127.4423 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 C :   -0.000000    2.000000
            Sum of atomic charges         :   -0.0000000
            Sum of atomic spin populations:    2.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 C s       :     3.997172  s :     3.997172
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000707  d :     0.002828
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.002121
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000002
                  f-3     :     0.000000
            
            SPIN
              0 C s       :    -0.000211  s :    -0.000211
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000053  d :     0.000211
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000158
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000002
                  f-3     :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 C :   -0.000000    2.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 C s       :     3.997172  s :     3.997172
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000707  d :     0.002828
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.002121
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000002
                  f-3     :     0.000000
            
            SPIN
              0 C s       :    -0.000211  s :    -0.000211
                  pz      :     0.999998  p :     1.999997
                  px      :     0.999998
                  py      :     0.000000
                  dz2     :     0.000053  d :     0.000211
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000158
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000003
                  f+1     :     0.000000
                  f-1     :     0.000000
                  f+2     :     0.000001
                  f-2     :     0.000000
                  f+3     :     0.000002
                  f-3     :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.0000     6.0000    -0.0000     2.0197     0.0000     2.0197
            
              Mayer bond orders larger than 0.100000
            
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 2 sec 
            
            Total time                  ....       2.130 sec
            Sum of individual times     ....       1.903 sec  ( 89.3%)
            
            Fock matrix formation       ....       1.756 sec  ( 82.4%)
            Diagonalization             ....       0.006 sec  (  0.3%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.002 sec  (  0.1%)
            Initial guess               ....       0.107 sec  (  5.0%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.003 sec  (  0.1%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -37.691762062972
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:     -0.00000       0.00000       0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :    -0.000000     0.000000     0.000000 
            x,y,z [Debye]:    -0.000000     0.000000     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        2.400 sec (=   0.040 min)
            GTO integral calculation        ...        0.229 sec (=   0.004 min)   9.5 %
            SCF iterations                  ...        2.171 sec (=   0.036 min)  90.5 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 2 seconds 586 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  3
            |  3> C     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14> end
            | 15> %basis
            | 16>      NewGTO   C
            | 17>      S  8
            | 18>      1           33980.00000000               0.00014681
            | 19>      2            5089.00000000               0.00111646
            | 20>      3            1157.00000000               0.00589089
            | 21>      4             326.60000000               0.02421726
            | 22>      5             106.10000000               0.08317164
            | 23>      6              38.11000000               0.22056848
            | 24>      7              14.75000000               0.42873150
            | 25>      8               6.03500000               0.36436142
            | 26>      S  7
            | 27>      1            5089.00000000              -0.00001002
            | 28>      2             326.60000000              -0.00043659
            | 29>      3             106.10000000              -0.00193231
            | 30>      4              38.11000000              -0.02148395
            | 31>      5              14.75000000              -0.09030917
            | 32>      6               6.03500000              -0.41879151
            | 33>      7               2.53000000              -0.53180191
            | 34>      S  1
            | 35>      1               0.73550000               1.00000000
            | 36>      S  1
            | 37>      1               0.29050000               1.00000000
            | 38>      S  1
            | 39>      1               0.11110000               1.00000000
            | 40>      S  1
            | 41>      1               0.04145000               1.00000000
            | 42>      P  3
            | 43>      1              34.51000000               0.03168786
            | 44>      2               7.91500000               0.21289431
            | 45>      3               2.36800000               0.83958675
            | 46>      P  1
            | 47>      1               0.81320000               1.00000000
            | 48>      P  1
            | 49>      1               0.28900000               1.00000000
            | 50>      P  1
            | 51>      1               0.10070000               1.00000000
            | 52>      P  1
            | 53>      1               0.03218000               1.00000000
            | 54>      D  1
            | 55>      1               1.84800000               1.00000000
            | 56>      D  1
            | 57>      1               0.64900000               1.00000000
            | 58>      D  1
            | 59>      1               0.22800000               1.00000000
            | 60>      F  1
            | 61>      1               1.41900000               1.00000000
            | 62>      F  1
            | 63>      1               0.48500000               1.00000000
            | 64>      G  1
            | 65>      1               1.01100000               1.00000000
            | 66>      end
            | 67> end
            | 68> 
            | 69>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              C      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 C     6.0000    0    12.011    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             C      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type C   : 19s7p3d2f1g contracted to 6s5p3d2f1g pattern {871111/31111/111/11/1}
            
            Atom   0C    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : C 
             NewGTO C 
             S 8 
               1   33980.0000000000      0.0001468100
               2    5089.0000000000      0.0011164600
               3    1157.0000000000      0.0058908900
               4     326.6000000000      0.0242172599
               5     106.1000000000      0.0831716395
               6      38.1100000000      0.2205684788
               7      14.7500000000      0.4287314976
               8       6.0350000000      0.3643614179
             S 7 
               1    5089.0000000000     -0.0000100200
               2     326.6000000000     -0.0004365900
               3     106.1000000000     -0.0019323100
               4      38.1100000000     -0.0214839499
               5      14.7500000000     -0.0903091694
               6       6.0350000000     -0.4187915074
               7       2.5300000000     -0.5318019067
             S 1 
               1       0.7355000000      1.0000000000
             S 1 
               1       0.2905000000      1.0000000000
             S 1 
               1       0.1111000000      1.0000000000
             S 1 
               1       0.0414500000      1.0000000000
             P 3 
               1      34.5100000000      0.0316878600
               2       7.9150000000      0.2128943097
               3       2.3680000000      0.8395867487
             P 1 
               1       0.8132000000      1.0000000000
             P 1 
               1       0.2890000000      1.0000000000
             P 1 
               1       0.1007000000      1.0000000000
             P 1 
               1       0.0321800000      1.0000000000
             D 1 
               1       1.8480000000      1.0000000000
             D 1 
               1       0.6490000000      1.0000000000
             D 1 
               1       0.2280000000      1.0000000000
             F 1 
               1       1.4190000000      1.0000000000
             F 1 
               1       0.4850000000      1.0000000000
             G 1 
               1       1.0110000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...   32
             # of primitive gaussian functions       ...   78
             # of contracted shells                  ...   17
             # of contracted basis functions         ...   59
             Highest angular momentum                ...    4
             Maximum contraction depth               ...    8
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    3
             Number of Electrons    NEL             ....    6
             Basis Dimension        Dim             ....   59
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.442e-02
            Time for diagonalization                   ...    0.001 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.002 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   3592 (   0.0 sec)
            # of grid points (after weights+screening)   ...   3592 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     3592
            Total number of batches                      ...       57
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     3592
            Average number of shells per batch           ...    14.79 (87.02%)
            Average number of basis functions per batch  ...    51.52 (87.32%)
            Average number of large shells per batch     ...    14.07 (95.10%)
            Average number of large basis fcns per batch ...    48.86 (94.85%)
            Maximum spatial batch extension              ...  32.44, 31.96, 31.96 au
            Average spatial batch extension              ...   8.49,  7.32,  7.29 au
            
            Time for grid setup =    0.036 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0    -37.6760934857   0.000000000000 0.00672366  0.00028551  0.1837575 0.7000
              1    -37.6801244565  -0.004030970796 0.00751016  0.00026404  0.1306023 0.7000
                                           ***Turning on DIIS***
              2    -37.6833625032  -0.003238046649 0.02203995  0.00071756  0.0922336 0.0000
              3    -37.6867119882  -0.003349485024 0.00943636  0.00027184  0.0080057 0.0000
              4    -37.6912084744  -0.004496486150 0.00746665  0.00018170  0.0043147 0.0000
              5    -37.6898688797   0.001339594676 0.00551686  0.00011685  0.0020875 0.0000
              6    -37.6919143806  -0.002045500886 0.00253443  0.00004796  0.0007155 0.0000
              7    -37.6933253010  -0.001410920384 0.00020276  0.00000581  0.0000814 0.0000
              8    -37.6933586420  -0.000033341014 0.00005234  0.00000144  0.0000196 0.0000
              9    -37.6933435086   0.000015133356 0.00000295  0.00000009  0.0000025 0.0000
             10    -37.6933431060   0.000000402622 0.00000077  0.00000002  0.0000003 0.0000
                                        ***DIIS convergence achieved***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  11 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :          -37.69334345 Eh           -1025.68802 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :          -37.69334345 Eh           -1025.68802 eV
            One Electron Energy:          -50.44931156 Eh           -1372.79556 eV
            Two Electron Energy:           12.75596811 Eh             347.10754 eV
            
            Virial components:
            Potential Energy   :          -75.38585691 Eh           -2051.35346 eV
            Kinetic Energy     :           37.69251346 Eh            1025.66544 eV
            Virial Ratio       :            2.00002202
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -3.3956e-07  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    4.0322e-08  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    1.3403e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.1620e-08  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     2.010349
            Ideal value S*(S+1) for S=1.0   :     2.000000
            Deviation                       :     0.010349
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.345926      -308.7383 
               1   1.0000      -0.829316       -22.5668 
               2   1.0000      -0.439001       -11.9458 
               3   1.0000      -0.439001       -11.9458 
               4   0.0000       0.017056         0.4641 
               5   0.0000       0.081584         2.2200 
               6   0.0000       0.083422         2.2700 
               7   0.0000       0.083422         2.2700 
               8   0.0000       0.107197         2.9170 
               9   0.0000       0.418921        11.3994 
              10   0.0000       0.418921        11.3994 
              11   0.0000       0.464826        12.6485 
              12   0.0000       0.492798        13.4097 
              13   0.0000       0.606201        16.4956 
              14   0.0000       0.606201        16.4956 
              15   0.0000       0.616849        16.7853 
              16   0.0000       0.616849        16.7853 
              17   0.0000       0.621793        16.9198 
              18   0.0000       1.563588        42.5474 
              19   0.0000       1.563588        42.5474 
              20   0.0000       1.598220        43.4898 
              21   0.0000       1.885006        51.2936 
              22   0.0000       1.886700        51.3397 
              23   0.0000       1.886700        51.3397 
              24   0.0000       1.891935        51.4822 
              25   0.0000       1.891935        51.4822 
              26   0.0000       1.900732        51.7215 
              27   0.0000       1.900732        51.7215 
              28   0.0000       2.054680        55.9107 
              29   0.0000       2.054680        55.9107 
              30   0.0000       2.066571        56.2343 
              31   0.0000       2.066571        56.2343 
              32   0.0000       2.067179        56.2508 
              33   0.0000       2.100823        57.1663 
              34   0.0000       5.075407       138.1088 
              35   0.0000       5.077869       138.1758 
              36   0.0000       5.077869       138.1758 
              37   0.0000       5.085267       138.3771 
              38   0.0000       5.085267       138.3771 
              39   0.0000       5.097631       138.7136 
              40   0.0000       5.097631       138.7136 
              41   0.0000       5.115002       139.1863 
              42   0.0000       5.115002       139.1863 
              43   0.0000       5.784885       157.4147 
              44   0.0000       5.784885       157.4147 
              45   0.0000       5.788064       157.5012 
              46   0.0000       6.208245       168.9349 
              47   0.0000       6.211507       169.0237 
              48   0.0000       6.211507       169.0237 
              49   0.0000       6.221366       169.2920 
              50   0.0000       6.221366       169.2920 
              51   0.0000       6.238042       169.7458 
              52   0.0000       6.238042       169.7458 
              53   0.0000       6.257109       170.2646 
              54   0.0000       6.259850       170.3392 
              55   0.0000       6.259850       170.3392 
              56   0.0000       6.268439       170.5729 
              57   0.0000       6.268439       170.5729 
              58   0.0000      20.444408       556.3206 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000     -11.300582      -307.5045 
               1   1.0000      -0.583549       -15.8792 
               2   0.0000       0.036156         0.9839 
               3   0.0000       0.058307         1.5866 
               4   0.0000       0.058307         1.5866 
               5   0.0000       0.090619         2.4659 
               6   0.0000       0.123592         3.3631 
               7   0.0000       0.161034         4.3820 
               8   0.0000       0.161034         4.3820 
               9   0.0000       0.484825        13.1928 
              10   0.0000       0.523068        14.2334 
              11   0.0000       0.523068        14.2334 
              12   0.0000       0.531375        14.4594 
              13   0.0000       0.649330        17.6692 
              14   0.0000       0.656548        17.8656 
              15   0.0000       0.656548        17.8656 
              16   0.0000       0.682595        18.5744 
              17   0.0000       0.682595        18.5744 
              18   0.0000       1.622045        44.1381 
              19   0.0000       1.675579        45.5948 
              20   0.0000       1.675579        45.5948 
              21   0.0000       1.912668        52.0463 
              22   0.0000       1.918056        52.1930 
              23   0.0000       1.918056        52.1930 
              24   0.0000       1.934248        52.6336 
              25   0.0000       1.934248        52.6336 
              26   0.0000       1.963157        53.4202 
              27   0.0000       1.963157        53.4202 
              28   0.0000       2.125589        57.8402 
              29   0.0000       2.140151        58.2365 
              30   0.0000       2.140151        58.2365 
              31   0.0000       2.162397        58.8418 
              32   0.0000       2.187708        59.5306 
              33   0.0000       2.187708        59.5306 
              34   0.0000       5.102380       138.8428 
              35   0.0000       5.106733       138.9613 
              36   0.0000       5.106733       138.9613 
              37   0.0000       5.119855       139.3183 
              38   0.0000       5.119855       139.3183 
              39   0.0000       5.141943       139.9194 
              40   0.0000       5.141943       139.9194 
              41   0.0000       5.173355       140.7741 
              42   0.0000       5.173355       140.7741 
              43   0.0000       5.807693       158.0353 
              44   0.0000       5.861559       159.5011 
              45   0.0000       5.861559       159.5011 
              46   0.0000       6.247861       170.0129 
              47   0.0000       6.255807       170.2292 
              48   0.0000       6.255807       170.2292 
              49   0.0000       6.279790       170.8818 
              50   0.0000       6.279790       170.8818 
              51   0.0000       6.300448       171.4439 
              52   0.0000       6.316396       171.8779 
              53   0.0000       6.316396       171.8779 
              54   0.0000       6.321514       172.0171 
              55   0.0000       6.321514       172.0171 
              56   0.0000       6.366042       173.2288 
              57   0.0000       6.366042       173.2288 
              58   0.0000      20.476206       557.1859 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 C :   -0.000000    2.000000
            Sum of atomic charges         :   -0.0000000
            Sum of atomic spin populations:    2.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 C s       :     3.997005  s :     3.997005
                  pz      :     0.042367  p :     1.999994
                  px      :     0.966550
                  py      :     0.991077
                  dz2     :     0.002626  d :     0.002995
                  dxz     :     0.000288
                  dyz     :     0.000077
                  dx2y2   :     0.000001
                  dxy     :     0.000003
                  f0      :     0.000001  f :     0.000006
                  f+1     :     0.000002
                  f-1     :     0.000002
                  f+2     :     0.000000
                  f-2     :     0.000000
                  f+3     :     0.000000
                  f-3     :     0.000000
                  g0      :     0.000000  g :     0.000000
                  g+1     :     0.000000
                  g-1     :     0.000000
                  g+2     :     0.000000
                  g-2     :     0.000000
                  g+3     :     0.000000
                  g-3     :     0.000000
                  g+4     :     0.000000
                  g-4     :     0.000000
            
            SPIN
              0 C s       :    -0.000252  s :    -0.000252
                  pz      :     0.042367  p :     1.999994
                  px      :     0.966550
                  py      :     0.991077
                  dz2     :     0.000221  d :     0.000252
                  dxz     :     0.000024
                  dyz     :     0.000006
                  dx2y2   :     0.000000
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000006
                  f+1     :     0.000002
                  f-1     :     0.000002
                  f+2     :     0.000000
                  f-2     :     0.000000
                  f+3     :     0.000000
                  f-3     :     0.000000
                  g0      :    -0.000000  g :    -0.000000
                  g+1     :    -0.000000
                  g-1     :    -0.000000
                  g+2     :    -0.000000
                  g-2     :    -0.000000
                  g+3     :    -0.000000
                  g-3     :    -0.000000
                  g+4     :    -0.000000
                  g-4     :    -0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 C :   -0.000000    2.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 C s       :     3.997005  s :     3.997005
                  pz      :     0.042367  p :     1.999994
                  px      :     0.966550
                  py      :     0.991077
                  dz2     :     0.002626  d :     0.002995
                  dxz     :     0.000288
                  dyz     :     0.000077
                  dx2y2   :     0.000001
                  dxy     :     0.000003
                  f0      :     0.000001  f :     0.000006
                  f+1     :     0.000002
                  f-1     :     0.000002
                  f+2     :     0.000000
                  f-2     :     0.000000
                  f+3     :     0.000000
                  f-3     :     0.000000
                  g0      :     0.000000  g :     0.000000
                  g+1     :     0.000000
                  g-1     :     0.000000
                  g+2     :     0.000000
                  g-2     :     0.000000
                  g+3     :     0.000000
                  g-3     :     0.000000
                  g+4     :     0.000000
                  g-4     :     0.000000
            
            SPIN
              0 C s       :    -0.000252  s :    -0.000252
                  pz      :     0.042367  p :     1.999994
                  px      :     0.966550
                  py      :     0.991077
                  dz2     :     0.000221  d :     0.000252
                  dxz     :     0.000024
                  dyz     :     0.000006
                  dx2y2   :     0.000000
                  dxy     :     0.000000
                  f0      :     0.000001  f :     0.000006
                  f+1     :     0.000002
                  f-1     :     0.000002
                  f+2     :     0.000000
                  f-2     :     0.000000
                  f+3     :     0.000000
                  f-3     :     0.000000
                  g0      :    -0.000000  g :    -0.000000
                  g+1     :    -0.000000
                  g-1     :    -0.000000
                  g+2     :    -0.000000
                  g-2     :    -0.000000
                  g+3     :    -0.000000
                  g-3     :    -0.000000
                  g+4     :    -0.000000
                  g-4     :    -0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 C      6.0000     6.0000    -0.0000     2.0207     0.0000     2.0207
            
              Mayer bond orders larger than 0.100000
            
            
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 3 sec 
            
            Total time                  ....       3.409 sec
            Sum of individual times     ....       2.922 sec  ( 85.7%)
            
            Fock matrix formation       ....       2.758 sec  ( 80.9%)
            Diagonalization             ....       0.011 sec  (  0.3%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.003 sec  (  0.1%)
            Initial guess               ....       0.111 sec  (  3.2%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.004 sec  (  0.1%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY       -37.693343445558
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000      -0.00000       0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000      -0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000    -0.000000     0.000000 
            x,y,z [Debye]:     0.000000    -0.000000     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        3.712 sec (=   0.062 min)
            GTO integral calculation        ...        0.253 sec (=   0.004 min)   6.8 %
            SCF iterations                  ...        3.459 sec (=   0.058 min)  93.2 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 3 seconds 882 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            WARNING: MDCI localization with Augmented Hessian Foster-Boys
              ===> : Switching off randomization!
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! CCSD(T) Printbasis
            |  2> * xyz   0  2
            |  3> H     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14>   NewNCore C     2 end
            | 15>   NewNCore H     0 end
            | 16> end
            | 17> %basis
            | 18>      NewGTO   H
            | 19>      S  3
            | 20>      1              18.73113696               0.03349460
            | 21>      2               2.82539437               0.23472695
            | 22>      3               0.64012169               0.81375733
            | 23>      S  1
            | 24>      1               0.16127776               1.00000000
            | 25>      P  1
            | 26>      1          100000.00000000               1.00000000
            | 27>      end
            | 28> end
            | 29> 
            | 30>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              H      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 H     1.0000    0     1.008    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type H   : 4s1p contracted to 2s1p pattern {31/1}
            
            Atom   0H    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      18.7311369600      0.0334946000
               2       2.8253943700      0.2347269502
               3       0.6401216900      0.8137573307
             S 1 
               1       0.1612777600      1.0000000000
             P 1 
               1  100000.0000000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...    5
             # of primitive gaussian functions       ...    7
             # of contracted shells                  ...    3
             # of contracted basis functions         ...    5
             Highest angular momentum                ...    1
             Maximum contraction depth               ...    3
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    2
             Number of Electrons    NEL             ....    1
             Basis Dimension        Dim             ....    5
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 3.417e-01
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   1840 (   0.0 sec)
            # of grid points (after weights+screening)   ...   1840 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     1840
            Total number of batches                      ...       29
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     1840
            Average number of shells per batch           ...     2.10 (70.00%)
            Average number of basis functions per batch  ...     2.43 (48.67%)
            Average number of large shells per batch     ...     2.10 (100.00%)
            Average number of large basis fcns per batch ...     2.43 (100.00%)
            Maximum spatial batch extension              ...  18.53, 28.34, 28.34 au
            Average spatial batch extension              ...   7.21,  8.13,  8.85 au
            
            Time for grid setup =    0.008 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0     -0.4959921993   0.000000000000 0.01326611  0.00207219  0.0348570 0.7000
              1     -0.4964694539  -0.000477254558 0.01231518  0.00192920  0.0288359 0.7000
                                           ***Turning on DIIS***
              2     -0.4968774982  -0.000408044356 0.03355218  0.00526548  0.0232197 0.0000
              3     -0.4981931045  -0.001315606248 0.01381509  0.00220417  0.0078746 0.0000
              4     -0.4982403607  -0.000047256224 0.00250610  0.00040171  0.0014038 0.0000
              5     -0.4982341359   0.000006224798 0.00046939  0.00007531  0.0002228 0.0000
              6     -0.4982329150   0.000001220888 0.00000282  0.00000045  0.0000013 0.0000
                                        ***DIIS convergence achieved***
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   7 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :           -0.49823291 Eh             -13.55761 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :           -0.49823291 Eh             -13.55761 eV
            One Electron Energy:           -0.49823291 Eh             -13.55761 eV
            Two Electron Energy:           -0.00000000 Eh              -0.00000 eV
            
            Virial components:
            Potential Energy   :           -1.00809958 Eh             -27.43178 eV
            Kinetic Energy     :            0.50986667 Eh              13.87418 eV
            Virial Ratio       :            1.97718274
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...    5.5558e-09  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    1.1259e-08  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    1.8066e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    5.3427e-09  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     0.750000
            Ideal value S*(S+1) for S=0.5   :     0.750000
            Deviation                       :     0.000000
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000      -0.498233       -13.5576 
               1   0.0000       0.916193        24.9309 
               2   0.0000   249664.590410   6793718.8910 
               3   0.0000   249664.590410   6793718.8910 
               4   0.0000   249664.590410   6793718.8910 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   0.0000       0.095023         2.5857 
               1   0.0000       1.108073        30.1522 
               2   0.0000   249664.590422   6793718.8914 
               3   0.0000   249664.590422   6793718.8914 
               4   0.0000   249664.590422   6793718.8914 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 H :   -0.000000    1.000000
            Sum of atomic charges         :   -0.0000000
            Sum of atomic spin populations:    1.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 H :   -0.000000    1.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 H      1.0000     1.0000    -0.0000     1.0000     0.0000     1.0000
            
              Mayer bond orders larger than 0.100000
            
            
            Local spin analysis not attempted because no beta electrons available
            --------------------------
            ATOM BASIS FOR ELEMENT H 
            --------------------------
             NewGTO H 
             S 4
                1         18.731136960000         0.014316609278
                2          2.825394370000         0.100329427140
                3          0.640121690000         0.347824596834
                4          0.161277760000         0.665449442047
             S 4
                1         18.731136960000         0.042129441428
                2          2.825394370000         0.295239092021
                3          0.640121690000         1.023542355212
                4          0.161277760000        -1.149751976566
             P 1
                1     100000.000000000000         1.000000000000
             end
              // -----------------------------------------------
              // The basis set
              // -----------------------------------------------
              BAS[ATNO] = new BFNGauss[NSH];
              // Basis function   1 L = s
              InitBFNGauss(BAS[ATNO][  0]);
              BAS[ATNO][  0].l  = 0;
              BAS[ATNO][  0].ng = 4;
              BAS[ATNO][  0].a[  0] =        18.731136960000;     BAS[ATNO][  0].d[  0] =         0.014316609278;
              BAS[ATNO][  0].a[  1] =         2.825394370000;     BAS[ATNO][  0].d[  1] =         0.100329427140;
              BAS[ATNO][  0].a[  2] =         0.640121690000;     BAS[ATNO][  0].d[  2] =         0.347824596834;
              BAS[ATNO][  0].a[  3] =         0.161277760000;     BAS[ATNO][  0].d[  3] =         0.665449442047;
            
              // Basis function   2 L = s
              InitBFNGauss(BAS[ATNO][  1]);
              BAS[ATNO][  1].l  = 0;
              BAS[ATNO][  1].ng = 4;
              BAS[ATNO][  1].a[  0] =        18.731136960000;     BAS[ATNO][  1].d[  0] =        -0.042129441428;
              BAS[ATNO][  1].a[  1] =         2.825394370000;     BAS[ATNO][  1].d[  1] =        -0.295239092021;
              BAS[ATNO][  1].a[  2] =         0.640121690000;     BAS[ATNO][  1].d[  2] =        -1.023542355212;
              BAS[ATNO][  1].a[  3] =         0.161277760000;     BAS[ATNO][  1].d[  3] =         1.149751976566;
            
              // Basis function   3 L = p
              InitBFNGauss(BAS[ATNO][  2]);
              BAS[ATNO][  2].l  = 1;
              BAS[ATNO][  2].ng = 1;
              BAS[ATNO][  2].a[  0] =    100000.000000000000;     BAS[ATNO][  2].d[  0] =         1.000000000000;
            
            -------------------------------------------
            RADIAL EXPECTATION VALUES <R**-3> TO <R**3>
            -------------------------------------------
               0 :     0.000000     2.038473     1.008100     1.480982     2.867301     6.725518
               1 :     0.000000     4.596391     1.315669     1.704538     4.311918    12.670505
               2 : 67283533.920538 133333.333333   336.417670     0.003364     0.000012     0.000000
               3 : 67283533.920538 133333.333333   336.417670     0.003364     0.000013     0.000000
               4 : 67283533.920537 133333.333333   336.417670     0.003364     0.000012     0.000000
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.666 sec
            Sum of individual times     ....       1.458 sec  ( 87.5%)
            
            Fock matrix formation       ....       1.339 sec  ( 80.3%)
            Diagonalization             ....       0.001 sec  (  0.0%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.000 sec  (  0.0%)
            Initial guess               ....       0.110 sec  (  6.6%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.0%)
            
            
            ------------------------------------------------------------------------------- 
                                          ORCA-MATRIX DRIVEN CI                            
            ------------------------------------------------------------------------------- 
            
            --------------------------------
            AUTOMATIC CHOICE OF INCORE LEVEL
            --------------------------------
            
            Memory available                           ...  32000.00 MB
            Memory needed for S+T                      ...      0.00 MB
            Memory needed for J+K                      ...      0.00 MB
            Memory needed for DIIS                     ...      0.01 MB
            Memory needed for 3-ext                    ...      0.00 MB
            Memory needed for 4-ext                    ...      0.00 MB
            Memory needed for triples                  ...      0.00 MB
             -> Final InCoreLevel    ... 5
             -> check shows that triples correction can be computed
            
            
            Wavefunction type
            -----------------
            Correlation treatment                      ...      CCSD     
            Single excitations                         ... ON
            Orbital optimization                       ... OFF
            Calculation of Z vector                    ... OFF
            Calculation of Brueckner orbitals          ... OFF
            Perturbative triple excitations            ... ON
            Calculation of F12 correction              ... OFF
            Frozen core treatment                      ... chemical core (0 el)
            Reference Wavefunction                     ... UHF
              Alpha-MOs occ    :     0 ...    0 (  1 MO's/  1 electrons)
              Beta-MOs occ     :     0 ...   -1 (  0 MO's/  0 electrons)
              Alpha-MOs virt   :     1 ...    4 (  4 MO's              )
              Beta-MOs virt    :     0 ...    4 (  5 MO's              )
            Number of AO's                             ...      5
            Number of electrons                        ...      1
            Number of correlated electrons             ...      1
            
            Algorithmic settings
            --------------------
            Integral transformation                    ... AO direct full transformation
            K(C) Formation                             ... FULL-MO TRAFO
            Maximum number of iterations               ...        50
            Convergence tolerance (max. residuum)      ... 2.500e-05
            Level shift for amplitude update           ... 2.000e-01
            Maximum number of DIIS vectors             ...         7
            DIIS turned on at iteration                ...         0
            Damping before turning on DIIS             ...     0.500
            Damping after turning on DIIS              ...     0.000
            Pair specific amplitude update             ... OFF
            Natural orbital iterations                 ... OFF
            Perturbative natural orbital generation    ... OFF
            Printlevel                                 ... 2
            
            Memory handling:
            ----------------
            Maximum memory for working arrays          ...  32000 MB
            Data storage in matrix containers          ... UNCOMPRESSED
            Data type for integral storage             ... DOUBLE
            In-Core Storage of quantities:
               Amplitudes+Sigma Vector      ... YES
               J+K operators                ... YES
               DIIS vectors                 ... YES
               3-external integrals         ... YES
               4-external integrals         ... YES
            
            
            Initializing the integral package          ... done
            Warning: reference  - re-canonicalizations have been set to INT 1 VIRT 1
            
            --------------------------
            UNRESTRICTED FOCK OPERATOR
            --------------------------
            
            <ss|ss>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.004 ms/b)
            <ss|sp>:            6 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <ss|pp>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <sp|sp>:            3 b            0 skpd (  0.0%)    0.000 s ( 0.002 ms/b)
            <sp|pp>: done
            <pp|pp>: done
            Recanonicalizing the internal orbitals
            Recanonicalizing the virtual orbitals
            Time needed for Fock operator              ...            0.001 sec
            Reference energy                           ...     -0.498232909
            Error (ORCA_MDCI): Number of processes (1) in parallel calculation exceeds number of pairs (0)
            [file orca_mdci/mdci_state.cpp, line 942]: . . . aborting the run
            
            
            ORCA finished by error termination in MDCI
            Calling Command: /home/project_g4mp2_2019/ORCA_4_2/orca_4_2_0_linux_x86-64_openmpi314/orca_mdci input.mdciinp.tmp 
            [file orca_tools/qcmsg.cpp, line 458]: 
              .... aborting the run
            
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            Setting NCore(C ) from 2 to 2
            Setting NCore(H ) from 0 to 0
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            WARNING: No MP2 level density has been requested!
                     To caclulate MP2 level properties use
                     %mp2 Density relaxed end
                     or
                     %mp2 Density unrelaxed end
            
            WARNING: Post HF methods need fully converged wavefunctions
              ===> : Setting SCFConvForced true
                     You can overwrite this default with %scf ConvForced false 
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! MP2 Printbasis
            |  2> * xyz   0  2
            |  3> H     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14>   NewNCore C     2 end
            | 15>   NewNCore H     0 end
            | 16> end
            | 17> %basis
            | 18>      NewGTO   H
            | 19>      S  3
            | 20>      1              33.86500000               0.02549381
            | 21>      2               5.09479000               0.19037311
            | 22>      3               1.15879000               0.85216149
            | 23>      S  1
            | 24>      1               0.32584000               1.00000000
            | 25>      S  1
            | 26>      1               0.10274100               1.00000000
            | 27>      S  1
            | 28>      1               0.03600000               1.00000000
            | 29>      P  1
            | 30>      1               1.50000000               1.00000000
            | 31>      P  1
            | 32>      1               0.37500000               1.00000000
            | 33>      end
            | 34> end
            | 35> 
            | 36>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              H      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 H     1.0000    0     1.008    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type H   : 6s2p contracted to 4s2p pattern {3111/11}
            
            Atom   0H    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      33.8650000000      0.0254938099
               2       5.0947900000      0.1903731093
               3       1.1587900000      0.8521614869
             S 1 
               1       0.3258400000      1.0000000000
             S 1 
               1       0.1027410000      1.0000000000
             S 1 
               1       0.0360000000      1.0000000000
             P 1 
               1       1.5000000000      1.0000000000
             P 1 
               1       0.3750000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...    8
             # of primitive gaussian functions       ...   12
             # of contracted shells                  ...    6
             # of contracted basis functions         ...   10
             Highest angular momentum                ...    1
             Maximum contraction depth               ...    3
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    2
             Number of Electrons    NEL             ....    1
             Basis Dimension        Dim             ....   10
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 1
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 4.866e-02
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.000 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   1840 (   0.0 sec)
            # of grid points (after weights+screening)   ...   1840 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     1840
            Total number of batches                      ...       29
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     1840
            Average number of shells per batch           ...     5.80 (96.67%)
            Average number of basis functions per batch  ...     9.67 (96.67%)
            Average number of large shells per batch     ...     5.60 (96.55%)
            Average number of large basis fcns per batch ...     9.27 (95.86%)
            Maximum spatial batch extension              ...  18.53, 28.34, 28.34 au
            Average spatial batch extension              ...   7.21,  8.13,  8.85 au
            
            Time for grid setup =    0.005 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0     -0.4942847025   0.000000000000 0.01155899  0.00113565  0.0442923 0.7000
              1     -0.4952877073  -0.001003004793 0.01195499  0.00114151  0.0379041 0.7000
                                           ***Turning on DIIS***
              2     -0.4962186277  -0.000930920353 0.03456059  0.00326857  0.0315923 0.0000
              3     -0.4995632493  -0.003344621663 0.02016085  0.00185630  0.0135072 0.0000
              4     -0.4998496375  -0.000286388124 0.00563955  0.00051519  0.0037926 0.0000
              5     -0.4998258258   0.000023811640 0.00134282  0.00015820  0.0012661 0.0000
              6     -0.4998150142   0.000010811644 0.00096472  0.00010872  0.0004527 0.0000
              7     -0.4998174294  -0.000002415191 0.00019067  0.00001974  0.0000338 0.0000
              8     -0.4998179120  -0.000000482670 0.00001563  0.00000156  0.0000026 0.0000
              9     -0.4998179156  -0.000000003574 0.00000031  0.00000003  0.0000001 0.0000
                             **** Energy Check signals convergence ****
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER  10 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :           -0.49981792 Eh             -13.60074 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :           -0.49981792 Eh             -13.60074 eV
            One Electron Energy:           -0.49981792 Eh             -13.60074 eV
            Two Electron Energy:            0.00000000 Eh               0.00000 eV
            
            Virial components:
            Potential Energy   :           -0.99918098 Eh             -27.18910 eV
            Kinetic Energy     :            0.49936306 Eh              13.58836 eV
            Virial Ratio       :            2.00091087
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -2.1536e-11  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    7.3645e-09  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    7.1237e-10  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.2923e-09  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     0.750000
            Ideal value S*(S+1) for S=0.5   :     0.750000
            Deviation                       :     0.000000
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000      -0.499818       -13.6007 
               1   0.0000       0.079181         2.1546 
               2   0.0000       0.495850        13.4928 
               3   0.0000       0.717114        19.5137 
               4   0.0000       0.717114        19.5137 
               5   0.0000       0.717114        19.5137 
               6   0.0000       2.618052        71.2408 
               7   0.0000       3.980964       108.3275 
               8   0.0000       3.980964       108.3275 
               9   0.0000       3.980964       108.3275 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   0.0000       0.020777         0.5654 
               1   0.0000       0.149158         4.0588 
               2   0.0000       0.614700        16.7268 
               3   0.0000       0.814449        22.1623 
               4   0.0000       0.814449        22.1623 
               5   0.0000       0.814449        22.1623 
               6   0.0000       2.742167        74.6182 
               7   0.0000       4.070088       110.7527 
               8   0.0000       4.070088       110.7527 
               9   0.0000       4.070088       110.7527 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 H :    0.000000    1.000000
            Sum of atomic charges         :    0.0000000
            Sum of atomic spin populations:    1.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 H :    0.000000    1.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 H      1.0000     1.0000     0.0000     1.0000     0.0000     1.0000
            
              Mayer bond orders larger than 0.100000
            
            
            Local spin analysis not attempted because no beta electrons available
            --------------------------
            ATOM BASIS FOR ELEMENT H 
            --------------------------
             NewGTO H 
             S 6
                1         33.865000000000         0.006057302628
                2          5.094790000000         0.045232452091
                3          1.158790000000         0.202472679939
                4          0.325840000000         0.506406095195
                5          0.102741000000         0.375216572663
                6          0.036000000000         0.008364874007
             S 6
                1         33.865000000000         0.002153961168
                2          5.094790000000         0.016084543123
                3          1.158790000000         0.071998761979
                4          0.325840000000        -0.012955225775
                5          0.102741000000         1.076602724575
                6          0.036000000000        -1.659518651130
             S 6
                1         33.865000000000         0.002586939089
                2          5.094790000000         0.019317773210
                3          1.158790000000         0.086471573648
                4          0.325840000000         1.590490306659
                5          0.102741000000        -2.698076843339
                6          0.036000000000         1.218064164901
             S 6
                1         33.865000000000         0.040452274771
                2          5.094790000000         0.302074321363
                3          1.158790000000         1.352166300080
                4          0.325840000000        -2.221474943467
                5          0.102741000000         1.505535383031
                6          0.036000000000        -0.531287431821
             P 2
                1          1.500000000000        -0.072204131053
                2          0.375000000000         1.039577969156
             P 2
                1          1.500000000000         1.217445490381
                2          0.375000000000        -0.637702598895
             end
              // -----------------------------------------------
              // The basis set
              // -----------------------------------------------
              BAS[ATNO] = new BFNGauss[NSH];
              // Basis function   1 L = s
              InitBFNGauss(BAS[ATNO][  0]);
              BAS[ATNO][  0].l  = 0;
              BAS[ATNO][  0].ng = 6;
              BAS[ATNO][  0].a[  0] =        33.865000000000;     BAS[ATNO][  0].d[  0] =         0.006057302628;
              BAS[ATNO][  0].a[  1] =         5.094790000000;     BAS[ATNO][  0].d[  1] =         0.045232452091;
              BAS[ATNO][  0].a[  2] =         1.158790000000;     BAS[ATNO][  0].d[  2] =         0.202472679939;
              BAS[ATNO][  0].a[  3] =         0.325840000000;     BAS[ATNO][  0].d[  3] =         0.506406095195;
              BAS[ATNO][  0].a[  4] =         0.102741000000;     BAS[ATNO][  0].d[  4] =         0.375216572663;
              BAS[ATNO][  0].a[  5] =         0.036000000000;     BAS[ATNO][  0].d[  5] =         0.008364874007;
            
              // Basis function   2 L = s
              InitBFNGauss(BAS[ATNO][  1]);
              BAS[ATNO][  1].l  = 0;
              BAS[ATNO][  1].ng = 6;
              BAS[ATNO][  1].a[  0] =        33.865000000000;     BAS[ATNO][  1].d[  0] =        -0.002153961168;
              BAS[ATNO][  1].a[  1] =         5.094790000000;     BAS[ATNO][  1].d[  1] =        -0.016084543123;
              BAS[ATNO][  1].a[  2] =         1.158790000000;     BAS[ATNO][  1].d[  2] =        -0.071998761979;
              BAS[ATNO][  1].a[  3] =         0.325840000000;     BAS[ATNO][  1].d[  3] =         0.012955225775;
              BAS[ATNO][  1].a[  4] =         0.102741000000;     BAS[ATNO][  1].d[  4] =        -1.076602724575;
              BAS[ATNO][  1].a[  5] =         0.036000000000;     BAS[ATNO][  1].d[  5] =         1.659518651130;
            
              // Basis function   3 L = s
              InitBFNGauss(BAS[ATNO][  2]);
              BAS[ATNO][  2].l  = 0;
              BAS[ATNO][  2].ng = 6;
              BAS[ATNO][  2].a[  0] =        33.865000000000;     BAS[ATNO][  2].d[  0] =        -0.002586939089;
              BAS[ATNO][  2].a[  1] =         5.094790000000;     BAS[ATNO][  2].d[  1] =        -0.019317773210;
              BAS[ATNO][  2].a[  2] =         1.158790000000;     BAS[ATNO][  2].d[  2] =        -0.086471573648;
              BAS[ATNO][  2].a[  3] =         0.325840000000;     BAS[ATNO][  2].d[  3] =        -1.590490306659;
              BAS[ATNO][  2].a[  4] =         0.102741000000;     BAS[ATNO][  2].d[  4] =         2.698076843339;
              BAS[ATNO][  2].a[  5] =         0.036000000000;     BAS[ATNO][  2].d[  5] =        -1.218064164901;
            
              // Basis function   4 L = s
              InitBFNGauss(BAS[ATNO][  3]);
              BAS[ATNO][  3].l  = 0;
              BAS[ATNO][  3].ng = 6;
              BAS[ATNO][  3].a[  0] =        33.865000000000;     BAS[ATNO][  3].d[  0] =        -0.040452274771;
              BAS[ATNO][  3].a[  1] =         5.094790000000;     BAS[ATNO][  3].d[  1] =        -0.302074321363;
              BAS[ATNO][  3].a[  2] =         1.158790000000;     BAS[ATNO][  3].d[  2] =        -1.352166300080;
              BAS[ATNO][  3].a[  3] =         0.325840000000;     BAS[ATNO][  3].d[  3] =         2.221474943467;
              BAS[ATNO][  3].a[  4] =         0.102741000000;     BAS[ATNO][  3].d[  4] =        -1.505535383031;
              BAS[ATNO][  3].a[  5] =         0.036000000000;     BAS[ATNO][  3].d[  5] =         0.531287431821;
            
              // Basis function   5 L = p
              InitBFNGauss(BAS[ATNO][  4]);
              BAS[ATNO][  4].l  = 1;
              BAS[ATNO][  4].ng = 2;
              BAS[ATNO][  4].a[  0] =         1.500000000000;     BAS[ATNO][  4].d[  0] =        -0.072204131053;
              BAS[ATNO][  4].a[  1] =         0.375000000000;     BAS[ATNO][  4].d[  1] =         1.039577969156;
            
              // Basis function   6 L = p
              InitBFNGauss(BAS[ATNO][  5]);
              BAS[ATNO][  5].l  = 1;
              BAS[ATNO][  5].ng = 2;
              BAS[ATNO][  5].a[  0] =         1.500000000000;     BAS[ATNO][  5].d[  0] =         1.217445490381;
              BAS[ATNO][  5].a[  1] =         0.375000000000;     BAS[ATNO][  5].d[  1] =        -0.637702598895;
            
            -------------------------------------------
            RADIAL EXPECTATION VALUES <R**-3> TO <R**3>
            -------------------------------------------
               0 :     0.000000     1.985137     0.999181     1.501275     3.006315     7.520212
               1 :     0.000000     0.169228     0.228734     5.598059    34.147215   221.740922
               2 :     0.000000     0.935036     0.568396     3.302743    15.326264    89.101079
               3 :     0.000000     9.186624     1.914776     1.358982     3.919421    18.283327
               4 :     0.382448     0.443368     0.622332     1.787596     3.492171     7.363410
               5 :     0.382448     0.443368     0.622332     1.787596     3.492171     7.363410
               6 :     0.382448     0.443368     0.622332     1.787596     3.492171     7.363410
               7 :     4.275571     2.056632     1.280552     1.017337     1.405576     2.550816
               8 :     4.275571     2.056632     1.280552     1.017337     1.405576     2.550816
               9 :     4.275571     2.056632     1.280552     1.017337     1.405576     2.550816
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.055 sec
            Sum of individual times     ....       0.879 sec  ( 83.4%)
            
            Fock matrix formation       ....       0.776 sec  ( 73.5%)
            Diagonalization             ....       0.001 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.000 sec  (  0.0%)
            Initial guess               ....       0.096 sec  (  9.1%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.1%)
            
            ------------------------------------------------------------------------------
                                            ORCA  MP2 
            ------------------------------------------------------------------------------
            
            Freezing NCore=0 chemical core electrons
            Warning: Single electron - no MP2 correction
            
            ---------------------------------------
            MP2 TOTAL ENERGY:       -0.499817916 Eh
            ---------------------------------------
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY        -0.499817915628
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
            
              WARNING: The energy has been calculated at the MP2 level but the densities
                       used in the property calculations are still SCF densities
                       MP2 response densities have not been calculated 
                       use %mp2 Density relaxed end
                       or  %mp2 Density unrelaxed end
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000      -0.00000       0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000      -0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000    -0.000000     0.000000 
            x,y,z [Debye]:     0.000000    -0.000000     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        1.302 sec (=   0.022 min)
            GTO integral calculation        ...        0.209 sec (=   0.003 min)  16.0 %
            SCF iterations                  ...        1.079 sec (=   0.018 min)  82.9 %
            MP2 module                      ...        0.015 sec (=   0.000 min)   1.1 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 1 seconds 443 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  2
            |  3> H     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14> end
            | 15> %basis
            | 16>      NewGTO   H
            | 17>      S  3
            | 18>      1              33.87000000               0.02549486
            | 19>      2               5.09500000               0.19036277
            | 20>      3               1.15900000               0.85216202
            | 21>      S  1
            | 22>      1               0.32580000               1.00000000
            | 23>      S  1
            | 24>      1               0.10270000               1.00000000
            | 25>      P  1
            | 26>      1               0.72700000               1.00000000
            | 27>      end
            | 28> end
            | 29> 
            | 30>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              H      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 H     1.0000    0     1.008    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type H   : 5s1p contracted to 3s1p pattern {311/1}
            
            Atom   0H    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      33.8700000000      0.0254948600
               2       5.0950000000      0.1903627700
               3       1.1590000000      0.8521620200
             S 1 
               1       0.3258000000      1.0000000000
             S 1 
               1       0.1027000000      1.0000000000
             P 1 
               1       0.7270000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...    6
             # of primitive gaussian functions       ...    8
             # of contracted shells                  ...    4
             # of contracted basis functions         ...    6
             Highest angular momentum                ...    1
             Maximum contraction depth               ...    3
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    2
             Number of Electrons    NEL             ....    1
             Basis Dimension        Dim             ....    6
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 1.093e-01
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.000 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   1840 (   0.0 sec)
            # of grid points (after weights+screening)   ...   1840 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     1840
            Total number of batches                      ...       29
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     1840
            Average number of shells per batch           ...     3.87 (96.67%)
            Average number of basis functions per batch  ...     5.80 (96.67%)
            Average number of large shells per batch     ...     3.77 (97.41%)
            Average number of large basis fcns per batch ...     5.70 (98.28%)
            Maximum spatial batch extension              ...  18.53, 28.34, 28.34 au
            Average spatial batch extension              ...   7.21,  8.13,  8.85 au
            
            Time for grid setup =    0.004 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0     -0.4950926645   0.000000000000 0.01892122  0.00258769  0.0437347 0.7000
              1     -0.4959770259  -0.000884361385 0.01890103  0.00264245  0.0373633 0.7000
                                           ***Turning on DIIS***
              2     -0.4967828095  -0.000805783679 0.05340169  0.00756332  0.0310756 0.0000
              3     -0.4996330207  -0.002850211198 0.02468181  0.00382766  0.0130977 0.0000
              4     -0.4998366351  -0.000203614372 0.00636160  0.00102833  0.0030670 0.0000
              5     -0.4998175131   0.000019121991 0.00234723  0.00036470  0.0007099 0.0000
              6     -0.4998095058   0.000008007324 0.00019516  0.00002882  0.0000479 0.0000
              7     -0.4998098015  -0.000000295671 0.00002216  0.00000323  0.0000049 0.0000
              8     -0.4998098113  -0.000000009778 0.00000068  0.00000010  0.0000001 0.0000
                             **** Energy Check signals convergence ****
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   9 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :           -0.49980981 Eh             -13.60052 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :           -0.49980981 Eh             -13.60052 eV
            One Electron Energy:           -0.49980981 Eh             -13.60052 eV
            Two Electron Energy:            0.00000000 Eh               0.00000 eV
            
            Virial components:
            Potential Energy   :           -0.99959694 Eh             -27.20042 eV
            Kinetic Energy     :            0.49978713 Eh              13.59990 eV
            Virial Ratio       :            2.00004539
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...   -4.8773e-11  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    9.4292e-09  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    1.3586e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.9674e-09  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     0.750000
            Ideal value S*(S+1) for S=0.5   :     0.750000
            Deviation                       :     0.000000
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000      -0.499810       -13.6005 
               1   0.0000       0.348764         9.4903 
               2   0.0000       1.442973        39.2653 
               3   0.0000       1.442973        39.2653 
               4   0.0000       1.442973        39.2653 
               5   0.0000       2.469733        67.2049 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   0.0000       0.056230         1.5301 
               1   0.0000       0.492239        13.3945 
               2   0.0000       1.573502        42.8172 
               3   0.0000       1.573502        42.8172 
               4   0.0000       1.573502        42.8172 
               5   0.0000       2.601264        70.7840 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 H :    0.000000    1.000000
            Sum of atomic charges         :    0.0000000
            Sum of atomic spin populations:    1.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 H :    0.000000    1.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 H      1.0000     1.0000     0.0000     1.0000     0.0000     1.0000
            
              Mayer bond orders larger than 0.100000
            
            
            Local spin analysis not attempted because no beta electrons available
            --------------------------
            ATOM BASIS FOR ELEMENT H 
            --------------------------
             NewGTO H 
             S 5
                1         33.870000000000         0.006067980830
                2          5.095000000000         0.045307863589
                3          1.159000000000         0.202821384444
                4          0.325800000000         0.503903789927
                5          0.102700000000         0.383420578478
             S 5
                1         33.870000000000         0.002435237260
                2          5.095000000000         0.018183214597
                3          1.159000000000         0.081397454351
                4          0.325800000000         1.318039683615
                5          0.102700000000        -1.557535087459
             S 5
                1         33.870000000000         0.039184366690
                2          5.095000000000         0.292578370061
                3          1.159000000000         1.309731807537
                4          0.325800000000        -1.881682343371
                5          0.102700000000         0.805583103718
             P 1
                1          0.727000000000         1.000000000000
             end
              // -----------------------------------------------
              // The basis set
              // -----------------------------------------------
              BAS[ATNO] = new BFNGauss[NSH];
              // Basis function   1 L = s
              InitBFNGauss(BAS[ATNO][  0]);
              BAS[ATNO][  0].l  = 0;
              BAS[ATNO][  0].ng = 5;
              BAS[ATNO][  0].a[  0] =        33.870000000000;     BAS[ATNO][  0].d[  0] =         0.006067980830;
              BAS[ATNO][  0].a[  1] =         5.095000000000;     BAS[ATNO][  0].d[  1] =         0.045307863589;
              BAS[ATNO][  0].a[  2] =         1.159000000000;     BAS[ATNO][  0].d[  2] =         0.202821384444;
              BAS[ATNO][  0].a[  3] =         0.325800000000;     BAS[ATNO][  0].d[  3] =         0.503903789927;
              BAS[ATNO][  0].a[  4] =         0.102700000000;     BAS[ATNO][  0].d[  4] =         0.383420578478;
            
              // Basis function   2 L = s
              InitBFNGauss(BAS[ATNO][  1]);
              BAS[ATNO][  1].l  = 0;
              BAS[ATNO][  1].ng = 5;
              BAS[ATNO][  1].a[  0] =        33.870000000000;     BAS[ATNO][  1].d[  0] =        -0.002435237260;
              BAS[ATNO][  1].a[  1] =         5.095000000000;     BAS[ATNO][  1].d[  1] =        -0.018183214597;
              BAS[ATNO][  1].a[  2] =         1.159000000000;     BAS[ATNO][  1].d[  2] =        -0.081397454351;
              BAS[ATNO][  1].a[  3] =         0.325800000000;     BAS[ATNO][  1].d[  3] =        -1.318039683615;
              BAS[ATNO][  1].a[  4] =         0.102700000000;     BAS[ATNO][  1].d[  4] =         1.557535087459;
            
              // Basis function   3 L = s
              InitBFNGauss(BAS[ATNO][  2]);
              BAS[ATNO][  2].l  = 0;
              BAS[ATNO][  2].ng = 5;
              BAS[ATNO][  2].a[  0] =        33.870000000000;     BAS[ATNO][  2].d[  0] =        -0.039184366690;
              BAS[ATNO][  2].a[  1] =         5.095000000000;     BAS[ATNO][  2].d[  1] =        -0.292578370061;
              BAS[ATNO][  2].a[  2] =         1.159000000000;     BAS[ATNO][  2].d[  2] =        -1.309731807537;
              BAS[ATNO][  2].a[  3] =         0.325800000000;     BAS[ATNO][  2].d[  3] =         1.881682343371;
              BAS[ATNO][  2].a[  4] =         0.102700000000;     BAS[ATNO][  2].d[  4] =        -0.805583103718;
            
              // Basis function   4 L = p
              InitBFNGauss(BAS[ATNO][  3]);
              BAS[ATNO][  3].l  = 1;
              BAS[ATNO][  3].ng = 1;
              BAS[ATNO][  3].a[  0] =         0.727000000000;     BAS[ATNO][  3].d[  0] =         1.000000000000;
            
            -------------------------------------------
            RADIAL EXPECTATION VALUES <R**-3> TO <R**3>
            -------------------------------------------
               0 :     0.000000     1.986605     0.999597     1.499123     2.991127     7.430096
               1 :     0.000000     0.881864     0.563669     2.941211    10.425016    40.249470
               2 :     0.000000     9.062207     1.917627     1.265316     2.952575     9.538994
               3 :     1.318896     0.969333     0.907081     1.247704     1.719395     2.574355
               4 :     1.318896     0.969333     0.907081     1.247704     1.719395     2.574355
               5 :     1.318896     0.969333     0.907081     1.247704     1.719395     2.574355
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.230 sec
            Sum of individual times     ....       0.776 sec  ( 63.1%)
            
            Fock matrix formation       ....       0.686 sec  ( 55.8%)
            Diagonalization             ....       0.001 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.1%)
            Initial guess               ....       0.084 sec  (  6.8%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.1%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY        -0.499809811301
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:     -0.00000       0.00000       0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :     -0.00000       0.00000       0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :    -0.000000     0.000000     0.000000 
            x,y,z [Debye]:    -0.000000     0.000000     0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        1.463 sec (=   0.024 min)
            GTO integral calculation        ...        0.203 sec (=   0.003 min)  13.9 %
            SCF iterations                  ...        1.260 sec (=   0.021 min)  86.1 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 1 seconds 620 msec
            
                                             *****************
                                             * O   R   C   A *
                                             *****************
            
                       --- An Ab Initio, DFT and Semiempirical electronic structure package ---
            
                              #######################################################
                              #                        -***-                        #
                              #          Department of theory and spectroscopy      #
                              #               Directorship: Frank Neese             #
                              #        Max Planck Institute fuer Kohlenforschung    #
                              #                Kaiser Wilhelm Platz 1               #
                              #                 D-45470 Muelheim/Ruhr               #
                              #                      Germany                        #
                              #                                                     #
                              #                  All rights reserved                #
                              #                        -***-                        #
                              #######################################################
            
            
                                     Program Version 4.2.0 -  RELEASE  -
            
            
             With contributions from (in alphabetic order):
               Daniel Aravena         : Magnetic Suceptibility
               Michael Atanasov       : Ab Initio Ligand Field Theory (pilot matlab implementation)
               Alexander A. Auer      : GIAO ZORA, VPT2
               Ute Becker             : Parallelization
               Giovanni Bistoni       : ED, misc. LED, open-shell LED, HFLED
               Martin Brehm           : Molecular dynamics
               Dmytro Bykov           : SCF Hessian
               Vijay G. Chilkuri      : MRCI spin determinant printing, contributions to CSF-ICE
               Dipayan Datta          : RHF DLPNO-CCSD density
               Achintya Kumar Dutta   : EOM-CC, STEOM-CC
               Dmitry Ganyushin       : Spin-Orbit,Spin-Spin,Magnetic field MRCI
               Miquel Garcia          : C-PCM Hessian, Gaussian charge scheme
               Yang Guo               : DLPNO-NEVPT2, CIM, IAO-localization
               Andreas Hansen         : Spin unrestricted coupled pair/coupled cluster methods
               Benjamin Helmich-Paris : CASSCF linear response (MC-RPA)
               Lee Huntington         : MR-EOM, pCC
               Robert Izsak           : Overlap fitted RIJCOSX, COSX-SCS-MP3, EOM
               Christian Kollmar      : KDIIS, OOCD, Brueckner-CCSD(T), CCSD density
               Simone Kossmann        : Meta GGA functionals, TD-DFT gradient, OOMP2, MP2 Hessian
               Martin Krupicka        : AUTO-CI
               Lucas Lang             : DCDCAS
               Dagmar Lenk            : GEPOL surface, SMD
               Dimitrios Liakos       : Extrapolation schemes; Compound Job, initial MDCI parallelization
               Dimitrios Manganas     : Further ROCIS development; embedding schemes
               Dimitrios Pantazis     : SARC Basis sets
               Taras Petrenko         : DFT Hessian,TD-DFT gradient, ASA, ECA, R-Raman, ABS, FL, XAS/XES, NRVS
               Peter Pinski           : DLPNO-MP2, DLPNO-MP2 Gradient
               Christoph Reimann      : Effective Core Potentials
               Marius Retegan         : Local ZFS, SOC
               Christoph Riplinger    : Optimizer, TS searches, QM/MM, DLPNO-CCSD(T), (RO)-DLPNO pert. Triples
               Tobias Risthaus        : Range-separated hybrids, TD-DFT gradient, RPA, STAB
               Michael Roemelt        : Original ROCIS implementation
               Masaaki Saitow         : Open-shell DLPNO-CCSD energy and density
               Barbara Sandhoefer     : DKH picture change effects
               Avijit Sen             : IP-ROCIS
               Kantharuban Sivalingam : CASSCF convergence, NEVPT2, FIC-MRCI
               Bernardo de Souza      : ESD, SOC TD-DFT
               Georgi Stoychev        : AutoAux, RI-MP2 NMR
               Willem Van den Heuvel  : Paramagnetic NMR
               Boris Wezisla          : Elementary symmetry handling
               Frank Wennmohs         : Technical directorship
            
            
             We gratefully acknowledge several colleagues who have allowed us to
             interface, adapt or use parts of their codes:
               Stefan Grimme, W. Hujo, H. Kruse,             : VdW corrections, initial TS optimization,
                              C. Bannwarth                     DFT functionals, gCP, sTDA/sTD-DF
               Ed Valeev, F. Pavosevic, A. Kumar             : LibInt (2-el integral package), F12 methods
               Garnet Chan, S. Sharma, J. Yang, R. Olivares  : DMRG
               Ulf Ekstrom                                   : XCFun DFT Library
               Mihaly Kallay                                 : mrcc  (arbitrary order and MRCC methods)
               Andreas Klamt, Michael Diedenhofen            : otool_cosmo (COSMO solvation model)
               Jiri Pittner, Ondrej Demel                    : Mk-CCSD
               Frank Weinhold                                : gennbo (NPA and NBO analysis)
               Christopher J. Cramer and Donald G. Truhlar   : smd solvation model
               Lars Goerigk                                  : TD-DFT with DH, B97 family of functionals
               V. Asgeirsson, H. Jonsson                     : NEB implementation
               FAccTs GmbH                                   : IRC, NEB, NEB-TS, Multilevel, MM, QM/MM, CI optimization
               S Lehtola, MJT Oliveira, MAL Marques          : LibXC Library
            
            
             Your calculation uses the libint2 library for the computation of 2-el integrals
             For citations please refer to: http://libint.valeyev.net
            
             Your ORCA version has been built with support for libXC version: 4.2.3
             For citations please refer to: https://tddft.org/programs/libxc/
            
             This ORCA versions uses:
               CBLAS   interface :  Fast vector & matrix operations
               LAPACKE interface :  Fast linear algebra routines
               SCALAPACK package :  Parallel linear algebra routines
            
            
            ----- Orbital basis set information -----
            Your calculation utilizes the basis: def2-SVP
               F. Weigend and R. Ahlrichs, Phys. Chem. Chem. Phys. 7, 3297 (2005).
            
            ================================================================================
                                                    WARNINGS
                                   Please study these warnings very carefully!
            ================================================================================
            
            
            WARNING: your system is open-shell and RHF/RKS was chosen
              ===> : WILL SWITCH to UHF/UKS
            
            
            INFO   : the flag for use of LIBINT has been found!
            
            ================================================================================
                                                   INPUT FILE
            ================================================================================
            NAME = input.com
            |  1> ! HF Printbasis
            |  2> * xyz   0  2
            |  3> H     0.00000000     0.00000000     0.00000000
            |  4> *
            |  5> %MaxCore    64000
            |  6> %scf
            |  7>   MaxIter 500
            |  8>   Convergence VeryTight
            |  9> end
            | 10> %pal nprocs     1
            | 11> end
            | 12> %method
            | 13>   IntAcc 7.0
            | 14> end
            | 15> %basis
            | 16>      NewGTO   H
            | 17>      S  3
            | 18>      1              82.64000000               0.02295076
            | 19>      2              12.41000000               0.17554012
            | 20>      3               2.82400000               0.86470355
            | 21>      S  1
            | 22>      1               0.79770000               1.00000000
            | 23>      S  1
            | 24>      1               0.25810000               1.00000000
            | 25>      S  1
            | 26>      1               0.08989000               1.00000000
            | 27>      P  1
            | 28>      1               1.40700000               1.00000000
            | 29>      P  1
            | 30>      1               0.38800000               1.00000000
            | 31>      D  1
            | 32>      1               1.05700000               1.00000000
            | 33>      end
            | 34> end
            | 35> 
            | 36>                          ****END OF INPUT****
            ================================================================================
            
                                   ****************************
                                   * Single Point Calculation *
                                   ****************************
            
            ---------------------------------
            CARTESIAN COORDINATES (ANGSTROEM)
            ---------------------------------
              H      0.000000    0.000000    0.000000
            
            ----------------------------
            CARTESIAN COORDINATES (A.U.)
            ----------------------------
              NO LB      ZA    FRAG     MASS         X           Y           Z
               0 H     1.0000    0     1.008    0.000000    0.000000    0.000000
            
            --------------------------------
            INTERNAL COORDINATES (ANGSTROEM)
            --------------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------------
            INTERNAL COORDINATES (A.U.)
            ---------------------------
             H      0   0   0     0.000000000000     0.00000000     0.00000000
            
            ---------------------
            BASIS SET INFORMATION
            ---------------------
            There are 1 groups of distinct atoms
            
             Group   1 Type H   : 6s2p1d contracted to 4s2p1d pattern {3111/11/1}
            
            Atom   0H    basis set group =>   1
            
            -------------------------
            BASIS SET IN INPUT FORMAT
            -------------------------
            
             # Basis set for element : H 
             NewGTO H 
             S 3 
               1      82.6400000000      0.0229507600
               2      12.4100000000      0.1755401198
               3       2.8240000000      0.8647035489
             S 1 
               1       0.7977000000      1.0000000000
             S 1 
               1       0.2581000000      1.0000000000
             S 1 
               1       0.0898900000      1.0000000000
             P 1 
               1       1.4070000000      1.0000000000
             P 1 
               1       0.3880000000      1.0000000000
             D 1 
               1       1.0570000000      1.0000000000
              end;
            
            ------------------------------------------------------------------------------
                                       ORCA GTO INTEGRAL CALCULATION
            ------------------------------------------------------------------------------
            
                                     BASIS SET STATISTICS AND STARTUP INFO
            
             # of primitive gaussian shells          ...    9
             # of primitive gaussian functions       ...   17
             # of contracted shells                  ...    7
             # of contracted basis functions         ...   15
             Highest angular momentum                ...    2
             Maximum contraction depth               ...    3
             Integral package used                   ... LIBINT
             Integral threshhold            Thresh   ...  1.000e-12
             Primitive cut-off              TCut     ...  1.000e-14
            
            
            ------------------------------ INTEGRAL EVALUATION ----------------------------
            
            
             * One electron integrals 
             Pre-screening matrix                    ... done
             Shell pair data                         ... done (   0.000 sec)
            
            -------------------------------------------------------------------------------
                                             ORCA SCF
            -------------------------------------------------------------------------------
            
            ------------
            SCF SETTINGS
            ------------
            Hamiltonian:
             Ab initio Hamiltonian  Method          .... Hartree-Fock(GTOs)
            
            
            General Settings:
             Integral files         IntName         .... input
             Hartree-Fock type      HFTyp           .... UHF
             Total Charge           Charge          ....    0
             Multiplicity           Mult            ....    2
             Number of Electrons    NEL             ....    1
             Basis Dimension        Dim             ....   15
             Nuclear Repulsion      ENuc            ....      0.0000000000 Eh
            
            Convergence Acceleration:
             DIIS                   CNVDIIS         .... on
               Start iteration      DIISMaxIt       ....    12
               Startup error        DIISStart       ....  0.200000
               # of expansion vecs  DIISMaxEq       ....     5
               Bias factor          DIISBfac        ....   1.050
               Max. coefficient     DIISMaxC        ....  10.000
             Newton-Raphson         CNVNR           .... off
             SOSCF                  CNVSOSCF        .... off
             Level Shifting         CNVShift        .... on
               Level shift para.    LevelShift      ....    0.2500
               Turn off err/grad.   ShiftErr        ....    0.0010
             Zerner damping         CNVZerner       .... off
             Static damping         CNVDamp         .... on
               Fraction old density DampFac         ....    0.7000
               Max. Damping (<1)    DampMax         ....    0.9800
               Min. Damping (>=0)   DampMin         ....    0.0000
               Turn off err/grad.   DampErr         ....    0.1000
             Fernandez-Rico         CNVRico         .... off
            
            SCF Procedure:
             Maximum # iterations   MaxIter         ....   500
             SCF integral mode      SCFMode         .... Direct
               Integral package                     .... LIBINT
             Reset frequency        DirectResetFreq ....    20
             Integral Threshold     Thresh          ....  1.000e-12 Eh
             Primitive CutOff       TCut            ....  1.000e-14 Eh
            
            Convergence Tolerance:
             Convergence Check Mode ConvCheckMode   .... Total+1el-Energy
             Convergence forced     ConvForced      .... 0
             Energy Change          TolE            ....  1.000e-09 Eh
             1-El. energy change                    ....  1.000e-06 Eh
             DIIS Error             TolErr          ....  1.000e-08
            
            
            Diagonalization of the overlap matrix:
            Smallest eigenvalue                        ... 4.655e-02
            Time for diagonalization                   ...    0.000 sec
            Threshold for overlap eigenvalues          ... 1.000e-08
            Number of eigenvalues below threshold      ... 0
            Time for construction of square roots      ...    0.000 sec
            Total time needed                          ...    0.001 sec
            
            -------------------
            DFT GRID GENERATION
            -------------------
            
            General Integration Accuracy     IntAcc      ...  7.000
            Radial Grid Type                 RadialGrid  ... Gauss-Chebyshev
            Angular Grid (max. acc.)         AngularGrid ... Lebedev-110
            Angular grid pruning method      GridPruning ... 3 (G Style)
            Weight generation scheme         WeightScheme... Becke
            Basis function cutoff            BFCut       ...    1.0000e-12
            Integration weight cutoff        WCut        ...    1.0000e-14
            Grids for H and He will be reduced by one unit
            
            # of grid points (after initial pruning)     ...   1840 (   0.0 sec)
            # of grid points (after weights+screening)   ...   1840 (   0.0 sec)
            Grid point division into batches done        ...    0.0 sec
            Reduced shell lists constructed in    0.0 sec
            
            Total number of grid points                  ...     1840
            Total number of batches                      ...       29
            Average number of points per batch           ...       63
            Average number of grid points per atom       ...     1840
            Average number of shells per batch           ...     6.63 (94.76%)
            Average number of basis functions per batch  ...    14.37 (95.78%)
            Average number of large shells per batch     ...     6.47 (97.49%)
            Average number of large basis fcns per batch ...    14.00 (97.45%)
            Maximum spatial batch extension              ...  18.53, 28.34, 28.34 au
            Average spatial batch extension              ...   7.21,  8.13,  8.85 au
            
            Time for grid setup =    0.007 sec
            
            ------------------------------
            INITIAL GUESS: MODEL POTENTIAL
            ------------------------------
            Loading Hartree-Fock densities                     ... done
            Calculating cut-offs                               ... done
            Setting up the integral package                    ... done
            Initializing the effective Hamiltonian             ... done
            Starting the Coulomb interaction                   ... done (   0.0 sec)
            Reading the grid                                   ... done
            Mapping shells                                     ... done
            Starting the XC term evaluation                    ... done (   0.0 sec)
            Transforming the Hamiltonian                       ... done (   0.0 sec)
            Diagonalizing the Hamiltonian                      ... done (   0.0 sec)
            Back transforming the eigenvectors                 ... done (   0.0 sec)
            Now organizing SCF variables                       ... done
                                  ------------------
                                  INITIAL GUESS DONE (   0.1 sec)
                                  ------------------
            --------------
            SCF ITERATIONS
            --------------
            ITER       Energy         Delta-E        Max-DP      RMS-DP      [F,P]     Damp
                           ***  Starting incremental Fock matrix formation  ***
              0     -0.4948799739   0.000000000000 0.01647762  0.00095716  0.0453832 0.7000
              1     -0.4958149581  -0.000934984105 0.01682258  0.00101371  0.0388718 0.7000
                                           ***Turning on DIIS***
              2     -0.4966737156  -0.000858757543 0.04792349  0.00295093  0.0323608 0.0000
              3     -0.4997381347  -0.003064419102 0.02144220  0.00149609  0.0136942 0.0000
              4     -0.4999724014  -0.000234266722 0.00681663  0.00045457  0.0034468 0.0000
              5     -0.4999538271   0.000018574326 0.00322045  0.00019713  0.0009020 0.0000
              6     -0.4999444245   0.000009402632 0.00047499  0.00002720  0.0000823 0.0000
              7     -0.4999455588  -0.000001134370 0.00005742  0.00000332  0.0000095 0.0000
              8     -0.4999455690  -0.000000010149 0.00000034  0.00000002  0.0000002 0.0000
                             **** Energy Check signals convergence ****
            
                           *****************************************************
                           *                     SUCCESS                       *
                           *           SCF CONVERGED AFTER   9 CYCLES          *
                           *****************************************************
            
            
            ----------------
            TOTAL SCF ENERGY
            ----------------
            
            Total Energy       :           -0.49994557 Eh             -13.60421 eV
            
            Components:
            Nuclear Repulsion  :            0.00000000 Eh               0.00000 eV
            Electronic Energy  :           -0.49994557 Eh             -13.60421 eV
            One Electron Energy:           -0.49994557 Eh             -13.60421 eV
            Two Electron Energy:           -0.00000000 Eh              -0.00000 eV
            
            Virial components:
            Potential Energy   :           -0.99989036 Eh             -27.20840 eV
            Kinetic Energy     :            0.49994479 Eh              13.60419 eV
            Virial Ratio       :            2.00000156
            
            
            ---------------
            SCF CONVERGENCE
            ---------------
            
              Last Energy change         ...    3.9378e-10  Tolerance :   1.0000e-09
              Last MAX-Density change    ...    1.7169e-07  Tolerance :   1.0000e-08
              Last RMS-Density change    ...    9.3028e-09  Tolerance :   1.0000e-09
              Last DIIS Error            ...    1.8614e-08  Tolerance :   1.0000e-08
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
                         **** ENERGY FILE WAS UPDATED (input.en.tmp) ****
            ----------------------
            UHF SPIN CONTAMINATION
            ----------------------
            
            Expectation value of <S**2>     :     0.750000
            Ideal value S*(S+1) for S=0.5   :     0.750000
            Deviation                       :     0.000000
            
                         **** THE GBW FILE WAS UPDATED (input.gbw) ****
                         **** DENSITY FILE WAS UPDATED (input.scfp) ****
            ----------------
            ORBITAL ENERGIES
            ----------------
                             SPIN UP ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   1.0000      -0.499946       -13.6042 
               1   0.0000       0.267390         7.2761 
               2   0.0000       0.737487        20.0680 
               3   0.0000       0.737487        20.0680 
               4   0.0000       0.737487        20.0680 
               5   0.0000       1.491512        40.5861 
               6   0.0000       3.429886        93.3319 
               7   0.0000       3.429886        93.3319 
               8   0.0000       3.429886        93.3319 
               9   0.0000       3.429886        93.3319 
              10   0.0000       3.429886        93.3319 
              11   0.0000       3.846024       104.6556 
              12   0.0000       3.846024       104.6556 
              13   0.0000       3.846024       104.6556 
              14   0.0000       7.297110       198.5645 
            
                             SPIN DOWN ORBITALS
              NO   OCC          E(Eh)            E(eV) 
               0   0.0000       0.048258         1.3132 
               1   0.0000       0.390589        10.6285 
               2   0.0000       0.835347        22.7309 
               3   0.0000       0.835347        22.7309 
               4   0.0000       0.835347        22.7309 
               5   0.0000       1.612930        43.8900 
               6   0.0000       3.486466        94.8716 
               7   0.0000       3.486466        94.8716 
               8   0.0000       3.486466        94.8716 
               9   0.0000       3.486466        94.8716 
              10   0.0000       3.486466        94.8716 
              11   0.0000       3.933602       107.0387 
              12   0.0000       3.933602       107.0387 
              13   0.0000       3.933602       107.0387 
              14   0.0000       7.380432       200.8318 
            
                                ********************************
                                * MULLIKEN POPULATION ANALYSIS *
                                ********************************
            
            --------------------------------------------
            MULLIKEN ATOMIC CHARGES AND SPIN POPULATIONS
            --------------------------------------------
               0 H :   -0.000000    1.000000
            Sum of atomic charges         :   -0.0000000
            Sum of atomic spin populations:    1.0000000
            
            -----------------------------------------------------
            MULLIKEN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            -----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
                  dz2     :     0.000000  d :     0.000000
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
                  dz2     :     0.000000  d :     0.000000
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            
                                 *******************************
                                 * LOEWDIN POPULATION ANALYSIS *
                                 *******************************
            
            -------------------------------------------
            LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
            -------------------------------------------
               0 H :   -0.000000    1.000000
            
            ----------------------------------------------------
            LOEWDIN REDUCED ORBITAL CHARGES AND SPIN POPULATIONS
            ----------------------------------------------------
            CHARGE
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
                  dz2     :     0.000000  d :     0.000000
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            SPIN
              0 H s       :     1.000000  s :     1.000000
                  pz      :     0.000000  p :     0.000000
                  px      :     0.000000
                  py      :     0.000000
                  dz2     :     0.000000  d :     0.000000
                  dxz     :     0.000000
                  dyz     :     0.000000
                  dx2y2   :     0.000000
                  dxy     :     0.000000
            
            
                                  *****************************
                                  * MAYER POPULATION ANALYSIS *
                                  *****************************
            
              NA   - Mulliken gross atomic population
              ZA   - Total nuclear charge
              QA   - Mulliken gross atomic charge
              VA   - Mayer's total valence
              BVA  - Mayer's bonded valence
              FA   - Mayer's free valence
            
              ATOM       NA         ZA         QA         VA         BVA        FA
              0 H      1.0000     1.0000    -0.0000     1.0000     0.0000     1.0000
            
              Mayer bond orders larger than 0.100000
            
            
            Local spin analysis not attempted because no beta electrons available
            --------------------------
            ATOM BASIS FOR ELEMENT H 
            --------------------------
             NewGTO H 
             S 6
                1         82.640000000000         0.002006028566
                2         12.410000000000         0.015343217182
                3          2.824000000000         0.075580068909
                4          0.797700000000         0.256873877689
                5          0.258100000000         0.497369345580
                6          0.089890000000         0.296132289000
             S 6
                1         82.640000000000         0.001809879809
                2         12.410000000000         0.013842962884
                3          2.824000000000         0.068189876753
                4          0.797700000000        -0.058576882292
                5          0.258100000000         1.504178391169
                6          0.089890000000        -1.739774328067
             S 6
                1         82.640000000000         0.000491291030
                2         12.410000000000         0.003757665817
                3          2.824000000000         0.018510110233
                4          0.797700000000         1.889607346963
                5          0.258100000000        -2.591238695558
                6          0.089890000000         1.082095485165
             S 6
                1         82.640000000000         0.037432485683
                2         12.410000000000         0.286304376358
                3          2.824000000000         1.410323808694
                4          0.797700000000        -2.137557853761
                5          0.258100000000         1.428868812264
                6          0.089890000000        -0.493705805382
             P 2
                1          1.407000000000        -0.093234487709
                2          0.388000000000         1.054625569916
             P 2
                1          1.407000000000         1.264659250317
                2          0.388000000000        -0.704145294942
             D 1
                1          1.057000000000         1.000000000000
             end
              // -----------------------------------------------
              // The basis set
              // -----------------------------------------------
              BAS[ATNO] = new BFNGauss[NSH];
              // Basis function   1 L = s
              InitBFNGauss(BAS[ATNO][  0]);
              BAS[ATNO][  0].l  = 0;
              BAS[ATNO][  0].ng = 6;
              BAS[ATNO][  0].a[  0] =        82.640000000000;     BAS[ATNO][  0].d[  0] =         0.002006028566;
              BAS[ATNO][  0].a[  1] =        12.410000000000;     BAS[ATNO][  0].d[  1] =         0.015343217182;
              BAS[ATNO][  0].a[  2] =         2.824000000000;     BAS[ATNO][  0].d[  2] =         0.075580068909;
              BAS[ATNO][  0].a[  3] =         0.797700000000;     BAS[ATNO][  0].d[  3] =         0.256873877689;
              BAS[ATNO][  0].a[  4] =         0.258100000000;     BAS[ATNO][  0].d[  4] =         0.497369345580;
              BAS[ATNO][  0].a[  5] =         0.089890000000;     BAS[ATNO][  0].d[  5] =         0.296132289000;
            
              // Basis function   2 L = s
              InitBFNGauss(BAS[ATNO][  1]);
              BAS[ATNO][  1].l  = 0;
              BAS[ATNO][  1].ng = 6;
              BAS[ATNO][  1].a[  0] =        82.640000000000;     BAS[ATNO][  1].d[  0] =        -0.001809879809;
              BAS[ATNO][  1].a[  1] =        12.410000000000;     BAS[ATNO][  1].d[  1] =        -0.013842962884;
              BAS[ATNO][  1].a[  2] =         2.824000000000;     BAS[ATNO][  1].d[  2] =        -0.068189876753;
              BAS[ATNO][  1].a[  3] =         0.797700000000;     BAS[ATNO][  1].d[  3] =         0.058576882292;
              BAS[ATNO][  1].a[  4] =         0.258100000000;     BAS[ATNO][  1].d[  4] =        -1.504178391169;
              BAS[ATNO][  1].a[  5] =         0.089890000000;     BAS[ATNO][  1].d[  5] =         1.739774328067;
            
              // Basis function   3 L = s
              InitBFNGauss(BAS[ATNO][  2]);
              BAS[ATNO][  2].l  = 0;
              BAS[ATNO][  2].ng = 6;
              BAS[ATNO][  2].a[  0] =        82.640000000000;     BAS[ATNO][  2].d[  0] =        -0.000491291030;
              BAS[ATNO][  2].a[  1] =        12.410000000000;     BAS[ATNO][  2].d[  1] =        -0.003757665817;
              BAS[ATNO][  2].a[  2] =         2.824000000000;     BAS[ATNO][  2].d[  2] =        -0.018510110233;
              BAS[ATNO][  2].a[  3] =         0.797700000000;     BAS[ATNO][  2].d[  3] =        -1.889607346963;
              BAS[ATNO][  2].a[  4] =         0.258100000000;     BAS[ATNO][  2].d[  4] =         2.591238695558;
              BAS[ATNO][  2].a[  5] =         0.089890000000;     BAS[ATNO][  2].d[  5] =        -1.082095485165;
            
              // Basis function   4 L = s
              InitBFNGauss(BAS[ATNO][  3]);
              BAS[ATNO][  3].l  = 0;
              BAS[ATNO][  3].ng = 6;
              BAS[ATNO][  3].a[  0] =        82.640000000000;     BAS[ATNO][  3].d[  0] =        -0.037432485683;
              BAS[ATNO][  3].a[  1] =        12.410000000000;     BAS[ATNO][  3].d[  1] =        -0.286304376358;
              BAS[ATNO][  3].a[  2] =         2.824000000000;     BAS[ATNO][  3].d[  2] =        -1.410323808694;
              BAS[ATNO][  3].a[  3] =         0.797700000000;     BAS[ATNO][  3].d[  3] =         2.137557853761;
              BAS[ATNO][  3].a[  4] =         0.258100000000;     BAS[ATNO][  3].d[  4] =        -1.428868812264;
              BAS[ATNO][  3].a[  5] =         0.089890000000;     BAS[ATNO][  3].d[  5] =         0.493705805382;
            
              // Basis function   5 L = p
              InitBFNGauss(BAS[ATNO][  4]);
              BAS[ATNO][  4].l  = 1;
              BAS[ATNO][  4].ng = 2;
              BAS[ATNO][  4].a[  0] =         1.407000000000;     BAS[ATNO][  4].d[  0] =        -0.093234487709;
              BAS[ATNO][  4].a[  1] =         0.388000000000;     BAS[ATNO][  4].d[  1] =         1.054625569916;
            
              // Basis function   6 L = p
              InitBFNGauss(BAS[ATNO][  5]);
              BAS[ATNO][  5].l  = 1;
              BAS[ATNO][  5].ng = 2;
              BAS[ATNO][  5].a[  0] =         1.407000000000;     BAS[ATNO][  5].d[  0] =         1.264659250317;
              BAS[ATNO][  5].a[  1] =         0.388000000000;     BAS[ATNO][  5].d[  1] =        -0.704145294942;
            
              // Basis function   7 L = d
              InitBFNGauss(BAS[ATNO][  6]);
              BAS[ATNO][  6].l  = 2;
              BAS[ATNO][  6].ng = 1;
              BAS[ATNO][  6].a[  0] =         1.057000000000;     BAS[ATNO][  6].d[  0] =         1.000000000000;
            
            -------------------------------------------
            RADIAL EXPECTATION VALUES <R**-3> TO <R**3>
            -------------------------------------------
               0 :     0.000000     1.994557     0.999890     1.499668     2.996607     7.471837
               1 :     0.000000     0.711624     0.464740     3.394066    13.331135    56.232206
               2 :     0.000000     2.745396     1.087644     1.803319     4.998421    17.970166
               3 :     0.000000    23.310482     3.174581     0.782759     1.370496     4.014322
               4 :     0.384042     0.446994     0.626133     1.771589     3.422531     7.125124
               5 :     0.384042     0.446994     0.626133     1.771589     3.422531     7.125124
               6 :     0.384042     0.446994     0.626133     1.771589     3.422531     7.125124
               7 :     3.953007     1.946340     1.243023     1.051401     1.492933     2.747560
               8 :     3.953007     1.946340     1.243023     1.051401     1.492933     2.747560
               9 :     3.953007     1.946340     1.243023     1.051401     1.492933     2.747560
              10 :     0.924871     0.845600     0.874996     1.241717     1.655629    11.747557
              11 :     0.924871     0.845600     0.874996     1.241717     1.655629    11.747557
              12 :     0.924871     0.845600     0.874996     1.241717     1.655629    11.747557
              13 :     0.924871     0.845600     0.874996     1.241717     1.655629    11.747557
              14 :     0.924871     0.845600     0.874996     1.241717     1.655629    11.747557
            -------
            TIMINGS
            -------
            
            Total SCF time: 0 days 0 hours 0 min 1 sec 
            
            Total time                  ....       1.122 sec
            Sum of individual times     ....       0.890 sec  ( 79.3%)
            
            Fock matrix formation       ....       0.780 sec  ( 69.5%)
            Diagonalization             ....       0.001 sec  (  0.1%)
            Density matrix formation    ....       0.000 sec  (  0.0%)
            Population analysis         ....       0.001 sec  (  0.1%)
            Initial guess               ....       0.100 sec  (  8.9%)
            Orbital Transformation      ....       0.000 sec  (  0.0%)
            Orbital Orthonormalization  ....       0.000 sec  (  0.0%)
            DIIS solution               ....       0.001 sec  (  0.1%)
            
            -------------------------   --------------------
            FINAL SINGLE POINT ENERGY        -0.499945568587
            -------------------------   --------------------
            
            
                                        ***************************************
                                        *     ORCA property calculations      *
                                        ***************************************
            
                                                ---------------------
                                                Active property flags
                                                ---------------------
               (+) Dipole Moment
            
            
            ------------------------------------------------------------------------------
                                   ORCA ELECTRIC PROPERTIES CALCULATION
            ------------------------------------------------------------------------------
            
            Dipole Moment Calculation                       ... on
            Quadrupole Moment Calculation                   ... off
            Polarizability Calculation                      ... off
            GBWName                                         ... input.gbw
            Electron density file                           ... input.scfp
            The origin for moment calculation is the CENTER OF MASS  = ( 0.000000,  0.000000  0.000000)
            
            -------------
            DIPOLE MOMENT
            -------------
                                            X             Y             Z
            Electronic contribution:      0.00000       0.00000      -0.00000
            Nuclear contribution   :      0.00000       0.00000       0.00000
                                    -----------------------------------------
            Total Dipole Moment    :      0.00000       0.00000      -0.00000
                                    -----------------------------------------
            Magnitude (a.u.)       :      0.00000
            Magnitude (Debye)      :      0.00000
            
            
            
            --------------------
            Rotational spectrum 
            --------------------
             
            Rotational constants in cm-1:     0.000000     0.000000     0.000000 
            Rotational constants in MHz :     0.000000     0.000000     0.000000 
            
             Dipole components along the rotational axes: 
            x,y,z [a.u.] :     0.000000     0.000000    -0.000000 
            x,y,z [Debye]:     0.000000     0.000000    -0.000000 
            
             
            
            Timings for individual modules:
            
            Sum of individual times         ...        1.382 sec (=   0.023 min)
            GTO integral calculation        ...        0.228 sec (=   0.004 min)  16.5 %
            SCF iterations                  ...        1.154 sec (=   0.019 min)  83.5 %
                                         ****ORCA TERMINATED NORMALLY****
            TOTAL RUN TIME: 0 days 0 hours 0 minutes 1 seconds 534 msec
