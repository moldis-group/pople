
## Manual

#### Input file structure
```
#=== Method and job ==================================================
method_type = ...
job_type    = ...

#=== first geometry, neutral =========================================
geom_1
...

end_geom

#=== second geometry, cation =========================================
geom_2
...

end_geom

#=== memory and processors ===========================================
maxcore_mb  = ...
nproc       = ...

#=== Paths ===========================================================
openmpi_dir = ...
orca_dir    = ...
```
#### Dependencies
```
numpy
```
