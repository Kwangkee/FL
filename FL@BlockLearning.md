Back to https://github.com/Kwangkee/FL
***


BlockLearning, https://github.com/hacdias/blocklearning

***
## Chapter 4
Framework Design and Implementation

![image](https://user-images.githubusercontent.com/109835677/203715657-351bf02a-4e84-4fe2-af15-395c87f802eb.png)

5. Finally, the model owner sends a transaction to the blockchain in order to terminate the round. At this point, the smart contract checks if the majority of the aggregators agreed on the aggregation. If so, the round is marked as terminated. Otherwise, the round fails, indicating that the aggregators did not reach an agreement, which may indicate that some of the aggregators are compromised.

![image](https://user-images.githubusercontent.com/109835677/203715747-32e3853b-e737-4d67-8834-0b81b0dba763.png)

#### 4.1.1.1 Smart Contracts
The first component of the framework is the smart contracts. The smart contracts live on the blockchain and are the main means of communication between FL clients and
servers. In addition, the smart contracts hold information regarding the current status of the round, as well as the updates, scores, aggregations, among others. 

#### 4.2.1 Smart Contracts

![image](https://user-images.githubusercontent.com/109835677/203719280-702de149-7a33-4421-b856-29d5b628dd8b.png)


#### 5.2 Client Sampling

#### 5.2.1 Horizontal

In order to perform the horizontal client sampling, we used a publicly available tool [79] that supports sampling from the MNIST data set directly using the Dirichlet distribution.
>- Personalized Federated Learning Platform, https://github.com/TsingZ0/PFL-Non-IID

![image](https://user-images.githubusercontent.com/109835677/203723606-0bd6126c-0aa7-4a74-bdf3-a25f0b3480f3.png)

#### 5.2.2 Vertical

![image](https://user-images.githubusercontent.com/109835677/203723907-6811dfa4-48bc-41d7-8823-f3f18650ccf7.png)

#### 5.4 Hardware and Software Specifications
![image](https://user-images.githubusercontent.com/109835677/203725101-f4615a3f-3fab-4252-b089-08a8e7cb8d51.png)

#### 5.5.3 Model Accuracy
To compare the model accuracy, we use a global Accuracy metric for the FL model, where the model owner, that is, the one that initiates the process, has **some data set with which it can test the model.** The logs produced by the model owner contain the accuracy and are used to extract the accuracy of each round.

#### Chapter 6
Impact Analysis of Consensus Algorithms

#### Chapter 7
Impact Analysis of Participant Selection and Scoring Algorithms in Horizontal Blockchain-based Federated Learning

#### Chapter 8
Proof of Concept of Vertical Blockchain-based Federated Learning

#### Chapter 9
Conclusions and Future Directions

