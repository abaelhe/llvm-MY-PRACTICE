# llvm-MY-PRACTICE
BUILD:<br/>
https://llvm.org/docs/UserGuides.html<br/>

notes:<br/>
0. decompress source tarball:<br/>
<code>$ tar -xf ~/Src/llvm-project-llvmorg-10.0.1.tar.gz</code>
<br/>
1.build commands:<br/>
<code>$ cd llvm-project-llvmorg-10.0.1</code><br/>
<code>$ mkdir build</code><br/>
<code>$ cd build</code><br/>
<code>$ cmake -DLLVM_ENABLE_PROJECTS='clang;lldb' -DLLDB_TEST_COMPILER=/usr/bin/gcc  -DLLDB_USE_SYSTEM_DEBUGSERVER=ON -DLLDB_INCLUDE_TESTS=OFF -G "Unix Makefiles" ../llvm</code><br/>
<code>$ make -j10 lldb</code><br/>
