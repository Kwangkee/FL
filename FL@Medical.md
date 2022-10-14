Back to https://github.com/Kwangkee/FL
***

## list

- [JIP/DKTK] Joint Imaging Platform ( JIP ) is a strategic initiative within the German Cancer Consortium (DKTK), https://jip.dktk.dkfz.de/jiphomepage/
  >The underlying infrastructure facilitates applications like federated learning across multiple clinical centers.
- [JIP/DKTK] Joint Imaging Platform for Federated Clinical Data Analytics, https://ascopubs.org/doi/full/10.1200/CCI.20.00045
- Towards Real-World Federated Learning in Medical Image Analysis Using Kaapana, https://link.springer.com/chapter/10.1007/978-3-031-18523-6_13

- [CVPR 2022, NVIDIA] Closing the Generalization Gap of Cross-Silo Federated Medical Image Segmentation, https://openaccess.thecvf.com/content/CVPR2022/html/Xu_Closing_the_Generalization_Gap_of_Cross-Silo_Federated_Medical_Image_Segmentation_CVPR_2022_paper.html
  >https://github.com/NVIDIA/NVFlare/examples/FedSM

- Reward Systems for Trustworthy Medical Federated Learning, https://arxiv.org/abs/2205.00470
  >- We publish the source code of our experiments, including the random seeds of the data splits, on GitHub: https://github.com/kpandl/Reward-System-forTrustworthy-Medical-Federated-Learning - this allows future research to reproduce and build on our results. We run our work on a computing cluster consisting of NVIDIA Tesla V100 and NVIDIA GeForce RTX 3090 GPUs using Python 3.7.11 and PyTorch 1.10.2.
  >- https://github.com/kpandl/Reward-System-for-Trustworthy-Medical-Federated-Learning


- When Collaborative Federated Learning Meets Blockchain to Preserve Privacy in Healthcare, https://ieeexplore.ieee.org/abstract/document/9906419
- A framework for privacy-preservation of IoT healthcare data using Federated Learning and blockchain technology, https://www.sciencedirect.com/science/article/abs/pii/S0167739X21004726
- Federated Learning for Smart Healthcare: A Survey, https://dl.acm.org/doi/full/10.1145/3501296  
- FedHome: Cloud-Edge Based Personalized Federated Learning for In-Home Health Monitoring, https://arxiv.org/abs/2012.07450 

- [[Contribution-Aware Federated Learning for Smart Healthcare](https://github.com/Kwangkee/FL/blob/main/FL@Nanyang.md#carefl)], https://ojs.aaai.org/index.php/AAAI/article/view/21505

- [[삼성병원: 신수용 교수](https://github.com/Kwangkee/FL/blob/main/FL@Medical.md#%EC%82%BC%EC%84%B1%EB%B3%91%EC%9B%90-%EC%8B%A0%EC%88%98%EC%9A%A9-%EA%B5%90%EC%88%98)] 
- [[KAIST](https://github.com/Kwangkee/FL/blob/main/FL@Medical.md#kaist)]
- [[Google: Privacy-first Health Research with Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL@Medical.md#google-privacy-first-health-research-with-federated-learning)]
- [[Havard: A Review of Medical Federated Learning](https://github.com/Kwangkee/FL/blob/main/FL@Medical.md#harvard)]
- Federated learning for smart healthcare: A survey, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Federated+Learning+for+Smart+Healthcare%3A+A+Survey&btnG=

***
## 서울과기대
서울과기대 박종혁 교수, https://scholar.google.com/citations?hl=en&user=IshTErgAAAAJ&view_op=list_works&sortby=pubdate  
-	FusionFedBlock: Fusion of Blockchain and Federated Learning to Preserve Privacy in Industry 5.0, https://www.sciencedirect.com/science/article/abs/pii/S1566253522001658
-	Federated Learning-based secure Electronic Health Record sharing scheme in Medical Informatics, https://ieeexplore.ieee.org/abstract/document/9774951 




***
## 서울대
Federated Learning for Thyroid Ultrasound Image Analysis to Protect Personal Information: Validation Study in a Real Health Care Environment, https://medinform.jmir.org/2021/5/e25869/

***
## 성균관대
- Open problems in medical federated learning, https://www.emerald.com/insight/content/doi/10.1108/IJWIS-04-2022-0080/full/html
- Federated Learning: Issues in Medical Application, https://arxiv.org/abs/2109.00202
- Personalized Federated Learning with Clustering: Non-IID Heart Rate Variability Data Application, https://arxiv.org/abs/2108.01903 

***
## 삼성병원: 신수용 교수
https://sooyongshin.wordpress.com/2020/11/22/federated-learning/  
Reliability and Performance Assessment of Federated Learning on Clinical Benchmark Data, https://arxiv.org/abs/2005.11756  
Federated Learning on Clinical Benchmark Data: Performance Assessment, https://www.jmir.org/2020/10/e20891  
To evaluate FL in a realistic setting, we implemented FL using a client-server architecture with Python. The implemented client-server version of the FL software was deployed to Amazon Web Services. Modified National Institute of Standards and Technology (MNIST), Medical Information Mart for Intensive Care-III (MIMIC-III), and electrocardiogram (ECG) datasets were used to evaluate the performance of FL. To test FL in a realistic setting, the MNIST dataset was split into 10 different clients, with one digit for each client. In addition, we conducted four different experiments according to basic, imbalanced, skewed, and a combination of imbalanced and skewed data distributions. We also compared the performance of FL to that of the state-of-the-art method with respect to in-hospital mortality using the MIMIC-III dataset. Likewise, we conducted experiments comparing basic and imbalanced data distributions using MIMIC-III and ECG data.

https://saihst.skku.edu/m/45_3_view.php?bbs_data=aWR4PTIxNSZzdGFydFBhZ2U9MTU=%7C%7C  
http://www.hitnews.co.kr/news/articleView.html?idxno=19310  
https://zdnet.co.kr/view/?no=20191101095900  


***
## KAIST

#### Towards the Practical Utility of Federated Learning in the Medical Domain
Towards the Practical Utility of Federated Learning in the Medical Domain, https://arxiv.org/abs/2207.03075  
GitHub: https://github.com/wns823/medical_federated  
- eICU 포함 3가지 dataset 에 대해, Cross-silo 관점에서 실험 -> **D-3. 실증에 참고**
- Kaist 양은호 교수, 건양의대 김종엽 교수  

In this work, for the first time, we test well-known FL algorithms proposed by the machine learning community on three medical datasets in order to evaluate their utility in terms of both performance and monetary cost. Specifically, we select basic FL algorithms as well as those designed for heterogeneous data distributions among different clients (i.e., hospitals). 

We test all algorithms on the three representative real-world medical datasets with different modalities involving structured (i.e., tabular), visual, and signal data as follows:  
• Longitudinal electronic health records (eICU) [35] collected from multiple hospitals in the US for six clinical prediction tasks such as mortality prediction and length-of-stay prediction;  
• Medical images, specifically skin images collected by five institutions from multiple countries for diagnosing multiple skin cancer types;  
• Electrocardiogram signals collected from five institutions from multiple countries, for diagnosing diverse heart conditions.  

>Federated Learning for Electronic Health Records, https://scholar.google.com/citations?view_op=view_citation&hl=ko&user=F2ET1WsAAAAJ&sortby=pubdate&citation_for_view=F2ET1WsAAAAJ:yB1At4FlUx8C  
>[60] Tom J Pollard, Alistair EW Johnson, Jesse D Rafa, Leo A Celi, Roger G Mark, and Omar Badawi. 2018. The eICU Collaborative Research Database, a freely available multi-center database for critical care research. Scientiic data 5, 1 (2018), 1ś13., https://www.nature.com/articles/sdata2018178 

#### Federated Split Vision Transformer for COVID-19 CXR Diagnosis using Task-Agnostic Training
Federated Split Vision Transformer for COVID-19 CXR Diagnosis using Task-Agnostic Training, https://arxiv.org/abs/2111.01338

Sangjoon Park
Bio Imaging, Signal Processing & Learning Lab, Korea advanced institute of science and technology, https://scholar.google.com/citations?user=3H5NDOsAAAAJ&hl=ko&oi=ao 

***
## Google: Privacy-first Health Research with Federated Learning
[Google] Privacy-first Health Research with Federated Learning, https://research.google/pubs/pub50116/

We show on a diverse set of health studies that federated models can achieve the same level of accuracy, precision, and generalizability, and result in the same interpretation as standard centralized statistical models whilst achieving significantly stronger privacy protections.

The federated learning approach enables two types of benefits. 
- First, a higher quality model can be learned by leveraging a broader set of data points, beyond what could be done with the data held by any one participant or data silo. This is particularly important for modern machine learning models that often involve large numbers of parameters and by extension require large amounts of data for training. 
- The second benefit is privacy -- everyone involved keeps their raw and -- in general -- sensitive data local and private. Differential privacy is directly incorporated into the approach to protect individuals’ privacy

At this point, however, only specific large homogenous units of federation, such as at the level of a healthcare system, have been studied in detail in prior work, and the focus has been on traditional classification tasks.

2.2. Electronic medical records (MIMIC-III)
MIMIC-III is a freely available critical care electronic health records (EHR) database involving comprehensive data from approximately 40,000 distinct patients age 16 and older, spanning over 53,000 hospital admissions to Beth Israel Deaconess Medical Center between 2001 and 2012 (Johnson et al., 2016)

To demonstrate the efficacy of federated learning on this dataset, we compare the ROC curve of three different experiments: 
(1) TF centralized model: A traditional server-side trained model assumes all data is available on a centralized server. 
(2) TF federated cross-device model: A model trained on clients on a per-patient basis. Each training round has 16 participating patients, and we trained the model for 500 rounds. 
(3) TF federated cross-silo model: A model training on clients on a per-silo basis. We use a Dirichlet distribution with parameter alpha of 10 to randomly group all patents to 20 groups of various sizes according to the distribution, and select 5 groups to participate in each federated training round.

***
## Harvard
A Review of Medical Federated Learning: Applications in Oncology and Cancer Research, https://link.springer.com/chapter/10.1007/978-3-031-08999-2_1  
Download conference paper PDF, https://link.springer.com/content/pdf/10.1007/978-3-031-08999-2_1.pdf

Federated Learning emerged as a distributed learning paradigm that takes into account several practical challenges, and differentiates itself from traditional distributed learning settings, as noted by Google [20], by addressing four main themes: 
- statistical heterogeneity of data across nodes, 
- data imbalance across nodes, 
- limited communication in the distributed network (e.g., loss of synchronization, variability of communication capabilities), 
- and the possibility of a large number of nodes relative to the amounts of data.


***
Back to the [Top](#list)  
Back to https://github.com/Kwangkee/FL
