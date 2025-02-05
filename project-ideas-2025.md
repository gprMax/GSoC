# GSoC 2025 - Project Ideas List

gprMax is hoping to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2025 program, following successful GSoCs in 2019, 2021, 2023, and 2024. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Dr Antonis Giannopoulos
- Dr Iraklis Giannakis

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

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. The project will require building on the already existing initial Apple Metal port and developing and testing it to ensure all main features in gprMax execute correctly and efficiently.

**Expected outcomes:** A working port of the FDTD solver engine for gprMax using Apple Metal.

**Skills required:** Python, C

**Difficulty:** Medium

**Length:** 350hrs


## 3. AMD ROCm HIP port

The aim of the project is to develop an [HIP](https://github.com/ROCm/HIP) port. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. The project will require porting existing code from the PyCUDA-based solver we already have, to the HIP API. There are automated translation tools, such as [HIPIFY](https://github.com/ROCm/HIPIFY) that can be used to support the process.

**Expected outcomes:** An initial working port of the FDTD solver engine for gprMax using HIP.

**Skills required:** Python, C

**Difficulty:** Medium

**Length:** 350hrs