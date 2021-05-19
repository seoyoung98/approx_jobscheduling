# Approx_JobScheduling
## 1. 근사 알고리즘
근사해를 찾는 대신에 다항식 시간의 복잡도를 가진다
근사해가 얼마나 최적해에 근사한지 나타내는 근사비율(Approximation Ratio)을 알고리즘과 함께 제시
근사 비율은 1.0에 가까울수록 정확도가 높은 알고리즘
근사 비율을 계산하려면 최적해를 알아야하는 모순이 생김
따라서 최적해를 대신할 수 있는 간접적인 최적해를 찾고 이를 최적해로 삼아 근사 비율을 계산함

## 2. 작업 스케줄링(Job Scheduling)
### 작업 스케줄링이란?
```n```개의 작업, 각 작업의 수행시간 ti, i=1,2,3,,,n 그리고 m개의 동일한 기계가 주어질 때 모든 작업이 가장 빨리 종료되도록 작업을 기계에 배정하는 문제
</br>한 작업은 배정된 기계에서 연속적으로 수행
</br>기계는 한번에 하나의 작업만을 수행

### 알고리즘 수행 과정
입력 : n개의 작업, 각 작업 수행 시간 ti, i=1,2,3,,,,n, 기계 Mj, j=1,2,,,,m
출력 : 모든 작업이 종료된 시간
작업의 수행시간이 각각 5,2,4,3,4,7,9,2,4,1이고 기계가 4개일 때

### 시간 복잡도
 모든 기계의 마지막 작업 종료 시간인 L[j]를 살펴보아야 하므로 O(m) 시간이 걸린다
따라서 시간복잡도는 n개의 작업을 배정해야하고 배열 L을 탐색해야하므로 n*O(m)+O(m) = O(nm)

### 근사 비율
근사 작업 스케줄링 알고리즘의 근사해를 OPT'라 하고, 최적해를 OPT라고 할 때,
```OPT' <= 2OPT```
즉, 근사해는 최적해의 2배를 넘지 않는다
