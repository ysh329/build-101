# CMake

## installation

First download and intall cmake [here](https://cmake.org/download/). 

I executed this process using a container of docker image ubuntu:16.04 as below:

```shell
# update package and install prebuild tools
$ apt update
$ apt install -y wget
$ apt-get install -y build-essential git

# download latest cmake from its website and unzip it
$ mkdir ~/download && cd ~/download
$ wget -c https://cmake.org/files/v3.11/cmake-3.11.3.tar.gz
$ tar -zxvf cmake-3.11.3.tar.gz

# install
$ mkdir ~/software 
$ mv cmake-3.11.3 ~/software/
$ cd ~/software/cmake-3.11.3

# build helper and choose installation directory
# default build to system directory
$ ./bootstrap --help

# build cmake
$ ./bootstrap --prefix=/root/software/cmake-3.11.3
make
```
Second, add `cmake` command to user's PATH: `~/.bashrc`.

```shell
# CMAKE
export CMAKE_HOME=/root/software/cmake
export PATH=$CMAKE_HOME/bin:$PATH
```
Last, check version of `cmake`:

```shell
$ cmake --version

cmake version 3.11.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

## Step by Step

### t1_hello_world

In-source compilation example.

Keypoint:
  
- PROJECT  
- SET
- MESSAGE
- ADD_EXECUTABLE

### t2_hello_world

Out-source compilation example.

Keypoint:

- CMAKE_MINIMUM_REQUIRED
- ADD_SUBDIRECTORY

### t3_hello_world

More detailed out-source compilation example.

Keypoint:

- CMAKE_INSTALL_PREFIX  
`make install` install to one of three common directories:  
1. Default: `/usr/local` use command `cmake ..`  
2. System directory: `/usr` use command `cmake -DCMAKE_INSTALL_PREFIX=/usr ..`  
3. Others you defined directory: use command `cmake -DCMAKE_INSTALL_PREFIX=/PATH/YOU/DEFINED ..`
