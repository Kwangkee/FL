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

