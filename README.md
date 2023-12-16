This project - Calculator for Large Numerical Values - is OOP implemented in both Python and C++. The C++ version is the most comprehensive and is less prone to errors. Both versions operate in the same way and leverage the multiprocessing approach.

Python version utilizes the multiprocessing library, while C++ version uses pthread. You will need to install pthread, please follow the instructions in the following resource: https://www.youtube.com/watch?v=4GdTcqE0iqg.

# Python and C++ Library Choices
## Python Library:
- Numpy: This is a crucial library as one of the Python versions relies on Numpy extensively for its . library
- Numba: This library is designed for GPU . Even this project does not include the code using Numba because it's failed but I will talk about it a little bit.
- Multiprocessing: As the name , this library enables efficient multiprocessing on CPU, allowing us to take of the full potential of our hardware.
## C++ Library:
- String, Vector, Array, Algorithm, and more: These widely-used libraries are integral components of any C++ project, providing essential functionality and flexibility.
- Pthread: Similar to Python’s multiprocessing library, Pthread enables efficient CPU multiprocessing, allowing for optimal utilization of system resources.

# Problems and Choices of Solving Problems
## Problems:
The objective of this task is to construct a class called UIntN that can effectively represent unsigned integers of extremely large magnitude. This requires defining arithmetic and comparison operations that are optimized to handle large integers with speed and efficiency. In addition, a method must be implemented to determine the primality of a given UIntN. Optimize the data structure to prevent the program from slowing down with large numbers.
![image](https://github.com/ChiTrug/Calculator-for-Large-Numerical-Values/assets/125122891/8a6830a0-652c-400d-8a62-5b718abf9cfb)
Additional methods include utilizing binary form for computation and comparison, as well as implementing vector<int> or vector<char> in C++. Nevertheless, the outcomes produced were unsatisfactory, leading to the abandonment of these approaches.

Regarding the method for testing primality, it is planned to incorporate AKS and other enhanced techniques based on existing algorithms in the near future, in addition to the Miller-Rabin method, with the aim of achieving superior outcomes.
