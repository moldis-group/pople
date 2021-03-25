
## Manual

### Basic Input file structure (pople.inp)
The simplest input file requires 6 keywords and one or two geometry blocks (Cartesian coordinates in Angstrom). 
* When job_type is 'HF' (heat of formation) or 'AE' (atomization energy), one geometry is required.
* When job_type is 'IP' (ionization energy), 'EA' (electron affinity), 'PA' (proton affinity) or 'BE' (binding energy), two geometries are required. 
* Examples for each job_type are given below

```
method_type = ...
job_type    = ...
geom_1
...

end_geom
maxcore_mb  = ...
nproc       = ...
openmpi_dir = ...
orca_dir    = ...
```
#### Dependencies
```
numpy
```
