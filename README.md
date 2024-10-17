# SKN05-2ST-3TEAM

## 2차 프로젝트 - 통신사 고객 이탈 분석 및 예측 📈
  - 기간 2024.10.16 ~ 2024.10.17


## 0. 팀 소개 

  ### 팀명 
  [ 나 혼자 산다 🏠 ]
  
  ### 팀원 👥
  
  | 남석준           | 황호준        | 장정호       | 김지연         | 조주영        |
  |---------------------------|-----------------------|-----------------------|-----------------------|-----------------------|



## 1. 프로젝트 개요 📌


### 소개
본 프로젝트는 통신사 고객의 이탈을 분석하고 예측하기 위해 진행되었습니다. Kaggle의 cell2cell 데이터셋을 활용하여 고객의 행동 패턴과 이탈 요인을 분석하고, 머신러닝과 딥러닝 기법을 통해 예측 모델을 개발했습니다. 

또한, Customer Churn Prediction in Telecommunication Industry Using Deep Learning 논문을 참고하여 전처리 작업과 모델 성능을 개선하는 데 중점을 두었습니다.


### 필요성
통신사 같은 구독 기반 서비스에서 고객 이탈은 기업에 큰 손실을 초래할 수 있습니다. 따라서 이를 예측하는 것이 수익성 유지와 경쟁력 확보에 필수적입니다.



### 목표
이 프로젝트의 주요 목표는 전처리 작업의 중요성 강조와, 데이터 전처리를 통한 모델 성능 개선입니다. 논문을 기반으로 더 나은 결과를 도출하기 위해 다양한 기법을 적용하여 전처리 작업을 강화하고, 이를 통해 보다 정확하게 예측하는 모델을 구축하려 하였습니다. 



## 2. 기술스택 
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=ffffff) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=ffffff) ![Machine Learning](https://img.shields.io/badge/Machine%20Learning-FF6F20?style=flat&logo=google&logoColor=ffffff) ![Deep Learning](https://img.shields.io/badge/Deep%20Learning-FF6F20?style=flat&logo=tensorflow&logoColor=ffffff)



## 3. 과정 📌

### 1) EDA

  - 타겟 시각화

    
![image](https://github.com/user-attachments/assets/655e949a-fb15-4c4a-b5ad-2497403c5dae)

 




### 2) 데이터 전처리 요약

#### 1. 결측치 처리
- **최빈값 대체**: `Handsets`, `HandsetModels`, `CurrentEquipmentDays`의 결측치는 각 컬럼의 최빈값으로 대체.
- **컬럼 삭제**:
  - `AgeHH1`, `AgeHH2`: 다수의 0값이 결측치로 존재하여 삭제.
  - `HandsetPrice`, `MaritalStatus`: 'unknown' 값으로 결측치 다수 존재 → 삭제.
  
#### 2. 범주형 데이터 처리
- **`CreditRating`**: 
  - 범주형 변수로, ('1-Highest', '4-Medium', '3-Good', '6-VeryLow', '2-High', '5-Low', '7-Lowest') 의미가 있는 서열을 가짐.
  - **Ordinal Encoder**를 적용하여 순서를 반영.

#### 3. 서비스 지역 분류
- **서비스 지역**: 
  - 동부, 서부, 중부, Q(동부, 서부, 중부에 속하지 않는 지역) 총 4가지 분류로 매핑.
    
    ![2](https://github.com/user-attachments/assets/da3a2670-9979-4f72-a894-ea09803a07d0)


#### 4. 수치형 데이터 처리
- **중앙값 대체**: 
  - `MonthlyRevenue`, `TotalRecurringCharge`, `DirectorAssistedCalls`, `OverageMinutes`, `RoamingCalls`, `PercChangeMinutes` 등은 중앙값으로 결측치 대체.
- **최빈값 대체**:
  - `MonthlyMinutes`는 최빈값으로 대체.

#### 5. 추가 피처 생성
- **Call 관련 컬럼**: 휴대폰 사용료 대비 사용량을 계산하여 새로운 컬럼으로 변환.
  
#### 6. 변화율 데이터 이진화
- **`PercChangeMinutes`, `PercChangeRevenues`**: 
  - 통화시간 변화율과 수익 변화율을 0과 1로 이진화 처리. 양의 증가율은 1, 음의 증가율은 0으로 변환.



  #### 인코딩
  - 이진형 데이터 인코딩
  - one-hot encoding(Service Area, PrizmCode, Occupation)

    
  #### df -> int형으로 전환




### 3) 모델



##  4. 한 줄 회고 
- 남석준 👨‍💻

  최고의 팀 '나혼자 산다' 여러분 모두 고생하셨습니다. 또 만납시다~😁

- 장정호 👨‍💻

  좋은 팀원들을 만나 좋았습니다

- 김지연 👩‍💻

  배운 것을 한번 씩 사용해 볼 수 있는 좋은 기회였던 것 같습니다. 팀원분들 도와주셔서 감사합니다!

- 조주영 👨‍💻

  머신러닝이나 딥러닝을 배울때 전처리를 하지 않으면 데이터가 불명확해져서 학습하는데 어려움을 겪는다는 강사님의 말을 이번 프로젝트를 통해서 알게되었습니다. 
  자료를 확인하는 것도 중요하지만 그것을 어떻게 활용하는지가 더 중요한 것이라고 생각하는 프로젝트였습니다.

- 황호준 👨‍💻

  많은 성장을 하는 계기가 되었습니다.
  