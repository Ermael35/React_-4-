# React_-4-

# [3주차] React 입문: 팀과제


# 문제 4번

🔐 event listener는 등록되면 반드시 해제되어야 합니다.
클래스형 컴포넌트에서는 컴포넌트가 화면에서 사라질 때(unmount 될 때) event listener를 해제합니다. (componentWillUnmount에서요!)
그럼 라이프사이클 메소드를 사용할 수 없는 함수형 컴포넌트에서는 event listener를 해제할 때 어떻게 해야할까요?


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Solution)

```
생명주기함수(라이프사이클 메소드)란 단어가 딱딱할 수 있지만, 쉽게 인간으로 말씀드리면 태어나서 죽을 때까지의 기간입니다. 즉, 생명주기 함수란, 컴포넌트가 생성되고 소멸될 때까지의 과정입니다.

이 함수는 크게 생성 -> 갱신 -> 소멸 3단계를 거칩니다.
```

아무튼 이 생명주기 함수(라이프사이클 메소드)의 소멸단계에서 event listener를 해제할때에는 어떻게 처리를 하는지 알아보면 다음과 같습니다.

먼저, 클래스형 컴포넌트와 함수형 컴포넌트의 작용이 서로 다릅니다.

먼저 클래스형 컴포넌트는 componentWillUnmount() 함수의 작용을 하면 되는데, 함수형 컴포넌트는 Hook을 사용해서 `useEffect` 함수를 통해 관리합니다. 

이 방법의 장점으로는 Hooks를 사용하여 함수로 Class기능을 구현할 수 있다는 것 말고도 다음과 같은 장점이 있습니다.

- 자바스크립트 함수이기 때문에 읽기 및 테스트가 매우 쉽습니다.
- 적은 코드로 작성할 수 있습니다.
- state를 생각해서 컨테이너, 프레젠테이션 컴포넌트를 더 쉽게 분리할 수 있습니다.
- 퍼포먼스 역시 뛰어납니다.
