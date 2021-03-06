# 배열 (Array)
C++의 기본문법 중 하나인 `T[]`를 통한 배열 선언  
배열을 열심히 사용하기 보다는 `vector`나 `string` 같이 만들어진 자료구조를 추천

## 특징
- 배열을 그대로 출력하면 첫 요소의 주소를 얻을 수 있다 `cout << arr`
- 포인터에 배열을 할당하면 포인터를 배열처럼 사용할 수 있다 `ptr[0]`

## 사용법
``` C++
int arr1[10];                   // 크기가 10인 배열 선언, 초기화되지 않음
int arr2[3] = { 0, };           // 크기가 3인 배열 선언, 요소를 모두 0으로 초기화
int arr3[5] = { 1, 2 };         // 크기가 5인 배열 선언, 요소 1, 2 이후 0으로 초기화
int arr4[] = { 1, 2, 3 };       // 크기가 3인 배열 선언, 요소 1, 2, 3으로 초기화

int *ptr1 = arr1;               // arr1을 가리키는 포인터
int *ptr2 = new int[10]         // int[10] 인 배열을 가리키는 포인터

char str1[] = "good";           // 크기가 5인 배열을 선언 및 "good"+'\0' 로 초기화
char str2[10] = "wow";          // 크기가 10인 배열을 선언 및 "wow" 이후 '\0' 로 초기화
```

## 길이
배열의 길이는 기본적으로 `sizeof(arr) / sizeof(T)` 공식으로 알아낼 수 있다  
하지만 배열을 포인터로 변환하거나 매개변수로 전달하면 배열의 길이를 알 수 없다  
그러나 예외적으로 `strlen`으로 문자열 끝에 `'\0'`이 있는 것을 이용해 문자열의 개수를 확인할 수 있다
``` C++
void func1(const char* str) {      // 포인터 형식으로 배열을 받아 사용
  int length = strlen(arr);        // '\0' 전까지 탐색 후 4를 반환
}

int main() {
  int arr[] = { 1, 2, 3 };
  cout << sizeof(arr) / sizeof(int) << endl;		// 3 출력

  char str[] = "good";
  cout << sizeof(str) / sizeof(char) << endl;		// 5 출력
  
  func1(str);
}
```
