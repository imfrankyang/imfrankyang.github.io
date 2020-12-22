# CODE_note


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

## mpi programming
```fortran

```

```cpp
#include <mpi.h>
#include <stdio.h>
int MPI_Init(int *argc, char **argv)

int MPI_Finalize(void)
```


