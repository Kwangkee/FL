Back to https://github.com/Kwangkee/FL
***

## Papers 
- [[RL-Based Federated Learning Framework Over Blockchain (RL-FL-BC)](https://github.com/Kwangkee/FL/blob/main/BCFL.md#rl-fl-bc)], https://ieeexplore.ieee.org/abstract/document/10034683  

- Privacy-Preserving Blockchain-Based Federated Learning for IoT Devices, https://ieeexplore.ieee.org/abstract/document/9170559
>- To help manufacturers develop a smart home system, we design a federated learning (FL) system leveraging a reputation mechanism to assist home appliance manufacturers to train a machine learning model based on customers’ data. Then, manufacturers can predict customers’ requirements and consumption behaviors in the future. 

- TrustFed: A framework for fair and trustworthy cross-device federated learning in IIoT, https://scholar.google.co.kr/scholar?hl=ko&as_sdt=0%2C5&q=TrustFed%3A+A+Framework+for+Fair+and+Trustworthy+Cross-Device+Federated+Learning+in+IIoT&btnG=
>- Cross-device federated learning (CDFL) systems 
>- TrustFed provides fairness by detecting and removing the attackers from the training distributions. It uses blockchain smart contracts to maintain participating devices' reputations to compel the participants in bringing active and honest model contributions. 
>- We implemented the TrustFed using a Python-simulated federated learning framework, blockchain smart contracts, and statistical outlier detection techniques. We tested it over the large-scale industrial Internet of things dataset and multiple attack models. 
>- https://github.com/habibcomsats/TrustFed

***

## RL-FL-BC
RL-Based Federated Learning Framework Over Blockchain (RL-FL-BC), https://ieeexplore.ieee.org/abstract/document/10034683

- To this end, the contributions of this paper are summarized as follows:
>- We propose and implement an Ethereum private Blockchain to share among participants the machine learning model parameters generated from data centers, in order to facilitate the trust between data owners and preserve participant privacy,
>- We design and implement a protocol for the decentralization of the machine learning model aggregations through Blockchain,
>- We propose an RL-based algorithm to address the tradeoff between transaction cost, learning information age, and data skewness, i.e., non-iid,
>- We develop a complete framework in a containerized environment and conduct a comprehensive comparative study to compare our solution with baselines techniques.

- In this work, we tried to optimize the BC-based federated learning system to address the trade-off between transaction cost, learning information age, and data skewness. In doing that we designed a protocol to facilitate the exchange of key parameters between blockchain participants (nodes). The agent running within the smart contract can use these parameters to optimize the performance.

***
Back to the [Top](#papers)  
Back to https://github.com/Kwangkee/FL
