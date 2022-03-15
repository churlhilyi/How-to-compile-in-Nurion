## wannier_tools_2.6.0


Ref: <https://ylqk9.wordpress.com/build-arpack-for-linux-and-windows/>

__Linux build for ARPACK__

>First one need to edit the ARmake.inc file. 

    Let FC = ifort, PLAT = LINUX and home = /home/yourid/Software/ARPACK. 
    
>And set some other options to FCFLAGS such as loop unrolling.
>Here I simply set FCFLAGS = -O3. Now GNU make will use Intel Fortran as compiler.

>Second one need to tell GNU make do not build LAPACK and BLAS.

    To do this you can comment this line DIRS = $(BLASdir) $(LAPACKdir) $(UTILdir) $(SRCdir) and uncomment this line DIRS = $(UTILdir) $(SRCdir). 
    
>Then GNU make will skip $(BLASdir) which is the BLAS directory and $(LAPACKdir) which is the LAPACK directory. 
>After these steps you can just type make all and you will find libarpack_LINUX.a in your ARPACK directory.

>Third, to use it, you can just use it as a static library (In my opinion: a pack of .o files). 
    The command line is: ifort yourcode.o libarpack_LINUX.a -Wl,--start-group $(MKLROOT)/lib/intel64/libmkl_intel_lp64.a $(MKLROOT)/lib/intel64/libmkl_sequential.a $(MKLROOT)/lib/intel64/libmkl_core.a -Wl,--end-group -lpthread -lm. 
>This will give you a 64bit executable file (Check here for how to link MKL).

>The difference of using MKL instead of original LAPACK+BLAS is: one always need to link against MKL when using ARPACK. 
>I didn’t dig it too much to make a package since it is a common thing to rebuilt software in Linux when you move to a new machine.

-------------------------------
If you are installed ARPACK then
1. modify Makefile.intel-mpi file in /src/:

         LIBS = ${ARPACK} \
                 -Wl,--start-group ${MKLROOT}/lib/intel64/libmkl_intel_lp64.a \
                 ${MKLROOT}/lib/intel64/libmkl_sequential.a \
                 ${MKLROOT}/lib/intel64/libmkl_core.a -Wl,--end-group -lpthread -lm -ldl \


2. Use __make__ command:

         make
