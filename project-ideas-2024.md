# GSoC 2024 - Project Ideas List

gprMax is hoping to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2024 program, following a successful GSoCs in 2019, 2021, and 2023. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Dr Antonis Giannopoulos
- Dr Iraklis Giannakis
- Dr Rania Patsia

If a project is successfully selected you will be allocated a primary mentor and supported by the rest of the team. If you are interested in learning more about a particular project idea please contact us using [info@gprmax.com](mailto:info@gprmax.com) or on our [gprMax Slack channel](https://gprmax-fdtd.slack.com). 


## 1. AI Chatbot for support

The aim of the project is to develop an AI chatbot that can handle basic questions and enquiries about gprMax.

We currently have a vibrant user community that engage with the development team through our [GitHub issue tracker](https://github.com/gprMax/gprMax/issues) and our [Google group](https://groups.google.com/g/gprmax). This project will consider harvesting question and answer data from our Google group to train an AI chatbot that can provide automated responses to basic support questions about gprMax.

**Expected outcomes:** A functional AI chatbot that can handle basic gprMax support queries.

**Skills required:** Python, machine learning

**Difficulty:** Medium

**Length:** 350hrs


## 2. Apple Metal port

The aim of the project is to develop an [Apple Metal](https://developer.apple.com/metal/) port. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. The project will require porting existing code, either from the PyCUDA or PyOpenCL-based solvers we already have, to the Apple Metal framework.

**Expected outcomes:** An initial working port of the FDTD solver engine for gprMax using Apple Metal.

**Skills required:** Python, C

**Difficulty:** Medium

**Length:** 350hrs


## 3. Optimisation of CUDA and OpenCL performance

The aim of the project is to optimise our CUDA and OpenCL based solvers. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. We have solvers written using [PyCUDA](https://github.com/inducer/pycuda) and [PyOpenCL](https://github.com/inducer/pyopencl). The speed-up can be significant (x30 compared with CUDA compared to OpenMP parallelised CPU), but we would like to further tune and optimise the performance. 

**Expected outcomes:** Benchmarks and improvements to the performance of the current CUDA and OpenCL based solvers.

**Skills required:** Python, CUDA

**Difficulty:** Medium

**Length:** 175hrs


## 4. Optimisation of OpenMP performance on Apple silicon hardware

The aim of this project is to maximise the performance of gprMax on Apple silicon hardware.

gprMax is predominately written in Python, but some of the performance-critical parts of the code are written in [Cython](https://cython.org), which must be built and compiled. For CPU-based parallelisation, Cython uses OpenMP, which has worked well on Intel-based CPUs using gcc (Linux/macOS) and Microsoft Visual Studio compilers. However, this project will explore how to best optimise gprMax for running on Apple silicon CPUs.

**Expected outcomes:** Benchmarks and improvements to the performance of the current OpenMP based solver.

**Skills required:** Python, tools and compilers macOS operating systems.

**Difficulty:** Medium

**Length:** 175hrs


## 5. Performance gains through memory usage and cache access

The aim of this project is to optimise the performance of the CPU-based solver through investigation of memory and cache accessing.

gprMax is predominately written in Python, but some of the performance-critical parts of the code are written in [Cython](https://cython.org), which must be built and compiled. The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, whose performance is largely limited by memory bandwidth. This project will look at strategies to improve memory and cache access such as the [FDTD XPU technology](https://ieeexplore.ieee.org/abstract/document/7481533).

**Expected outcomes:** Benchmarks and improvements to the performance of the current CPU solver through optimisation memory and cache access.

**Skills required:** Python, compilers and benchmarking tools on multiple (Linux, Windows, macOS) operating systems

**Difficulty:** Medium

**Length:** 350hrs


## 6. De-coupled model building and execution

The aim of this project is to investigate de-coupling the model building and execution phases.

Currently the modeling building phase takes place (which is mostly a serial process) on CPU. Once that is complete the model can then be executed using either the CPU-based (OpenMP) or GPU-based (CUDA) solver. The next model cannot be built until the previous model has finished executing, and this can sometimes cause a performance bottleneck. If the model building and execution phases could be made more independent and a queuing system implemented then this may solve this performance problem.

**Expected outcomes:** An initial framework and basic working model that demonstrates de-coupled model building and running behaviour.

**Skills required:** Python, CUDA

**Difficulty:** Hard

**Length:** 350hrs