pintos-project2
===============

Adding user programs support in Pintos kernel: loading executables / System calls handling Mechanism / IPC 

References: [https://github.com/pindexis/pintos-project2](https://github.com/pindexis/pintos-project2)

# Cac buoc tien hanh

## Step modifi

Clone project:


```bash
git clone git@github.com:pindexis/pintos-project2.git
```

### Step 1:

- Mo file `utils/pintos-gdb`, thay GDBMACROS = _<full duong dan den /src/misc/gdb-macros>_

- Mo `utils/Makfile` sua `LOADLIBES` thanh `LDLIBS`

Mo terminal thu muc `/src/utils`, go `make`

### Step 2:

- Sua trong file `/src/userprog/Make.vars`

_Line 7_: sua `bochs` thanh `qemu` 

Mo termianl thu muc `/src/userprog`. Go `make`

### Step 3:

Sua file `/utils/pintos`

- Line 103: Sua `bochs` thanh `qemu`
- Line 257: Sua `kernel.bin` thanh full path den kernel.bin (...src/userprog/build/kernel.bin)
- Line 621: Sua `qemu-system-i386` thanh `qemu-system-x86_64`

### Step 4:

Sua file `utils/Pintos.pm`

- Line 362: Sua `loader.bin` thanh full path den loader.bin (...src/userprog/build/loader.bin)

### Step 5:

- Sua file `.bashrc` tai folder `/home`, them dong sau:

`export PATH=/home/.../pintos/src/utils:$PATH`

### Step 6:

Go `make check` tai `src/userprog`

**Chu y: Neu tai buoc make check bi loi Error 255 thi thoat terminal ra, vao lai r make check**
