## How to install elpa 2022.11.001 version in KISTI

0. Load required modules:

            module load craype-network-opa craype-mic-knl intel/19.1.2 impi/19.1.2 fftw_mpi/3.3.7 python/3.9.5

1. Get source files:

            git clone https://gitlab.mpcdf.mpg.de/elpa/elpa.git

2. Run __./configure_ command with options:

            FC=mpiifort CC=mpiicc ./configure FCFLAGS="-O3 -xCORE-AVX512" CFLAGS="-O3 -xCORE-AVX512" --enable-option-checking=fatal SCALAPACK_LDFLAGS="-L$MKLROOT/lib/intel64 -lmkl_scalapack_lp64 -lmkl_intel_lp64 -lmkl_sequential -lmkl_core -lmkl_blacs_intelmpi_lp64 -lpthread " SCALAPACK_FCFLAGS="-I$MKLROOT/include/intel64/lp64" --enable-avx2 --enable-avx512

3. Use __make__ command:

            make
            make check
            make install
            
Done!

-------------------------------
Ref: 

            https://gitlab.mpcdf.mpg.de/elpa/elpa/-/blob/master/documentation/INSTALL.md
