# Giac

Julia interface to the [Giac computer algebra system](http://www-fourier.univ-grenoble-alpes.fr/~parisse/giac.html).

## Installation
Giac/Xcas has to be [installed](https://www-fourier.univ-grenoble-alpes.fr/~parisse/install_en) first. 
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
leave Julia, and from a terminal before running Julia run
```
export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libgmp.so.10
```

## Examples
+ [Giac_examples.ipynb](https://github.com/HaraldHofstaetter/Giac.jl/blob/master/examples/Giac_examples.ipynb)
+ [Giac_basics.ipynb](https://github.com/HaraldHofstaetter/Giac.jl/blob/master/examples/Giac_basics.ipynb)
