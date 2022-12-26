Back to https://github.com/Kwangkee/FL
***

## Zhenge Jia
- Zhenge Jia, https://scholar.google.com/citations?hl=en&user=ROgpsv0AAAAJ&view_op=list_works&sortby=pubdate
- https://zhengejia.github.io/

#### Personalized Deep Learning for IoT-Enabled Health Monitoring, https://scholar.google.com/citations?view_op=view_citation&hl=en&user=ROgpsv0AAAAJ&sortby=pubdate&citation_for_view=ROgpsv0AAAAJ:Se3iqnhoufwC

However, directly applying deep learning is not always feasible for IoT-enabled health monitoring.  
- [Meta-Learning] First, biosignals are highly variable among patients in terms of morphological characteristics due to individual differences. The detection performances of the pre-trained deep learning model would degrade significantly on some patients. Therefore, effective model personalization methods are in urgent need in patient-specific detection. 
- [SSL] Second, the deep model personalization process still requires an extensive amount of labeled data. In practice, for some applications, it is impractical to obtain adequate labeled samples due to the overwhelmed workload in manual labeling. 
- [FL] Third, the data access is limited due to privacy concerns in certain health monitoring applications, where aggregating personal health data in a centralized server is strictly restricted. 
To address the aforementioned challenges, this dissertation proposes several techniques to enable personalized deep learning for IoT-enabled health monitoring.  
- First, a novel metalearning algorithm and a prior knowledge incorporated learning approach are proposed to obtain a well-generalized model initialization and to regularize the personalization process with medical knowledge. 
- Second, a system-level design is proposed to conduct self-supervised and on-device model personalization. 
- Finally, we propose a personalized meta-federated learning method for distributed IoT health monitors to generate a patient-specific model through collaborative training without accessing personal health data.

***
## Jingtong Hu
- Jingtong Hu, https://scholar.google.com/citations?hl=en&user=OcWo8CYAAAAJ&view_op=list_works&sortby=pubdate

- Federated Learning Framework Aims to Improve Fairness in AI Screening Tools, https://healthitanalytics.com/news/federated-learning-framework-aims-to-improve-fairness-in-ai-screening-tools
>-	October 27, 2022 - A research team from the University of Pittsburgh (Pitt) Swanson School of Engineering has been awarded a $1.7 million National Institutes of Health grant to develop a federated learning (FL)-based approach to achieve fairness in artificial intelligence (AI)-assisted medical screening tools.
- https://news.engineering.pitt.edu/engineering-more-race-inclusive-ai-in-medicine/
>-	Unlike existing frameworks, this framework would rely on **unsupervised learning with data coming from a variety of smartphone models and other devices**, allowing more people to participate in the study. The framework would also have to consider the fairness of different machine learning models. The team will develop a machine learning framework that will automatically search existing learning models and use the best architectures for datasets with diverse data.
- Achieve Fairness in AI-Assisted **Mobile Healthcare Apps through Unsupervised Federated Learning**, https://www.nibib.nih.gov/node/136866

***
## list

- Achieving Fairness in Dermatological Disease Diagnosis through Automatic Weight Adjusting Federated Learning and Personalization, https://scholar.google.com/citations?view_op=view_citation&hl=en&user=OcWo8CYAAAAJ&sortby=pubdate&citation_for_view=OcWo8CYAAAAJ:bz8QjSJIRt4C
>-	In the first in-FL stage, clients with different skin types are trained in a federated learning process to construct a global model for all skin types. An automatic **weight aggregator is used in this process to assign higher weights to the client with higher loss**, and the intensity of the aggregator is determined by the level of difference between losses. 
>-	In the latter post-FL stage, **each client fine-tune its personalized model based on the global model in the in-FL stage**. To achieve better fairness, models from different epochs are selected for each client to …

- Personalized Neural Network for Patient-Specific Health Monitoring in IoT: A Meta-Learning Approach, https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Personalized+Neural+Network+for+Patient-Specific+Health+Monitoring+in+IoT%3A+A+Metalearning+Approach&btnG=
>-	To address the problem, we propose a **metalearning-based personalization** method to generate the personalized neural network for each patient to conduct patient-specific detection. 
>-	Specifically, the proposed metalearning method leverages a novel patientwise training tasks formatting strategy to train the neural network that ends up with a well-generalized model initialization containing across-patient knowledge. The well-generalized model initialization would then be utilized to perform a quick adaptation to the specific patient’s data domain. 
>-	In this way, **a new patient could be immediately assigned with a personalized neural network using limited labeled data**.

- Learning to learn personalized neural network for ventricular arrhythmias detection on intracardiac egms, https://scholar.google.co.kr/scholar?hl=ko&as_sdt=0%2C5&q=Learning+to+learn+personalized+neural+network+for+ventricular+arrhythmias+detection+on+intracardiac+egms&btnG=


***
Back to the [Top](#list)  
Back to https://github.com/Kwangkee/FL
