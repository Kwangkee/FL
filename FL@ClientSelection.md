Back to https://github.com/Kwangkee/FL
***

## Papers 

- [Oort: Informed Participant Selection for Scalable Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL%40ClientSelection.md#oort), https://arxiv.org/abs/2010.06081
  >- [FedScale](https://github.com/Kwangkee/FL/blob/main/FL%40ClientSelection.md#fedscale) 로 진화/발전!!!

- Client selection in federated learning: Convergence analysis and power-of-choice selection strategies, https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#yae-jee-cho

- Client Selection for Federated Learning With Non-IID Data in Mobile Edge Computing, https://www.researchgate.net/publication/349012712_Client_Selection_for_Federated_Learning_With_Non-IID_Data_in_Mobile_Edge_Computing

- [원문 못 구함] Contribution-based Federated Learning client selection, https://onlinelibrary.wiley.com/doi/10.1002/int.22879?af=R
  >Github: https://github.com/xuyinhai22/Client-selection-of-Federated-Learning  
  >Our algorithm CBE3 is based on the federal learning framework [Flsim](https://github.com/Kwangkee/FL/blob/main/FL%40Meta.md#federated-learning-simulator-flsim).
  
  >In this paper, we propose the contribution-based selection algorithm (Contribution-Based Exponential-weight algorithm for Exploration and Exploitation, CBE3), which dynamically updates the selection weights according to the impact of clients' data. As a novel component of CBE3, a scaling factor, which helps maintain a good balance between global model accuracy and convergence speed, is proposed to improve the algorithm's adaptability.  
  >Empirically, extensive experiments conducted on Non-Independent Identically Distributed data demonstrate the superior performance of CBE3—with up to 10% accuracy improvement compared with K-Center and Greedy and up to 100% faster convergence compared with the Random algorithm.

- Stochastic Client Selection for Federated Learning with Volatile Clients, https://arxiv.org/abs/2011.08756  

- Learning Advanced Client Selection Strategy for Federated Learning, https://aaai-2022.virtualchair.net/poster_aaai12714

## ETC
- Client Selection@Awesome Federated Machine Learning
https://github.com/innovation-cat/Awesome-Federated-Machine-Learning#15-client-selection

- Multi-armed bandit-based client scheduling for federated learning, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Multi-Armed-Bandit-Based-Client-Scheduling-for-Federated-Learning&btnG=

- Client selection for federated learning with heterogeneous resources in mobile edge, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Client+Selection+for+Federated+Learning+with+Heterogeneous+Resources+in+Mobile+Edge&btnG=
- 
- [원문 못 구함] VFedCS: Optimizing Client Selection for Volatile Federated Learning, https://ieeexplore.ieee.org/abstract/document/9846900
- A Contribution-based Device Selection Scheme in Federated Learning, https://arxiv.org/abs/2203.05369

## Large-Scale

- Characterizing Impacts of Heterogeneity in Federated Learning upon Large-Scale Smartphone Data, https://arxiv.org/abs/2006.06983v3  
  >https://github.com/PKU-Chengxu/FLASH  

***

## Oort
Oort: Informed Participant Selection for Scalable Federated Learning, https://arxiv.org/abs/2010.06081

- https://www.usenix.org/conference/osdi21/presentation/lai     
  >Presentation Video: https://www.youtube.com/watch?v=5npOel4T4Mw  
  >slides: https://www.usenix.org/system/files/osdi21_slides_lai.pdf  
  
  >As a result, data characteristics and device capabilities vary widely across clients. Yet, existing efforts randomly select FL participants, which leads to poor model and system efficiency. In this paper, we propose Oort to improve the performance of federated training and testing with guided participant selection. With an aim to improve time-to-accuracy performance in model training, Oort prioritizes the use of those clients who have both data that offers the greatest utility in improving model accuracy and the capability to run training quickly.  
  
  >Consequently, a fundamental problem in practical FL is the *selection of a “good” subset of clients as participants*, where each participant locally processes its own data, and only their results are collected and aggregated at a (logically) centralized coordinator.

- Oort is available at https://github.com/SymbioticLab/Oort
  >- This repo is outdated and no longer actively maintained. Instead, Oort has been merged as part of [FedScale](https://github.com/SymbioticLab/FedScale), a diverse set of challenging and realistic FL benchmark. Please try it!
  >- FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367
  >- Harsha Madhyastha, https://scholar.google.com/citations?hl=ko&user=kxDm9EsAAAAJ&view_op=list_works&sortby=pubdate 
  
#### Issue: loss-based statistical utility design
  >As such, we consider clients that currently accumulate a bigger loss to be more important for future rounds.  
  >>Our statistical utility can capture the heterogeneous data utility across and within categories and samples for various tasks. We present the theoretical proof for its effectiveness over random sampling in our technical report [45], and empirically show its close-to-optimal performance (§7.2.2).
  >>>By taking account of the oracle and the effectiveness of loss-based approximation, we propose our loss-based statistical
utility design, whereby we achieve the close to upper-bound statistical performance (§7.2.2).

#### Issue: MAB (Multi-Armed Bandit) problem, exploration-exploitation
  >Online exploration-exploitation of high-utility clients. 
  >>Selecting participants out of numerous clients can be modeled as a **multi-armed bandit problem**, where each client is an “arm” of the bandit, and the utility obtained is the “reward” [14]. In contrast to sophisticated designs (e.g., reinforcement learning), the bandit model is scalable and flexible even when the solution space (e.g., number of clients) varies dramatically over time. 
  >
  >>Next, we adaptively balance the exploration and exploitation of different arms to maximize the long-term reward.
  

## FedScale 
A scalable and extensible federated learning engine and benchmark, http://fedscale.ai/  
FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367  
Swan: A Neural Engine for Efficient DNN Training on Smartphone SoCs, https://arxiv.org/abs/2206.04687   

FedScale, https://github.com/symbioticlab/fedscale
>- FedScale Benchmarking Datasets, https://github.com/SymbioticLab/FedScale/tree/master/benchmark/dataset
>- FedScale Runtime: A Deployment and Evaluation Platform for Federated Learning, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/core
>- Setup Android Edge Device From Scratch, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/deploy/mobile

#### FedScale Repo Structure

```
Repo Root
|---- fedscale          # FedScale source code
  |---- core            # Core of FedScale service
  |---- utils           # Auxiliaries (e.g, model zoo and FL optimizer)
  |---- deploy          # Deployment backends (e.g., mobile)
  |---- dataloaders     # Data loaders of benchmarking dataset

|---- benchmark         # FedScale datasets and configs
  |---- dataset         # Benchmarking datasets

|---- examples          # Examples of implementing new FL designs
|---- docs              # FedScale tutorials and APIs
```

***
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
