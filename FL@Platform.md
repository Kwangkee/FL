Back to https://github.com/Kwangkee/FL
***

## List
[Flower](#flower)  
[FedScale](#fedscale)  
[FLSim](#flsim)  


***   

## Flower 

Flower: A Friendly Federated Learning Framework, https://flower.dev/

## FedScale
A scalable and extensible federated learning engine and benchmark, http://fedscale.ai/  
FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367  
Swan: A Neural Engine for Efficient DNN Training on Smartphone SoCs, https://arxiv.org/abs/2206.04687   

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
