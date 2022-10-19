
## FedRL
- https://scholar.google.com/citations?hl=en&user=rkb3_FgAAAAJ&view_op=list_works&sortby=pubdate
>- e λ is the testing accuracy of the global models on the validation set after t rounds
- 

## BC
- Novel smart homecare IoT system with Edge-AI and Blockchain, https://www.researchgate.net/publication/364122174_Novel_smart_homecare_IoT_system_with_Edge-AI_and_Blockchain

- https://scholar.google.com/citations?hl=ko&user=8RfIQ9cAAAAJ&view_op=list_works&sortby=pubdate
- Towards a Remote Monitoring of Patient Vital Signs Based on IoT-Based Blockchain Integrity Management Platforms in Smart Hospitals, https://www.mdpi.com/1424-8220/20/8/2195
- Improving blockchain performance in clinical trials using intelligent optimal transaction traffic control mechanism in smart healthcare applications, https://www.sciencedirect.com/science/article/abs/pii/S0360835222003801
- HealthBlock: Asecureblockchain-basedhealthcaredatamanagementsystem, https://www.sciencedirect.com/science/article/abs/pii/S1389128621004382

## FL Client Selection
- A Snapshot of the Frontiers of Client Selection in Federated Learning, https://arxiv.org/abs/2210.04607
- A Multi-agent Reinforcement Learning Approach for Efficient Client Selection in Federated Learning, https://arxiv.org/abs/2201.02932
- FusionFedBlock: Fusion of blockchain and federated learning to preserve privacy in industry 5.0, https://www.sciencedirect.com/science/article/pii/S1566253522001658?casa_token=Auk-KEz5MVwAAAAA:b22Xfdso55xBMPassPW_VF4cHOda2h2vuujBJ41JKkIcsAR0LmIoQduiLa7V-UvnKNtXAh6zptc
- Fed-CBS: A Heterogeneity-Aware Client Sampling Mechanism for Federated Learning via Class-Imbalance Reduction, https://arxiv.org/abs/2209.15245
- Game of Gradients: Mitigating Irrelevant Clients in Federated Learning, https://ojs.aaai.org/index.php/AAAI/article/view/17093   
- Secure Shapley Value for Cross-Silo Federated Learning, https://arxiv.org/abs/2209.04856  

- Empirical Measurement of Client Contribution for Federated Learning with Data Size Diversification, https://ieeexplore.ieee.org/document/9906094
- FedCCEA : A Practical Approach of Client Contribution Evaluation for Federated Learning, https://arxiv.org/abs/2106.02310

## Asynch FL 
- A Survey on Heterogeneous Federated Learning, https://arxiv.org/abs/2210.04505
- A Study on Blockchain-Based Asynchronous Federated Learning Framework, https://koreascience.kr/article/CFKO202220859352236.pdf
- BAFL: A Blockchain-Based Asynchronous Federated Learning Framework, https://ieeexplore.ieee.org/document/9399813
- PersA-FL: Personalized Asynchronous Federated Learning, https://arxiv.org/abs/2210.01176
- Analysis and Evaluation of Synchronous and Asynchronous FLchain, https://arxiv.org/abs/2112.07938

## FL Market
- FL-Market: Trading Private Models in Federated Learning, https://arxiv.org/abs/2106.04384
- Blockchain-enhanced Federated Learning Market with Social Internet of Things, https://ieeexplore.ieee.org/abstract/document/9918042

## FL
- A Study of Blockchain-Based Federated Learning, https://link.springer.com/chapter/10.1007/978-3-031-11748-0_7
- Securing federated learning with blockchain: a systematic literature review, https://link.springer.com/article/10.1007/s10462-022-10271-9
- Federated Learning Design and FunctionalModels: Survey, https://www.researchsquare.com/article/rs-2101865/latest.pdf
- Meta Knowledge Condensation for Federated Learning, https://arxiv.org/abs/2209.14851
- FedTA: Teacher Assistant Knowledge Distillation in non-IID Federated Learning, https://jeremyzhang1.github.io/assets/CS242_Report.pdf

## rPPG
- Deep Physiological Sensing Toolbox, https://arxiv.org/abs/2210.00716
- Real-Time Monitoring of User Stress, Heart Rate, and Heart Rate Variability on Mobile Devices, https://arxiv.org/pdf/2210.01791
- Adaptive-Weight Network for imaging photoplethysmography signal extraction and heart rate estimation, https://ieeexplore.ieee.org/abstract/document/9912354
- Contactless Blood Pressure Estimation System Using a Computer Vision System, https://www.mdpi.com/2411-5134/7/3/84/htm


## FedFOR
FedFOR: Stateless Heterogeneous Federated Learning with First-Order Regularization, https://arxiv.org/abs/2209.10537  

We derive a first-order gradient regularization to penalize inconsistent local updates due to local data heterogeneity. Specifically, to mitigate weight divergence, we introduce a first-order approximation of the global data distribution into local objectives, which intuitively penalizes updates in the opposite direction of the global update. The end result is a stateless FL algorithm that achieves 1) significantly faster convergence (i.e., fewer communication rounds) and 2) higher overall converged performance than SOTA methods under non-IID data distribution. Importantly, our approach does not impose unrealistic limits on the client size, enabling learning from a large number of clients as is typical in most FL applications.

Our code will be released at https://github.com/GT-RIPL/FedFOR.

Most FL algorithms can be categorized under innovation to one of the components. 
- **ServerOpt** methods improve convergence by adding server-side momentum or adaptive optimizers. FedAvgM (Hsu, Qi, and Brown 2019) and SlowMo (Wang et al. 2019) simulates imbalanced data distribution, which is one form of data heterogeneity, and proposes to use server side momentum to improve convergence. FedAdagrad/FedYogi/FedAdam (Reddi et al. 2020) extends FedAvg by including several adaptive optimizers on the server-side to combat data heterogeneity.  
- **ClientOpt** methods add client-side regularization to reduce the effects of data heterogeneity. FedProx (Li et al. 2020) proposes to add a proximal term (L2 regularization) to limit the impact of non-IID data. FedCurv (Shoham et al. 2019) adapts a second-order gradient regularization method, EWC (Kirkpatrick et al. 2017), from continual learning to FL. Recent works, FedPD (Zhang et al. 2020) and FedDyn (Acar et al. 2021) improve convergence on non-IID data by including a first-order regularization term, which seeks consensus among clients. ClientOpt is investigated more heavily than ServerOpt because poor performance due to data heterogeneity is a direct result of local optimization. Furthermore, ClientOpt is more difficult to design because of the stateless requirement for FL when the number of clients is large. For example, FedPD and FedDyn are stateful algorithms and can be difficult to apply to large-scale, real-world FL settings. 

In this paper, we focus on the ClientOpt component to improve convergence under non-IID data distribution and compare analytically and empirically to all ClientOpt methods mentioned in this section.
