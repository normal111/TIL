# 그래프 (Graph)
그래프는 꼭짓점(V)들과 변들(E)의 집합이다

`G = (V, E)`

## 용어

- **인접**: 두 꼭짓점에 사이에 변이 존해하는 경우 (변에 의해 발생)
- **병렬 변**: 인접한 꼭짓점을 사이에  변이 복수개 존재할 경우 
- **루프**: 변의 양 꼭짓점이 같은 경우
- **고립 꼭짓점**: 인접한 꼭짓점이 없는 꼭짓점
- **동형**: 꼭짓점과 변의 이름만 제외하고는 모두 동일한 그래프들
- **차수**: 꼭짓점에 인접한 변의 개수
- **총 차수**: 모든 꼭짓점의 차수의 합 (`2*|E|`)
- **워크**: 꼭짓점에서 꼭짓점으로 갈 수 있는 꼭짓점과 변들을 나열한 것
- **트레일**: 변들이 모두 서로 다른 워크
- **경로**: 꼭짓점이 모두 서로 다른 트레일 `Path ⊂ Trail ⊂ Walk`
- **닫힌 워크**: 시작점과 끝점이 같은 워크
- **사이클**: 닫힌 경로
- **연결**: 꼭짓점에서 꼭짓점으로 갈 수 있는 경로가 존재하는 상태

## 그래프의 종류

#### 방향 그래프

변이 방향을 가지는 그래프

#### 무향 그래프

변이 방향을 가지고 있지 않은 그래프

#### 단순 그래프

루프와 병렬 변을 가지지 않는 무향 그래프

#### 부분 그래프

하나의 그래프에서 꼭짓점과 변이 0개 이상 제거된 그래프

#### 신장 부분 그래프

하나의 그래프에서 변이 0개 이상 제거된 그래프

#### 연결 그래프

모든 꼭짓점이 서로 연결된 그래프

#### 완전 그래프

모든 꼭짓점이 서로 인접한 단순 그래프

각 꼭짓점의 차수는 `|V|-1`이고 모든 꼭짓점의 차수의 합은 `n(n-1) / 2`이다

#### 이분 그래프

 `V₁ ⊂ V, V₂ = V - V₁`일 때, 모든 변이 `V₁`과 `V₂` 사이에만 존재하는 그래프

#### 완전 이분 그래프

 `V₁ ⊂ V, V₂ = V - V₁`일 때, 모든 `V₁`과 `V₂` 사이에 변이 존재하는 그래프

#### 정규 그래프

모든 꼭짓점이 동일한 차수를 가지는 그래프

## 그래프의 표현

#### 발생 행렬

꼭짓점을 행으로 변을 열로 하여 변과 꼭짓점 상이의 발생관계를 표현한 행렬

#### 인접 행렬

꼭짓점과 꼭짓점의 사이의 인접관계를 표현한 행렬

#### 인접 리스트

각 꼭짓점에 인접하는 꼭짓점들을 차례로 연결 리스트로 표현한 것
