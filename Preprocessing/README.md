### 모델링 이전 데이터 전처리




 - 0619 - 
 - => gender column의 other를 구분해주는게 모델의 학습에 도움이 될 것 이다. (해당 성분을 구분할때 unlabeled data를 학습에 이용하는게 도움이 될것이다.)
 - 1. unlabeled data 전처리 하기
 - 2. unlabeled data 와 train data 합치기 (gender column을 분류하기 위한 새로운 데이터셋 만들기)
 - 3. 분류 모델을 이용해서 other에 해당하는 데이터 female과 male로 분류하기
