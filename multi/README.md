# MULTI CAMPUS 내용 정리

그날그날 수업한걸 올리는 방식으로 진행함
참고했던 사이트나 자료 무작위로 같이 첨부할 예정
>> 기존것들은 시간되는 대로 정리할 예정

## 7월 30일

오랜만에 올리는 수업내용 정리..
금일 일단 문제해결 빅데이터 구현에서 회귀/군집화 부분들을 배웠는데
마지막 날이다보니 수업속도가 빨라 손타이핑이 거의 없었다..ㅠㅠ
(강사님이 그럴 시간을 못주심..ㅠㅠ)
그래서 아쉬운데로 수업노트적고, 내용물은 정리되는대로 다시 올릴예정!


## 6월 22일
project 미팅 2차
디장고 셋업
디장고 어드민 비번이 이상하게 되서 ㅋㅋㅋ admin아이디 날림ㅋㅋㅋ
https://docs.djangoproject.com/ko/3.2/intro/tutorial02/

## 6월 21일

까먹음.... 비쥬얼스튜디오 셋업

## 6월 18일
Regression과 classification의 차이
regresstion (회귀분석)은 연속적인 값들에 대한 분석에 사용
Classification은 카테고리화된 데이터들에 대한 분석에 사용


## 6월 17일
tip.csv파일로 계속 돌려보는 수업
여러 변수간의 관계를 확률로 나타내고 공분산으로 그 관계성을 파악하기 위해
tip/size의 각 평균과 분산에 대해 2X2 matrix로 관계성을 파악함
참고로 두 변수간 covariance가 0이라면 원형(?)에 가까운 값들이 있는것이고
각각 미분으로 양의 기울기, 음의 기울기에 따라 1, -1에 가까운 값을 가짐

오늘의 중요 내용은 각각 어느 상황일때
데이터 프로세싱의 RFE. PCA, Regreession 등의 방법을 쓰느냐인데
오늘까지 내가 이해한 바로는 다음과 같을때 각각을 주로 쓴다

RFE : Supervised되는 항목이므로 fit할때 목표변수(즉 y)값이 있다
      ANOVA로 생각하면 됨
      
PCA : 한마디로 목표변수는 버리고 인풋파라미터끼리 그 중요도를 따져 차원을 버리는 것 (Dimensional Reduction)

Regression : Pearson상관관계로 input/output다 numerical일때 그 경향성(?)을 보는것

사실 이론도 이론이지만 수업 따라가면서 사실 벅찬게
아이들이 번갈아대며 불러대니 갔다오면 수업 내용을 놓치기 일쑤다.ㅠㅠㅠ
그래서 이론도 그렇지만 교수님께서 코드를 짜실때 이걸 왜 쓰는지에 대해 놓치는 부분이 많아
요새 살짝 내가 이걸 배울수 있을까 회의감이 든다 ㅠㅠㅠㅠㅠ


## 6월 16일
SQL Workbench : 직관적으로 데이터셋을 분석할 수 있도록 도와주는 툴
오늘은 SEABORN과 matplotlib 등을 통해 데이터를 Visualization하는 법들을 배움
SEABORN은 HUE라는 카테고리가 있는데 X-Y data set에서 하나의 분리요소로 CLASS가 있는 라벨을 삽입하는 개념이 있다
SEABORN에서는 REGRESSION을 통해 데이터를 의미있게 사용/분석할 수 있다
tip.csv파일을 통해 우리가 추가 변수를 만들고 그 변수를 분석에 이용해봄
target = y hat(통계용어) = 목표변수
**생각해볼 수 있는 목표변수**
1. 매출
2. 팁
3. 요일별 사이즈
4. tip rate
5. 요일별 방문예상팀수
pairplot을 이용한 쌍대비교
데이터는 어떻게 분석하는지도 중요하지만 **무엇을 예측해야하는지**가 제일 중요하다

>> 수업 진행한 파일들(내 컴퓨터 기준, 기타 PPT/Csv파일등은 제외)
>> 3-matplotlib.ipynb
>> 4-seaborn.ipynb
>> plot1.ipynb
>> tips_pandas.ipynb 등..

>> 수업에 참고한 링크들
>> https://pandas.pydata.org/pandas-docs/stable/getting_started/comparison/comparison_with_sql.html#compare-with-sql
>> https://matplotlib.org/stable/tutorials/introductory/usage.html#sphx-glr-tutorials-introductory-usage-py
>> https://seaborn.pydata.org/tutorial/regression.html#functions-to-draw-linear-regression-models 



## 6월 15일

잉...??? 어제 분명 작성했는데 사라짐 ㅠㅠㅠㅠ
JOIN LEFT JOIN이런거 했는데;;


## 6월 14일

오늘부터는 풀스택 프로그래밍으로 SQL설치부터 Data understanding의 개념등을 배웠다
전통의 SQL, 그래고 noSQL(not only SQL, 모바일 등 개인에 대한 로그)의 개념
SQL Workbench 설치 및 설정(MySQL 8.0.25v)
SQL의 기본 문법 등
개인적으로 SQL의 기본(정~말 기본)문법은 어렵진 않다고 느꼈다.
하지만 강사님께서 얘기하신 대로 NULL값등을 포함한 Raw data를 다각화된 관점으로 돌려보고 그 요지와 관련성, 연관성, 목표변수를 찾아내는 것이 중요하다

참고로 오늘 수업 링크 및 첨부파일은 저장을 안해서 다 날림 ㅠㅠㅠㅠ
하지만 대부분 수업 교재를 바탕으로 진행함.


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




