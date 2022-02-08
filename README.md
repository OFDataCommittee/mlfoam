# OpenFOAM special interest group on data-driven modeling

All activities of the official OpenFOAM special interest group (SIG) on data-driven modeling are currently organized in this repository.

## Current activities

### Collection of resources

The following documents contain curated lists of contents related to data-driven modeling and OpenFOAM. You are very welcome to [extend these lists](CONTRIBUTING.md).

- [research projects](research.md)
- [software projects](software.md)
- [educational material](education.md)

### Committee meetings

Meetings take place about every two month. Get in touch if you would like to participate.

- Feb 8 2022, online, [slides](https://andreweiner.github.io/reveal.js/ofml_tc_1.html#/)

## Our scope and objectives in a nutshell

For us, data-driven modeling comprises a variety of different topics, some of which are listed below:
- machine learning (ML): combining CFD and ML, e.g., using ML models in CFD or deriving ML models from CFD data
- data science: analyzing CFD data to guide modeling and decision making
- data engineering: aggregating, storing, and processing CFD data

The following list briefly summarizes our current objectives. The technical roadmap below details **how** we plan to achieve our objectives.

- short term objectives
  - reduce the technical barrier to get started with data-riven modeling in OpenFOAM to enable more people to include data-driven workflows in their applications or research
  - promote data-driven techniques that are already available in OpenFOAM, e.g., dynamic mode decomposition (DMD)
  - promote third-party library for data-driven modeling that are based on or built for OpenFOAM
- long term objectives
  - aid the understanding of when and how to use data-driven modeling in the CFD workflow
  - accelerate developments and applications of data-driven approaches around OpenFOAM
  - establish tested data-driven techniques as a natural element of CFD simulations to improve accuracy and/or speed

## Current committee members

- Andre Weiner, TU Braunschweig, GER **(chair)**
- Dirk Gründing, TU Darmstadt, GER
- Holger Marschall, TU Darmstadt, GER
- Karthik Kashinath, Nvidia, USA
- Neil Ashton, Amazon Web Services, UK
- Tomislav Marić, TU Darmstadt, GER **(co-chair)**

If you are interest in contributing to this SIG, feel free to get in touch.

## Workflow

We would like to have short virtual meetings (max. 1h) every **two** month and meet in person, if possible, at the OpenFOAM conference and workshop. The bi-monthly meetings serve to update all members about the recent progress and to coordinate upcoming efforts. Everybody is welcome to join our meetings.

## Technical roadmap

This section lists several steps to achieve the objectives outlined before. The list is mostly motived by the initiator's previous experience and current projects, and presents by no means a comprehensive list of all possibilities for data-driven modeling with OpenFOAM.

- integration of the PyTorch C++ API [libtroch](https://pytorch.org/cppdocs/installing.html) with OpenFOAM; libtorch can be used to execute existing PyTorch ML models in OpenFOAM but also to implement the entire ML workflow in C++ (data-processing, training, hyperparameter tuning, ...) 
  - adjustment of the default OpenFOAM C++ standard, e.g, C++11 -> C++14
  - third-party install script to compile and set up libtorch
  - simplify construction of standard neural network architectures with runtime-selectable components
  - normalization of data as part of ML pipeline
  - adapters for OpenFOAM field data to work with
    - full geometric fields
    - boundary fields
    - sub-sets of fields
  - base class adapters with support for ML models, e.g.,
    - boundary conditions
    - Lagrangian models
    - pressure-velocity coupling
    - ...
   - high-performance enabled computations with OpenFOAM and libtorch
     - distributed training with geometric field data
     - offload workloads to GPU(s)
- provide an accessible interface between OpenFOAM and Python; Python is the most widely used programming language for data analysis and ML; therefore, there should be an easy way to access OpenFOAM data in Python; there exist a number of Python packages to access OpenFOAM data, but for all of them at least one of the following points applies: only partial access, bad or missing documentation, overly complicated access to data, no active development or support, not applicable to large data (too slow/inefficient); a few options that could be explored are
  - improve documentation of existing packages
  - continue development of packages with partial access
  - create Python bindings for selected OpenFOAM classes
- compile and create documentation and tutorials
  - OpenFOAM tutorials demonstrating how to enable ML with OpenFOAM
  - open-source research projects and proposals around OpenFOAM and ML
  - blog posts, presentations, videos
  - lecture material
- organize an OpenFOAM + ML hackathon once a year

## How to get in touch

If you would like to contribute to this repository, provide additional ideas or spark up a discussion, the most direct way to get in touch is to open an issue at:

[https://github.com/AndreWeiner/mlfoam](https://github.com/AndreWeiner/mlfoam)
