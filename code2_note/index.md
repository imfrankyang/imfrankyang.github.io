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
#include<stdio.h>
#include<mpi.h>
int main(int argc, char **argv) {
int myrank, nprocs;
MPI_Init(&argc, &argv);
MPI_Comm_size(MPI_COMM_WORLD,&nprocs);
MPI_Comm_rank(MPI_COMM_WORLD,&myrank);
printf("Hello from processor %d of %d\n", myrank, nprocs);
while(1) {}
MPI_Finalize();
return 0;
}
```

```cpp
#include <mpi.h>
#include <stdio.h>
int MPI_Init(int *argc, char **argv)
int MPI_Comm_size(MPI_Comm comm, int *rank)
int MPI_Finalize(void)



#include <stdio.h>
#include <mpi.h>

int main(int argc, char **argv)
{
	int myid, numprocs;
	MPI_Init(&argc, &argv);

    MPI_Comm_size(MPI_COMM_WORLD, &numprocs);

	//your code here

	//end of your code

	printf("Hello World!I'm rank %d of %d\n", myid, numprocs);

	MPI_Finalize();
	return 0;



#include<stdio.h>
#include<mpi.h>

int main(int argc, char **argv)
{
	int myid, numprocs;
	double start, finish;
	
	MPI_Init(&argc, &argv);

    MPI_Comm_rank(MPI_COMM_WORLD, &myid);
    MPI_Comm_size(MPI_COMM_WORLD, &numprocs);

	//your code here
	
	//end of your code 
	
	start = MPI_Wtime();
	
	printf("The precision is: %f\n", MPI_Wtick());
	
	finish = MPI_Wtime();
	
	printf("Hello World!I'm rank %d of %d, running %f seconds.\n", myid, numprocs, finish-start);

	MPI_Finalize();
	return 0;
}



#include <stdio.h>
#include <mpi.h>

int main(int argc, char **argv)
{
	int myid, numprocs, source;
	MPI_Status status;
	char message[100];

	MPI_Init(&argc, &argv);
	MPI_Comm_rank(MPI_COMM_WORLD, &myid);
    MPI_Comm_size(MPI_COMM_WORLD, &numprocs);
    
    if(myid != 0) {
    	strcpy(message, "hello world!");
    	
    	//your code here
    	
    	//end of your code
	}
	else { //myid == 0
		for(source=1; source<numprocs; source++) {
			//your code here
			
			//end of your code
			
			printf("%s\n", message);
		}
	}

	MPI_Finalize();
	return 0;
}

```


