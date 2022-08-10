Back to https://github.com/Kwangkee/FL
***

## List
[Flower](#flower)  
[FedScale](#fedscale)  


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

***
Back to the [Top](#list)  
Back to https://github.com/Kwangkee/FL
