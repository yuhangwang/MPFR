# MPFR
The GNU MPFR Library for multiple-precision floating-point computations with correct rounding

## Compilation notes

### Compilation steps
```bash
wget ftp://gcc.gnu.org/pub/gcc/infrastructure/mpfr-2.4.2.tar.bz2
tar xvf mpfr-2.4.2.tar
cd mpfr-2.4.2
curl http://www.mpfr.org/mpfr-2.4.2/patches | patch -N -Z -p1
```

The output of the patching step suggests the source is up to date:
```shell
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
Dload  Upload   Total   Spent    Left  Speed
108   216  108   216    0     0     87      0  0:00:02  0:00:02 --:--:--  1911
patch: **** Only garbage was found in the patch input.

```


