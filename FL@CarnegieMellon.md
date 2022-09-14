Back to https://github.com/Kwangkee/FL
***


## Virginia Smith
https://scholar.google.com/citations?hl=ko&user=bldHpWIAAAAJ&view_op=list_works&sortby=pubdate  

[[Ditto: Fair and Robust Federated Learning Through Personalization](https://github.com/Kwangkee/FL/blob/main/FL@Fair.md#ditto)], https://proceedings.mlr.press/v139/li21h.html

## Gauri Joshi
https://scholar.google.com/citations?hl=ko&user=yqIoH34AAAAJ&view_op=list_works&sortby=pubdate

## Yae Jee Cho
https://scholar.google.com/citations?hl=ko&user=MR333jsAAAAJ&view_op=list_works&sortby=pubdate  
https://yaejeec.github.io/   

- [[Towards Understanding Biased Client Selection in Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#biased-client-selection)], https://proceedings.mlr.press/v151/jee-cho22a.html    
- [[To Federate or Not To Federate: Incentivizing Client Participation in Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL@CarnegieMellon.md#incfl)], https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=MR333jsAAAAJ&sortby=pubdate&citation_for_view=MR333jsAAAAJ:UebtZRa9Y70C  

***

## Biased Client Selection
Towards Understanding Biased Client Selection in Federated Learning, https://proceedings.mlr.press/v151/jee-cho22a.html    

>Client Selection in Federated Learning: Convergence Analysis and Power-of-Choice Selection Strategies, https://arxiv.org/abs/2010.01243

In our work, we present the convergence analysis of federated learning with biased client selection and quantify how the bias affects convergence speed. **We show that biasing client selection towards clients with higher local loss yields faster error convergence.** From this insight, we propose Power-of-Choice, a communication- and computation-efficient client selection framework that flexibly spans the trade-off between convergence speed and solution bias. Extensive experiments demonstrate that Power-of-Choice can converge up to 3× faster and give 10% higher test accuracy than the baseline random selection.  

## IncFL
To Federate or Not To Federate: Incentivizing Client Participation in Federated Learning, https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=MR333jsAAAAJ&sortby=pubdate&citation_for_view=MR333jsAAAAJ:UebtZRa9Y70C  

In this paper, we propose an algorithm called IncFL that explicitly maximizes the fraction of clients who are incentivized to use the global model by dynamically adjusting the aggregation weights assigned to their updates. Our experiments show that IncFL increases the number of incentivized clients by 30-55% compared to standard federated training algorithms, and can also improve the generalization performance of the global model on unseen clients.

![image](https://user-images.githubusercontent.com/109835677/183677084-d0f54ace-f702-48d3-9f5f-0fe099bc1911.png) 
Figure 2: Aggregating weight qk(w) for any clientk versus  the emprical incentive gap Fk(w) − Fk(wb k). The weight qk(w) is small for clients that already have a very large incentive (global much better than local) or no incentive at all (local much better than global), and is highest for clients that are moderately incentivized (global similar to local).


Personalizing or Not: Dynamically Personalized Federated Learning with Incentives, https://arxiv.org/abs/2208.06192
![image](https://user-images.githubusercontent.com/109835677/185824356-d46592a1-fa83-4026-b25d-98cee3ba48d9.png)


***
Back to the [Top](#list)  
Back to https://github.com/Kwangkee/FL
