Back to https://github.com/Kwangkee/FL
***

- Federated learning for smart healthcare: A survey, https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&q=Federated+Learning+for+Smart+Healthcare%3A+A+Survey&btnG=


***

## 신수용
https://sooyongshin.wordpress.com/2020/11/22/federated-learning/  
Reliability and Performance Assessment of Federated Learning on Clinical Benchmark Data, https://arxiv.org/abs/2005.11756  
Federated Learning on Clinical Benchmark Data: Performance Assessment, https://www.jmir.org/2020/10/e20891  
To evaluate FL in a realistic setting, we implemented FL using a client-server architecture with Python. The implemented client-server version of the FL software was deployed to Amazon Web Services. Modified National Institute of Standards and Technology (MNIST), Medical Information Mart for Intensive Care-III (MIMIC-III), and electrocardiogram (ECG) datasets were used to evaluate the performance of FL. To test FL in a realistic setting, the MNIST dataset was split into 10 different clients, with one digit for each client. In addition, we conducted four different experiments according to basic, imbalanced, skewed, and a combination of imbalanced and skewed data distributions. We also compared the performance of FL to that of the state-of-the-art method with respect to in-hospital mortality using the MIMIC-III dataset. Likewise, we conducted experiments comparing basic and imbalanced data distributions using MIMIC-III and ECG data.

https://saihst.skku.edu/m/45_3_view.php?bbs_data=aWR4PTIxNSZzdGFydFBhZ2U9MTU=%7C%7C  
http://www.hitnews.co.kr/news/articleView.html?idxno=19310  
https://zdnet.co.kr/view/?no=20191101095900  


## Google
Privacy-first Health Research with Federated Learning, https://research.google/pubs/pub50116/

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

## KAIST
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
