SYCL-BLAS samples
===

## How to compile the samples

At the moment any project using SYCL-BLAS requires:

* OpenCL
* [ComputeCpp](http://www.computecpp.com)
* SYCL-BLAS, either:
  * as a library (install the library and include `sycl_blas.h` in an application)
  * as a header-only framework (include `sycl_blas.hpp` in an application)

### With CMake

This folder contains a basic CMake configuration file and a module to find
SYCL-BLAS (which will be used as a header-only framework). It also uses a module
to find ComputeCpp that is located in the folder `cmake/Modules`.

Usage:

* set `ComputeCpp_DIR` to your ComputeCpp root path
* set `SyclBLAS_DIR` to your SYCL-BLAS root path

```bash
mkdir build
cd build
cmake .. -GNinja -DComputeCpp_DIR=/path/to/computecpp \
                 -DSyclBLAS_DIR=~/path/to/syclblas
ninja
```
