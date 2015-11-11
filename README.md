# Fast Artificial Neural Network Library
## FANN

**Fast Artificial Neural Network (FANN) Library** is a free open source neural network library, which implements multilayer artificial neural networks in C with support for both fully connected and sparsely connected networks.

Cross-platform execution in both fixed and floating point are supported. It includes a framework for easy handling of training data sets. It is easy to use, versatile, well documented, and fast. 

Bindings to more than 15 programming languages are available. 

An easy to read introduction article and a reference manual accompanies the library with examples and recommendations on how to use the library. 

Several graphical user interfaces are also available for the library.

## FANN Features

* Multilayer Artificial Neural Network Library in C
* Backpropagation training (RPROP, Quickprop, Batch, Incremental)
* Evolving topology training which dynamically builds and trains the ANN (Cascade2)
* Easy to use (create, train and run an ANN with just three function calls)
* Fast (up to 150 times faster execution than other libraries)
* Versatile (possible to adjust many parameters and features on-the-fly)
* Well documented (An easy to read introduction article, a thorough reference manual, and a 50+ page university report describing the implementation considerations etc.)
* Cross-platform (configure script for linux and unix, dll files for windows, project files for MSVC++ and Borland compilers are also reported to work)
* Several different activation functions implemented (including stepwise linear functions for that extra bit of speed)
* Easy to save and load entire ANNs
* Several easy to use examples
* Can use both floating point and fixed point numbers (actually both float, double and int are available)
* Cache optimized (for that extra bit of speed)
* Open source, but can still be used in commercial applications (licenced under LGPL)
* Framework for easy handling of training data sets
* Graphical Interfaces
* Language Bindings to a large number of different programming languages
* Widely used (approximately 100 downloads a day)

## To Install

### On Linux

#### From Source

First you'll want to clone the repository:

`git clone https://github.com/libfann/fann.git`

Once that's finished, navigate to the Root directory. In this case it would be ./fann:

`cd ./fann`

Then run CMake

`cmake .`

After that, you'll need to use elevated priviledges to install the library:

`sudo make install`

That's it! If everything went right, you should see a lot of text, and FANN should be installed!

## To Learn More

To get started with FANN, go to the [FANN help site](http://leenissen.dk/fann/wp/help/), which will include links to all the available resources. 

For more information about FANN, please refer to the [FANN website](http://leenissen.dk/fann/wp/)

## This Fork:

Ex. 

```shell
$ cd fann/
$ ls
biicode.conf  bin  cmake  CMakeLists.txt  datasets  docs  examples  ignore.bii  lib  LICENSE.md  README.md  src  tests  VS2010
$ gedit README.md 
$ cmake .
-- The C compiler identification is GNU 4.8.1
-- The CXX compiler identification is GNU 4.8.1
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- FANN is used as APPLICATION_NAME
-- Try OpenMP C flag = [-fopenmp]
-- Performing Test OpenMP_FLAG_DETECTED
-- Performing Test OpenMP_FLAG_DETECTED - Success
-- Try OpenMP CXX flag = [-fopenmp]
-- Performing Test OpenMP_FLAG_DETECTED
-- Performing Test OpenMP_FLAG_DETECTED - Success
-- Found OpenMP: -fopenmp  
-- Found PythonInterp: /home/cobalt/anaconda3/bin/python (found version "3.4.3") 
-- Looking for include file pthread.h
-- Looking for include file pthread.h - found
-- Looking for pthread_create
-- Looking for pthread_create - not found
-- Looking for pthread_create in pthreads
-- Looking for pthread_create in pthreads - not found
-- Looking for pthread_create in pthread
-- Looking for pthread_create in pthread - found
-- Found Threads: TRUE  
-- Performing Test COMPILER_SUPPORTS_CXX14
-- Performing Test COMPILER_SUPPORTS_CXX14 - Success
-- Performing Test COMPILER_SUPPORTS_CXX11
-- Performing Test COMPILER_SUPPORTS_CXX11 - Success
-- Performing Test COMPILER_SUPPORTS_CXX0X
-- Performing Test COMPILER_SUPPORTS_CXX0X - Success
-- The compiler /usr/bin/c++ has C++14 support.
-- Configuring done
-- Generating done
-- Build files have been written to: /home/cobalt/repos/fann
```

Install:

```shell
$ sudo make install
[ 15%] Built target doublefann
[ 30%] Built target fann
[ 38%] Built target fixedfann
[ 53%] Built target floatfann
[ 61%] Built target gtest
[ 69%] Built target gtest_main
Scanning dependencies of target fann_tests
[ 76%] Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o
Linking CXX executable fann_tests
[100%] Built target fann_tests
Install the project...
-- Install configuration: "Release"
-- Installing: /usr/local/lib/pkgconfig/fann.pc
-- Installing: /usr/local/lib/cmake/fann/fann-config.cmake
-- Installing: /usr/local/lib/cmake/fann/fann-use.cmake
-- Installing: /usr/local/lib/libfloatfann.so.2.2.0
-- Installing: /usr/local/lib/libfloatfann.so.2
-- Installing: /usr/local/lib/libfloatfann.so
-- Installing: /usr/local/lib/libdoublefann.so.2.2.0
-- Installing: /usr/local/lib/libdoublefann.so.2
-- Installing: /usr/local/lib/libdoublefann.so
-- Installing: /usr/local/lib/libfixedfann.so.2.2.0
-- Installing: /usr/local/lib/libfixedfann.so.2
-- Installing: /usr/local/lib/libfixedfann.so
-- Installing: /usr/local/lib/libfann.so.2.2.0
-- Installing: /usr/local/lib/libfann.so.2
-- Installing: /usr/local/lib/libfann.so
-- Installing: /usr/local/include/fann.h
-- Installing: /usr/local/include/doublefann.h
-- Installing: /usr/local/include/fann_internal.h
-- Installing: /usr/local/include/floatfann.h
-- Installing: /usr/local/include/fann_data.h
-- Installing: /usr/local/include/fixedfann.h
-- Installing: /usr/local/include/fann_activation.h
-- Installing: /usr/local/include/fann_cascade.h
-- Installing: /usr/local/include/fann_error.h
-- Installing: /usr/local/include/fann_train.h
-- Installing: /usr/local/include/fann_io.h
-- Installing: /usr/local/include/fann_cpp.h
-- Installing: /usr/local/include/fann_data_cpp.h
-- Installing: /usr/local/include/fann_training_data_cpp.h
-- Installing: /usr/local/include/parallel_fann.h
-- Installing: /usr/local/include/parallel_fann.hpp
```
