
<h2>Swift-Jupyter:<h2><br/>
<code>https://github.com/google/swift-jupyter</code></br>
<br/>


# ParallelSTL+
BUILD:<br/>
<code>$ tar -xf ~/Downloads/oneTBB-2020.3.tar.gz && cd oneTBB-2020.3</code>
<code>CXX=g++ CC=gcc  stdver=c++14 make all && sudo make install && cd ..</code>
<code></code>

# llvm-MY-PRACTICE
BUILD:<br/>
https://llvm.org/docs/UserGuides.html<br/>

notes:<br/>
0. decompress source tarball:<br/>
<code>$ tar -xf ~/Src/llvm-project-llvmorg-10.0.1.tar.gz</code>
<br/>
.LLVM build commands:<br/>
<code>$ cd llvm-project-llvmorg-10.0.1</code><br/>
<code>$ mkdir build && cd build</code><br/>
<code>$cmake -DLLVM_ENABLE_PROJECTS='lld;clang;clang-tools-extra;compiler-rt;lldb;libcxx;libcxxabi;libunwind;polly' -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang++ -DLLVM_ENABLE_MODULES=ON -DLLVM_INSTALL_BINUTILS_SYMLINKS=ON -DLLVM_INSTALL_CCTOOLS_SYMLINKS=ON -DLLVM_INSTALL_UTILS=ON -DLLVM_ENABLE_LIBCXX=ON -DLLVM_BUILD_LLVM_C_DYLIB=ON -DLLVM_BUILD_LLVM_C_DYLIB=ON -DLLVM_ENABLE_FFI=ON  -DLLVM_INCLUDE_EXAMPLES=OFF -DLLVM_INCLUDE_TESTS=OFF -DCMAKE_BUILD_TYPE=RelWithDebInfo -DLLDB_USE_SYSTEM_DEBUGSERVER=ON -DLLDB_INCLUDE_TESTS=OFF -DLLDB_ENABLE_LUA=ON -DLLDB_ENABLE_PYTHON=ON -G "Unix Makefiles" ../llvm</code><br/>
<code>$ make -j20 lldb</code><br/>

.WebAssembly:<br/>
<code>cmake ../llvm -DCMAKE_BUILD_TYPE=Release -DLLVM_ENABLE_PROJECTS='lld;clang' -DLLVM_TARGETS_TO_BUILD="host;WebAssembly" -DLLVM_INCLUDE_EXAMPLES=OFF -DLLVM_INCLUDE_TESTS=OFF</code>
