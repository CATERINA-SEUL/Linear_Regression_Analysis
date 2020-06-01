# Linear_Regression_Analysis

-----

> ### Dacon - AI 프렌즈 시즌1 온도 추정 경진대회
> ![dacon](https://user-images.githubusercontent.com/46242120/83408422-87712e00-a44d-11ea-8145-675cb8b7e92e.png)

-----
## 1. 데이터 설명

![proj](https://user-images.githubusercontent.com/46242120/83408345-6ad4f600-a44d-11ea-83fe-df27162702c7.png)

- **각 위치에서 기온, 누적강수량, 풍속, 풍향, 해면기압, 현지기압, 일사량, 습도 모두 측정**
- 대전지역에서 측정한 실내외 19곳의 센서데이터와 주변 지역의 기상청 공공데이터를 semi-비식별화하여 제공합니다. 
    - 센서는 온도를 측정하였습니다. 
    - 모든 데이터는 시간 순으로 정렬 되어 있으며 10분 단위 데이터 입니다. 
    - 예측 대상(target variable)은 Y18입니다. 
    
> ### train.csv 
    - 30일 간의 기상청 데이터 (X00~X39) 및 센서데이터 (Y00~Y17)
    - 이후 3일 간의 기상청 데이터 (X00~X39) 및 센서데이터 (Y18)
> ### test.csv 
    - train.csv 기간 이후 80일 간의 기상청 데이터 (X00~X39)
------
## 2. 분석과정

![data_info](https://user-images.githubusercontent.com/46242120/83408515-b091be80-a44d-11ea-93c1-3041b18494bd.png)

----
## 3. Package

    from sklearn.model_selection import KFold
    from sklearn.ensemble import RandomForestRegressor
    from sklearn.model_selection import GridSearchCV
    from sklearn.model_selection import train_test_split
    from sklearn.metrics import mean_squared_error, accuracy_score, make_scorer
    from sklearn.linear_model import Lasso, Ridge
    %matplotlib inline
	
----
## 4. 결과

> MSE 3.94 / 상위 11% (378명 참가) 
[Linear Regression Project](https://github.com/CATERINA-SEUL/Linear_Regression_Analysis/files/4711156/Linear_regression_temperature.pdf)

