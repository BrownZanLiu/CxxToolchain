# CxxToolChain
It holds xz packages of gcc source files.
All xz package is a combination of offical gcc package and its prerequisites.

Install steps:
0) cd archive
1) tar -xJf gcc-x.y.x-with-prerequisites.tar.xz
2) cd gcc-x.y.z
3) contrib/download_prerequisties  # might be skipped if mpc/mpfr/isl/gmp already exist
4) mkdir objdir
5) ../configure --prefix=/usr/local/gcc-x.y.z --program-suffix=-x.y.z --enable-lto --enable-vtable-verify --enable-werror --enable-languages=c,c++ --disable-multilib  # might disable werror
# ../configure --prefix=/usr/local/gcc-13.1.0 --program-suffix=-13.1.0 --enable-lto --enable-vtable-verify --enable-werror --enable-languages=c,c++ --disable-multilib
# ../configure --prefix=/usr/local/gcc-12.2.0 --program-suffix=-12.2.0 --enable-lto --enable-vtable-verify --enable-werror --enable-languages=c,c++ --disable-multilib
# ../configure --prefix=/usr/local/gcc-11.3.0 --program-suffix=-11.3.0 --enable-lto --enable-vtable-verify --enable-werror --enable-languages=c,c++ --disable-multilib
# ../configure --prefix=/usr/local/gcc-10.4.0 --program-suffix=-10.4.0 --enable-lto --enable-vtable-verify --enable-languages=c,c++ --disable-multilib
# ../configure --prefix=/usr/local/gcc-9.5.0 --program-suffix=-9.5.0 --enable-lto --enable-vtable-verify --enable-languages=c,c++ --disable-multilib
