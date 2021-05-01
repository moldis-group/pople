---
layout: default
---

# Content:
[1. Basic input](#basic_input)  
[2. Optional input](#optional_input)  
[3. Advanced input](#advanced_input)  

   

## <a name="basic_input">1. Basic input</a>

Every calculation requires four essential input arguments for the input keywords  `code`, `code_exe`, `method`, and `xyz`. 

These inputs are processed by the 'calculator' function of the pople code as arbitray keyword arguments ([\*\*kwargs](https://www.w3schools.com/python/gloss_python_function_arbitrary_keyword_arguments.asp)) .

These keywords and their arguments are provided to the 'calculator' function as 
```
pople.calculator(key1=arg1, key2=arg2, key3=arg3, key4=arg4)
```

Here is a specific example
```
from pople import calculator as calc
out = calc(code='orca', code_exe='/home/Lib/ORCA_420/orca', method='g4mp2', xyz=geom)
```

See also example-1 from [Tutorials](https://moldis-group.github.io/pople/tutorials.html#3-simple-calculation)


Keyword: `code`   
>Argument (string): presently, `'orca'` is the only allowed argument   
>Usage: 
>```  
>code='orca'  
>```     
 
Keyword: `code_exe`    
>Argument (string): Absolute path of the executable binary of the code    
>Usage-1:    
>```   
>code_exe='/home/Lib/ORCA_420/orca'   
>```   
> 
>Usage-2:    
>```   
>exe='/home/Lib/ORCA_420/orca'   
>code_exe=exe   
>```
    
Keyword: `method`    
>Argument (string): Pople (version-21.04.0) supports `'g4mp2'` and `'g4mp2-xp'` calculations   
>Usage:    
>```   
>method='g4mp2-xp'    
>```   
    
Keyword: `xyz`      
>Argument (string): Name of the geometry block. The geometry block collects the charge, multiplicity and Cartesian coodinates (in Angstroem) of the atom/molecule under consideration.      
>Usage:    
>```   
>geom='''  
>0   1   
>O      0.0         0.0      0.0   
>H      0.96854     0.0      0.0   
>H     -0.22812     0.0     -0.94129   
>'''   
>   
>xyz=geom   
>```    

* * *

## <a name="optional_input">2. Optional input</a>

Keyword: `nproc`      
>Argument (integer): Number of cpu-cores for a parallel calculation    
>Default: 1    
>Usage:    
>```   
>nproc=4    
>```   
Usage of this keyword assumes that the library variables are set properly. For example, these may be set on the terminal (or in a job script) as follows
```
export OMP_NUM_THREADS=1
export PATH=/apps/openmpi-3.0.0_install/bin:$PATH
export LD_LIBRARY_PATH=/apps/openmpi-3.0.0_install/lib:$LD_LIBRARY_PATH
```

Keyword: `mem_mb`     
>Argument (integer): RAM memory per core in megabytes   
>Default: 1000   
>Usage:   
>```    
>mem_mb=4000   
>```   

Keyword: `frozengeom`    
>Argument (string): `'true'` for a frozen-geometry calculation.   
>Usage:    
>```   
>frozengeom='true'    
>```    
If set to `'true'`, the keyword `'freqcmi'` [next keyword below] has to be provided to 'calculator' 
See the test job `test_003_enthalpy_H2_frozen_geom`
    
Keyword: `freqcmi`      
>Argument (string): Name of the frequency block  containing harmonic wavenumbers in cm^-1 
>Usage:    
>```   
>freq='''     
>1671.78  
>3808.42   
>3912.50   
>'''   
>   
>freqcmi=freq   
>```  
See the test job `test_003_enthalpy_H2_frozen_geom`

* * *

## <a name="advanced_input">3. Advanced input</a>
Coming soon

* * *

