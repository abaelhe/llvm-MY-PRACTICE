# llvm-MY-PRACTICE
notes:

BUILD:
https://llvm.org/docs/UserGuides.html

0. decompress source tarball:
$ tar -xf ~/Src/llvm-project-llvmorg-10.0.1.tar.gz 
1.build commands:
$ cd llvm-project-llvmorg-10.0.1
$ mkdir build
$ cd build
$ cmake -DLLVM_ENABLE_PROJECTS='clang;lldb' -DLLDB_TEST_COMPILER=/usr/bin/gcc  -DLLDB_USE_SYSTEM_DEBUGSERVER=ON -DLLDB_INCLUDE_TESTS=OFF -G "Unix Makefiles" ../llvm
$ make -j10 lldb
