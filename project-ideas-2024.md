# GSoC 2024 - Project Ideas List

gprMax is planning to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2024 program, following a successful participation in 2019, 2021, and 2023. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Dr Antonis Giannopoulos
- Dr Iraklis Giannakis
- Dr Rania Patsia

If a project is successfully selected you will be allocated a primary mentor and supported by the rest of the team. If you are interested in learning more about a particular project idea please contact us using [info@gprmax.com](mailto:info@gprmax.com) or on our [gprMax Slack channel](https://gprmax-fdtd.slack.com). 


## 1. Optimisation of GPU performance

The aim of the project is to optimise our CUDA-based solver for GPUs. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. We have GPU-based solver which uses NVIDIA CUDA (with PyCUDA). The speed-up is significant (x30 compared to parallelised CPU), but we would like to further tune and optimise the performance. 

**Skills required:** Python, CUDA

**Difficulty:** Medium

**Length:** 175hrs

<!--
## 1. Multi-GPU model execution

The aim of the project is to investigate multi-GPU model execution, i.e. allow a model to execute (and share memory) across multiple GPUs.

Currently with our GPU-based (PyCuda) solver, a model must fit within the memory of a single GPU. Simulations are becoming ever larger and more complex, which often means their memory requirements exceed that available on a single GPU. A solution is required to allow a model to execute (and share memory) across multiple GPUs. This may involve a MPI type domain decomposition or simpler memory sharing approach.

**Skills required:** Python, CUDA

**Difficulty:** Hard

**Length:** 350hrs
-->


## 2. Optimisation for Apple silicon CPUs

The aim of this project is to maximise the performance of gprMax on Apple silicon CPUs.

gprMax is predominately written in Python, but some of the performance-critical parts of the code are written in [Cython](https://cython.org), which must be built and compiled. For CPU-based parallelisation, Cython uses OpenMP, which has worked well on Intel-based CPUs using gcc (Linux/macOS) and Microsoft Visual Studio compilers. However, this project will explore how to best optimise gprMax for running on Apple silicon CPUs.

**Skills required:** Python, tools and compilers macOS operating systems.

**Difficulty:** Medium

**Length:** 175hrs


## 3. Performance gains through memory usage and cache access

The aim of this project is to optimise the performance of the CPU-based solver through investigation of memory and cache accessing.

gprMax is predominately written in Python, but some of the performance-critical parts of the code are written in [Cython](https://cython.org), which must be built and compiled. The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, whose performance is largely limited by memory bandwidth. This project will look at strategies to improve memory and cache access such as the [FDTD XPU technology](https://ieeexplore.ieee.org/abstract/document/7481533). 

**Skills required:** Python, compilers and benchmarking tools on multiple (Linux, Windows, macOS) operating systems

**Difficulty:** Medium

**Length:** 350hrs


## 4. De-coupled model building and execution

The aim of this project is to investigate de-coupling the model building and execution phases.

Currently the modeling building phase takes place (which is mostly a serial process) on CPU. Once that is complete the model can then be executed using either the CPU-based (OpenMP) or GPU-based (CUDA) solver. The next model cannot be built until the previous model has finished executing, and this can sometimes cause a performance bottleneck. If the model building and execution phases could be made more independent and a queuing system implemented then this may solve this performance problem.

**Skills required:** Python, CUDA

**Difficulty:** Hard

**Length:** 350hrs