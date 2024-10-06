## How to build

```
CFLAGS="-g" ./configure --prefix=`pwd`/install
make install
```

## How to test

```
clang test.c -nostdinc -nostdlib -nodefaultlibs -I install/include -L install/lib -g \
    install/lib/crt1.o install/lib/crti.o \
    -lc install/lib/crtn.o \
    -static -o my_program
```

>! Need to seperate default incude and lib path
