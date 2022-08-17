Back to https://github.com/Kwangkee/FL
***


## fedscale.ai
A scalable and extensible federated learning engine and benchmark, http://fedscale.ai/  

## FedScale
FedScale: Benchmarking Model and System Performance of Federated Learning at Scale, https://arxiv.org/abs/2105.11367  
![image](https://user-images.githubusercontent.com/109835677/185089825-e67182b6-d70f-4009-87d1-ceb3bff2c367.png)
>Second, existing benchmarks often overlook system speed, connectivity, and availability of the clients (e.g., FedML (He et al., 2020) and Flower (Beutel et al., 2021)). This discourages FL efforts from considering system efficiency and leads to overly optimistic statistical performance (§2).
>
>FedScale 에 비하면 Flower 는 장난감. Massive scale 지원, 다양한 practical FL setting 지원


## Swan
Swan: A Neural Engine for Efficient DNN Training on Smartphone SoCs, https://arxiv.org/abs/2206.04687   
>Swan is built within Termux, a Linux Terminal emulator for Android, and can efficiently train unmodified PyTorch models.
>
>Mobile On-device Training의 대안으로 Swan 제시. TFLote, PyTorch Mobile 쓰지 않고, unmodified PyTorch models 그대로 사용.

#### FedScale, https://github.com/symbioticlab/fedscale
- FedScale Benchmarking Datasets, https://github.com/SymbioticLab/FedScale/tree/master/benchmark/dataset
- FedScale Runtime: A Deployment and Evaluation Platform for Federated Learning, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/core
- Setup Android Edge Device From Scratch, https://github.com/SymbioticLab/FedScale/tree/master/fedscale/deploy/mobile

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
Back to [Papers](#papers)  
Back to https://github.com/Kwangkee/FL
