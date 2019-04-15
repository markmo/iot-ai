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
   
2. Privacy Preserving Machine Learning
   * Federated Learning
   * Secure Multiparty Computation
   * Differential Privacy
   
   While the privacy features apart from Differential Privacy do not impact the prediction accuracy, 
   the current implementation of the framework introduces an overhead in performance.

3. Enhanced automation, transparency and traceability in the supply chain
   * Increase volume of data collection while maintaining trust
   * See [markmo/foodchain](https://github.com/markmo/foodchain) for a proof of concept.
   
3. Scalability
   * Intel Secure Guard Extensions (SGX)
    

Possible solutions:

1. [PySyft](https://github.com/OpenMined/PySyft) from [OpenMined](https://www.openmined.org/).
2. [Hyperledger Fabric](https://www.hyperledger.org/) from the Linux Foundation.


Notes:

Some adjustments are made to the traditional elements of a convolutional network due to the specificities 
of Multiparty Computation (MPC): average pooling is used instead of max pooling and approximate higher-degree 
sigmoid instead of relu as an activation function.

The PySyft implementation uses the [SPDZ protocol](https://mortendahl.github.io/2017/09/03/the-spdz-protocol-part1/).
Since the SPDZ protocol assumes that the data is given as integers, we added into the chain a node
called the FixedPrecisionTensor that converts float numbers into fixed precision numbers. This node
encodes the value into an integer and stores the position of the radix point.


Thoughts:

So far, the PySyft implementation does not come with a mechanism to ensure that every player
behaves honestly. Could we use Blockchain for secure MPC. 


References:

1. [A generic framework for privacy preserving deep learning](https://arxiv.org/pdf/1811.04017.pdf), Trask et al.
2. [Multiparty Computation from Somewhat Homomorphic Encryption](https://eprint.iacr.org/2011/535.pdf).
