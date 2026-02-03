# GSoC 2026 - Project Ideas List

gprMax is hoping to participate in the [Google Summer of Code](https://summerofcode.withgoogle.com) 2026 program, following successful GSoCs in 2019, 2021, 2023, 2024, and 2025. 

Below is list of some potential project ideas (in no particular order). These ideas have been discussed with all mentors in our team: 
- Dr Craig Warren
- Professor Antonis Giannopoulos
- Dr Iraklis Giannakis
- Miss Petroula Karacosta
- Mr Zach Wilson

If a project is successfully selected you will be allocated a primary mentor and supported by the rest of the team. If you are interested in learning more about a particular project idea please contact us using [info@gprmax.com](mailto:info@gprmax.com) or on our [Zulip channel](https://gprmax.zulipchat.com/join/stpagw5qy775k7p2tcjkkk4q/). 

## Statement on Responsible Use of AI in GSoC 2026 for gprMax

We understand that AI tools like large language models have become helpful resources in many aspects of work and learning, including proposal writing. We want to support you in using these tools responsibly while ensuring your proposal genuinely represents you.

**Ways AI Can Help:**
AI tools can be wonderful for checking grammar, improving clarity, exploring ideas, learning new concepts, and refining your writing. We encourage you to use these tools as learning partners that help you develop and express your ideas more effectively.

**What We're Looking For:**
- Proposals that reflect your authentic understanding and enthusiasm for the project
- Technical approaches that align with your actual skill level and that you're prepared to implement
- A genuine sense of who you are as a contributor and what you bring to the project
- Transparency about your capabilities so mentors can provide appropriate guidance and support

**What to Avoid:**
- Relying on AI to generate content you don't fully understand or can't explain
- Presenting technical solutions or experience levels that don't match your actual abilities
- Submitting work that doesn't reflect your own voice and thinking

**Why This Matters:**
The proposal process helps us match contributors with projects where they'll thrive and learn. When your proposal authentically represents your skills and interests, we can create better mentorship pairings and set everyone up for a successful, rewarding summer. We're excited to see your genuine ideas and to support your growth throughout GSoC.


## 1. GPU Acceleration of Plane Wave Source Formulations in gprMax

gprMax is one of the few open-source FDTD solvers that leverages a ragne of GPUs to accelerate the main FDTD update kernels. 
However, our relatively new addition of a Plane Wave (TF/SF) excitation source, using the Discrete Plane Wave (DPW) formulation, 
that was initially developed during a previous GSoC project, remains as an only CPU-based solver implementation using Cython. 

This project aims to port this (TF/SF) plane wave injection source to the GPU solvers of gprMax, 
ensuring that the entire simulation pipeline remains on the GPU, minimizing data transfer between CPU and GPU 
and maximizing throughput.

**Objectives & Deliverables:**
Develop GPU kernels - prioritising CUDA - to handle the injection of the incident field at the TF/SF interfaces.
Move the DPW 1D FDTD auxiliary Cython update (used to calculate the incident field) to the GPU.
Optimize the storage, as needed, of the TF/SF boundary fields to ensure coalesced memory access during the main update loop.
Create a small testing suite of simple models to compare the GPU-accelerated plane wave results against the existing Cython implementation to ensure numerical consistency.

**Expected outcome:** Enable the use of TF/SF sources when the user executes gprMax on a GPU 

**Skills required:** Python, GPU programming using Python bindings 

**Difficulty:** Medium

**Length:** 350 hours


## 2. Reactive Simulation & Analytics: Integrating marimo with gprMax

gprMax users typically interact with the software via terminal commands or by using
static Jupyter notebooks. Although, Jupyter notebooks are very convenient workflows based on them can 
lead to errors when parameters are changed out of order and feel cumbersome to the user. Equally, terminal 
based execution does not allow for an integrated simulation experience as it offers very limited data analysis.
 
This project aims to build a reactive, web-based dashboarding interface for gprMax using [marimo](https://marimo.io/).

By integrating marimo, we will provide users with a new concept of a "computational notebook" that doubles 
as an interactive GUI for building models, monitoring simulations in real-time, and performing 
simple data post-processing (A-scan/B-scan analysis) with synchronized plotting. The aim is to build an 
initial framework that can also be easily extended in future by its users. 


**Objectives & Deliverables:**
Create a marimo-based UI where users can adjust physical parameters (permittivity, geometry, antenna position) via sliders and see the gprMax commands or API calls 
or model preview update instantly.
Develop a reactive hook to track gprMax log files or output arrays, updating a progress bar and some selected field-preview within the notebook.
Build a library of marimo-native components for gprMax post-processing, including:
Create a set of "Reactive Recipes" for common modelling and data analysis scenarios (e.g., A-Scan or B-Scan modelling, Antenna parameters calculations, etc.).


**Expected outcome:** A reactive notebook interface for better user experience and easier adoption of gprMax for electromagnetic simulations.

**Skills required:** Python and good proficiency in numerical stacks (e.g. NumPy, Pandas, H5py), Experience with reactive programming concepts (preferably using marimo). 
Familiarity with data visualisation using Python (Plotly, Matplotlib, or Bokeh). Some basic understanding of GPR related gprMax outputs (A-Scans, B-Scans, etc.)

**Difficulty:** Medium

**Length:** 350 hours
