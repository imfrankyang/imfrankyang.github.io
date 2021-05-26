# Linux envrionment


## Linux tutorial
**bolg**
- [Linux Cluster Blog](https://thelinuxcluster.com/) is a collection of how-to and tutorials for Linux Cluster and Enterprise Linux
- [Linux 命令收藏](https://openfoam.top/linuxLearning/)

**Video tutorial**
- [莫烦 linux 建议教学](https://mofanpy.com/tutorials/others/linux-basic/)
- [Learn CentOS "LearnLinuxTV"](https://www.youtube.com/watch?v=Mi6GUcSW5xs&list=PLT98CRl2KxKHjHLIHrmmi5FmBGIZ8cNJE)
- [计算机科学课堂中学不到的知识 The Missing Semester of Your CS Education(2020)](https://www.bilibili.com/video/BV1x7411H7wa)

**Ubuntu**
- [List of releases](https://wiki.ubuntu.com/Releases)  
- [releases downloads](https://releases.ubuntu.com/)  
- [Mirror Tsinghua](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/) 

**CentOS**
- [Mirror Tsinghua Centos6](https://mirror.tuna.tsinghua.edu.cn/help/centos-vault/)
- [Mirror Tsinghua Centos7 8](https://mirror.tuna.tsinghua.edu.cn/help/centos/)



<br><br><br>


## Fortran
* [fcode](http://v.fcode.cn/)
  [[bilibili]](https://www.bilibili.com/video/BV1tx411u7o4)

* [[Fortran Tuto 2] Basics about variables](https://www.youtube.com/watch?v=GSJL6E1A6gM&list=PLvkU6i2iQ2fprrVmmkNP_V36mh0BMnS5L&index=2)


* [ustc doc](http://micro.ustc.edu.cn/Fortran/)
* [Mistakes in Fortran 90 Programs That Might Surprise You](http://www.cs.rpi.edu/~szymansk/OOF90/bugs.html)
* [Clion Fortran](https://www.jetbrains.com/help/clion/fortran-support.html)





<br><br><br>


## Python

### anaconda  
  install
```bash
  wget https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh
  bash Anaconda3-2020.11-Linux-x86_64.sh
```

### tutorial

- MorvanZhou  
  https://github.com/MorvanZhou/tutorials
- [Python Documentation contents](https://docs.python.org/3/contents.html)  
- https://www.runoob.com/python/python-tutorial.html
- [Python 入門教學課程](https://www.youtube.com/watch?v=wqRlKVRUV_k&list=PL-g0fdC5RMboYEyt6QS2iLb_1m7QcgfHk)


**numpy**  
- [Python NumPy 入門教學課程](https://www.youtube.com/watch?v=nJUMpIo5rmg&list=PL-g0fdC5RMboq4yOQmvwYXamPDL4uZYEL)


NumPy 官网 http://www.numpy.org/  
NumPy 源代码：https://github.com/numpy/numpy  
SciPy 官网：https://www.scipy.org/  
SciPy 源代码：https://github.com/scipy/scipy  
Matplotlib 官网：https://matplotlib.org/  
Matplotlib 源代码：https://github.com/matplotlib/matplotlib  

NumPy官方文档  
https://numpy.org/doc/stable/user/whatisnumpy.html

runoob  
https://www.runoob.com/numpy/numpy-tutorial.html

from-python-to-numpy  
https://www.labri.fr/perso/nrougier/from-python-to-numpy




<br><br><br>








## julia
https://docs.julialang.org/en/v1/

https://www.youtube.com/c/TheJuliaLanguage/videos

### install julia

1. download from https://julialang.org/downloads/
2. decompress
```bash
tar zxf julia-1.6.0-linux-x86_64.tar.gz 
cd julia-1.6.0
```

env
```bash
export PATH=~/julia-1.6.0/bin/:$PATH
```

test
```julia
#!/usr/bin/env julia
println("Greetings! 你好! こんにちわ! 안녕하세요?")
```

install packages
```bash
julia   # activate julia env

using Pkg
Pkg.add("Plots")
Pkg.add("PyPlot")

Pkg.update("Plots")
Pkg.rm("Plots")

```



## java
[Java SE Development Kit 15 Downloads](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html)



## git 

- [git命令查询](https://www.bookstack.cn/read/git-tutorial/docs-basic.md)  
- [GitHub Documentation](https://docs.github.com/en) 

**tutorial**
- [Lecture 6 - Version Control (git) (2020)](https://www.bilibili.com/video/BV1x7411H7wa?p=6)
- [Git 版本管理 教学 tutorial "Morvan"](https://www.youtube.com/playlist?list=PLXO45tsB95cKysjmSNln65YoUt9lwEl7-)



## complier

### Intel oneAPI Base Toolkit 
Intel oneAPI is the new version for free and the old version is intel parallel studio.

**Document**
* [Intel homepage](https://www.intel.com/content/www/us/en/homepage.html)  

Download from
* [Free Intel® Software Development Tools](https://software.intel.com/content/www/us/en/develop/articles/qualify-for-free-software.html#educator)  
* [Get the Intel® oneAPI Base Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/base-toolkit/download.html)  
* [Get the Intel® oneAPI HPC Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/hpc-toolkit/download.html)  

Release Notes
- [Intel® oneAPI Base Toolkit Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-oneapi-toolkit-release-notes.html)
- [Intel® oneAPI HPC Toolkit Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-oneapi-hpc-toolkit-release-notes.html)  

* [Get Started with the Intel® oneAPI Base Toolkit for Linux*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-base-linux/top.html)  
* [Get Started with the Intel® oneAPI Base Toolkit for Windows*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-base-windows/top.html)  
* [Get Started with the Intel® oneAPI HPC Toolkit for Linux*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-hpc-linux/top.html)  
* [Get Started with the Intel® oneAPI HPC Toolkit for Windows*](https://software.intel.com/content/www/us/en/develop/documentation/get-started-with-intel-oneapi-hpc-windows/top/before-you-begin.html)  
* [Intel® Performance Libraries for oneAPI](https://software.intel.com/content/www/us/en/develop/tools/performance-libraries.html)  
  1. Intel® oneAPI Math Kernel Library  
  2. Intel® Integrated Performance Primitives  
  3. Intel® oneAPI Threading Building Blocks  
  4. Intel® oneAPI Data Analytics Library  
  5. [Intel® MPI Library](https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/mpi-library.html)

* [Intel® Parallel Studio XE and oneAPI Toolkits Supported and Unsupported Product Versions](https://software.intel.com/content/www/us/en/develop/articles/intel-parallel-studio-xe-supported-and-unsupported-product-versions.html) 


Installation
* [Intel® oneAPI Toolkits Installation Guide for Linux* OS](https://software.intel.com/content/www/us/en/develop/documentation/installation-guide-for-intel-oneapi-toolkits-linux/top.html)  
* [Installing Intel® oneAPI Toolkits via APT](https://software.intel.com/content/www/us/en/develop/articles/installing-intel-oneapi-toolkits-via-apt.html) 


Compiler
* [Intel® C++ and Fortran Compilers Redistributable Libraries by Version](https://software.intel.com/content/www/us/en/develop/articles/intel-compilers-redistributable-libraries-by-version.html)  
* [Intel® Fortran Compiler for oneAPI Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-oneapi-fortran-compiler-release-notes.html#top)  

MPI Libarary
* [Intel® MPI Library Release Notes](https://software.intel.com/content/www/us/en/develop/articles/intel-mpi-library-release-notes.html)  

Others
* [oneAPI-samples for vscode](https://github.com/oneapi-src/oneAPI-samples)  
* [Intel® oneAPI Toolkit Forums](https://software.intel.com/content/www/us/en/develop/tools/oneapi/support.html)  


**pre-install**

- MacOS

  Install Xcode, then go to [developer.apple.com](developer.apple.com) and download Command Line Tools for your Xcode version.

- Windows

  Install latest Visual Studio Community edition  

**install**

```bash  
sudo sh ./<installer>.sh     #launch the GUI Installer as the root 
sh ./<installer>.sh          #launch the GUI Installer as the current user

#default location
/opt/intel/oneapi
C:\Program Files (x86)\Intel\oneAPI
```

1. install the oneAPI **Base** Toolkit with these options  
    threaded building blocks  
    C++ compiler  
    C++ Library  
    Math Kernal Library  
    (optional) GDB debugger  
2. Install the oneAPI **HPC** toolkit with these options  
    Intel MPI library  
    Intel C++ compiler  
    Intel Fortran compiler  

**env set**
For Intel oneAPI  
- linux  

永久生效：vi /etc/profile or vi ~/.bashrc
```bash
source ~/intel/oneapi/setvars.sh intel64
or
source /opt/intel/oneapi/setvars.sh
```

临时使用 terminal：  
```bash
source /opt/intel/oneapi/setvars.sh
or
. /opt/intel/oneapi/setvars.sh
or
~/intel/oneapi/setvars.sh
```

- Windows  
  OneAPI command prompt is installed in Start menu. Or run setvars.bat

- MacOS  
```bash
. /opt/intel/oneapi/setvars.sh
```



For the intel parallel studio 2020
```bash
source /opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/bin/mpivars.sh intel64
or
export PATH=$PATH:/opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/bin
export LD_LIBRARY_PATH=/opt/intel/compilers_and_libraries_2020.4.304/linux/mpi/intel64/lib
```
For the intel parallel studio 2018
```bash
export PATH=$PATH:/opt/intel/impi/2018.0.128/bin64
export LD_LIBRARY_PATH=/opt/intel/impi/2018.0.128/lib64
```

**test**
```bash
mpiicc -o test  test.c
mpirun -r ssh -f mpd.hosts -n <Number of processes>  ./test
```


{{< admonition type=warning title="error and solution" open=true >}}
**Errors like stdio.h isn't found**

be sure you've installed Xcode Command Line Tools.
{{< /admonition >}}

**reference**  
- https://zhuanlan.zhihu.com/p/347913888


### GCC 
* [GCC, the GNU Compiler Collection](https://gcc.gnu.org/)
  [[download]](http://ftp.gnu.org/gnu/gcc/)  
* gfortran supports 95 2003 2008 2018


### CMake
* [CMake Community Wiki](https://gitlab.kitware.com/cmake/community)
* [CMake Documentation](https://cmake.org/cmake/help/latest/index.html#)




## Parallel Computing 

### mpi tutorial
* [easyhpc](https://easyhpc.net/)



## GPU Computing

- [programming courses collections](https://www.bu.edu/pasi/materials/)
- [Programming GPUs with Fortran](https://www.youtube.com/watch?v=COjvWNpxnxc&feature=emb_logo)

### CUDA
Download old version from [CUDA archive](https://developer.nvidia.com/cuda-toolkit-archive) or the new one [CUDA 10.2](https://developer.nvidia.com/cuda-10.2-download-archive?target_os=Linux&target_arch=x86_64&target_distro=CentOS&target_version=6) for Ubuntu 18 16/Centos 8 7 6 or [CUDA 11](https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal) for Ubuntu 20.04 18.04 16.04/Centos 8 7.

- [CUDA source code](https://developer.download.nvidia.com/compute/cuda/opensource/)
- [CUDA Toolkit Documentation](https://docs.nvidia.com/cuda/)  
  
- [CUDA 编程入门: 8 小时掌握 GPU 计算 (失效)](https://www.youtube.com/playlist?list=PLSVM68VUM1eWsEX0yPliaL3pTZoKqJWfi)


## Machine Learning
- [Learn With Me: Intro to Machine Learning](https://www.youtube.com/playlist?list=PLqFaTIg4myu9-T-fat2zjC5HmTpSybNfa)
- [有趣的机器学习 "Morvan"](https://www.youtube.com/playlist?list=PLXO45tsB95cIFm8Y8vMkNNPPXAtYXwKin)
- [秒懂神经网络 Neural Networks](https://www.youtube.com/playlist?list=PLXO45tsB95cJ0U2DKySDmhRqQI9IaGxck)

- Shusen Wang  
  - [website](http://wangshusen.github.io/)
  - [homepage school](https://faculty.stevens.edu/swang134)
  - [googlescholar](https://scholar.google.com/citations?user=HAf4pEoAAAAJ&hl=en)
 
  [深度强化学习Deep Reinforcement Learning course](https://www.youtube.com/playlist?list=PLvOO0btloRnsiqM72G4Uid0UWljikENlU)  
