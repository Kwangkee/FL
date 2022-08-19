Back to https://github.com/Kwangkee/FL
***


■ 공정한 연합학습 (Fair Federated Learning)  

[[Ditto: Fair and Robust Federated Learning Through Personalization](https://github.com/Kwangkee/FL/blob/main/FL@Fair.md#ditto)], https://proceedings.mlr.press/v139/li21h.html

[[No One Left Behind: Inclusive Federated Learning over Heterogeneous Devices](https://github.com/Kwangkee/FL/blob/main/FL@Fair.md#inclusivefl)], https://dl.acm.org/doi/10.1145/3534678.3539086

Improving Fairness via Federated Learning, https://arxiv.org/abs/2110.15545?context=cs  
KDD 2021 Tutorial on Towards Fair Federated Learning, www.cas.mcmaster.ca/~chul9/Contents/KDD_2021_Tutorial.html  


## Ditto 
Ditto: Fair and Robust Federated Learning Through Personalization, https://proceedings.mlr.press/v139/li21h.html  
Github: https://github.com/litian96/ditto  

Fairness and robustness are two important concerns for federated learning systems. In this work, we identify that 
- *robustness* to data and model poisoning attacks and  
- *fairness*, measured as the uniformity of performance across devices,  

are competing constraints in statistically heterogeneous networks. To address these constraints, we propose employing a simple, general framework for personalized federated learning, Ditto, that can inherently provide fairness and robustness benefits, and develop a scalable solver for it. Theoretically, we analyze the **ability of Ditto to achieve fairness and robustness simultaneously** on a class of linear problems. Empirically, across a suite of federated datasets, we show that Ditto not only achieves competitive performance relative to recent personalization methods, but also enables more accurate, robust, and fair models relative to state-of-the-art fair or robust baselines.

>Simultaneously satisfying these varied constraints can be exceptionally difficult (Kairouz et al., 2019).  
>
>Many prior efforts have separately considered fairness or robustness in federated learning.  
>
>we show that the constraints of fairness and robustness can directly compete with one another when training a single global model, and that simultaneously optimizing for accuracy, fairness, and robustness requires careful consideration. For example, as we empirically demonstrate (Section 4), current fairness approaches can render FL systems highly susceptible to training time attacks from malicious devices. On the other hand, robust methods may filter out rare but informative updates, causing unfairness (Wang et al., 2020).
>
>Our work differs from these approaches by simultaneously learning local and global models via a global-regularized MTL framework, which applies to non-convex ML objectives.
>
>Finally, a key contribution of our work is jointly exploring the robustness and fairness benefits of personalized FL. The benefits of personalization for fairness alone have been demonstrated empirically in prior work (Wang et al., 2019; Hao et al., 2020). Connections between personalization and robustness have also been explored in Yu et al. (2020), although the authors propose using personalization methods on top of robust mechanisms. Our work differs from these works by arguing that MTL itself offers inherent robustness and fairness benefits, and exploring the challenges that exist when attempting to satisfy both constraints simultaneously.
>
>Here the hyperparameter λ controls the interpolation between local and global models. 
>- When λ is set to 0, Ditto is reduced to training local models; 
>- as λ grows large, it recovers global model objective (Global Obj) (λ → +∞).
>
>Ditto with an appropriate value of λ offers a tradeoff between these two extremes: the smaller λ, the more the personalized models vk can deviate from the (corrupted) global model w, potentially providing robustness at the expense of generalization. In the heterogeneous case (which can lead to issues of unfairness as described in Section 2), a finite λ exists to offer robustness and fairness jointly. We explore these ideas more rigorously in Section 3.3 by analyzing the tradeoffs between accuracy, fairness, and robustness in terms of λ for a class of linear regression problems, and demonstrate fairness/robustness benefits of Ditto empirically in Section 4.

## InclusiveFL
No One Left Behind: Inclusive Federated Learning over Heterogeneous Devices, https://dl.acm.org/doi/10.1145/3534678.3539086

***
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
