Back to https://github.com/Kwangkee/FL
***

## Papers 

- [[Oort: Efficient Federated Learning  via Guided Participant Selection](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#oort)], https://arxiv.org/abs/2010.06081
  >- Now merged as part of FedScale. More detials, https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#fedscale

- [Contribution-based selection algorithm (Contribution-Based Exponential-weight algorithm for Exploration and Exploitation, CBE3)](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#cbe3)

- Client selection in federated learning: Convergence analysis and power-of-choice selection strategies, https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#yae-jee-cho

- [[FedBalancer: Data and Pace Control for Efficient Federated Learning on Heterogeneous Clients (ACM MobiSys 2022)](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#fedbalancer)], https://dl.acm.org/doi/abs/10.1145/3498361.3538917 


[Takayuki Nishio] https://scholar.google.com/citations?hl=en&user=hHnMMMkAAAAJ&view_op=list_works&sortby=pubdate   
- [FedCS] Client selection for federated learning with heterogeneous resources in mobile edge, https://arxiv.org/abs/1804.08333  
  >Specifically, FedCS solves a client selection problem with resource constraints, which allows the server to aggregate as many client updates as possible and to accelerate performance improvement in ML models. We conducted an experimental evaluation using publicly-available large-scale image datasets to train deep neural networks on MEC environment simulations. The experimental results show that FedCS is able to complete its training process in a significantly shorter time compared to the original FL protocol.
- MAB-based Client Selection for Federated Learning with Uncertain Resources in Mobile Networks, https://arxiv.org/abs/2009.13879

Zhenzhe Zheng, https://scholar.google.com/citations?hl=en&user=kx_5xxEAAAAJ&view_op=list_works&sortby=pubdate
- [[ODE: A Data Sampling Method for Practical Federated Learning with Streaming Data and Limited Buffer](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#ode-a-framework-of-online-data-selection)], https://arxiv.org/abs/2209.00195 
- Online Data Valuation and Pricing for Machine Learning Tasks in Mobile Health, https://ieeexplore-ieee-org.libproxy.kw.ac.kr/document/9796669?arnumber=9796669&SID=EBSCO:edseee
- Data-Free Evaluation of User Contributions in Federated Learning, https://ieeexplore-ieee-org.libproxy.kw.ac.kr/document/9589136?arnumber=9589136&SID=EBSCO:edseee
- Toward Understanding the Influence of Individual Clients in Federated Learning, https://ojs.aaai.org/index.php/AAAI/article/view/17263

Lam Duc Nguyen, https://lamnd09.github.io/lamnd09/     
- A Contribution-based Device Selection Scheme in Federated Learning, https://arxiv.org/abs/2203.05369
- FedToken: Tokenized Incentives for Data Contribution in Federated Learning, https://arxiv.org/abs/2209.09775
- A Marketplace for Trading AI Models based on Blockchain and Incentives for IoT Data, https://arxiv.org/abs/2112.02870
- Modeling and Analysis of Data Trading on Blockchain-Based Market in IoT Networks, https://ieeexplore.ieee.org/abstract/document/9324804

- Client Selection for Asynchronous Federated Learning with Fairness Consideration, https://ieeexplore.ieee.org/document/9814669  
- Client Selection for Federated Learning With Label Noise, https://ieeexplore.ieee.org/document/9632344  
 

## ETC

- Federated learning with workload-aware client scheduling in heterogeneous systems, https://www.sciencedirect.com/science/article/abs/pii/S0893608022002957

- Client Selection for Federated Learning With Non-IID Data in Mobile Edge Computing, https://www.researchgate.net/publication/349012712_Client_Selection_for_Federated_Learning_With_Non-IID_Data_in_Mobile_Edge_Computing

- Multi-armed bandit-based client scheduling for federated learning, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Multi-Armed-Bandit-Based-Client-Scheduling-for-Federated-Learning&btnG=

- A Contribution-based Device Selection Scheme in Federated Learning, https://arxiv.org/abs/2203.05369

- Learning Advanced Client Selection Strategy for Federated Learning, https://aaai-2022.virtualchair.net/poster_aaai12714

- Client Selection@Awesome Federated Machine Learning
https://github.com/innovation-cat/Awesome-Federated-Machine-Learning#15-client-selection

  
  
***  
## ODE, a framework of Online Data sElection  
Zhenzhe Zheng, https://scholar.google.com/citations?hl=en&user=kx_5xxEAAAAJ&view_op=list_works&sortby=pubdate  
ODE: A Data Sampling Method for Practical Federated Learning with Streaming Data and Limited Buffer, https://arxiv.org/abs/2209.00195 

We first define a new data valuation metric for data selection in FL: **the projection of local gradient over an on-device data sample onto the global gradient over the data from all devices**. We further design ODE, a framework of Online Data sElection for FL, to coordinate networked devices to store valuable data samples collaboratively, with theoretical guarantees for speeding up model convergence and enhancing final model accuracy, simultaneously.

Therefore, a fundamental problem when applying FL to mobile network is *how to filter valuable samples from the streaming data on device to simultaneously accelerate model training convergence and enhance inference accuracy of the final global FL model?*

#### Design Challenges
The design of such an online data selection framework for FL with limited on-device storage involves three key challenges:
- (1) There is still no theoretical understanding about the impact of local on-device data on the training speedup and accuracy enhancement of global model in FL. Due to the lack of information about raw data and local model updates of the other devices, it is challenging for a specific device to derive the impact of one individual local data sample on the performance of the global model, which is an aggregation of all the devices’ local models in FL. Furthermore, the sample-level correlation between convergence rate and model accuracy is undiscovered and complicated in FL. Due to the data heterogeneity across devices, the impacts of local data samples on convergence rate and model accuracy could be quite different, and thus it is hard to simultaneously guarantee these two aspects through optimizing a unified data valuation metric.
- (2) The lack of multiple dimensional information significantly complicates the online data selection in FL. For streaming networked data, we could not access the data samples coming from the future or discarded in the past, which we call as temporal information. With the lack of temporal information, one device is not able to leverage the complete statistical information (e.g. unbiased local data distribution) for accurate data quality evaluation1, such as outliers detection and noise removal [48, 67]. Additionally, due to the distributed paradigm of FL, one specific device has only local view, and cannot conduct efficient and effective online data selection without the knowledge of the other devices’ stored data and local models, which we call as spatial information. This is because the valuable data samples selected locally by different devices could be overlapped with each other and then the local valuable data may not be the global valuable one, which distorts the distribution of training data collected by all the devices.
- (3) The on-device data selection needs to be low computation-and-memory-cost due to the conflict of limited hardware resources and requirement on QoE (Quality of user Experience) guarantee. As the additional computation and memory costs introduced by online data selection process influence the performance of mobile systems as well as user experience, the real-time data samples must be evaluated in a computation and memory efficient way. However, the streaming data and complex ML model structure raise several difficulties to achieve this goal. The streaming format of on-device data reduces the parallelism of GPU and CPU and increases per-sample evaluation delay. The complex ML model structure with large-scale parameters leads to high computational complexity and memory footprint for storing intermediate model outputs during the data selection process.

#### Limitations of Related Works
The prior works on data evaluation and selection in ML failed to solve the above challenges.
- (1) The data selection in centralized ML, such as leave-one-out test [20], Data Shapley [29] and Importance Sampling [53, 63, 68, 71], is not appropriate for online data selection in FL due to the first challenge: they could only measure the valuation of each data sample corresponding to the model trained locally, instead of the aggregated global model in FL.
- (2) The prior works on data selection in FL did not consider the two new properties of FL devices identified in this work. Mercury [86], FedBalancer [67] and the work from Li et al. [48] adopt importance sampling framework [87] to select the data samples with high loss or gradient norm for reducing the training time per epoch but they failed to solve the second challenge of lacking temporal and spatial information. These methods need to inspect all the data in each training round for normalized sampling weight computation2 as well as noise and outliers removal [35, 48].

#### Our Solutions. 
The challenges for FL in networked scenario and the limitations of existing methods motivate us to investigate the online data selection for FL with limited on-device storage. To this end, we design ODE, an online data valuation framework that coordinates networked devices to select and store valuable data samples locally and collaboratively for model training in FL, with the theoretical guarantee for speeding up model convergence and enhancing final model accuracy, simultaneously.


#### 5 RELATED WORKS

>- **Federated Learning** is a distributed learning framework that aims to collaboratively learn a global statistical model over the networked devices’ data under the constraint that the data is stored and processed locally [51, 55]. Existing works mostly focus on how to overcome the data heterogeneity problem [13, 18, 78, 85], reduce the communication cost [34, 42, 42, 82], select important clients [19, 47, 50, 59] or train a personalized model for each client [25, 36]. Despite that
there exist a few works considering the problem of online FL or continuous FL [17, 31, 83], they did not consider the device properties of limited on-device storage and streaming networked data, and thus cannot be applied to the practical FL scenarios.
>- **Data Selection.** In FL, selecting data from streaming data can be seen as sampling batches of data from its data distribution, which is similar to mini-batch SGD. To accelerate the training process of SGD, the majority of existing methods quantify the importance of each data sample (such as loss [53, 63, 68], gradient norm [38, 87], uncertainty [14, 79]) and leverage importance sampling to select training samples for each round. Another closer area to our work is data evaluation, which
tries to measure the contribution/importance of each data sample to the training process, such as leave-one-out test [20] and data shapley [29]. These methods fail to work for the network scenario as they require arbitrary access to the full dataset for model retraining.


***

## Oort
Oort: Efficient Federated Learning  via Guided Participant Selection, https://www.usenix.org/conference/osdi21/presentation/lai, https://arxiv.org/abs/2010.06081

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
![image](https://user-images.githubusercontent.com/109835677/185089825-e67182b6-d70f-4009-87d1-ceb3bff2c367.png)
>Second, existing benchmarks often overlook system speed, connectivity, and availability of the clients (e.g., FedML (He et al., 2020) and Flower (Beutel et al., 2021)). This discourages FL efforts from considering system efficiency and leads to overly optimistic statistical performance (§2).
>
>FedScale 에 비하면 Flower 는 장난감. Massive scale 지원, 다양한 practical FL setting 지원


#### Swan
Swan: A Neural Engine for Efficient DNN Training on Smartphone SoCs, https://arxiv.org/abs/2206.04687   
>Swan is built within Termux, a Linux Terminal emulator for Android, and can efficiently train unmodified PyTorch models.
>
>Mobile On-device Training의 대안으로 Swan 제시. TFLote, PyTorch Mobile 쓰지 않고, unmodified PyTorch models 그대로 사용.

#### FedScale, https://github.com/symbioticlab/fedscale
- FedScale Benchmarking Datasets, https://github.com/SymbioticLab/FedScale/tree/master/benchmark/dataset
- FedScale Runtime: A Deployment and Evaluation Platform for Federated Learning, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/core
- Setup Android Edge Device From Scratch, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/deploy/mobile

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
- https://github.com/Kwangkee/FL/blob/main/AFL.md#t1-kaist

#### 3.2 Client Sample Selection 
>In Section 2.2, we observed that existing FL methods consume large portion of time to train samples that contribute only small gradient to the model. As these samples are quickly learned after few rounds, we design FedBalancer to start training with all samples and **gradually remove already-learned samples**. This enables FedBalancer to efficiently **focus on more important samples at each round** while optimizing the training process of FL. However, implementing such design in FL is non-trivial as the following question needs to be addressed: *How should FedBalancer distinguish between important and non-important samples at each stage of FL?*  

>Note that FedBalancer uses the **loss of a sample to measure the statistical utility (and thus the importance) of a sample to the current model**, similar to Importance Sampling [52, 61]. While other studies have also leveraged gradient norm or gradient norm upper bound [5, 34, 42] to achieve the same goal, we use loss as it is more widely applicable to FL tasks with non gradient-based optimizations [59].

#### 3.2.3 Client selection with sample selection. 
>Researchers have studied on how to select a group of clients for a training round to optimize convergence speed and model performance in heterogeneous FL[14, 15, 38]. While these approaches prioritize clients with higher statistical utility from the data, applying them along with FedBalancer is non-trivial as the samples are dynamically selected with the loss threshold. To address this issue, we propose a new formulation to calculate the statistical utility of a client 𝑖 along with the sample selection strategy of FedBalancer as follow ......

#### 4.1 Experimental Setup
>*Sample selection method*: We implement the baseline sample selection method that is a combination of the following: (1) We determined how many samples to select based on FedSS [12], which controls the training dataset size on clients with larger datasets for each training round. (2) There were several approaches that propose which samples to select based on loss [52, 61], gradient [5], or gradient norm upper bound [34, 42] of samples. As in FedBalancer, we use loss to select samples for the
baseline experiment.  
>- [12] Lingshuang Cai, Di Lin, Jiale Zhang, and Shui Yu. 2020. Dynamic sample selection for federated learning with heterogeneous data in fog computing. In ICC
2020-2020 IEEE International Conference on Communications (ICC). IEEE, 1–6   
>- Dynamic Sample Selection for Federated Learning with Heterogeneous Data in Fog Computing, https://ieeexplore.ieee.org/abstract/document/9148586  


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
