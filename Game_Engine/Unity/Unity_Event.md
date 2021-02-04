# Unity Event [#API](https://docs.unity3d.com/ScriptReference/Events.UnityEvent.html)
C#의 델리게이트 또는 옵저버 패턴처럼 특정 이벤트가 발생하면 연결된 함수들을 호출해주는 편리한 기능

## 사용법
``` C#
using UnityEngine.Events;

public UnityEvent m_Event;

void A() {
  m_Event.AddListener(Func1);
  m_Event.Invoke();
  
  m_Event?.Invoke();  // 아래와 같다
  
  if(m_Event != null)
    m_Event.Invoke();
}
```
![UnityEvent](https://user-images.githubusercontent.com/37904040/106713127-5761d680-663d-11eb-8729-304a7166abd3.PNG)
해당 스크립트를 넣은 오브젝트에서 이벤트(함수)를 할당할 수 있다.

$$

## 장점
- 느슨한 연결을 사용하여 