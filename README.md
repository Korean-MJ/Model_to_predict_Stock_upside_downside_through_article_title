# Semi-Project : Model to predict Stock upside, downside through article title

멀티캠퍼스 세미 프로젝트 2023.06 - 2023.07

<img width="406" alt="image" src="https://github.com/Korean-MJ/Model_to_predict_Stock_upside_downside_through_article_title/assets/131749711/f551e342-ea75-4b0d-9d7e-45530cd7252e">












분석 배경
-------------------------------------------------------------------------------
1. 2020년을 기점으로 주식 붐이 일면서 주식 시장에 많은 투자자 유입
2. 하지만 주식에 무지하며, 주변의 영향으로 또는 자신의 직관에 의존해 투자하는 경우가 빈번
3. 이에 주식 투자 판단에 도움을 줄 수 있는 숏리뷰 서비스를 개발하여, 주식 입문자들에게 제공하고자 함


모델 플로우
-------------------------------------------------------------------------------
1. 한경 컨센서스와 네이버 뉴스 제목을 데이터로 수집
2. 불용어 제거 및 OKT와 MECAB으로 형태소 분석
3. KERAS/ TF-IDF/ COUNTVECTORIZER/ WORD2VEC으로 벡터화 진행
4. train/test 데이터셋 분리
5. 모델링 시 Machine Learning 모델로 RandomForest, AdaBoost, Naive Bayes Classifier 사용
6. 모델링 시 Deep Learning 모델로 LSTM과 BERT 사용
7. 결과 도출


요약
-------------------------------------------------------------------------------
1. 뉴스 제목으로 주식의 상향/하향을 분류하는 모델 개발
2. 3개의 조와 SentenceTransformer를 이용해 총 4가지 방식으로 데이터 전처리를 진행함
3. RandomForest, 나이브베이즈, AdaBoost, LSTM, BERT 모델을 이용하여 각 모델별로 성능을 비교함
4. 실험결과, b조의 전처리+Mecab+Keras+AdaBoost모델의 가장 높은 accuracy 점수를 보임
5. 그러나 실전 적용에서는 SentenceTransformer+Naive Bayes Classifier가 가장 잘 분류함


추후 시사점
-------------------------------------------------------------------------------
1. GridSearchCV와 파라미터 조정 등 성능 개선을 시도했지만 유의미한 결과가 나오지 않음
2. 데이터셋이 237개로 작아 학습이 잘 되지 않아 전반적으로 모델 성능이 뛰어나지 않음
3. 학습에 활용된 한경 컨센서스의 데이터 중 상향/하향 또한 "예측"에 불과하고 실제 상향/하향과 차이가 있음
4. 리포트와 뉴스의 차이점을 잘 반영하지 못해 분류가 잘 되지 않는 모델이 있음
5. 보완점 : 본 프로젝트에선 데이터셋을 늘려 진행하면 성능이 나아질 것으로 예상


