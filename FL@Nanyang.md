Back to https://github.com/Kwangkee/FL
***

## Han Yu,  
https://personal.ntu.edu.sg/han.yu/, [Complete Website](https://sites.google.com/site/hanyushomepage/home), [Google Scholar](https://scholar.google.com.sg/citations?user=eXgoTXMAAAAJ&hl=en),  
Lab: [Trustworthy Federated Ubiquitous Learning (TrustFUL) Research Lab](https://trustful.federated-learning.org/)  
YouTube, Towards Trustworthy Federated Learning, https://www.youtube.com/watch?v=8KQndP_jDQ0   

## Papers 
- [[Towards personalized federated learning](#towards-personalized-federated-learning)], https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=eXgoTXMAAAAJ&sortby=pubdate&citation_for_view=eXgoTXMAAAAJ:0d9pApVQ-n0C
- Towards Verifiable Federated Learning, https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=eXgoTXMAAAAJ&sortby=pubdate&citation_for_view=eXgoTXMAAAAJ:3AIi9tQMIrsC
- Towards Fairness-Aware Federated Learning, https://arxiv.org/abs/2111.01872
- Collaborative Fairness in Federated Learning
- Threats to Federated Learning

- [[CAreFL: Contribution-Aware Federated Learning for Smart Healthcare](https://github.com/Kwangkee/FL/blob/main/FL@Nanyang.md#carefl)], https://ojs.aaai.org/index.php/AAAI/article/view/21505
- [[CrowdFL: A Marketplace for Crowdsourced Federated Learning](#crowdfl)], AAAI-22 Demonstration Track, https://ojs.aaai.org/index.php/AAAI/article/view/21715   
- Federated Graph Neural Networks: Overview, Techniques and Challenges
- Personalised Federated Learning: A Combinational Approach
- FedCoin: A Peer-to-Peer Payment System for Federated Learning
- Federated Learning: Privacy and Incentive

***

## CAreFL
CAreFL: Contribution-Aware Federated Learning for Smart Healthcare, https://ojs.aaai.org/index.php/AAAI/article/view/21505

It provides fair and explainable FL participant contribution evaluation in an efficient and privacy-preserving manner, and optimizes the FL model aggregation approach based on the evaluation results. Since its deployment in Yidu Cloud Technology Inc. in March 2021, CAreFL has served 8 well-established medical institutions in China to build healthcare decision support models. It can perform contribution evaluations 2.84 times faster than the best existing approach, and has improved the average accuracy of the resulting models by 2.62% compared to the previous system (which is significant in industrial settings). To our knowledge, it is the first contribution-aware federated learning successfully deployed in the healthcare industry.

FL participant **contribution evaluation** is an active subfield of FL (Ghorbani and Zou 2019; Jia et al. 2019; Song, Tong, and Wei 2019; Wang et al. 2020; Wei et al. 2020). The aim is to estimate the value of each FL participant by evaluating its impact on the performance of the resulting FL model, without exposing their sensitive local data. To bridge the aforementioned gaps in FL frameworks for smart healthcare, we propose the Contribution-Aware Federated Learning (CAreFL) framework. The advantages are:
1. **Fast and Accurate Contribution Evaluation**: it is incorporated with our proposed GTG-Shapley (Liu et al. 2022) approach, which can evaluate fair and accurate FL participant contribution in a highly efficient manner.
2. **Contribution-Aware FL Model Aggregation**: during the contribution evaluation process, GTG-Shapley builds a large number of aggregated FL sub-models involving local model updates from different combinations of FL participants. With this knowledge, CAreFL provides a novel FL aggregation approach which selects the best performing sub-model to be distributed to the FL participants for the next round of local training. This differs from FedAvg-based approaches (which always aggregate all received local models), and can better deal with data heterogeneity issues.
3. **Contribution-based FL Participant Reputation Management**: historical contribution evaluation records are converted into reputation values for the FL participants. This information can serve as a basis stakeholder management decision support.


- Hence, the canonical SV cannot be directly used for contribution evaluation in the context of FL.  
- The key idea of GTG-Shapley is to opportunistically reduce the need for sub-model retraining with model reconstruction and strategic sampling of combinations of participants. It truncates unnecessary sub-model evaluations to reduce computational costs, while maintaining high accuracy of estimated SVs.  

#### Application Use and Payoff
The CAreFL framework has been deployed in Yidu Cloud Technology Inc. since March 2021 in two lines of their business: 
1) clinical research services, and : Clinical research focuses on training FL models involving data silos from multiple hospitals. 
2) and real-world trial research services. : Real world trial research is often initiated by a pharmaceutical company which aims to leverage data from multiple hospitals to build models.  

Both services require data which need to be collected by the hospitals over months or years under their respective Institutional Review Board (IRB) supervision. So far, CAreFL has been used to help eight well-known medical institutions in China to train AI models for risk prediction, disease diagnosis and influence factor analysis.

#### Conclusions and Future Work
In future, we will continue the explore the applicability of CAreFL in other smart healthcare application scenarios. We will also extend the CAreFL framework with contribution-based data pricing mechanisms (Pei 2020) to support the emergence of an **FL-based healthcare data exchange marketplace**. Eventually, we aim to incorporate these functionalities into the opensource FATE framework and make them available to more developers, researchers and practitioners.

## CrowdFL
CrowdFL: A Marketplace for Crowdsourced Federated Learning, AAAI-22 Demonstration Track, https://ojs.aaai.org/index.php/AAAI/article/view/21715   
Poster: https://www.ntu.edu.sg/docs/librariesprovider118/technovationposter/apr2021/feng-daifei_fypposter.pdf?sfvrsn=873bb53e_2  
YouTube: https://www.youtube.com/watch?v=_jZTPCgWkeI  

In this paper, we present CrowdFL, a platform to facilitate the crowdsourcing of FL model training. It coordinates client selection, model training, and reputation management, which are essential steps for the FL crowdsourcing operations. By implementing model training on actual mobile devices, we demonstrate that the platform improves model performance and training efficiency. To the best of our knowledge, it is the first platform to support crowdsourcing-based FL on edge devices.


## Towards personalized federated learning    
https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=eXgoTXMAAAAJ&sortby=pubdate&citation_for_view=eXgoTXMAAAAJ:0d9pApVQ-n0C

In this survey, we explore the domain of Personalized FL (PFL) to address the fundamental challenges of FL on heterogeneous data, a universal characteristic inherent in all real-world datasets. We analyze the key motivations for PFL and present a unique taxonomy of PFL techniques categorized according to the key challenges and personalization strategies in PFL. We highlight their key ideas, challenges and opportunities and envision promising future trajectories of research towards new PFL architectural design, realistic PFL benchmarking, and trustworthy PFL approaches.

However, the general FL approach faces several fundamental challenges: 
- poor convergence on highly heterogeneous data, and 
- lack of solution personalization.  

These issues deteriorate the performance of the global FL model on individual clients in the presence of heterogeneous local data distributions, and may even disincentivize affected clients from joining the FL process. Compared to traditional FL, PFL research seeks to address these two challenges.

Four categories of PFL approaches: 
>1) data-based, 
>2) model-based 
>3) architecture-based, 
>4) similarity-based.

![image](https://user-images.githubusercontent.com/109835677/182019639-2d17287e-0c6f-4c44-b8d3-e9747fc6b66b.png)

Strategy I: Global Model Personalization. Based on our proposed taxonomy, they are divided into Databased Approaches and Model-based Approaches as follows.

![image](https://user-images.githubusercontent.com/109835677/182019596-fcdc5743-3d74-4d7c-947e-8d58e82de872.png)


***
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
