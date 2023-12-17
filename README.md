# Introduce
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
## Choices of Solving
After a brief summary of the problem and solving method, in this section I will discuss about why I choose them.
- **Integer format**: 
The string library is a widely used built-in library in both Python and C++, making looping through strings a highly efficient process, and optimizing memory usage by using a string instead of an int or char array is much better (Python Array version will show this result). From this, it can be inferred that using string conversion will yield much better results than using arrays or binary conversion.
- **Arithmetic and comparison operations definition**: Converting integers to binary form can lead to numerous complications, and converting extremely large binary numbers can be a time-intensive process without the use of pre-existing libraries. Additionally, pre-existing libraries are often unable to handle binary numbers larger than 264. As a result, the binary conversion method is not utilized.
- **Determining primality**: 
The main reason for abstaining from the brute force method (i.e. looping until the square root of the number) is its excessive time consumption. Consequently, we are compelled to rely on primality test techniques. Although these methods may still exhibit some degree of error, the magnitude of such errors is negligible, thereby rendering the resulting solutions still acceptable. For instance, the Miller-Rabin method that i implement entails an error rate < = ~ 0.097%.

To sum up, the utilization of multiprocessing in Primality testing has significantly improved the speed of reality, using directly store. The speed is still considerably even with the implementation of vector<long long> to store each element with nine digits per element.

# Results
![image](https://github.com/ChiTrug/Calculator-for-Large-Numerical-Values/assets/125122891/e2eb1f7d-797a-49d8-9625-817afb76fd27)

Will be updated soon

# References
Miller rabin test:
- https://en.wikipedia.org/wiki/Miller%E2%80%93Rabin_primality_test
- https://www.geeksforgeeks.org/primality-test-set-3-miller-rabin/
- https://www.codeproject.com/Articles/60108/BigInteger-Library-2
BigInt: 
- https://www.geeksforgeeks.org/bigint-big-integers-in-c-with-example/
- https://github.com/WHU-Cryptography/BigInteger

Modular exponentiation:
- https://en.wikipedia.org/wiki/Modular_exponentiation
- https://homepages.math.uic.edu/~leon/cs-mcs401-s08/handouts/fastexp.pdf
