Back to https://github.com/Kwangkee/FL
***

## Researcher 

#### Duc Lam Nguyen
- Duc Lam Nguyen, https://scholar.google.co.kr/citations?hl=ko&user=HDaJwWUAAAAJ&view_op=list_works&sortby=pubdate
- Duc Lam Nguyen, https://lamnd09.github.io/lamnd09/
- BDSP: A Fair Blockchain-enabled Framework for Privacy-Enhanced Enterprise Data Sharing
- FedToken: Tokenized Incentives for Data Contribution in Federated Learning, 
- A Contribution-based Device Selection Scheme in Federated Learning

- Blockchain for internet of things: Data markets, learning, and sustainability (Ph.D. Dissertation), https://vbn.aau.dk/ws/files/478977327/phd_DLN_e_pdf.pdf
>- C Modeling and Analysis of Data Trading on Blockchain-based Market in IoT Networks 47
>- D A Marketplace for Trading AI Models based on Blockchain and Incentives for IoT Data


#### Zhenzhe Zheng
- Zhenzhe Zheng, https://scholar.google.com/citations?hl=en&user=kx_5xxEAAAAJ&view_op=list_works&sortby=pubdate
- [[ODE: A Data Sampling Method for Practical Federated Learning with Streaming Data and Limited Buffer](https://github.com/Kwangkee/FL/blob/main/FL@ClientSelection.md#ode-a-framework-of-online-data-selection)], https://arxiv.org/abs/2209.00195 
- Online Data Valuation and Pricing for Machine Learning Tasks in Mobile Health, https://ieeexplore-ieee-org.libproxy.kw.ac.kr/document/9796669?arnumber=9796669&SID=EBSCO:edseee
- Data-Free Evaluation of User Contributions in Federated Learning, https://arxiv.org/abs/2108.10623
- Toward Understanding the Influence of Individual Clients in Federated Learning, https://ojs.aaai.org/index.php/AAAI/article/view/17263


***  
## Fed-Influence
Toward Understanding the Influence of Individual Clients in Federated Learning, https://ojs.aaai.org/index.php/AAAI/article/view/17263  




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
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
