# 2020BIGCONTEST
# 스포츠투아이상(최우수상)

최종_득안타_데이터전처리 : 득점, 안타수, 타수 예측을 위한 데이터 전처리

최종_실자이_데이터전처리 : 실점, 자책점, 이닝 수 예측을 위한 데이터 전처리

승률모델:  득점**2 / 득점**2 + 실점**2

타율모델: 안타수 / 타수

방어율모델: (자책점*9)/이닝수

target의 따라 크게 승률, 타율, 방어율 모델로써 후보모델은 Random Forest, XGBoost, LightGBM, MLP

프로젝트 요약

4명이 한 팀으로 진행 하였으며 2016년 정규시즌-2020년 정규시즌 7월 19일까지 약 3200경기 데이터와  크롤링을 통해 추가 수집한  9월 27일 이전까지의 추가 데이터를 분석하여 2020년 9월 27일 이후 경기 결과를 예측하여 잔여시즌 동안 팀 별 승률 타율 방어율을 예측했다.

“강우콜드 게임”은 이상치로 판단하여 단순히 5회 6회에서 끝난 경기 뿐만 아닌 9회나 연장에서 비가 와서 콜드 경기로 처리된 경기까지 찾아낼 수 있는 파생변수를 생성하여 이상치를 찾고 득실점이 비슷한 정상적인 경기로 대체 하였다.

EDA와 도메인 지식에 근거하여 다양한 파생변수를 생성하였으며, 야구의 통계학적 지표인 세이버메트릭스를 기반으로 한 예측 선발투수 변수, 선발 선수 변수, 타순 변수, 상대팀 전적과 최근 경기의 가중평균을 한 변수 등의 파생변수를 사용하였다.

모델링은 직전 경기 묶음을 통해 다음 경기를 Target으로 하는 방식으로 진행하였으며  random Forest, XGBoost, LightGBM, MLP 등 다양한 머신러닝, 딥러닝 기법을 비교 및 평가하여 최종 승률 타율 방어율 모델을 구축하였다. 
