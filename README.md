# mlfoam
Thoughts about ML committee for OpenFOAM

## libtorch C++ API seamlessly integrated with OpenFOAM

- Simplified construction of Neural Networks (NN) in OpenFOAM. 
- Enabled RTS for activation functions. 
- Created a CI test pipeline for unit tests. 
- Simplified learning of field data in OpenFOAM
  - Learning geometric fields in OpenFOAM.
  - Learning near-boudary fields. 
  - Learning field sub-sets.
- Developed adapter class hierarchy roots for ML models in OpenFOAM
  - ML boundary condition
  - ML lagrangian models 
  - ML pressure-velocity coupling algorithm
- Document / automate workflows for hyperparameter tuning.
