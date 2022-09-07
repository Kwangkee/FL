Back to https://github.com/Kwangkee/FL
***

## List
[Flower](#flower)  
[FedSclae](https://github.com/Kwangkee/FL/blob/main/FL%40FedScale.md)  
[FedML](#fedml)  
[FLSim](#flsim)  

TensorFlow Federated (TFF), https://www.tensorflow.org/federated?hl=ko    
PySyft, https://github.com/OpenMined/PySyft     
LEAF: A Benchmark for Federated Settings, https://arxiv.org/abs/1812.01097, https://leaf.cmu.edu/ 

[OpenFed](#openfed)  
FL_PyTorch: optimization research simulator for federated learning, https://dl.acm.org/doi/abs/10.1145/3488659.3493775  
https://github.com/burlachenkok/flpytorch  

***   

## FedML
FedML: https://fedml.ai/
https://fedml.ai/platform-tutorial/
https://doc.fedml.ai/  


## Flower 

Flower: A Friendly Federated Learning Framework, https://flower.dev/  

Flower: A Friendly Federated Learning Research Framework, https://arxiv.org/abs/2007.14390  
https://www.youtube.com/watch?v=t5WdERBPQfk&t=1s  
However, it also means Flower inherits the limitations of these frameworks that currently offer very limited support for on-device training (unlike the extensive solutions for on-device inference). It is anticipated that ML frameworks will address this short-coming within the next 12 months.

Complementing conventional supervised applications, we also expect Flower to be indispensable in the exploration of the rapidly maturing area of unsupervised, semi-supervised and self-learning (Xie et al., 2019b). FL using supervised methods are often not practical simply because it is difficult to acquire labeled data from users. But in contrast, devices have plentiful access to virtually unlimited amounts of unlabeled data. Furthermore, these learning approaches significantly increase the amount of data to be trained upon as unlabeled data is much more prevalent and so benefits from FL ability to distribute the training computation.

On-device Federated Learning with Flower, https://arxiv.org/abs/2104.03042  
https://www.youtube.com/watch?v=QJEX5c0y1I8&t=2s  
First, we present how Flower clients can be developed in Java and deployed on Android phones in the AWS Device Farm for federated model training.  

By design, Flower is language-agnostic and can work with any ML framework on the FL client, which maximizes its ability to federate existing training pipelines. However, it also means Flower inherits the limitations of these frameworks that currently offer limited support for on-device training on Android devices.  

Next, we define a Head Model which corresponds to the task-specific classifier that we want to train using federated learning.  

https://friendly-flower.slack.com/archives/C01F120R7B4/p1628093090000400

Flower Summit 2021  
- https://flower.dev/conf/flower-summit-2021
- https://www.youtube.com/watch?v=XEH9UCUlVO8&list=PLNG4feLHqCWkfu4GGq4xPrS5jve7WSqF7

Flower Summit 2022  
- https://flower.dev/conf/flower-summit-2022
- https://www.youtube.com/playlist?list=PLNG4feLHqCWni5zfOBaZNtaPlCce0OnJ6

## FLSim

https://github.com/facebookresearch/FLSim  
Federated Learning Simulator (FLSim) is a flexible, standalone library written in PyTorch that simulates FL settings with a minimal, easy-to-use API. FLSim is domain-agnostic and accommodates many use cases such as computer vision and natural text. Currently FLSim supports cross-device FL, where millions of clients' devices (e.g. phones) train a model collaboratively together.

FLSim is scalable and fast. It supports differential privacy (DP), secure aggregation (secAgg), and a variety of compression techniques.  
In FL, a model is trained collaboratively by multiple clients that each have their own local data, and a central server moderates training, e.g. by aggregating model updates from multiple clients.  
In FLSim, developers only need to define a dataset, model, and metrics reporter. All other aspects of FL training are handled internally by the FLSim core library. 

https://github.com/Kwangkee/FL/blob/main/FL%40Meta.md
***
Back to the [Top](#list)  
Back to https://github.com/Kwangkee/FL

## OpenFed 
OpenFed, https://arxiv.org/abs/2109.07852, https://github.com/FederalLab/OpenFed   

![image](https://user-images.githubusercontent.com/109835677/187823947-d676ab14-82c3-4468-aff8-c8b03a668af1.png)
