# mlfoam

Thoughts about ML committee for OpenFOAM

## Interoperability of OpenFOAM and other ML software

### foamtorch: libtorch C++ API seamlessly integrated with OpenFOAM

- Simplified construction of libtorch Neural Networks (NN) in OpenFOAM. 
- Enabled RTS for activation functions. 
- Created a CI test pipeline for unit tests. 
- Simplified learning of field data in OpenFOAM (libtorch - OpenFOAM adapters)
  - Learning geometric fields in OpenFOAM.
  - Learning near-boudary fields. 
  - Learning field sub-sets.
- Developed adapter class hierarchy roots for ML models in OpenFOAM
  - ML boundary condition
  - ML lagrangian models 
  - ML pressure-velocity coupling algorithm
- High-Performance Computing with OpenFOAM and libtorch
  - Learning OpenFOAM geometric fields in parallel
  - Offloading to the GPU 
  - Global training vs weak NN conditions on process boundaries
- Documentation 
  - Tutorial cases:
    1. Learning a pressure field (internal field)
    2. Learning a boundary field (BCs)
    3. Learning a surface (sub-set of a geometric field)
  - Workflows for hyperparameter tuning.
