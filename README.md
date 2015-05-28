# MPFR
**The GNU MPFR Library for multiple-precision floating-point computations with correct rounding**

This is an unofficial verbatim redistribution of the binary&source form of the GNU MPFR library (a prerequisite for compiling programs like GCC), under the terms of LGPL 3.0 license.

This redistribution is under the the same LGPL 3.0.

Please visit the official website for more details: http://www.mpfr.org

## Usage
The binary/ folder contains both a tar.gz file and a folder, which are equivalent. You can use either one.

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
```bash
wget ftp://gcc.gnu.org/pub/gcc/infrastructure/mpfr-2.4.2.tar.bz2
tar xvf mpfr-2.4.2.tar
cd mpfr-2.4.2
curl http://www.mpfr.org/mpfr-2.4.2/patches | patch -N -Z -p1
cd ..
mkdir build_mpfr-2.4.2
cd build_mpfr-2.4.2
../mpfr-2.4.2/configure --prefix=/home/steven/install/libmpfr/2.4.2 --enable-thread-safe=yes --with-gmp=/home/steven/install/libgmp/4.3.2
make -j10
make check
make install
```

The output of the patching step suggests the source is up to date:
```shell
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
Dload  Upload   Total   Spent    Left  Speed
108   216  108   216    0     0     87      0  0:00:02  0:00:02 --:--:--  1911
patch: **** Only garbage was found in the patch input.

```

### Quality verification
See the "QualityVerification.txt" for the output of "make check".

