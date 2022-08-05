***
Back to https://github.com/Kwangkee/FL
  


# 동적인 디바이스 환경에서 적응적 연합학습기술 개발 (Adaptive Federated Learning in Dynamic Heterogeneous Environment)  
- iitp 차세대인공지능핵심원천기술개발 사업, https://ezone.iitp.kr/common/co_0701/view?PMS_TSK_DGR_ID=2021-0-00900-002 
- 개요, https://itfind.or.kr/WZIN/jugidong/2052/file7276313400751184193-205203.pdf
- PPT, https://drive.google.com/drive/u/0/folders/1AQqRxsYB34W7xzvkt2xQo2PnAwGyy3Kt

## R&R
>- [T1] KAIST, https://nmsl.kaist.ac.kr/
>- [T2] 성균관대 CSI그룹, http://comnet.skku.edu/
>- [T3] TVSTorm, http://tvstorm.com
>- [N1] 가천대, https://sites.google.com/view/keylee
>- [N2] 광운대, http://bcml.kw.ac.kr/ 

![image](https://user-images.githubusercontent.com/109835677/182520164-95e3b716-983b-4237-9d51-08193f8a2167.png)

## [Paper]
#### [T1, KAIST] 
-	FedBalancer: Data and Pace Control for Efficient Federated Learning on Heterogeneous Clients (ACM MobiSys 2022), https://dl.acm.org/doi/abs/10.1145/3498361.3538917 : 이기종 사용자 기기가 포함된 환경에서의 최적화된 사용자 학습 데이터 선택 및 연합학습 라운드의 데드라인 제어를 통한 효율적인 연합학습 알고리즘 연구
> The source code of our FedBalancer implementation are available at https://github.com/jaemin-shin/FedBalancer
>> For the testbed experiment on Android devices in our paper (Section 4.6), please refer to the following repository: [flower-FedBalancer-testbed](https://github.com/jaemin-shin/flower-FedBalancer-testbed).  

>	보도자료: http://www.aitimes.kr/news/articleView.html?idxno=25693  

-	MyDJ: Sensing Food Intakes with an Attachable on Your Eyeglass Frame (ACM CHI 2022, best paper award honorable mention), https://dl.acm.org/doi/abs/10.1145/3491102.3502041 : 딥러닝 기반의 안경 부착형 웨어러블 기술 개발

#### [T2, 성균관대] 
-	An Efficient Combinatorial Optimization Model Using Learning-to-Rank Distillation (AAAI 2022), https://ojs.aaai.org/index.php/AAAI/article/view/20845  
-	Structure Learning-Based Task Decomposition for Reinforcement Learning In Non-Stationary Environments (AAAI 2022), https://aaai-2022.virtualchair.net/poster_aaai4189 : 동적 환경에서의 다중 태스크에 대한 강화학습 기반 최적 제어 정책을 생성하기 위한 태스크 임베딩 기법 연구
-	Differentiable Ranking Metric Using Relaxed Sorting for Top-K Recommendation (IEEE ACCESS 2021), https://ieeexplore.ieee.org/abstract/document/9514867
- Gemma: Reinforcement Learning-Based Graph Embedding and Mapping for Virtual Network Applications (IEEE ACCESS 2021), https://ieeexplore.ieee.org/document/9496654
-	Repot: Transferable Reinforcement Learning for Quality-Centric Networked Monitoring in Various Environments (IEEE Access 2021), https://ieeexplore.ieee.org/document/9599665 : [T2] 이종/동적 환경에서의 강화학습 기반 네트워크 리소스 관리 에이전트 연구  
- Federated Offline Reinforcement Learning for Autonomous Systems, 2022
- Integrating A Deep Learning-based Plane Detector in Mobile AR Systems for Improvement of Plane Detection, ICCAI, 2022
- Iterative Pruning-based Model Compression for Pose Estimation on Resource-constrained Devices, ICMVA, 2022
- Mean-variance Based Risk-sensitive Reinforcement Learning with Interpretable Attention, ICMWA, 2022
- Reinforcement Learning based Load Balancing in a Distributed Heterogeneous Storage System, ICOIN, 2022
- Transfer Learning based Precise Pose Estimation with Insufficient Data, ICMWA, 2022

#### [T3, TVS] 
-	Assessment of ROI Selection for Facial Video-Based rPPG (MDPI Sensors 2021), https://www.mdpi.com/1424-8220/21/23/7923 : [T3-1] 헬스케어 서비스 분야에서, 원격-PPG 기반 생체징후인식 실세계 적용 시나리오에 적응적 연합학습 기술을 적용하기 위한 기반기술
>The software is available on GitHub (https://github.com/TVS-AI/Pytorch_rppgs (accessed date 26 November 2021)) for experimentation.

-	MovieDIRec: Drafted-Input-Based Recommendation System for Movies (MDPI Appl. Sci. 2021): [T3-2] 콘텐츠 서비스 분야에서 개인맞춤형 추천 실세계 적용 시나리오에 적응적 연합학습 기술을 적용하기 위한 기반기술, https://www.mdpi.com/2076-3417/11/21/10412

## [공개 SW]
-	[T1, KAIST] Federated MetaSense, https://github.com/nmsl-kaist/federated-metasense : Flower framework을 기반으로 다양한 Federated MetaSense 알고리즘 후보를 구현하고, 그 결과를 여러 데이터셋을 활용하여 분석
-	[T3, TVS] Implementation of Deep Learning based Rppg Model using pytorch, https://github.com/TVS-AI/Pytorch_rppgs : [T3-1] 헬스케어 시나리오(rPPG 기반 Vital Sign Monitoring)에 적응적 연합학습 기술을 적용하기 위한 Backbone Deep Learning 알고리즘을 시험/평가하기 위한 프레임워크

## [SW 등록]
- [T2, 성균관] 연합 강화학습 개인화를 위한 리플레이버퍼 공유 기반 가속 학습 방법
- [T2, 성균관] 위험 강화학습에서의 행동 분석 프로그램


## [성과홍보]
-	동적인 디바이스 환경에서 적응적 연합학습 기술, https://itfind.or.kr/publication/regular/weeklytrend/pastList/read.do?selectedId=1237 
- KAIST-칭화대 공동연구팀, 모바일 기기에서 인공지능 '연합학습 속도 4.5배' 높이는 획기적 기법 개발, http://www.aitimes.kr/news/articleView.html?idxno=25693
- 제한된 네트워크 환경에서의 전이 강화 학습 기반 드론 운행 기법

## [Reference]
- IITP, 인공지능 기술청사진 2030 2차년도 보고서, https://www.iitp.kr/kr/1/knowledge/openReference/view.it?ArticleIdx=5248&count=true  
- “중앙집중식 ML 방식에서 로컬라이징” [특별기획 AI 2030] ⑲ 연합학습, https://www.aitimes.com/news/articleView.html?idxno=136724  

***
Back to the [Top](#Paper)  
Back to https://github.com/Kwangkee/FL
