# Build 

Execute commands below or script `make.sh`.

```shell
rm -rf build
mkdir build
cd build
cmake ..
make
make install
```
The command `make install` is equal to `make; make install`.

CMake logs as below:

```shell
root@a5165728184a:/home/yuanshuai/code/build-101/cmake/t3_hello_world# ./make.sh
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
-- DESTINATION: 
-- install FILES: COPYRIGHT README.md to /share/doc/cmake/t3
-- install PROGRAMS: run_hello.sh to /bin
-- install DIRECTORY: doc/ to /share/doc/cmake/t3
-- Configuring done
-- Generating done
-- Build files have been written to: /home/yuanshuai/code/build-101/cmake/t3_hello_world/build
Scanning dependencies of target hello
[ 50%] Building C object bin/CMakeFiles/hello.dir/main.c.o
[100%] Linking C executable hello
[100%] Built target hello
[100%] Built target hello
Install the project...
-- Install configuration: ""
-- Up-to-date: /usr/local/share/doc/cmake_t3/COPYRIGHT
-- Installing: /usr/local/share/doc/cmake_t3/README.md
-- Up-to-date: /usr/local/bin/run_hello.sh
-- Up-to-date: /usr/local/share/doc/cmake_t3
-- Up-to-date: /usr/local/share/doc/cmake_t3/hello.txt
-- Installing: /usr/local/bin/hello
```

Run binary executable file using command below or script `./run_hello_from_source.sh`:

```shell
./build/bin/hello
```

After `make install` executed, you can execute `hello` or `run_hello.sh` everywhere if you execute `cmake .. -DCMAKE_INSTALL_PATH=/usr`.
