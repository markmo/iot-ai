# AI on IoT

Potential requirements:

1. Federated data ownership / Federated Machine Learning
   * ML using remote datasets; i.e. we want to train a model on data, with permission of the data owner,
     without having a local copy of the data
   * Why useful? Parties in a supply chain want to retain ownership of and protect their data while
     benefiting from ML models trained on all data that optimise the supply chain as a whole.
   * Encryption Using Secure Multi-Party Computation (SMPC) requires a third party to be trusted to 
     not collude with any of the existing parties.
   * See [markmo/federated_learning](https://github.com/markmo/federated_learning) for a proof of concept.
   
2. Enhanced automation, transparency and traceability in the supply chain
   * Increase volume of data collection while maintaining trust
   * See [markmo/foodchain](https://github.com/markmo/foodchain) for a proof of concept.
    

Possible solutions:

1. [PySyft](https://github.com/OpenMined/PySyft) from [OpenMined](https://www.openmined.org/).
2. [Hyperledger Fabric](https://www.hyperledger.org/) from the Linux Foundation.