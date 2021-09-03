# 2020BIGCONTEST
2020 빅콘테스트 모델링 코드
target의 따라 크게 승률, 타율, 방어율 모델로써 후보모델은 Random Forest, XGBoost, LightGBM, MLP

승률모델은 득점**2 / 득점**2 + 실점**2

타율모델은 안타수 / 타수

방어율모델은 (자책점*9)/이닝수
