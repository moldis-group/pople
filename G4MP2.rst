.. Automated NFS-G4(MP2) documentation.

==================
   NFS-G4(MP2) 
==================

The Original G4(MP2) protocol is inherent to Gaussian software package. This remodelled code runs the normal G4(MP2) protocol using ORCA suite of package along with the devised NFS-G4(MP2) protocols for high speed-accuracy trade-off. The script also provide the opportunity to the user to explore the affects of selection of Theory/Basis-set combination in the composite model and its overall affect on the prediction of the Thermochemical properties.

Current version is |release|.

.. _GitHub: https://github.com/Sambit1994/FAcT.github.io/


Key Features
============

- Prediction of user defined Thermochemical properties including, Enthalpy of Formation, Ionization Potential, Atomization Energy, Electron Affinity, Proton Affinity and Binding Energy.

- User defined Theory-Basis set combination at various levels.

- Geometry optimization free Energy calculation.

- HLC free Energy calculation.

Script/Dependent-libraries Installations
========================================

Installing running Script
-------------------------

.. code-block:: bash

   $ pip install ----

----statement----

.. code-block:: bash

   $ pip install -----

----statement----

Installing dependent libraries
------------------------------

.. code-block:: bash

   $ pip install ----

----statement----

Running The Script
==================

Input Files
-----------

The script requires the following files to run and generate the required thermochemical properties. 

- ``geom.xyz``: The cartesian coordinates (Angstrom unit) of the molecule along with information about the total no. of atoms, charge and multiplicity. One such example for methane molecule is given below.

.. code-block:: text

             5 [Total no. of atoms]
             0           1 [charge and multiplicity]
    C        0.00000000     0.00000000     0.00000000 [Cartesian Coordinates] 
    H        1.09336000     0.00000000     0.00000000
    H       -0.36445000     0.00000000    -1.03083000
    H       -0.36445000    -0.97188000     0.34361000
    H       -0.36445000     0.97188000     0.34361000

- ``orca_g4mp2.inp``: This input file contains the technical details for the various steps involved in the composite procedure. One such example for running the normal G4(MP2) protocol is :ref:`G4MP2-inp`. It also allows the user to manipulate the settings as per their choice. For detailed information, please go to the tutorial section.

- ``read_geom_freq.dat``: The user can choose to determine the G4(MP2) energy on a pre-optimized geometry. In that case, they have to provide this input file along with the above two, contating information regarding the optimzed geometry and vibrational frequencies. To be noted, all vibrational frequencies must be included to run the script, i.e., 3N-5 for linear systems and 3N-6 for non-linear systems. One such example for pre-optimized methane molecule is given below:

.. code-block:: text

             5 [Total no. of atoms]
   Optimized atomic coordinates (Angstrom) [Title line]
         C     -0.00000123    -0.00000000    -0.00000079 [Optimized geometry coordinates]
         H      0.68957985     0.00051101    -0.84657788
         H     -1.02803745     0.00063322    -0.36792717
         H      0.16896006    -0.89208896     0.60649423
         H      0.16951220     0.89094474     0.60802020
  1343.36 [Vibrational frequencies at the optimized geometry]
  1343.36
  1343.38
  1564.11
  1564.17
  3042.96
  3156.57
  3156.61
  3156.67

Output Files
------------

The script produces three output files, ``ORCA_G4MP2.com``, ``ORCA_G4MP2.out``, and ``Thermochemistry.out``. The ``ORCA_G4MP2.com`` file compiles all the ORCA input files created by the script on-the-fly --- for the various steps involved in the composite procedure. Similarly, the output files generated from these corresponding input files are collected in ``ORCA_G4MP2.out``. The ``Thermochemistry.out`` file collects all the required energies and energy corrections involved in the G4(MP2) protocol along with the predicted value of the thermochemical property asked by the user. One such output files genrerated for methane molecule is given here. :ref:`G4MP2-com`, :ref:`G4MP2-out`, and :ref:`G4MP2-Thermo`. 

Tutorial
========

Please see :ref:`G4MP2-Demo` for the details information regarding ``orca_g4mp2.inp``


Source code
===========

The project is hosted on GitHub_

Please feel free to file an issue on the `bug tracker
<https://github.com/>`_ if you have found a bug
or have some suggestion in order to improve the library.

Dependencies
============

Communication channels
======================

Contributing
============

