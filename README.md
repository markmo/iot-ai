# AI on IoT

Potential requirements:

1. Federated data ownership / Federated Learning
   * ML using remote datasets; i.e. we want to train a model on data, with permission of the data owner,
     without having a local copy of the data
   * Why useful? Parties in a supply chain want to retain ownership of and protect their data while
     benefiting from ML models trained on all data that optimise the supply chain as a whole.
   * Encryption Using Secure Multi-Party Computation (SMPC) requires a third party to be trusted to 
     not collude with any of the existing parties. 
    

Possible solutions:

1. [PySyft](https://github.com/OpenMined/PySyft) from [OpenMined](https://www.openmined.org/).