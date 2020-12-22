# CODE

## Ubuntu
* [List of releases](https://wiki.ubuntu.com/Releases)  
* [releases downloads](https://releases.ubuntu.com/)  
  


## Fortran
* [fcode](http://v.fcode.cn/)
  [[bilibili]](https://www.bilibili.com/video/BV1tx411u7o4)
* [15分钟Fortran从0到够用 #030](https://www.bilibili.com/video/BV1Lv41117Lz)
* [[Fortran Tuto 2] Basics about variables](https://www.youtube.com/watch?v=GSJL6E1A6gM&list=PLvkU6i2iQ2fprrVmmkNP_V36mh0BMnS5L&index=2)


* [ustc](http://micro.ustc.edu.cn/Fortran/)
* [Mistakes in Fortran 90 Programs That Might Surprise You](http://www.cs.rpi.edu/~szymansk/OOF90/bugs.html)
* [Clion Fortran](https://www.jetbrains.com/help/clion/fortran-support.html)


## Python
* [Python Documentation contents](https://docs.python.org/3/contents.html)  


## Machine Learning
* [Learn With Me: Intro to Machine Learning](https://www.youtube.com/playlist?list=PLqFaTIg4myu9-T-fat2zjC5HmTpSybNfa)
* [有趣的机器学习 "Morvan"](https://www.youtube.com/playlist?list=PLXO45tsB95cIFm8Y8vMkNNPPXAtYXwKin)
* [秒懂神经网络 Neural Networks](https://www.youtube.com/playlist?list=PLXO45tsB95cJ0U2DKySDmhRqQI9IaGxck)


## git 
* [Git 版本管理 教学 tutorial "Morvan"](https://www.youtube.com/playlist?list=PLXO45tsB95cKysjmSNln65YoUt9lwEl7-)


## Intel oneAPI Base Toolkit (intel parallel studio)
* [Intel homepage](https://www.intel.com/content/www/us/en/homepage.html)  
* [Get the Intel® oneAPI Base Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/base-toolkit/download.html)  
* [Get the Intel® oneAPI HPC Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/hpc-toolkit/download.html)  
* [Get Started with the Intel® oneAPI Base Toolkit for Linux*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-base-linux/top.html)  
* [Get Started with the Intel® oneAPI Base Toolkit for Windows*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-base-windows/top.html)  
* [Get Started with the Intel® oneAPI HPC Toolkit for Windows*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-hpc-windows/top/before-you-begin.html)  
* [Get Started with the Intel® oneAPI HPC Toolkit for Linux*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-hpc-linux/top.html)  
* [Intel® Performance Libraries for oneAPI](https://software.intel.com/content/www/us/en/develop/tools/performance-libraries.html)  
  1. Intel® oneAPI Math Kernel Library  
  2. Intel® Integrated Performance Primitives  
  3. Intel® oneAPI Threading Building Blocks  
  4. Intel® oneAPI Data Analytics Library  
  5. Intel® MPI Library
  
* [Intel® oneAPI Toolkit Forums](https://software.intel.com/content/www/us/en/develop/tools/oneapi/support.html)  
* [Free Intel® Software Development Tools](https://software.intel.com/content/www/us/en/develop/articles/qualify-for-free-software.html#educator)  
* [Intel® oneAPI Toolkits Installation Guide for Linux* OS](https://software.intel.com/content/www/us/en/develop/documentation/installation-guide-for-intel-oneapi-toolkits-linux/top.html)  
* [oneAPI-samples](https://github.com/oneapi-src/oneAPI-samples)  
* [Intel® C++ and Fortran Compilers Redistributable Libraries by Version](https://software.intel.com/content/www/us/en/develop/articles/intel-compilers-redistributable-libraries-by-version.html)  
* [Installing Intel® oneAPI Toolkits via APT](https://software.intel.com/content/www/us/en/develop/articles/installing-intel-oneapi-toolkits-via-apt.html)  
* [Free Intel® Software Development Tools](https://software.intel.com/content/www/us/en/develop/articles/qualify-for-free-software.html)  

### install
```bash  
sudo sh ./<installer>.sh     //launch the GUI Installer as the root 
sh ./<installer>.sh    //launch the GUI Installer as the current user

/opt/intel/oneapi
C:\Program Files (x86)\Intel\oneAPI
```

For MacOS and Windows, there is a distinct step you need to do first:
1. MacOS: Install Xcode, then go to developer.apple.com and download and install Command Line Tools for your Xcode version
2. Windows: Install latest Visual Studio Community edition  

3. install the oneAPI Base Toolkit with these options  
threaded building blocks  
C++ compiler  
C++ Library  
Math Kernal Library  
(optional) GDB debugger  
2. Install the oneAPI HPC toolkit with these options  
Intel MPI library  
Intel C++ compiler  
Intel Fortran compiler  

### usage
Windows  
On Windows a Start menu shortcut for a oneAPI command prompt is installed. CMake et al should just find the Intel compiler when in the oneAPI command prompt. Otherwise run setvars.bat as per oneAPI documentation.

Linux  
each time you wish to use Intel oneAPI, do
```bash
. /opt/intel/oneapi/setvars.sh
~/intel/oneapi/setvars.sh
```
MacOS  
each time you wish to use Intel oneAPI, do
```bash
. /opt/intel/oneapi/setvars.sh
```
If upon compiling a C program you get errors like stdio.h isn’t found, be sure you’ve installed Xcode Command Line Tools.
<br>
<br>

* [Intel® oneAPI HPC Toolkit Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-oneapi-hpc-toolkit-release-notes.html)  
* [Intel® Fortran Compiler for oneAPI Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-oneapi-fortran-compiler-release-notes.html#top)  
* [Intel® Parallel Studio XE and oneAPI Toolkits Supported and Unsupported Product Versions](https://software.intel.com/content/www/us/en/develop/articles/intel-parallel-studio-xe-supported-and-unsupported-product-versions.html) 
  
* [Intel® MPI Library](https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/mpi-library.html)
* [Intel® MPI Library Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-mpi-library-release-notes.html)  


## GCC 
* [GCC, the GNU Compiler Collection](https://gcc.gnu.org/)
  [[download]](http://ftp.gnu.org/gnu/gcc/)  
  gfortran supports 95 2003 2008 2018


## CMake
[CMake Community Wiki](https://gitlab.kitware.com/cmake/community)
[CMake Documentation](https://cmake.org/cmake/help/latest/index.html#)

## intel mpi
```bash
env:
source /opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/bin/mpivars.sh intel64
or
export PATH=$PATH:/opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/bin
export LD_LIBRARY_PATH=/opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/lib
or
export PATH=$PATH:/opt/intel/impi/2018.0.128/bin64
export LD_LIBRARY_PATH=/opt/intel/impi/2018.0.128/lib64

mpiicc -o test  test.c
mpirun -r ssh -f mpd.hosts -n <# of processes> ./test


```
