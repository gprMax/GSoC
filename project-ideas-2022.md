# GSoC 2022 - Project Ideas List

gprMax is planning to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2022 program, following a successful participation in 2019 and 2021. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Dr Antonis Giannopoulos
- Dr Iraklis Giannakis
- Dr John Hartley
- Ms Rania Patsia
- Mr Dimitris Angelis

If a project is successfully selected you will be allocated a primary mentor and supported by the rest of the team. If you are interested in learning more about a particular project idea please contact us using [info@gprmax.com](mailto:iinfo@gprmax.com) or through our [gprMax GSoC2022 Gitter channel](https://gitter.im/gprMax/GSoC2022?source=orgpage). 

## 1. Multi-GPU model execution

The aim of the project is to investigate multi-GPU model execution, i.e. allow a model to execute (and share memory) across multiple GPUs.

Currently with our GPU-based (PyCuda) solver, a model must fit within the memory of a single GPU. Simulations are becoming ever larger and more complex, which often means their memory requirements exceed that available on a single GPU. A solution is required to allow a model to execute (and share memory) across multiple GPUs. This may involve a MPI type domain decomposition or simpler memory sharing approach.

**Skills required:** Python, CUDA

**Difficulty:** Hard

**Length:** 350hrs


## 2. Google Colab / Jupyter notebook integration

The aim of this project is to allow gprMax to run on Google Colab or a Jupyter notebook type environment.

The ability to run gprMax on Google Colab (or a Jupyter notebook type environment) would be very beneficial to many of our users, especially the access to GPU compute resource. Additional tools and scripts will be required to enable this functionality, particularly the ability to view [Visualization Toolkit (VTK)](https://vtk.org) format geometry information with a notebook environment.

**Skills required:** Python, familiarity with VTK/Paraview would beneficial.

**Difficulty:** Medium

**Length:** 350hrs


## 3. De-coupled model building and execution

The aim of this project is to investigate de-coupling the model building and execution phases.

Currently the modeling building phase takes place (which is mostly a serial process) on CPU. Once that is complete the model can then be executed using either the CPU-based (OpenMP) or GPU-based (CUDA) solver. The next model cannot be built until the previous model has finished executing, and this can sometimes cause a performance bottleneck. If the model building and execution phases could be made more independent and a queuing system implemented then this may solve this performance problem.

**Skills required:** Python, CUDA

**Difficulty:** Medium

**Length:** 350hrs


## 4. Optimising GPU performance

The aim of the project is to optimise our CUDA-based solver for GPUs. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. We have GPU-based solver which uses NVIDIA CUDA (with PyCUDA). The speed-up is significant (x30 compared to parallelised CPU), but we would like to further tune and optimise the performance. 

**Skills required:** Python, CUDA

**Difficulty:** Medium

**Length:** 175hrs


## 5. Improved installation tools

The aim of this project is to create a simplified and more user-friendly installation workflow for the software.

gprMax is predominately written in Python, but some of the performance-critical parts of the code are written in [Cython](https://cython.org), which must be built and compiled. The current installation involves building a Python environment, installing a C compiler with OpenMP support, and building and installing the gprMax package. This can be a lengthy and complex procedure, depending on your operating system, especially for first-time or inexperienced users.

**Skills required:** Python, Cython, tools and compilers on multiple (Linux, Windows, macOS) operating systems

**Difficulty:** Medium

**Length:** 175hrs


## 6. Comprehensive test and benchmarking suite

The aim of this project is to develop a comprehensive test suite and benchmarking toolset.

Currently gprMax includes a series of tests that verify specific simulation results against reference solutions. This only tests large chunks of code at a relatively high level. As the functionality and complexity of the code base increases a more comprehensive, fine-grained set of tests is required. The performance of the code is also an important element, as simulations can be extremely large and complex, with some requiring weeks of runtime on [high-performance computing (HPC)](https://en.wikipedia.org/wiki/Supercomputer). It is therefore key to have some models that can be used to benchmark code features with both the multi-threaded CPU (OpenMP), and GPU accelerated solvers.

**Skills required:** Python, tools and compilers on multiple (Linux, Windows, macOS) operating systems, some knowledge of GPU and HPC would be beneficial.

**Difficulty:** Medium

**Length:** 350hrs


## 7. Arbitary placement of Perfectly Matched Layer (PML) material

The aim of this project is to provide the ability for users to use Perfectly Matched Layer (PML) material with geometry primitives, i.e. PML material should not be confined to being used at the boundaries of the domain.

Currently PMLs are used as absorbing boundaries to effectively and efficiently terminate the model domain. There are scenarios where use of the PML material with geometry primitives, i.e. boxes, cylinders etc..., would be beneficial, e.g. building antenna models.

**Skills required:** Python.

**Difficulty:** Medium

**Length:** 175hrs


## 8. Clutter Simulation for the Mars Radars SHARAD and MARSIS 

The aim of this project is to tune, organise, parallelise, and automate existing code that generates a radar cluttergram based on:
- topographic data from Mars 
- the orbit of the sattelite

Currently there is no available software that does this, and planetary scientists need to develop a code from scratch, which is often unnatainable due to lack of background on computational electrodynamics. This compromises research on that area and makes interpretation of planetary satelite radar exclusive to research groups with expertise in computational electrodynamics.

A user-friendly, automatic and parellised open-source simulation tool will greatly advance research on planetary radar i.e. exploring Mars subsurface for subglacial lakes, lava tubes, caves etc. 

**Skills required:** Python, MATLAB

**Difficulty:** Medium

**Length:** 350hrs