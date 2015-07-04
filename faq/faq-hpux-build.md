# HP-UX Build FAQ #

* What software prerequisites are needed to build ClamAV on PA-RISC HP-UX?

First and foremost, a suitable GCC version must be installed, because older versions of GCC have bugs which are checked for during the configure process. Version 4.7.0 or higher is recommended.
Unfortunately, the newest available version of GCC available from the Porting and Archiving Centre is at this writing version 4.2.3, which is not suitable for a ClamAV build. Hewlett Packard provides a package

bz2, zlib

To run the unit tests, the Check software is required.


* Where can I find prerequisite software?

The HP-UX Porting and Archiving Centre provides depots for many open-source packages: http://hpux.connect.org.uk/ 

* 

* Compile command line for HP-UX 11.11 PA-RISC
env CC="/opt/hp-gcc/bin/gcc -static-libgcc" CFLAGS=-mpa-risc-2-0 ./configure --prefix=/opt/clamav --disable-clamav --with-libbz2-prefix=/usr/local --with-zlib=/usr/local --with-included-ltdl --disable-ipv6 --with-libncurses-prefix=/usr/local --with-libcheck-prefix=/usr/local

5-minute timeout on checks - export T=300

[privacy policy]: http://www.cisco.com/web/siteassets/legal/privacy.html
[Sourceforge]: http://sourceforge.net/projects/clamav/files/clamav/win32/
