Back to https://github.com/Kwangkee/FL
***

## Papers 

- [[Oort: Informed Participant Selection for Scalable Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#oort)], https://arxiv.org/abs/2010.06081
  >- Now merged as part of [FedScale](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#fedscale)

- [Contribution-based selection algorithm (Contribution-Based Exponential-weight algorithm for Exploration and Exploitation, CBE3)](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#cbe3)

- Client selection in federated learning: Convergence analysis and power-of-choice selection strategies, https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#yae-jee-cho

- [[FedBalancer: Data and Pace Control for Efficient Federated Learning on Heterogeneous Clients (ACM MobiSys 2022)](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#fedbalancer)], https://dl.acm.org/doi/abs/10.1145/3498361.3538917 
 

## ETC

- [FedCS] Client selection for federated learning with heterogeneous resources in mobile edge, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Client+Selection+for+Federated+Learning+with+Heterogeneous+Resources+in+Mobile+Edge&btnG=
  >Specifically, FedCS solves a client selection problem with resource constraints, which allows the server to aggregate as many client updates as possible and to accelerate performance improvement in ML models. We conducted an experimental evaluation using publicly-available large-scale image datasets to train deep neural networks on MEC environment simulations. The experimental results show that FedCS is able to complete its training process in a significantly shorter time compared to the original FL protocol.

- Federated learning with workload-aware client scheduling in heterogeneous systems, https://www.sciencedirect.com/science/article/abs/pii/S0893608022002957

- Client Selection for Federated Learning With Non-IID Data in Mobile Edge Computing, https://www.researchgate.net/publication/349012712_Client_Selection_for_Federated_Learning_With_Non-IID_Data_in_Mobile_Edge_Computing

- Multi-armed bandit-based client scheduling for federated learning, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Multi-Armed-Bandit-Based-Client-Scheduling-for-Federated-Learning&btnG=

- A Contribution-based Device Selection Scheme in Federated Learning, https://arxiv.org/abs/2203.05369

- Learning Advanced Client Selection Strategy for Federated Learning, https://aaai-2022.virtualchair.net/poster_aaai12714

- Client Selection@Awesome Federated Machine Learning
https://github.com/innovation-cat/Awesome-Federated-Machine-Learning#15-client-selection

  
***

## Oort
Oort: Informed Participant Selection for Scalable Federated Learning, https://arxiv.org/abs/2010.06081

- https://www.usenix.org/conference/osdi21/presentation/lai     
  >Presentation Video: https://www.youtube.com/watch?v=5npOel4T4Mw  
  >slides: https://www.usenix.org/system/files/osdi21_slides_lai.pdf  
  
  >As a result, data characteristics and device capabilities vary widely across clients. Yet, existing efforts randomly select FL participants, which leads to poor model and system efficiency. In this paper, we propose Oort to improve the performance of federated training and testing with guided participant selection. **With an aim to improve time-to-accuracy performance in model training, Oort prioritizes the use of those clients who have both data that offers the greatest utility in improving model accuracy and the capability to run training quickly**.  
  
  >Consequently, a fundamental problem in practical FL is the *selection of a “good” subset of clients as participants*, where each participant locally processes its own data, and only their results are collected and aggregated at a (logically) centralized coordinator.

- Oort is available at https://github.com/SymbioticLab/Oort
  >- This repo is outdated and no longer actively maintained. Instead, Oort has been merged as part of [FedScale](https://github.com/SymbioticLab/FedScale), a diverse set of challenging and realistic FL benchmark. Please try it!
  >- FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367
  >- Harsha Madhyastha, https://scholar.google.com/citations?hl=ko&user=kxDm9EsAAAAJ&view_op=list_works&sortby=pubdate 
  
#### 주요 아이디어: loss-based statistical utility design
  >As such, we consider clients that currently accumulate a bigger loss to be more important for future rounds.  
  >>Our statistical utility can capture the heterogeneous data utility across and within categories and samples for various tasks. We present the theoretical proof for its effectiveness over random sampling in our technical report [45], and empirically show its close-to-optimal performance (§7.2.2).
  >>>By taking account of the oracle and the effectiveness of loss-based approximation, we propose our loss-based statistical
utility design, whereby we achieve the close to upper-bound statistical performance (§7.2.2).

#### 주요 아이디어: MAB (Multi-Armed Bandit) problem, exploration-exploitation
  >Online exploration-exploitation of high-utility clients. 
  >>Selecting participants out of numerous clients can be modeled as a **multi-armed bandit problem**, where each client is an “arm” of the bandit, and the utility obtained is the “reward” [14]. In contrast to sophisticated designs (e.g., reinforcement learning), the bandit model is scalable and flexible even when the solution space (e.g., number of clients) varies dramatically over time. 
  >
  >>Next, we adaptively balance the exploration and exploitation of different arms to maximize the long-term reward.
  

## FedScale 
A scalable and extensible federated learning engine and benchmark, http://fedscale.ai/  
#### FedScale
FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367  
#### Swan
Swan: A Neural Engine for Efficient DNN Training on Smartphone SoCs, https://arxiv.org/abs/2206.04687   
>• Swan is built within Termux, a Linux Terminal emulator for Android, and can efficiently train unmodified PyTorch models.

#### FedScale, https://github.com/symbioticlab/fedscale
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

## CBE3

### Contribution-based Federated Learning client selection, https://onlinelibrary.wiley.com/doi/10.1002/int.22879?af=R  
- https://onlinelibrary.wiley.com/doi/full/10.1002/int.22879?casa_token=wSdU803SnX0AAAAA%3AHBvDCzTClNGB1PavHfnxm_nUy2L9E500PRB3nmQ56ohnQkJvqs6y-CA-s512jrNb6HYT-sNr6HfGRGqT  
- https://onlinelibrary.wiley.com/doi/epdf/10.1002/int.22879  
- Github: https://github.com/xuyinhai22/Client-selection-of-Federated-Learning  
  
Our algorithm CBE3 is based on the federal learning framework [Flsim](https://github.com/Kwangkee/FL/blob/main/FL%40Meta.md#federated-learning-simulator-flsim).
  >In this paper, we propose the **contribution-based selection algorithm (Contribution-Based Exponential-weight algorithm for Exploration and Exploitation, CBE3)**, which dynamically updates the selection weights according to the impact of clients' data. As a novel component of CBE3, a scaling factor, which helps maintain a good balance between global model accuracy and convergence speed, is proposed to improve the algorithm's adaptability.  
  >Empirically, extensive experiments conducted on Non-Independent Identically Distributed data demonstrate the superior performance of CBE3—with up to 10% accuracy improvement compared with K-Center and Greedy and up to 100% faster convergence compared with the Random algorithm.

- **[The random selection algorithm and FedCS selection(greedy) algorithm)]** ignore the local data quality of the clients and are unable to reduce the number of selections for clients with poor quality of data, which leads to low accuracy of global model and slow convergence.  
- Recently, some researchers have attempted to address the problem of unfair client selection and large bias in data distribution by assigning fairness factors to clients to ensure that all clients have a certain probability of being selected.10, 11 Experimental results show that the **[fairness-based client selection algorithm]** can reduce the risk of overfitting while ensuring training efficiency when appropriate fairness values are chosen.   
>[11] Stochastic Client Selection for Federated Learning with Volatile Clients, https://arxiv.org/abs/2011.08756   

>However, the current fairness studies involved suffer from several flaws: (1) They blindly impose fairness constraints for each client while ignoring the actual contributions of those clients. (2) Fairness quotas need to be assigned before training and that particular metric may have a profound impact on the performance of the algorithm. When the fairness quota is set too low, the algorithm approaches greedy selection, which does not guarantee that all of the clients' local data will be learned efficiently; when the quota is set too high, the algorithm approaches random selection, which can lead to severe overfitting of some of the clients' data. In short, an inappropriate fairness quota can severely reduce the training effectiveness of the algorithm. Inspired by the current literature, this paper aims to propose a new and improved algorithm that can overcome the above-mentioned drawbacks.   
- The goal of federal learning client selection is to select superior clients who accelerate the convergence of the global model and improve global model accuracy while remaining within bandwidth limits. This paper is goal-oriented and directly uses the amount of contribution to global model accuracy as a criterion for judging the value of clients. **[A client selection algorithm based on the contribution]** is proposed, inspired by the theory of Adversarial Bandit in Multiarmed Bandit (MAB).12   
>The client selection algorithm in this paper updates the client selection weights by estimating the contribution of the client, solving the problem of blindly imposing fairness constraints on the client while ignoring the actual contribution of the client in fairness client selection, and the approach in this paper (from the perspective of the contribution is more comprehensive than the approach in the literature11 (only considers the case of client failure). It also does not affect the privacy-preserving mechanism of FL. The experimental results demonstrate that the algorithm in this paper performs excellently even in the case of Non-IID.

Main contributions of the paper  
To mitigate the impact of differences in clients' values on training of FL, we propose a contribution-based client selection algorithm for the client selection problem in FL. This paper makes the following major contributions:  
1. We propose a new client evaluation criterion based on contribution and an objective function. The amount of impact of each client on global model accuracy in each round is taken as the client's contribution to the global model, and the objective function is the expected improvement of global model accuracy in each round.  
2. We transformed client selection into the Adversarial MABs12 problem, and propose a contribution-based FL client selection algorithm (Contribution-Based Exponential-weight algorithm for Exploration and Exploitation, CBE3). The CBE3 algorithm is goal-oriented, defines the change in accuracy as the client contribution. It allocates selection probabilities based on the contribution of clients, effectively distinguishing the selection differences between clients of different values.  
3. To improve the applicability of the client selection algorithm, we propose contribution amplification factors that can be adjusted depending on the scenario requirements.  

Weiwei Lin(林伟伟), https://scholar.google.com/citations?hl=ko&user=IWsha94AAAAJ&view_op=list_works&sortby=pubdate   
Tiansheng Huang, https://scholar.google.com/citations?hl=ko&user=zz6Oq8wAAAAJ&view_op=list_works&sortby=pubdate  
- [원문 못 구함] VFedCS: Optimizing Client Selection for Volatile Federated Learning, https://ieeexplore.ieee.org/abstract/document/9846900
 
## FedBalancer 
FedBalancer: Data and Pace Control for Efficient Federated Learning on Heterogeneous Clients (ACM MobiSys 2022), https://dl.acm.org/doi/abs/10.1145/3498361.3538917 
- https://nmsl.kaist.ac.kr/projects/fedbalancer/  
- The source code of our FedBalancer implementation are available at https://github.com/jaemin-shin/FedBalancer
- For the testbed experiment on Android devices in our paper (Section 4.6), please refer to the following repository: [flower-FedBalancer-testbed](https://github.com/jaemin-shin/flower-FedBalancer-testbed).  


#### 3.2 Client Sample Selection 
>In Section 2.2, we observed that existing FL methods consume large portion of time to train samples that contribute only small gradient to the model. As these samples are quickly learned after few rounds, we design FedBalancer to start training with all samples and **gradually remove already-learned samples**. This enables FedBalancer to efficiently **focus on more important samples at each round** while optimizing the training process of FL. However, implementing such design in FL is non-trivial as the following question needs to be addressed: *How should FedBalancer distinguish between important and non-important samples at each stage of FL?*  

>Note that FedBalancer uses the **loss of a sample to measure the statistical utility (and thus the importance) of a sample to the current model**, similar to Importance Sampling [52, 61]. While other studies have also leveraged gradient norm or gradient norm upper bound [5, 34, 42] to achieve the same goal, we use loss as it is more widely applicable to FL tasks with non gradient-based optimizations [59].

#### 3.2.3 Client selection with sample selection. 
>Researchers have studied on how to select a group of clients for a training round to optimize convergence speed and model performance in heterogeneous FL[14, 15, 38]. While these approaches prioritize clients with higher statistical utility from the data, applying them along with FedBalancer is non-trivial as the samples are dynamically selected with the loss threshold. To address this issue, we propose a new formulation to calculate the statistical utility of a client 𝑖 along with the sample selection strategy of FedBalancer as follow ......


#### Future work 
>**Robustness of Sample Selection.**  
>One of the possible limitation of FedBalancer is that it might perform worse on FL tasks with noisy data, as noisy samples are highly likely to be selected by the sample selection module that prioritizes high loss. As we observed the performance improvement with FedBalancer on five real-world user datasets which may already have certain noise level, we expect FedBalancer would be helpful on most FL tasks. To improve further, we could systematically involve robust training approaches at centralized learning [60, 64, 65] to actively deal with noisy data. This is part of our future work.

#### IncFL 
https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#incfl

[References]
- [14] Yae Jee Cho, Bandit-based Communication-Efficient Client Selection Strategies for Federated Learning, https://doi.org/10.1109/IEEECONF51394.2020.9443523
- [15] Yae Jee Cho, Towards Understanding Biased Client Selection in Federated Learning, https://proceedings.mlr.press/v151/jee-cho22a.html
- [38] Oort: Informed Participant Selection for Scalable Federated Learning, https://arxiv.org/abs/2010.06081
- [75] Characterizing Impacts of Heterogeneity in Federated Learning upon Large-Scale Smartphone Data, https://arxiv.org/abs/2006.06983  
  >https://github.com/PKU-Chengxu/FLASH 
  
***
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
