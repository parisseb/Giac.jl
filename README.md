# Giac

Julia interface to the [Giac computer algebra system](http://www-fourier.univ-grenoble-alpes.fr/~parisse/giac.html). 
Should work on Linux-based systems, including inside [WSL](https://learn.microsoft.com/windows/wsl/install) for Windows users. Mac is not yet supported, it requires changes in deps/src/Makefile, INCLUDE should be /Applications/usr/include and LIBS should list /Applications/usr/lib as well as /Applications/usr/lib_[architecture], and the library should have dylib extension instead of so.

## Installation
Giac/Xcas has to be [installed](https://www-fourier.univ-grenoble-alpes.fr/~parisse/install_en%23packages) first. 
Then, in a Julia session, type:

```julia
using Pkg
Pkg.add(PackageSpec(url="https://github.com/parisseb/Giac.jl"))
```
## Quick Check
```julia
using Giac
@giac x,y,z
factor(x^4-1)
```
On Linux x86_64, if you get an error like
```
ERROR: InitError: could not load library "/home/parisse/.julia/packages/Giac/WH00q/src/../deps/lib/libgiac_c.so"
/lib/x86_64-linux-gnu/libecm.so.1: undefined symbol: __gmpn_add_nc
```
leave Julia, then from a terminal, before running julia, run
```
export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libgmp.so.10
```

## Examples
+ [Giac_examples.ipynb](https://github.com/parisseb/Giac.jl/blob/master/examples/Giac_examples.ipynb)
+ [Giac_basics.ipynb](https://github.com/parisseb/Giac.jl/blob/master/examples/Giac_basics.ipynb)
