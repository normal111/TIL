# 관계 (Relation)
집합 `X`에서 집합 `Y`로의 관계 `R`은 `X*Y`의 부분집합

```
학생X = {민수, 영수, 소영}
과목Y = {수학, 국어, 영어}

    |수학|국어|영어|
|민수| o |   |   |
|영수|   | o |   |
|소영|   | o | o |

수강관계R = {(민수,수학), (영수,국어), (소영,국어), (소영,영어)}
```

## 관계의 표현

#### 화살표 도표

집합의 원소에서 다른 집합의 원소를 가리키는 화살표를 그려 관계를 표현할 수 있다

// 화살표 도표 예시

#### 방향 그래프

집합 `X`에서 집합 `X`로의 관계는 방향 그래프로 표현할 수 있다

// 방향 그래프 표시

#### 부울 행렬

집합의 관계를 부울 행렬을 사용해 표현할 수 있다

```
    수학 국어 영어 
민수| 1 | 0 | 0 |
영수| 0 | 1 | 0 |
소영| 0 | 1 | 1 |
```

## 관계의 성질

#### 반사적

관계의 원소가 집합의 모든 원소에 대하여 `(a,a)`와 같은 순서쌍을 가지고있는 상태

```
A = {1, 2, 3}
R = {(1,1), (2,2), (3,3)}
```

#### 대칭적

관계의 원소 중 `(a,b)`가 있다면 `(b,a)`가 있는 상태

```
A = {1, 2, 3}
R = {(1,2), (2,1), (3,3)}
```

#### 추이적

관계의 원소 중 `(a,b)`와 `(b,c)`가 있다면 `(a,c)`가 있는 상태

```
A = {1, 2, 3}
R = {(1,2), (2,3), (1,3)}
```

## 관계의 종료

#### 역관계

관계 `R`의 순서쌍을 뒤집은 집합을 `R`의 역관계라고 한다

```
R   = {(1,3), (2,3)}
R-¹ = {(3,1), (3,2)}
```

#### 합성관계

집합 `R`의 원소가 `(a,b)`일 때 집합 `S`의 원소가 `(b,c)`인 `(a,c)`를 모두 가진 집합을 `R`과 `S`의 합성관계라고 한다

```
R = {(a,2), (c,1)}
S = {(2,z), (3,a)}

S·R = {(a,z)}
```

#### 동치관계

관계가 반사적, 대칭적, 추이적 관계일 때 동치관계라고 부른다

#### 동치류

관계 `R`에서 집합 `A`의 원소 `a`의 동치류는 `(a,x)`에 해당하는 `x`의 집합이고 `[a]`으로 표기한다

```
A = {1, 2, 3}
R = {(1,2), (1,3), (2,3)}

[1] = {2 ,3}
[2] = {3}
[3] = {}
```
