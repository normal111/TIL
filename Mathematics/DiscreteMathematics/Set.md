# 집합 (Set)
집합이란 중복되지 않는 원소들로 구성된 객체다

## 표기법

1. 원소나열법

   `S = {1, 2, 3}`

2. 조건나열법

   `S = { x | 0 < x < 4 인 자연수}`

이때 `2 ∈ S` 와 같이 특정 원소가 집합에 포함되는 것을 표기할 수도 있다

## 집합연산

#### 합집합

A의 원소와 B의 원소를 모두 가지고 있는 집합을 합집합이라고 한다

`A ∪ B = C`

`{1, 2} ∪ {2, 3} = {1, 2, 3}`

#### 교집합

A의 원소와 B의 원소 중 겹치는 원소만 가지고 있는 집합을 교집합이라고 한다

`A ∩ B = C`

`{1, 2} ∩ {2, 3} = {2}`

#### 차집합

A의 원소에서 B의 원소가 빠진 집합을 차집합이라고 한다

`A - B = C`

`{1, 2} - {2, 3} = {1}`

#### 여집합 (보집합)

전체집합(U)이 주어졌을 때 전체집합의 원소에서 A의 원소를 뺀 집합

`U = {1, 2, 3, 4, 5}`

`A = {1, 2, 3}`

`A' = {4, 5}`

#### 대칭차집합

A와 B에서 겹치지 않는 원소들의 집합을 대칭차집합이라고 한다

`A △ B = C`

`{1, 2} △ {2, 3} = {1, 3}`

#### 곱집합

A의 원소와 B의 원소로 만들어지는 순서쌍들의 집합을 곱집합이라고 한다

`A × B = C`

`{1, 2} × {a, b} = {(1, a), (1, b), (2, a), (2, b)}`

## 서로소

A와 B의 교집합이 공집합일 때 (겹치는 원소가 없을 때) A와 B를 쌍으로 서로소라고 한다

`A ∩ B = Ø`

`{1, 2} ∩ {3, 4} = Ø`

## 부분집합

A의 모든 원소가 B의 원소이면 A는 B의 부분집합이라고 한다

`A ⊂ B`  (A가 B에 포함된다)

`{1, 2} ⊂ {1, 2, 3}`

#### 진부분집합

A가 B의 부분집합일 때 A와 B가 같지 않다면 A는 B의 진부분집합이라고 한다

`{1, 2} ⊂ {1, 2, 3}`

 #### 상동

A와 B가 서로 부분집합일 때 서로 상동(같다)이라고 한다

`A = B`

`{1, 2, 3} = {1, 2, 3}`

## 분할

집합 A를 Ø이 아닌 부분집합들로 나눌 때 A의 모든 원소들이 각각 나누어진 부분집합들 중 하나에만 포함될 경우 이 부분집합들 전체의 집합을 A의 분할이라고 한다

`A = {1, 2, 3} 의 분할 {{1, 2}, {3}}`

## 멱집합

집합 A의 모든 부분집합들의 집합을 A의 멱집합이라고 하고 `P(A)`로 표기한다

`A = {1, 2}`

`P(A) = {Ø, {1}, {2}, {1, 2}}`

`|P(A)| = 2^n = 4`	(멱집합의 원소의 수는 2의 집합의 원소수 만큼 제곱한 수가 된다)

## 포함관계

포함관계에 따라 반드시 성립하는 식

` A ⊂ (A ∪ B)` , ` B ⊂ (A ∪ B)` 

`(A ∩ B) ⊂ A` , `(A ∩ B) ⊂ B` 

`A ⊂ B 이고 B ⊂ C 이면 A ⊂ C 이다` 

## 항등식

대부분의 대수 법칙이 적용된다

교환법칙: ` A ∪ B = B ∪ A` , ` A ∩ B = B ∩ A` 

결합법칙: `(A ∪ B) ∪ C = A ∪ (B ∪ C)` , `(A ∩ B) ∩ C = A ∩ (B ∩ C) `

분배법칙: `A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)` , `A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C) `

항등법칙: `A ∪ Ø = A`, `A ∩ U = A`

드모르간의 법칙: ` (A ∪ B)' = A' ∩ B'`, ` (A ∩ B)' = A' ∪ B'`