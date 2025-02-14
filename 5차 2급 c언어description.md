# 문제1
6명이 사다리 게임[^1] 을 할 때, 몇 번째 위치에서 시작하는 사람이 상품을 타는지 알고 싶습니다. 가로줄은 항상 인접한 세로줄만 연결할 수 있으며 주어진 순서대로 위에서부터 연결합니다.

예를 들어, 아래 사다리의 가로줄은 [[1, 2], [3, 4], [2, 3], [4, 5], [5, 6]] 으로 표현합니다. 이때 1번째 위치에서 시작한 사람이 상품을 탑니다.

 ![ladders.jpg](https://grepp-programmers.s3.amazonaws.com/files/ybm/4179093d4d/d2f78792-2661-41bd-9973-f072153ee229.jpg)

가로줄의 위치가 담긴 2차원 배열 ladders, 배열 ladders의 길이 ladders_len, 상품의 위치 win이 매개변수로 주어질 때, 당첨자의 시작 위치를 return 하도록 solution 함수를 작성하려 합니다. 빈칸을 채워 전체 코드를 완성해주세요.

---
##### 매개변수 설명
가로줄의 위치가 담긴 2차원 배열 ladders와 상품이 있는 위치 win이 solution 함수의 매개변수로 주어집니다.
* ladders_len은 1 이상 20 이하인 자연수입니다.
* win은 1 이상 6 이하인 자연수입니다.
* 가로줄은 항상 연결할 수 있는 형태만 주어집니다.

---
##### return 값 설명
승리하는 사람의 시작 위치를 return 합니다.

---
##### 예시

| ladders                                  | ladders_len | win | return |
|------------------------------------------|-------------|-----|--------|
| [[1, 2], [3, 4], [2, 3], [4, 5], [5, 6]] | 5           | 3   | 1      |


[^1]: 사다리 게임은 먼저 사람 수만큼 세로줄을 긋고 한쪽 편에는 이름을 쓰고 반대쪽에는 상품 위치를 씁니다. 서로 인접한 세로줄 사이에 가로줄을 무작위로 그은 다음 세로줄을 타고 내려가면서 가로줄을 만날 때마다 가로줄로 연결된 다른 세로줄로 가는 게임입니다.


# 문제2
공강이란 수업 시간 사이에 수업이 없이 비는 시간입니다. 시간표가 주어질 때 공강은 총 몇 시간인지 구하려 합니다. 시간표 상에 수업이 있는 시간은 1로, 수업이 없는 시간은 0으로 표시합니다. 모든 수업은 정각에 시작해 1시간 뒤에 끝납니다.

  ![스크린샷 2018-10-18 오전 10.04.02.png](https://grepp-programmers.s3.amazonaws.com/files/ybm/249829888e/337a6f09-4e9d-4a31-8406-bc2c95652273.png)

예를 들어, 위 시간표에서 공강은 총 3시간입니다. 
공강이 총 몇 시간인지 구하기 위해 다음과 같이 프로그램 구조를 작성했습니다.

```
1. 가장 첫 수업 시작 시각을 구합니다.
2. 가장 마지막 수업 시작 시각을 구합니다.
3. 1과 2사이에서 수업이 없는 시간을 셉니다.
```

시간표를 표현한 배열 time_table, 배열 time_table의 길이 time_table_len이 매개변수로 주어질 때 공강은 총 몇 시간인지 return 하도록 solution 함수를 작성하려 합니다. 위 구조를 참고하여 코드가 올바르게 동작할 수 있도록 빈칸에 주어진 func_a, func_b, func_c 함수와 매개변수를 알맞게 채워주세요.

---
##### 매개변수 설명
시간표를 표현한 배열 time_table이 solution 함수의 매개변수로 주어집니다.
* time_table_len 5 이상 15 이하인 자연수입니다.
* 시간표에서 수업이 있는 시간은 1로 표현하고 수업이 없는 시간은 0입니다.
* time_table의 원소는 0 또는 1입니다.

---

##### return 값 설명
공강이 총 몇 시간인지 return 해주세요.

---
##### 예시

| time_table                     | time_table_len | return |
|--------------------------------|----------------|--------|
| [1, 1, 0, 0, 1, 0, 1, 0, 0, 0] | 10             | 3      |

##### 예시 설명
문제에 나온 예와 같습니다.



# 문제3
모든 속도위반 차량이 낼 벌금이 총 몇만 원인지 알아내려 합니다. 벌금을 매기는 기준은 다음과 같습니다.

| 기준                   		 | 벌금  |
|---------------------------------|-------|
| 규정 속도 10% 이상 20% 미만 위반 | 3만 원 |
| 규정 속도 20% 이상 30% 미만 위반 | 5만 원 |
| 규정 속도 30% 이상 위반 		 | 7만 원 |

예를 들어 규정 속도가 100인 도로를 112로 달렸다면 규정 속도를 12% 위반하였습니다. 따라서 규정 속도를 10% 이상 20% 미만 위반하였으므로 벌금 3만 원을 부과합니다.

규정 속도 speed, 도로를 달리는 모든 차의 속도가 담긴 배열 cars, 배열 cars의 길이 cars_len이 매개변수로 주어질 때, 총벌금은 몇만 원인지 return 하도록 solution 함수를 작성하려 합니다. 빈칸을 채워 전체 코드를 완성해주세요.

---
##### 매개변수 설명
규정 속도 speed, 도로를 달리는 모든 차의 속도가 담긴 배열 cars, 배열 cars의 길이 cars_len이 매개변수로 주어집니다.
* 규정 속도는 30 이상 140 이하이며, 10으로 나누어 떨어지는 숫자입니다.
* cars_len은 1 이상 40 이하인 자연수입니다.
* 모든 차는 0km/h 이상 200km/h 이하로 달립니다.

---
##### return 값 설명
도로를 달리는 모든 차의 벌금은 총 몇만 원인지 return 해주세요.

---
##### 예시

| speed | cars                              | cars_len | return |
|-------|-----------------------------------|----------|--------|
| 100   | [110, 98, 125, 148, 120, 112, 89] | 7        | 23     |

##### 예시 설명

| 기준                         	| 위반 차량 | 총벌금 |
|----------------------------------|-----------|---------|
| 규정 속도 10% 이상 20% 미만 위반 | 2대   	| 6만원   |
| 규정 속도 20% 이상 30% 미만 위반 | 2대   	| 10만원  |
| 규정 속도 30% 이상 위반      	| 1대   	| 7만원   |


# 문제4
종목은 태권도, 500m 달리기, 사격 경기를 하려 합니다. 종목별 점수 산출 방식은 다음과 같습니다.

| 종목    	| 점수 산출 방식                                                                     	|
|-------------|----------------------------------------------------------------------------------------|
| 태권도  	| 25경기 이상 승리하면 250점. 그 외에는 승리당 8점              	|
| 500m 달리기 | 60초에 완주 시 250점. 그보다 빠르면 1초당 +5점 느리면 1초당 -5점                    	|
| 사격    	| 10번 사격해 과녁에 적힌 숫자의 합만큼 점수 획득. 7번 이상 10점에 맞추면 추가 점수 100점  |

태권도에서 승리한 횟수 taekwondo, 달리기 기록 running, 사격 기록이 담긴 배열 shooting, 배열 shooting의 길이 shooting_len이 매개변수로 주어질 때, 이 선수가 획득한 총점수를 return 하도록 solution 함수를 작성하려 합니다. 빈칸을 채워 전체 코드를 완성해주세요.

---
##### 매개변수 설명
태권도에서 승리한 횟수 taekwondo, 달리기 기록 running, 사격 기록이 담긴 배열 shooting, 배열 shooting의 길이 shooting_len이 solution 함수의 매개변수로 주어집니다.
* 태권도에서는 0회 이상 35회 이하 승리할 수 있습니다.
* 달리기 기록은 초 단위이며 40 이상 120 이하인 정수입니다.
* 사격 과녁에는 0부터 10까지의 숫자가 적혀있습니다.
* shooting_len은 항상 10입니다.

---
##### return 값 설명
이 선수가 획득한 총점수를 return 해주세요.

---
##### 예시

| taekwondo | running | shooting                              | shooting_len | return |
|-----------|---------|---------------------------------------|--------------|--------|
| 27        | 63      | [9, 10, 8, 10, 10, 10, 7, 10, 10, 10] | 10           | 23     |

##### 예시 설명
태권도에서 25회 이상 승리했기 때문에 250점을 획득했습니다.
달리기에서 60초보다 3초 느렸기 때문에 250점에서 15점을 뺀 235점을 획득했습니다.
사격에서 과녁을 맞혀 94점을 받았고, 10점을 7번 맞췄기 때문에 추가 점수 100점을 받아 총 194점을 획득했습니다.
따라서 이 선수가 받은 총점수는 679점입니다.



# 문제5
O일장은 O일마다 열리는 시장을 뜻합니다. 예를 들어 오늘 4일장이 열렸다면, 다음 4일장은 4일 뒤에 열립니다. 오늘부터 a일장과 b일장 제도를 시행하려 합니다. 정수 a, b가 주어졌을 때, a일장과 b일장이 같이 열리는 날은 며칠에 한 번씩 있는지 구하려 합니다.

예를 들어, a가 4이고 b가 6이라면 시장은 다음과 같이 열립니다.

  ![스크린샷 2018-10-18 오후 3.20.05.png](https://grepp-programmers.s3.amazonaws.com/files/ybm/8b5ccc6490/fbf2b7c5-4b29-4aa8-a227-b4d3754d54c7.png)

a와 b가 매개변수로 주어질 때, a일장과 b일장이 같이 열리는 날은 며칠에 한 번씩 있는지 return 하도록 solution 함수를 작성했습니다. 그러나, 그러나, 코드 일부분이 잘못되어있기 때문에, 몇몇 입력에 대해서는 올바르게 동작하지 않습니다. 주어진 코드에서 **한 줄**만 변경해서 모든 입력에 대해 올바르게 동작하도록 수정하세요.

---

##### 매개변수 설명
a일장이 열리는 주기인 a와 b일장이 열리는 주기인 b가 solution 함수의 매개변수로 주어집니다.

* a와 b는 1 이상 30 이하인 자연수입니다.

---

##### return 값 설명
a일장과 b일장이 같이 열리는 날은 며칠에 한 번씩 있는지 return 해주세요.

---
##### 예시

| a | b | return |
|--------|--------|--------|
| 4     | 6      | 12     |

##### 예시 설명
문제의 예와 같습니다.



# 문제6
국어 시험 점수와 영어 시험 점수가 나왔습니다. 이때 국어, 영어, 수학 시험의 평균이 70점 이상이려면 수학 시험 점수가 최소 몇 점이어야 하는지 알고 싶습니다.

국어 점수 korean과 영어 점수 english가 매개변수로 주어질 때, 평균 점수를 70점 이상 받기 위해 받아야 하는 수학 점수의 최솟값을 return 하도록 solution 함수를 작성했습니다. 그러나, 코드 일부분이 잘못되어있기 때문에, 몇몇 입력에 대해서는 올바르게 동작하지 않습니다. 주어진 코드에서 _**한 줄**_만 변경해서 모든 입력에 대해 올바르게 동작하도록 수정하세요.

---
##### 매개변수 설명
국어 점수 korean과 영어 점수 english가 solution 함수의 매개변수로 주어집니다.
* korean과 english는 0 이상 100 이하인 정수입니다.

---
##### return 값 설명
평균 70점을 넘기기 위해 받아야 하는 수학 점수의 최솟값을 return 합니다.
* 수학 점수를 100점을 받아도 평균 70점이 되지 않는 경우에는 -1을 return 합니다.

---
##### 예시

| korean | english | return |
|--------|---------|--------|
| 70 	| 60  	| 80 	|

##### 예시 설명
국어 점수가 70점, 영어 점수가 60점입니다. 따라서 평균이 70점 이상을 받으려면 수학 시험에서 최소 80점을 받아야 합니다.



# 문제7
XX 마트에선 구매할 물건이 3개 이하이면 소량 계산대에서, 그렇지 않으면 일반 계산대에서 계산해야 합니다. 두 계산대 모두 물건 한 개를 계산하는 데 1분이 걸립니다.

손님들이 구매할 물건 수가 담긴 배열 stuffs, 배열 stuffs의 길이 stuffs_len이 매개변수로 주어질 때, 모든 물건을 계산하는 데 필요한 시간을 return 하도록 solution 함수를 작성했습니다. 그러나, 코드 일부분이 잘못되어있기 때문에, 몇몇 입력에 대해서는 올바르게 동작하지 않습니다. 주어진 코드에서 _**한 줄**_만 변경해서 모든 입력에 대해 올바르게 동작하도록 수정하세요.

---

##### 매개변수 설명
손님들이 구매할 물건 수가 담긴 배열 stuffs, 배열 stuffs의 길이 stuffs_len이 solution 함수의 매개변수로 주어집니다.
* stuffs_len은 1 이상 100 이하입니다.
* 손님이 구입할 물건은 1개 이상 20개 이하입니다.

---

##### return 값 설명
모든 물건을 계산하는데 걸리는 시간을 return 해주세요.

---
##### 예시

| stuffs             | stuffs_len | return |
|--------------------|------------|--------|
| [5, 3, 4, 2, 3, 2] | 6          | 10     |

##### 예시 설명

첫 번째 손님, 세 번째 손님은 일반 계산대에서 계산합니다. 이때 9분이 걸립니다.
두 번째, 네 번째, 다섯 번째, 여섯 번째 손님은 소량 계산대에서 계산합니다. 이때 10분이 걸립니다.
따라서 모든 물건을 계산하는데 걸리는 시간은 10분입니다.



# 문제8
상수도 요금을 계산하려 합니다. 가정용 상수도 사용요금 계산방법은 아래와 같습니다.

| 단계  | 사용량	| 요금  |
|-------|-----------|-------|
| 1단계 | 0~20톤  | 430원 |
| 2단계 | 21~30톤 | 570원 |
| 3단계 | 31톤 이상 | 840원 |

사용료는 사용량에 따라 단계별로 적용됩니다. 예를 들어, 물을 35톤 사용했다면 다음과 같은 방식으로 계산합니다.

```
* 1단계 적용 : 20톤 x 430원 = 8,600원
* 2단계 적용 : 10톤 x 570원 = 5,700원
* 3단계 적용 : 5톤 x 840원 = 4,200원
총 사용요금 : 18,500원
```

상수도 사용량 usage가 매개변수로 주어질 때, 사용요금을 return 하도록 solution 함수를 작성했습니다. 그러나, 코드 일부분이 잘못되어있기 때문에, 몇몇 입력에 대해서는 올바르게 동작하지 않습니다. 주어진 코드에서 **한 줄**만 변경해서 모든 입력에 대해 올바르게 동작하도록 수정하세요.

---
##### 매개변수 설명
상수도 사용량 usage가 solution 함수의 매개변수로 주어집니다.
* 상수도 사용량은 0톤 이상 100톤 이하인 정수입니다.

---
##### return 값 설명
사용요금을 return 해주세요.

---
##### 예시

| usage | return |
|-------|--------|
| 35	| 18500  |

##### 예시 설명
문제에 나온 예와 같습니다.



# 문제9
시험 점수에 따라 학생의 순위를 매기려 합니다. 동점자 순위는 가능한 순위 중 가장 높은 순위로 매깁니다.
예를 들어 학생별 점수가 [90, 87, 87, 23, 35, 28, 12, 46]이면, 학생별 순위는 [1, 2, 2, 7, 5, 6, 8, 4]입니다.

모든 학생의 점수를 담은 배열 score, 배열 score의 길이 score_len이 매개변수로 주어질 때, 순위를 담은 배열을 return 하도록 solution 함수를 작성해주세요.

---

##### 매개변수 설명
모든 학생의 점수를 담은 배열 score, 배열 score의 길이 score_len이 solution 함수의 매개변수로 주어집니다.
* score_len은 1 이상 1,000 이하인 자연수입니다.
* 점수는 1 이상 100 이하인 정수입니다.

---

##### return 값 설명
* 순위를 담은 배열을 return 합니다.

---
##### 예시

| score                            | score_len | return                   |
|----------------------------------|-----------|--------------------------|
| [90, 87, 87, 23, 35, 28, 12, 46] | 8         | [1, 2, 2, 7, 5, 6, 8, 4] |
| [10, 20, 20, 30]                 | 4         | [4, 2, 2, 1]             |

##### 예시 설명
예시 #1
문제에 나온 예와 같습니다.

예시 #2
이들의 순위는 [4, 2, 2, 1]입니다.



# 문제10
n명이 시간표에 따라 교대 근무에 들어갑니다. 이때 가장 오래 일한 사람이 몇 시간 일했는지 알아내려 합니다. 근무 순번은 첫 번째 사람부터 n번째 사람 순으로 합니다. n번 사람이 일을 한 뒤에는 다시 첫 번째 사람부터 일을 합니다.

예를 들어 시간표가 [1, 5, 1, 9]이고 n이 3이면 첫 번째 사람은 1+9시간, 두 번째 사람은 5시간, 세 번째 사람은 1시간 근무합니다. 따라서 첫 번째 사람이 가장 오래 일했으며, 10시간 일했습니다.

근무 시간표를 담은 배열 time_table, 배열 time_table의 길이 time_table_len, 사람 수 n이 매개변수로 주어질 때, 가장 오래 일한 사람은 몇 시간 일했는지 return 하도록 solution 함수를 작성해주세요.

---
##### 매개변수 설명
시간표를 담은 배열 time_table, 배열 time_table의 길이 time_table_len, 사람 수 n이 solution 함수의 매개변수로 주어집니다.
* time_table_len은 1 이상 100 이하입니다.
* time_table의 원소는 1 이상 100 이하인 자연수입니다.
* n은 1 이상 `time_table_len` 이하인 자연수입니다.

---

##### return 값 설명
가장 오래 일한 사람이 몇 시간 일했는지 return 합니다.

---
##### 예시

| time_table            | time_table_len | n | return |
|-----------------------|----------------|---|--------|
| [1, 5, 1, 9]          | 4              | 3 | 10     |
| [4, 8, 2, 5, 4, 6, 7] | 7              | 4 | 14     |

---

##### 예시 설명
예시 #1
앞선 예와 같습니다.

예시 #2
첫 번째 사람은 4+4시간만큼 근무를 합니다.
두 번째 사람은 8+6시간만큼 근무를 합니다.
세 번째 사람은 2+7시간만큼 근무를 합니다.
네 번째 사람은 5시간만큼 근무를 합니다.
따라서, 가장 오래 근무를 한 사람은 14시간 일했습니다.



