## FL Client Selection
- FusionFedBlock: Fusion of blockchain and federated learning to preserve privacy in industry 5.0, https://www.sciencedirect.com/science/article/pii/S1566253522001658?casa_token=VXH5TQ4DZ2sAAAAA:AFQnf8oJj0TgA_nnluqCev-je0txTXht-0ZY2toq9DonlZdIwUzHaCtex7imVQC3yVz_TqVqMTE
- Fed-CBS: A Heterogeneity-Aware Client Sampling Mechanism for Federated Learning via Class-Imbalance Reduction, https://arxiv.org/abs/2209.15245
- Game of Gradients: Mitigating Irrelevant Clients in Federated Learning, https://ojs.aaai.org/index.php/AAAI/article/view/17093   
- Secure Shapley Value for Cross-Silo Federated Learning, https://arxiv.org/abs/2209.04856  

## Asynch FL 
- A Study on Blockchain-Based Asynchronous Federated Learning Framework, https://koreascience.kr/article/CFKO202220859352236.pdf
- BAFL: A Blockchain-Based Asynchronous Federated Learning Framework, https://ieeexplore.ieee.org/document/9399813
- PersA-FL: Personalized Asynchronous Federated Learning, https://arxiv.org/abs/2210.01176

## FL
- A Study of Blockchain-Based Federated Learning, https://link.springer.com/chapter/10.1007/978-3-031-11748-0_7
- Securing federated learning with blockchain: a systematic literature review, https://link.springer.com/article/10.1007/s10462-022-10271-9
- Federated Learning Design and FunctionalModels: Survey, https://www.researchsquare.com/article/rs-2101865/latest.pdf

## rPPG
- Deep Physiological Sensing Toolbox, https://arxiv.org/abs/2210.00716
- Real-Time Monitoring of User Stress, Heart Rate, and Heart Rate Variability on Mobile Devices, https://arxiv.org/pdf/2210.01791
- Adaptive-Weight Network for imaging photoplethysmography signal extraction and heart rate estimation, https://ieeexplore.ieee.org/abstract/document/9912354


## FedFOR
FedFOR: Stateless Heterogeneous Federated Learning with First-Order Regularization, https://arxiv.org/abs/2209.10537  

We derive a first-order gradient regularization to penalize inconsistent local updates due to local data heterogeneity. Specifically, to mitigate weight divergence, we introduce a first-order approximation of the global data distribution into local objectives, which intuitively penalizes updates in the opposite direction of the global update. The end result is a stateless FL algorithm that achieves 1) significantly faster convergence (i.e., fewer communication rounds) and 2) higher overall converged performance than SOTA methods under non-IID data distribution. Importantly, our approach does not impose unrealistic limits on the client size, enabling learning from a large number of clients as is typical in most FL applications.

Our code will be released at https://github.com/GT-RIPL/FedFOR.

Most FL algorithms can be categorized under innovation to one of the components. 
- **ServerOpt** methods improve convergence by adding server-side momentum or adaptive optimizers. FedAvgM (Hsu, Qi, and Brown 2019) and SlowMo (Wang et al. 2019) simulates imbalanced data distribution, which is one form of data heterogeneity, and proposes to use server side momentum to improve convergence. FedAdagrad/FedYogi/FedAdam (Reddi et al. 2020) extends FedAvg by including several adaptive optimizers on the server-side to combat data heterogeneity.  
- **ClientOpt** methods add client-side regularization to reduce the effects of data heterogeneity. FedProx (Li et al. 2020) proposes to add a proximal term (L2 regularization) to limit the impact of non-IID data. FedCurv (Shoham et al. 2019) adapts a second-order gradient regularization method, EWC (Kirkpatrick et al. 2017), from continual learning to FL. Recent works, FedPD (Zhang et al. 2020) and FedDyn (Acar et al. 2021) improve convergence on non-IID data by including a first-order regularization term, which seeks consensus among clients. ClientOpt is investigated more heavily than ServerOpt because poor performance due to data heterogeneity is a direct result of local optimization. Furthermore, ClientOpt is more difficult to design because of the stateless requirement for FL when the number of clients is large. For example, FedPD and FedDyn are stateful algorithms and can be difficult to apply to large-scale, real-world FL settings. 

In this paper, we focus on the ClientOpt component to improve convergence under non-IID data distribution and compare analytically and empirically to all ClientOpt methods mentioned in this section.
