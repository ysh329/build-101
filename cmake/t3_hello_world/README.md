# Build 

Execute commands below or script `make.sh`.

```shell
rm -rf build
mkdir build
cd build
cmake ..
make
```

CMake logs as below:

```shell
-- The C compiler identification is GNU 5.4.0
-- The CXX compiler identification is GNU 5.4.0
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
-- Configuring done
-- Generating done
-- Build files have been written to: /home/yuanshuai/code/build-101/cmake/t2_hello_world/build
Scanning dependencies of target hello
[ 50%] Building C object bin/CMakeFiles/hello.dir/main.c.o
[100%] Linking C executable hello
[100%] Built target hello
```

Run binary executable file using command below or script `./run_hello.sh`:

```shell
./build/bin/hello
```

`make install` == `make; make install`
