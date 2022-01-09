

# **영화추천시스템 ( 총 100 점 )**

MovieLens latest small 데이터셋을 다양한 방법으로 분석해보세요.데이터셋은 다음의 주소에서 다운로드 받을 수 있습니다.https://grouplens.org/datasets/movielens/latest/

sklearn, pytorch 등 외부 라이브러리 사용 가능합니다.하나의 ipynb파일에 다음 Task들을 모두 수행하여 제출하세요.파일명은 “이름_학번_p02.ipynb”로 하여 제출하세요.

## **Task 1. ( 15** 점 **)** 데이터 준비하기

● Task 1-1. (5 점) 파일을 다운로드 받고 (requests, zipfile 사용), ratings.csv 파일을 읽어서 80%20% 비율의 train, test 데이터로 나누기

● Task 1-2. (5 점) movies.csv 파일을 읽고, 장르를 집합으로 변환하기

● Task 1-3. (5 점) tags.csv 파일을 읽고, tag들을 모두 소문자로 변환 후, 영화별로 tag들을 묶어서집합으로 변환하기 (예: 122912번 영화(Avengers: Infinity War - Part I)의 tag집합 = {visuallystunning, visually appealing, thor, thanos, sad, robert downey jr., mcu, marvel, guardians ofthe galaxy, great villain, emotional, dr. strange, dark, comic book})

## **Task 2. ( 25** 점 **) Latent Factor** 모델을 이용하여 학습하기

● Task 2-1. (20 점) P, Q 등 파라미터 초기화 후, optimizer 등을 이용해서 학습하기

○ 기본 5 점

○ (+5 점) bias 추가

○ (+5 점) regularization 추가

○ (+5 점) hyper parameter (learning rate, regularization weight 등) 탐색

● Task 2-2. (5 점) 학습데이터와 검증데이터에 대해서 각각 RMSE값을 구하여 출력하기 (trainingRMSE, test RMSE)

## **Task 3. ( 20** 점 **) 514** 번 **User** 에게 추천하기 **(knn search, similarity)**

● Task 3-1. (10 점) 514번 user의 예상 별점이 가장 높은 영화 20 개를 찾아서 id 및 영화 이름출력하기

● Task 3-2. (10 점) 장르 및 tag를 기준으로, 514번 user가 5 점을 준 영화들을 찾고, 각각의 영화와가장 유사한 영화를 5 개씩 찾아서 id, 영화 이름, 유사도 점수 출력하기

## **Task 4. ( 15** 점 **)** 영화 클러스터링하기 **(k-means clustering)**

● Task 4-1. (5 점) cosine similarity를 기준으로 영화 벡터 (P혹은 Q)에서 k-means clustering구하기 (k=1, ..., 40 까지 바꿔가면서 cost 값을 계산)

● Task 4-2. (5 점) Task 4-1에서 구한 결과를 matplotlib를 활용하여 그래프로 그린 후 가장 적절해보이는 k값 선택하기

● Task 4-3. (5 점) 122912번 영화(Avengers: Infinity War - Part I)와 같은 cluster에 속한 다른 영화중 cosine similarity가 가장 높은 영화 20 개를 찾아서 id, 영화 이름, 유사도 점수 출력하기

## **Task 5. ( 25** 점 **)** 차원 축소 및 시각화 **(PCA)**

● Task 5-1. (5 점) P 행렬와 Q 행렬을 합쳐 Z행렬 만들기

● Task 5-2. (5 점) Z 행렬에서 PCA 수행하여 2 차원 데이터로 줄인 Zp 만들기

● Task 5-3. (15 점) matplotlib을 활용하여 Zp의 scatter plot 그리기

○ Task 5-3-1. (5 점) P행렬과 Q행렬의 점들을 서로 다른 색으로 그리기

○ Task 5-3-2. (5 점) Task 3-1의 결과 점들을 다른 색으로 그려 강조하기

○ Task 5-3-3. (5 점) Task 4-2의 k값으로 구한 cluster들을 각기 다른 색으로 그리기
