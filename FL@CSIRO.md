Back to https://github.com/Kwangkee/FL
***

## SIN KIT LO  
https://scholar.google.com/citations?hl=ko&user=TuL21poAAAAJ&view_op=list_works&sortby=pubdate

## Papers 
- [[FLRA: A Reference Architecture for Federated Learning Systems](https://github.com/Kwangkee/FL/blob/main/FL@CSIRO.md#flra-a-reference-architecture-for-federated-learning-systems)], https://arxiv.org/abs/2106.11570   
- [[Architectural patterns for the design of federated learning systems](https://github.com/Kwangkee/FL/blob/main/FL@CSIRO.md#architectural-patterns-for-the-design-of-federated-learning-systems)], https://arxiv.org/abs/2101.02373
- [[Towards Trustworthy AI: Blockchain-based Architecture Design for Accountability and Fairness of Federated Learning Systems](https://github.com/Kwangkee/FL/blob/main/FL%40CSIRO.md#towards-trustworthy-ai)], https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=TuL21poAAAAJ&sortby=pubdate&citation_for_view=TuL21poAAAAJ:koF6b02d8EEC
***

## FLRA: A Reference Architecture for Federated Learning Systems
FLRA: A Reference Architecture for Federated Learning Systems, https://arxiv.org/abs/2106.11570


## Architectural patterns for the design of federated learning systems
https://arxiv.org/abs/2101.02373

![image](https://user-images.githubusercontent.com/109835677/182032069-50c87806-b7a2-4483-8939-3958a372f877.png)

## Towards Trustworthy AI
Towards Trustworthy AI: Blockchain-based Architecture Design for Accountability and Fairness of Federated Learning Systems, https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=TuL21poAAAAJ&sortby=pubdate&citation_for_view=TuL21poAAAAJ:koF6b02d8EEC
- We designed the architecture based on a reference architecture for federated learning system named FLRA [6]. https://arxiv.org/abs/2106.11570
- GFL federated learning framework3 is used to perform the experiments. https://github.com/GalaxyLearning/GFL, https://galaxylearning.github.io/ 

However, federated learning systems struggle to achieve and embody responsible AI principles. In particular, federated learning systems face accountability and fairness challenges due to multi-stakeholder involvement and heterogeneity in client data distribution. To enhance the accountability and fairness of federated learning systems, we present a blockchain-based trustworthy federated learning architecture. 

![image](https://user-images.githubusercontent.com/109835677/182032146-cb8b1285-4b0d-4e69-acad-ef337d5cd3e1.png)


We adopted Parity consortium blockchain 1.9.3-stable, in which the consensus algorithm is Proof-of-Authority (PoA). The block gas limit is set to 80M and the block interval is configured to 5s. The smart contracts are written in Solidity with compiler v.0.4.26. We performed four tests to measure the latency of the aforementioned blockchain operations respectively, each test ran 100 times.

```
contract DataModelRegistry{ 
  struct Model{ 
    bool uploaded; 
    string data version;
    string model_parameter; 
  } 
  struct Client{ 
    uint num_model; 
  } 
  mapping ( address => mapping ( uint => Model) ) 
    public provenance; 
  mapping ( address => Client ) public client; 
  function getNumModel(address _client) public view returns ( uint ) { 
    return client[_client].num_model;
  }
    function storeData (string _data_version , string _model parameter) public{ 
      required ( provenance [msg. sender ][ client [msg. sender ]. num model+1]. uploaded == false ); 
      client[msg.sender].num model++; 
      provenance[msg.sender][client[msg.sender].num model].data_version = _data_version ; 
      provenance[msg.sender][client[msg.sender].num model].model_parameter = _model_parameter ; 
      provenance[msg.sender][client[msg.sender].num model].uploaded = true; 
    } 
  function retrieveDataVersion (address _client, uint _model) public view returns (string dataVersion ){ 
    return provenance[_client][_model].data_version;
  } 
  function retrieveUpdate (address _client, uint _model) public view returns ( string _modelPara ){ 
    return provenance[_client][_model].model_parameter;
  }
}
```
***
Back to the [Top](#papers)  
Back to https://github.com/Kwangkee/FL
