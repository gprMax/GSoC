# GSoC 2025 - Project Ideas List

gprMax is hoping to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2025 program, following successful GSoCs in 2019, 2021, 2023, and 2024. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Dr Antonis Giannopoulos
- Dr Iraklis Giannakis

If a project is successfully selected you will be allocated a primary mentor and supported by the rest of the team. If you are interested in learning more about a particular project idea please contact us using [info@gprmax.com](mailto:info@gprmax.com) or on our [Zulip channel](https://gprmax.zulipchat.com/join/stpagw5qy775k7p2tcjkkk4q/). 


## 1. AI Chatbot for support

This project will build upon the work done in the previous GSoC where an AI chatbot was developed capable of answering questions and assisting on building models with gprMax. For more information you can check the following [link](https://github.com/eddieleejw/gprmax_chatbot).

The developed chatbot is based on ChatGPT from OpenAI, therefore it is not free. The current project will aim at building light chatbots using open-source LLMs such as Lama and Deepsheek, in order to provide a free and computationally cheap chatbot for gprMax. 

Moreover, the next generation of gprMax AI chatbots will be capable of building models automatically based on some given instructions. We currently have a [set of gprMax commands](https://huggingface.co/datasets/IraGia/gprMax_Train) that we can use to fine-tune open-source LLMs. 

To summarise, this project will aim at building AI chatbots based on open-source LLMs, and fine-tune them not only to answer questions related to gprMax, but also to automatically build full gprMax models based on simple and intuitive instrustions by the user.

**Expected outcomes:** A functional AI chatbot based on open-source LLMs capable of automatically developing gprMax models using simple written commands.

**Skills required:** Python, machine learning

**Difficulty:** Medium

**Length:** 350hrs


## 2. Apple Metal port

The aim of the project is to develop an [Apple Metal](https://developer.apple.com/metal/) port. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. The project will require building on the already existing initial Apple Metal port and developing and testing it to ensure all main features in gprMax execute correctly and efficiently.

**Expected outcomes:** A working port of the FDTD solver engine for gprMax using Apple Metal.

**Skills required:** Python, C

**Hardware required:** You must have your own access to Apple hardware.

**Difficulty:** Medium

**Length:** 350hrs


## 3. AMD ROCm HIP port

The aim of the project is to develop an [HIP](https://github.com/ROCm/HIP) port. The performance (speed) of the solver is a critical feature as simulations become ever larger and more complex.

The solver is based on the [Finite-Difference Time-Domain (FDTD)](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method) method, which has shown significant performance benefits when parallelised – particularly on GPU. The project will require porting existing code from the PyCUDA-based solver we already have, to the HIP API. There are automated translation tools, such as [HIPIFY](https://github.com/ROCm/HIPIFY) that can be used to support the process.

**Expected outcomes:** An initial working port of the FDTD solver engine for gprMax using HIP.

**Skills required:** Python, C

**Hardware required:** You must have your own access to an AMD GPU.

**Difficulty:** Medium

**Length:** 350hrs


## 4. Implementation of a Near to Far Field Transformation (NFFT) calculation and output of relevant information

The aim of this project is to implement a Near-to-far-field Transformation output process in gprMax based in well known theory and an existing algorithm. 

NFFT outputs are needed when information of the electromagnetic field response is needed far away from the object of interest modelled in detail by gprMax using the FDTD numerical mehtod.Initially we need to implement such a process, which is well documented in the literature and algorithmically available, for objects located in a simple homogenous background. This feature will allow us to easily perform an number of additional modelling tasks like radar cross section (RCS) calcualtions and complicated antenna patterns that are not possible at the moment. 

**Skills required:** Python

**Difficulty:** Medium

**Length:** 350hrs
