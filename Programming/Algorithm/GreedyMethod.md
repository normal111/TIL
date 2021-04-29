# 욕심쟁이 방법 (Greedy Method)
해를 구하는 과정 중 각 단계에서 최선을 선택해서 전체적인 최적해를 구하는 방법

## 동전 거스름돈 문제

동전의 개수를 최소로하여 거스름돈을 돌려주는 방법을 찾는 문제

동전은 `[500, 100, 50, 10]`와 같은 종류가 있다

풀이 방법은 거스름돈이 0원이 될 때까지 동전의 금액이 큰 순서대로 뺄수 있는 만큼 빼주면 된다 

```
770원의 동전 개수

770 - 500 * 1 = 270		// 500원 1개
270 - 100 * 2 = 70		// 100원 2개
70 - 50 * 1 = 20		// 50원 1개
20 - 10 * 2 = 0			// 10원 2개
```

단 동전의 액면가가 `[120]`과 같이 임의로 정해진다면 욕심쟁이 방법으로 해결할 수 없다

## 배낭 문제

배낭의 용량을 초과하지 않고 물건의 이익의 합이 최대인 경우를 구하는 방법 (단 물체는 쪼개서 넣을 수 있다)

각 물체의 단위 무게당 이익이 큰 순서대로 물체를 배낭에 넣으면 된다

```
가방 용량: 10kg
물체(무게,이익): [바나나(6kg,18), 초콜릿(2kg,14), 물(4kg,8)]
단위 무게당 이익: [바나나(3), 초콜릿(7), 물(2)]

10 - 2 = 8		// 초콜릿(14)
8 - 6 = 2		// 바나나(18)
2 - (4/2) = 0	// 물(8/2)

최대 이익: 36
```

## 최소 신장 트리

주어진 무방향 가중치 그래프에서 가중치의 합이 최소인 신장 트리를 구하는 방법

#### 크루스칼 알고리즘

간선을 가중치순으로 정렬 후 사이클이 생기지 않는 경우 간선을 꺼내며 최소 신장 트리를 구하는 방법

#### 프림 알고리즘

연결된 정점에서 연결되지 않은 정점을 연결하는 간선 중 가중치가 가장 낮은 간선을 계속 선택하는 방법

## 다엑스트라 알고리즘

하나의 정점에서 나머지 정점들로 가는 최단 경로를 구하는 알고리즘

(단 음의 가중치를 갖는 간선이 없어야 한다)

```
1. [기준 정점]과 [인접 정점]들의 가중치를 [각 인접 정점]에 저장한다
2. [가중치가 가장 낮은 정점을] 탐색 완료 배열에 추가한다
3. [2번 정점에 저장된 가중치 + 2번 정점에서 미탐색 인접 정점과의 가중치]와 [미탐색 인접 정점에 저장된 가중치] 중 더 작은 것을 [미탐색 인접 정점에 저장한다]
4. 모든 정점이 탐색될 때까지 2~3을 반복한다
```

## 작업 스케줄링 문제

시작시간과 종료시간이 있는 작업들을 모두 처리하는데 필요한 처리장치의 수를 구하는 문제

시작시간이 빠른 작업 순서로 장치에 할당하고, 만약 작업 충돌이 일어나는 상황이라면 다른 장치를 추가해 할당한다

## 작업 선택 문제

처리장치 하나로 시작시간과 종료시간이 있는 작업들을 가장 많이 처리할 수 있는 경우를 구하는 문제

종료시간이 빠른 작업을 순서대로 할당하고, 만약 작업 충돌이 일어나는 상황이라면 해당 작업을 무시한다

## 허프만 코딩

문자열 중 빈도수가 높은 문자를 이진코드로 변환해 압축하는 방법

문자의 빈도수를 확인 후 허프만 트리를 통해 이진코드로 변환한다