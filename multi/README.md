# MULTI CAMPUS 내용 정리

그날그날 수업한걸 올리는 방식으로 진행함
참고했던 사이트나 자료 무작위로 같이 첨부할 예정
>> 기존것들은 시간되는 대로 정리할 예정



## 6월 11일

오늘의 KEY POINT는 머신러닝의 대표적인 방법론인
**CRISP_DM** 모델에 대해 집중적으로 확인했다
1. 이전에 배웠던 차원에 대한 축소가 필요하나 그와 동시에 비지니스 이해와 데이터의 이해를 통한 파생변수에 대한 정리도 필요하다.
2. 하지만, 우리가 사전 학습된 모델에서부터 머신러닝을 시작할 경우, model+dataset에 BIAS가 있을 수 있음을 이해해야 한다.
3. 따라서 우리가 어떤 프로젝트를 할때, CRISP-DM 모델로 진행하는 단계들을 표시하면서, 내가 시작한 지점이 어디인지도 보고서 형식으로 작성하는게 중요하다
4. CRISP-DM외에도 다른 방법론들이 있다. e.g.)Microsoft AZURE model

### [[머신 러닝 Data preparation에 대한 절차]]
5. One Hot encoding
    변수의 개수만큼 비트를 잡아 고유한 범주들에 매핑하는 작업
    e.g.)1~7로 작성된 월요일~일요일에 대한 데이터 값을 요일별 7개의 열로 나누어 값을 매핑
6. label encoding
    각각의 변수에 대해 변수개수-1개만큼 값을 지정하여 매핑
    e.g.) Male/Female => 0/1로 치환, 

### [[Feature selection method 선택방법]]
![image](https://user-images.githubusercontent.com/85263094/121691996-9380d880-cb02-11eb-9fe7-ece5acb4d91b.png)
선생님 강의 자료
Pearson : 변수간 데이터가 선형인 경우
spearman : 변수간 데이터가 비선형인 경우
Chi : 범주형 변수값이 여러개인 경우 쓰이나 실제로는 그런 경우 ANOVA 분석을 여러개 만들어 해결한다고 한다.

+ 중간평가 : 다행히 PASS...

>> 수업 진행한 파일들(내 컴퓨터 기준, 기타 PPT/Csv파일등은 제외)
>>  KBinsDiscretizer.ipynb
>>  Classification Feature Selection.ipynb
>>  one hot encode.ipynb

>> 수업에 참고한 링크들
>> https://docs.microsoft.com/ko-kr/azure/machine-learning/team-data-science-process/overview
>> https://www.2e.co.kr/news/articleView.html?idxno=301010
>> https://www.hanbit.co.kr/support/supplement_list.html
>> https://www.youtube.com/watch?v=vusSCU-gn4A



 
 
## 6월 10일

머신 러닝 Data preparation에 대한 절차를 확인함
그 중,

1. 데이터를 준비/수집하고
2. 결측치(imputer)를 처리하는 기본 과정이 필요함
    결측치는 simpleimputer를 임포트 하여 사용했음
3. 특징 추출(RFE)
    목표변수와 비교하여 분석에 필요한 column을 골라내서 분석할 차원을 줄여줌
    RFE분석은 Tree 알고리즘에 넣어서 decision하게됨
4. 데이터 정규화(Normalization과 Standardization)
    Normalization : 정규분포로 만드는 작업.
    Standardization : 표준정규분포로 만드는 작업(평균이 0, 분산이 1이 되도록)
    
 .....
 
 7. PCA 통한 차원축소 먼저 수업
    어제 배웠듯이 차원이 커지면 데이터 밀도가 줄어들어 학습 능력이 저하되기 때문에 차원의 저주를 피하기 위한 차원 축소가 필요함
    반대 예제 ) kernel trick
 
 RFE를 하는것과 PCA를 하는것의 차이
 PCA는 데이터를 쳐내는 개념, but RFE는 컬럼을 중요도에 따라 선택하는것
 
 기타)어제 앙상블 기법에 대해 배웠다는데 나는 기억이 나질 않는다... 찾아봐야지.....ㅠㅠㅠ

NeuarlNetwork(인공신경망)모델에서의 분석에는 Standard scaler로 데이터 세트를 표준화 하는 과정이 필요하다
XGBoost에서는 Tree algorithm을 씀으로 해서 data가 섞이지 않기때문에 Standard Scaler가 필요하지 않다.

>> 수업 진행한 파일들(내 컴퓨터 기준, 기타 PPT/Csv파일등은 제외)
imputer.ipynb
RFE.ipynb
RFE2.ipynb
12-0xgb.ipynb
3-NeuarlNetwork7.ipynb
xgboost_pdp_ice.ipynb
PCA.ipynb
PCA2.ipynb

>> 수업에 참고한 링크들
>> https://www.kaggle.com/uciml/horse-colic
>> https://gist.github.com/JSJeong-me/7d6a3f852eb0e9eb451e4c153af6cc6f
>> https://www.youtube.com/watch?v=g-Hb26agBFg
>> https://www.youtube.com/watch?v=e50Bj7jn9IQ


 
 
## 6월 09일

Recall / Precision의 구분. 개념정리
보통 imbalanced된 data set에서는 Recall 매트릭스로 진행함

**다중공선성 : 같은 방향성을 가진 column을 하나로 통일하는것

데이터 분석에서 다중공선성 제거가 중요한 이유
1. 분산값을 교란시킴
2. 연산(computing power)를 약화시킴
3. 차원을 줄여 data빈곳을 줄여줌(차원의 저주)

**그러므로 차원축소(다중공선성)제거가 필요하다!!

최근 API trend 중 하나 : transformer (encording, decording을 같이 하는것)




