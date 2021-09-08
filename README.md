# OpenFOAM technical committee on data-driven modeling

This document represents a draft roadmap for the potential initiation of a technical committee on data-driven modeling with OpenFOAM. The structure of this documents mirrors the wiki pages of [existing technical committees](https://www.openfoam.com/governance/technical-committees).

## Our objectives in a nutshell

This section briefly summarizes **why** we would like to initiate a technical committee on data-driven modeling. The technical roadmap details **how** we plan to achieve our objectives.

- short term objectives
  - reduce the technical barrier to get started with data-riven modeling in OpenFOAM to enable more people to include data-driven workflows in their applications or research
  - promote data-driven techniques that are already available in OpenFOAM, e.g., dynamic mode decomposition (DMD)
- long term objectives
  - aid the understanding of when to use data-driven models in the CFD workflow
  - accelerate developments and applications of machine learning (ML) with OpenFOAM
  - establish tested ML models as a natural element of CFD simulations to improve accuracy and/or speed

## Potential workflow

We would like to have short virtual meetings (max. 1h) every **two** month and meet in person, if possible, at the OpenFOAM conference and workshop. The bi-monthly meetings serve to update all members about the recent progress and to coordinate upcoming efforts.

## Interaction with existing committees

Data-driven modeling and in particular machine learning is going to touch every aspect CFD with OpenFOAM and requires coordination with all other technical committees. We still need to clarify if our objectives and efforts might be embedded in an existing committee, or if a new committee should be formed that coordinates with existing ones whenever necessary. Our currently preferred mode would be to get in touch with the most suitable available committee when new developments are available (tutorials, models, numerics, ...), but to organize and bundle all efforts within separate committee. Otherwise, transferable technical and practical knowledge might be too scattered.

To find the most suitable structure, we will get in touch with the existing committees.

## Technical roadmap

This section lists several steps to achieve the objectives outlined before.

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
- provide an easy to use interface between OpenFOAM and Python; Python is the most widely used programming language for data analysis and ML; therefore, there should be an easy way to access OpenFOAM data in Python; there exist a number of Python packages to access OpenFOAM data, but for all of them at least one of the following points applies: only partial access, bad or missing documentation, overly complicated access to data, no active support, not applicable to large data (too slow/inefficient); a few options that could be explored are
  - improve documentation of existing packages
  - continue development of packages with partial access
  - create Python bindings for selected OpenFOAM classes
- compile and create documentation and tutorials
  - OpenFOAM tutorials demonstrating how to enable ML with OpenFOAM
  - open-source research projects around OpenFOAM and ML
  - blog posts, presentations, videos
  - lecture material

## How to get in touch

The idea for the new technical committee is currently worked out and put forward by

- Tomislav Marić, TU Darmstadt, Germany
- Andre Weiner, TU Braunschweig, Germany

If you would like to contribute to this roadmap, provide additional ideas or spark up a discussion, the most direct way to get in touch would be to open an issue in this repository.
