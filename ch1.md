# Chapter One - Cython Essentials

There is advantage and disadvantage for C compare to Python. Cython is trying to create a middle ground between both of thoes. 
So How Cython achieve this? 


By creating a simple programming language that blends Python with the static type system
of C / C++. Cython compile into a Python extension module or a standalone executable.


## Cython Vs C extension Vs Pure C:

#### C extension: 
Include dozen of C code (boilerplate), which call Python/C API. The moudle (extension) convert python object to into C data , compute the result and return its by converting back to python object. This process convert and convert back result an overhead time compared to pure c code.

#### Cython:
Similarly cython code compile and translate cython code into C extension moudle. So evrey code created by cython can be created by C extension as well. 
However, Cython is more limited than writing extension by hand.

