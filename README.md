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

## This Fork (modified by mkc):

## Build

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

### Install:

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


### Possible Installation error:

```shell
[root@cobalt fann]# cmake . -DCMAKE_CXX_COMPILER=/usr/local/bin/g++ -DCMAKE_CC_COMPILER=/usr/local/bin/gcc
-- FANN is used as APPLICATION_NAME
-- The compiler /usr/local/bin/g++ has C++14 support.
-- Configuring done
You have changed variables that require your cache to be deleted.
Configure will be re-run and you may have to reset some variables.
The following variables have changed:
CMAKE_CXX_COMPILER= /usr/local/bin/g++

-- The C compiler identification is GNU 4.9.3
-- The CXX compiler identification is GNU 4.9.3
-- Check for working C compiler: /usr/local/bin/gcc
-- Check for working C compiler: /usr/local/bin/gcc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working CXX compiler: /usr/local/bin/g++
-- Check for working CXX compiler: /usr/local/bin/g++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- FANN is used as APPLICATION_NAME
-- Try OpenMP C flag = [-fopenmp]
-- Performing Test OpenMP_FLAG_DETECTED
-- Performing Test OpenMP_FLAG_DETECTED - Success
-- Try OpenMP CXX flag = [-fopenmp]
-- Performing Test OpenMP_FLAG_DETECTED
-- Performing Test OpenMP_FLAG_DETECTED - Success
-- Found OpenMP: -fopenmp  
-- Found PythonInterp: /root/anaconda/bin/python (found version "2.7.10") 
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
-- The compiler /usr/local/bin/g++ has C++14 support.
-- Configuring done
-- Generating done
CMake Warning:
  Manually-specified variables were not used by the project:

    CMAKE_CC_COMPILER


-- Build files have been written to: /home/cobalt/repos/fann
[root@cobalt fann]# make -j8
Scanning dependencies of target fann
Scanning dependencies of target fixedfann
[ 15%] [ 15%] [ 38%] [ 38%] [ 38%] [ 46%] [ 53%] [ 61%] Building C object src/CMakeFiles/doublefann.dir/doublefann.c.o
Building CXX object src/CMakeFiles/doublefann.dir/parallel_doublefann_cpp.cpp.o
Building C object src/CMakeFiles/floatfann.dir/floatfann.c.o
Building CXX object src/CMakeFiles/fann.dir/parallel_floatfann_cpp.cpp.o
Building C object src/CMakeFiles/fann.dir/floatfann.c.o
Building CXX object src/CMakeFiles/floatfann.dir/parallel_floatfann_cpp.cpp.o
Building C object src/CMakeFiles/fixedfann.dir/fixedfann.c.o
Building CXX object lib/googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
Linking C shared library libfixedfann.so
[ 61%] Built target fixedfann
Linking CXX shared library libdoublefann.so
[ 61%] Built target doublefann
Linking CXX shared library libfann.so
Linking CXX shared library libfloatfann.so
[ 61%] Built target fann
[ 61%] Built target floatfann
Linking CXX shared library libgtest.so
[ 61%] Built target gtest
[ 69%] [ 76%] [ 84%] [ 92%] [100%] Building CXX object tests/CMakeFiles/fann_tests.dir/main.cpp.o
Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test.cpp.o
Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o
Building CXX object lib/googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test_data.cpp.o
Linking CXX shared library libgtest_main.so
[100%] Built target gtest_main
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateStandardThreeLayers_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:64:67: error: taking address of temporary array
     AssertCreateAndCopy(net, 3, (unsigned int[]) {2, 3, 4}, 11, 25);
                                                                   ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp: In member function ‘virtual void FannTestTrain_TrainSimpleIncrementalXor_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test_train.cpp:28:64: error: taking address of temporary array
         net.train((fann_type[]) {0.0, 0.0}, (fann_type[]) {0.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:29:64: error: taking address of temporary array
         net.train((fann_type[]) {1.0, 0.0}, (fann_type[]) {1.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:30:64: error: taking address of temporary array
         net.train((fann_type[]) {0.0, 1.0}, (fann_type[]) {1.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:31:64: error: taking address of temporary array
         net.train((fann_type[]) {1.0, 1.0}, (fann_type[]) {0.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateSparseFourLayers_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:93:69: error: taking address of temporary array
     AssertCreateAndCopy(net, 4, (unsigned int[]){2, 3, 4, 5}, 17, 31);
                                                                     ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateSparseFourLayersUsingCreateMethod_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:98:69: error: taking address of temporary array
     AssertCreateAndCopy(net, 4, (unsigned int[]){2, 3, 4, 5}, 17, 31);
                                                                     ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateShortcutFourLayers_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:121:69: error: taking address of temporary array
     AssertCreateAndCopy(net, 4, (unsigned int[]){2, 3, 4, 5}, 15, 83);
                                                                     ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateShortcutFourLayersUsingCreateMethod_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:127:69: error: taking address of temporary array
     AssertCreateAndCopy(net, 4, (unsigned int[]){2, 3, 4, 5}, 15, 83);
                                                                     ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateFromFile_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:151:76: error: taking address of temporary array
     AssertCreateAndCopy(netToBeLoaded, 3, (unsigned int[]){2, 3, 4}, 11, 25);
                                                                            ^
/home/cobalt/repos/fann/tests/fann_test.cpp: In member function ‘virtual void FannTest_CreateFromFileUsingCreateMethod_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test.cpp:161:66: error: taking address of temporary array
     AssertCreateAndCopy(net, 3, (unsigned int[]){2, 3, 4}, 11, 25);
                                                                  ^
make[2]: *** [tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o] Error 1
make[2]: *** Waiting for unfinished jobs....
make[2]: *** [tests/CMakeFiles/fann_tests.dir/fann_test.cpp.o] Error 1
make[1]: *** [tests/CMakeFiles/fann_tests.dir/all] Error 2
make: *** [all] Error 2
```

### Work-around:

Modify '(unsigned int[]){2, 3, 4}' into '(const unsigned int[]){2, 3, 4}'

Ex.
```cpp
 AssertCreateAndCopy(net, 3, (const unsigned int[]){2, 3, 4}, 11, 25);
```

### Next error:
```cpp
[root@cobalt fann]# make -j8
[ 15%] [ 30%] [ 38%] Built target fann
[ 53%] Built target doublefann
Built target fixedfann
Built target floatfann
[ 61%] Built target gtest
Scanning dependencies of target fann_tests
[ 69%] Built target gtest_main
[ 84%] [ 84%] Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test.cpp.o
Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o
/home/cobalt/repos/fann/tests/fann_test_train.cpp: In member function ‘virtual void FannTestTrain_TrainSimpleIncrementalXor_Test::TestBody()’:
/home/cobalt/repos/fann/tests/fann_test_train.cpp:28:64: error: taking address of temporary array
         net.train((fann_type[]) {0.0, 0.0}, (fann_type[]) {0.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:29:64: error: taking address of temporary array
         net.train((fann_type[]) {1.0, 0.0}, (fann_type[]) {1.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:30:64: error: taking address of temporary array
         net.train((fann_type[]) {0.0, 1.0}, (fann_type[]) {1.0});
                                                                ^
/home/cobalt/repos/fann/tests/fann_test_train.cpp:31:64: error: taking address of temporary array
         net.train((fann_type[]) {1.0, 1.0}, (fann_type[]) {0.0});
                                                                ^
make[2]: *** [tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o] Error 1
make[2]: *** Waiting for unfinished jobs....
make[1]: *** [tests/CMakeFiles/fann_tests.dir/all] Error 2
make: *** [all] Error 2
[root@cobalt fann]# 
```

### Ugly hack: 

In 'fann/tests/fann_test_train.cpp'

```cpp
for(int i = 0; i < 100000; i++) {
        net.train((fann_type*)(const fann_type[]) {0.0, 0.0}, (fann_type*)(const fann_type[]) {0.0});
        net.train((fann_type*)(const fann_type[]) {1.0, 0.0}, (fann_type*)(const fann_type[]) {1.0});
        net.train((fann_type*)(const fann_type[]) {0.0, 1.0}, (fann_type*)(const fann_type[]){1.0});
        net.train((fann_type*)(const fann_type[]) {1.0, 1.0}, (fann_type*)(const fann_type[]){0.0});
    }
```
TODO: look for a better solution...

### Final Successful Install:

```shell
[root@cobalt fann]# make j8
make: *** No rule to make target `j8'.  Stop.
[root@cobalt fann]# make -j8
[  7%] [ 15%] [ 30%] Built target fixedfann
Built target gtest
[ 46%] Built target doublefann
Built target floatfann
[ 61%] Built target fann
Scanning dependencies of target fann_tests
[ 69%] Built target gtest_main
[ 76%] Building CXX object tests/CMakeFiles/fann_tests.dir/fann_test_train.cpp.o
Linking CXX executable fann_tests
[100%] Built target fann_tests

[root@cobalt fann]# ls
biicode.conf         CPackSourceConfig.cmake    lib
bin                  datasets                   LICENSE.md
cmake                docs                       Makefile
CMakeCache.txt       examples                   README.md
CMakeFiles           fann-config.cmake          src
cmake_install.cmake  fann_doc_complete_1.0.pdf  tests
CMakeLists.txt       fann.pc                    VS2010
CPackConfig.cmake    ignore.bii
```

```shell
[root@cobalt fann]# make install
[ 15%] Built target doublefann
[ 30%] Built target fann
[ 38%] Built target fixedfann
[ 53%] Built target floatfann
[ 61%] Built target gtest
[ 69%] Built target gtest_main
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
[root@cobalt fann]# 
```



### XOR Sample Train:

```shell
$ ls
cascade_train.c  momentums.c  parallel_train.c  scaling_test.c   simple_test.c   steepness_train.c  xor_sample.cpp  xor_test.c
Makefile         mushroom.c   robot.c           scaling_train.c  simple_train.c  xor.data           xor_test        xor_train.c

$ g++ xor_train.c -o xor_train -lfann -lm

$ ls
cascade_train.c  momentums.c  parallel_train.c  scaling_test.c   simple_test.c   steepness_train.c  xor_sample.cpp  xor_test.c  xor_train.c
Makefile         mushroom.c   robot.c           scaling_train.c  simple_train.c  xor.data           xor_test        xor_train

$ cat xor.data
4 2 1
-1 -1
-1
-1 1
1
1 -1
1
1 1
-1

$ ./xor_train xor.data 
Creating network.
Training network.
Max epochs     1000. Desired error: 0.0000000000.
Epochs            1. Current error: 0.2890214324. Bit fail 4.
Epochs           10. Current error: 0.1758149415. Bit fail 4.
Epochs           20. Current error: 0.0201370474. Bit fail 4.
Epochs           30. Current error: 0.0011721312. Bit fail 4.
Epochs           40. Current error: 0.0000835651. Bit fail 2.
Epochs           45. Current error: 0.0000196561. Bit fail 0.
Testing network. 0.000008
XOR test (-1.000000,-1.000000) -> -0.994789, should be -1.000000, difference=0.005211
XOR test (-1.000000,1.000000) -> 0.993131, should be 1.000000, difference=0.006869
XOR test (1.000000,-1.000000) -> 0.996434, should be 1.000000, difference=0.003566
XOR test (1.000000,1.000000) -> -0.993053, should be -1.000000, difference=0.006947
Saving network.
Cleaning up.


$ ls
cascade_train.c  mushroom.c        scaling_test.c   simple_train.c     xor_fixed.data  xor_sample.cpp  xor_train
Makefile         parallel_train.c  scaling_train.c  steepness_train.c  xor_fixed.net   xor_test        xor_train.c
momentums.c      robot.c           simple_test.c    xor.data           xor_float.net   xor_test.c
```

### Testing XOR:

```shell
$ g++ xor_test.c -o xor_test -lfann -lm
$ ./xor_test
Creating network.
Layer / Neuron 0123456
L   1 / N    3 lBa....
L   1 / N    4 Ccc....
L   1 / N    5 CCC....
L   1 / N    6 .......
L   2 / N    7 ...DDDA
L   2 / N    8 .......
Input layer                          :   2 neurons, 1 bias
  Hidden layer                       :   3 neurons, 1 bias
Output layer                         :   1 neurons
Total neurons and biases             :   8
Total connections                    :  13
Connection rate                      :   1.000
Network type                         :   FANN_NETTYPE_LAYER
Training algorithm                   :   FANN_TRAIN_RPROP
Training error function              :   FANN_ERRORFUNC_TANH
Training stop function               :   FANN_STOPFUNC_BIT
Bit fail limit                       :   0.010
Learning rate                        :   0.700
Learning momentum                    :   0.000
Quickprop decay                      :  -0.000100
Quickprop mu                         :   1.750
RPROP increase factor                :   1.200
RPROP decrease factor                :   0.500
RPROP delta min                      :   0.000
RPROP delta max                      :  50.000
Cascade output change fraction       :   0.010000
Cascade candidate change fraction    :   0.010000
Cascade output stagnation epochs     :  12
Cascade candidate stagnation epochs  :  12
Cascade max output epochs            : 150
Cascade min output epochs            :  50
Cascade max candidate epochs         : 150
Cascade min candidate epochs         :  50
Cascade weight multiplier            :   0.400
Cascade candidate limit              :1000.000
Cascade activation functions[0]      :   FANN_SIGMOID
Cascade activation functions[1]      :   FANN_SIGMOID_SYMMETRIC
Cascade activation functions[2]      :   FANN_GAUSSIAN
Cascade activation functions[3]      :   FANN_GAUSSIAN_SYMMETRIC
Cascade activation functions[4]      :   FANN_ELLIOT
Cascade activation functions[5]      :   FANN_ELLIOT_SYMMETRIC
Cascade activation functions[6]      :   FANN_SIN_SYMMETRIC
Cascade activation functions[7]      :   FANN_COS_SYMMETRIC
Cascade activation functions[8]      :   FANN_SIN
Cascade activation functions[9]      :   FANN_COS
Cascade activation steepnesses[0]    :   0.250
Cascade activation steepnesses[1]    :   0.500
Cascade activation steepnesses[2]    :   0.750
Cascade activation steepnesses[3]    :   1.000
Cascade candidate groups             :   2
Cascade no. of candidates            :  80
Testing network.
XOR test (-1.000000, -1.000000) -> -0.994789, should be -1.000000, difference=0.005211
XOR test (-1.000000, 1.000000) -> 0.993131, should be 1.000000, difference=0.006869
XOR test (1.000000, -1.000000) -> 0.996434, should be 1.000000, difference=0.003566
XOR test (1.000000, 1.000000) -> -0.993053, should be -1.000000, difference=0.006947
Cleaning up.
```
