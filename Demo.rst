.. _G4MP2-Demo:

Demo
====

.. currentmodule:: G4MP2

.. code-block:: text


Libraries and Machine Details
-----------------------------

.. code-block:: text

   openmpi_dir ="/apps/openmpi-3.0.0_install/"
   orca_dir ="/home/project_g4mp2_2019/ORCA_4_2/orca_4_2_0_linux_x86-64_openmpi314/"
   install_dir ="/apps/orca_g4mp2/"
  
   maxcore_mb = 32000
   nproc = 1

Geometry Optimization
---------------------

.. code-block:: text

   method_opt_freq = "B3LYP/G "
   basis_opt_freq = "GTBAS3"
   custombasis_opt_freq = .true.
  
   String_Opt = "TightOpt"
  
   MGGA = .false.
  
   FROZEN_GEOM = .false.

CCSD(T) Energy Determination
----------------------------

.. code-block:: text
  
   method_ccsdt = "CCSD(T) "
   basis_ccsdt = "GTBAS1"
   custombasis_ccsdt = .true.
   DLPNO_CCSDT = .false.
   switch_RIMP2_small=.false.
  
   switch_read_RIMP2_small = .false.
  
   method_mp2_s = "MP2 "
   basis_mp2_s = "GTBAS1"
   custombasis_mp2_s = .true.

MP2 Energy Determination
------------------------

.. code-block:: text

   method_mp2 = "MP2 "
   basis_mp2 = "GTMP2largeXP"
   custombasis_mp2 = .true.
   flag_RIMP2 = .false.
   flag_DLPNOMP2 = .false.

HF Energies Determination
-------------------------

.. code-block:: text

   method_hf3 = "HF "
   basis_hf3 = "GFHFB3"
   custombasis_hf3 = .true.
  
   method_hf4 = "HF "
   basis_hf4 = "GFHFB4"
   custombasis_hf4 = .true.

Thermochemical Property Determination
-------------------------------------

.. code-block:: text

   scalfac = 0.9854
  
   calc_IP = .false.
   verticalIP = .false.
  
   calc_EA = .false.
   verticalEA = .false.
  
   calc_PA = .false.
  
   calc_AE = .false.
  
   calc_BE = .false.
  
   calc_HF = .false.

Additional Details
------------------

.. code-block:: text

   conv_scf = "VeryTight"
  
   HLCeqZERO = .false.
  
   SOSCF    = .false.
   SCFDIIS  = .false.
  
   SO_3rdrow_mols = .true.
  
   LSHIFT  = .false.
  
   optdiis = .false.
  
   HF_CBS_default      = .true.
   HF_CBS_orca_23_def2 = .false.
   HF_CBS_orca_34_def2 = .false.
   HF_CBS_orca_23_cc   = .false.
   HF_CBS_orca_34_cc   = .false.
  
   restart_cc = .false.
   restart_mp2 = .false.
   restart_hf3 = .false.
   restart_hf4 = .false.

