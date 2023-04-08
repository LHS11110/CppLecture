# 객체 지향
- 객체 지향이란 프로그램 구현에 객체를 사용하여 상호작용하는 방식을 말한다. 객체는 모두 정렬되지 않은 멤버 변수와 멤버 함수(메소드)를 가진다.
# 객체
- 속성을 가지며 물리적 또는 추상적 의미로 존재하는 식별 가능한 것
- 프로그래밍에서 쓰이는 의미가 아닌 사람이 실제로 인식하고 구별할 수 있는 무언가를 말한다.
# 클래스
- 객체를 구성하는 틀 또는 구조를 말한다.
- 변수 또는 메소드들의 집합으로 정의된다.
# 인스턴스
- 클래스를 통해 메모리에 실체화된 객체를 말한다.
- 클래스를 통해 메모리에 실체화되는 것을 클래스의 인스턴스화라고 한다.
# Class
C++의 객체 지향에는 class라는 키워드를 통해 구현된다. class는 사용자 정의 자료형으로 여러 자료형을 사용자 정의대로 나열할 수 있으며 메소드라는 멤버 함수를 정의할 수도 있다.

```cpp
class MyClass
{
public:
    int num;
    char c;
};
```

제일 기본적인 형태이다. 구조체와 비슷하며 struct 키워드 대신 class를 사용하고, 접근 제어 지시자를 사용해 해당 멤버의 접근 범위를 명시할 수 있다.
사실 class는 구조체(struct)와 다를게 없다. 구조체 또한 C에서는 없었지만 C++에서는 접근 제어 지시자를 사용할 수 있고 메소드 또한 정의가 가능하다.
접근 제어 지시자를 명시하지 않으면 `class`는 기본으로 `private`을 사용하고 `struct`는 `public`을 사용한다.
위 코드에서 작성된 클래스는 구조체와 다를게 없다.

```cpp
MyClass obj;
```

위 코드는 인스턴스를 생성하는 코드이다.
## 접근 제어 지시자
- 멤버의 접근 범위를 명시한다.
- `private`: 여기에 포함된 멤버는 오직 해당 클래스의 메소드를 통해서만 접근이 가능하다.
- `protected`: 해당 클래스 또는 상속된 클래스의 메소드를 통해서만 접근이 가능하다. 상속은 나중에 다루겠다.
- `public`: 모든 함수 또는 메소드에서 접근이 가능하다.
## 멤버 변수
- 구조체의 멤버 변수와 다를게 없다. 위 코드에서 `num`과 `c`라는 변수가 멤버 변수이다.
## 메소드
- 멤버 함수라고도 하며, 클래스 내부에 정의된다.

```cpp
class MyClass
{
public:
    int num;
    char c;

    int add(void)
    {
        return num + c;
    }
};
```

- MyClass 내부에 `add`라는 메소드를 정의하는 코드이다. 해당 메소드는 4바이트 정수형 변수 `num`에서 1바이트 문자(정수)형 변수 `c`를 더한 값을 반환한다.
- `add`라는 메소드와 `num`, `c`라는 멤버 변수들은 모두 `public`으로 설정되어 있기 때문에 모든 외부 함수에서도 접근할 수 있다.