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



## Python Slow? Why?


> "Python is an interpreted, high-level, general-purpose programming language. It is dynamically typed and garbage-collected"


### Interpreted & Dynamic:
- **Python is interpreted:**  Therefore, source file is being compiled into bytecode. Because python is dynamic we canot decide if action is legal before we seeing the actual value. In simple termes, Python convert the source code into byte code and uses the interpeter to convert the byte code into machine code to run on the cpu, while checking the integrity of the action.

- **Loops:**  Most compile languages can infer the number of iteration in the loop and unroll the loop for faster execution. Which canot be done in Interpreted languages.



### memory management
- **Garbage collection:**  Python keeps track of how many refrence there are for each object. If object refrence count is 0 then python conclude the varible isn't beeing use and can be deallocated.

- **Objects:**  Evrey Python varible is an PyObject. PyObject possessed memory address, typecode of the varible(integer,str,....), value (the value in the memeory address), refrence counter (talked above). On Assignment of used varible, new PyObject is created (insted of changing the value in the address like statictyped). Furthermore, when two PyObject are added(+) Python has to check the typed of both PyObject and search the right `__add__` function to call.

- **Immutable objects:** Python uses memory pools and internalizing frequently on float,int,string. Which increase the overhead time of creating and destroying objects. Operation on immutable (like adding two floats) involve creating and destroying PyObject(heap allocated memory)
