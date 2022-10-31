# Chapter Two - Compiling & running

Compile languages takes time to compile, same applay for C. Cython can be applied to selectivly small sections of python. Thus compilatoin requirement can be minimized.

Cython code can be compile and used in the following options: 
- can be compiled and runned by IPython interpreter.
- can be compiled autoimaticly at import time.
- can be spertely compiled by build tools(distutils).
- can be integrated into std build(CMake).



### Pipline:
Cython code is first compiled into (optimize,platform-independent) C/C++ code and then recompiled into shared library with C/C++ compiler.
**First Step:** Cython Package has cythonize command, which takes cython file and compiled it into C/C++ Code.
<br/>
**Second Step:** Python distutils can compile C source into an extension moudle.
<br/>

sdsd



