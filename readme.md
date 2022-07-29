기조연설 주제: 웹 3.0, 블록체인과 미래사회 전망(부산대 김호원 교수)
BCFL을 Web 3.0 관점에서 설명, https://youtu.be/IwEjUQbFb2Y?t=3123 
블록체인 플랫폼 연구센터, http://itrc.pusan.ac.kr/sub1-3/
![image](https://user-images.githubusercontent.com/109835677/181742952-cdb5957f-949c-48f3-8175-7e8cada2cf92.png)


A Review of Medical Federated Learning: Applications in Oncology and Cancer Research, https://link.springer.com/chapter/10.1007/978-3-031-08999-2_1 
Download conference paper PDF

Federated Learning emerged as a distributed learning paradigm that takes into account several practical challenges, and differentiates itself from traditional distributed learning settings, as noted by Google [20], by addressing four main themes: 
- statistical heterogeneity of data across nodes, 
- data imbalance across nodes, 
- limited communication in the distributed network (e.g., loss of synchronization, variability of communication capabilities), 
- and the possibility of a large number of nodes relative to the amounts of data.


[Where to Begin? Exploring the Impact of Pre-Training and Initialization in Federated Learning](https://arxiv.org/abs/2206.15387)

All experiments were performed using the open-source federated learning simulation framework FLSim [[1]](https://github.com/facebookresearch/FLSim)

How does the initialization (random, or pre-trained) impact the behavior of federated optimization methods?

#6. Recommendations
In this work, we study the affect of pre-training on federated optimization methods. Our results inform a series of the following recommendations:
- When evaluate FL algorithms, researchers should experiment with both pre-trained (if available) and random weights as they have different behaviors.
- When deploying FL to production environment, researchers should use adaptive server optimizers such as FedAdam and SGD at client. This setup works well and should be used a baseline before trying out more complex methods.
- Heterogeneity is not as a big of a problem when there is public data to pre-trained a model. We encourage researchers to pay attention other more complex tasks when there is no public data such as recommendation systems or semi-supervised learning.

#Conclusion
In this paper we present a thorough empirical analysis of initialization on federated learning by
evaluating it on twelve federated learning algorithms across four vision and text tasks. We find that
pre-training on public data can recover most of the accuracy drop from heterogeneity. We show that client updates starting from pre-trained weights have higher cosine similarity, which explains why initialized with pre-trained weights can speed up convergence and achieve high accuracy even in heterogeneous settings. We further show that using simple SGD locally can be as good as other local optimizers.. 


