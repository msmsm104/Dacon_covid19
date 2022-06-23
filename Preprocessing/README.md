### 모델링 이전 데이터 전처리




 - 0619 - 
 - => gender column의 other를 구분해주는게 모델의 학습에 도움이 될 것 이다. (해당 성분을 구분할때 unlabeled data를 학습에 이용하는게 도움이 될것이다.)
 - 1. unlabeled data 전처리 하기
 - 2. unlabeled data 와 train data 합치기 (gender column을 분류하기 위한 새로운 데이터셋 만들기)
 - 3. 분류 모델을 이용해서 other에 해당하는 데이터 female과 male로 분류하기
### 대성공 (성능 향상)


### 0621
 - gender column을 one-hot-Encoding해주었는데 drop first로 column개수 줄이기 (성능에 영향을 줄지 미지수)
   - => 성능을 직접 확인해보지는 않았지만 악영향을 주는것 같다.
 - 신경망 학습에 있어 모든 입력 feature를 평균 0 , 분산 1이 되도록 변경 (scaling) => 성능에 영향을 줄거라고 예측
 => 전처리된 train, test data set에 대하여 학습, 평가 진행 (결과 이전과 비교)
 
 => 정규화, 표준화 모두 처리후 성능이 떨어짐.
 
 
 - GridSearchCV를 통한 best parameter찾기 (StratifiedKFold사용) => scoring을 무엇으로 정할지가 중요(우선은 roc_auc 값으로 진행 -> hidden_layer_sizes 결과 비교)

  => 성능이 떨어짐


### 0623

=> under sampling적용해보기
