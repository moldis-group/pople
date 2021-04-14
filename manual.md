---
layout: default
---

# Content:
1 [Basic input options](#1-basic-input-options)  

2 [Advanced input options](#2-advanced-input-options)

   

## 1 Basic input options

Every calculation requires four essential input arguments for the input keywords  `code`, `code_exe`, `method`, and `xyz`. 

These inputs are processed by the 'calculator' function of the pople code as arbitray keyword arguments (\*\*kwargs)[https://www.w3schools.com/python/gloss_python_function_arbitrary_keyword_arguments.asp].


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
>\```
>`method='g4mp2-xp'` 
>```
    
Keyword: `xyz`   
>Argument (string): Name of the geometry block
>Usage: 
>```
>geom=```
>0   1
>O      0.0         0.0      0.0
>H      0.96854     0.0      0.0
>H     -0.22812     0.0     -0.94129
>```
>
>xyz=geom
>```

    if 'xyz' in kwargs:
        geom=kwargs['xyz']
    if 'nproc' in kwargs:
        nproc=kwargs['nproc']
    if 'mem_mb' in kwargs:
        mem_mb=kwargs['mem_mb']
        
    if 'frozengeom' in kwargs:
        frozengeom=kwargs['frozengeom']

    if frozengeom == 'true':
        if 'freqcmi' in kwargs:
            freq=kwargs['freqcmi']

RAM memory per core in megabytes, 1024 stands for 1 GB. The value has to be an integer.


## 2 Advanced input options
>> Coming soon.
