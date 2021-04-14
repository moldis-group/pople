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
 Argument:  presently, `orca` is the only allowed argument   
 Usage: `code='pople'`   

    
    
For other possible keywords (and their arguments) that can be provided to 'calculator', 
    if 'code' in kwargs:
        code=kwargs['code']
    if 'code_exe' in kwargs:
        code_exe=kwargs['code_exe']
    if 'method' in kwargs:
        method=kwargs['method']
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
