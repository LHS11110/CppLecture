# 상수
- 상수는 변수와 다르게 값을 재할당할 수 없으며 반드시 선언과 초기화가 동시에 이루어져야 한다.

```cpp
const float kPi = 3.141592;
```

- `kPi`는 상수이므로 값을 재할당할 수 없다.
# 정적 변수
- `static`은 정적 변수를 선언할때 쓰이는 키워드이다.
- 정적 변수란 선언 및 초기화가 한번만 이루어지고 내부적으로 그것만을 가르키는 변수이다.
- `지역 변수`의 특징으로는 `지역 내에서만 접근`이 가능하고 `선언 및 초기화`가 선언될 때마다 `주기적`으로 이루어진다는 것이다.
- `전역 변수`의 특징으로는 `모든 지역에서 접근`이 가능하고 `선언 및 초기화`가 `한번`만 이루어진다는 것이다.
- `정적 변수`의 특징으로는 `지역 내에서만 접근`이 가능하고 `선언 및 초기화`가 `한번`만 이루어진다는 것이다.

```cpp
#include <iostream>
using namespace std;

int func()
{
    // 정적 지역 변수 선언
    static int num = 0; // 처음 선언만 유효하고 0이 초기화된다. 이후의 선언 및 초기화는 무시된다.
    cout << num << '\n';
    return num++;
}

int main(void)
{
    for (int i = 0; i < 10; i++)
        func();

    return 0;
}
```

출력은 아래와 같다.

```cpp
0
1
2
3
4
5
6
7
8
9
```

정적 변수는 이러한 특징을 가지고 있어 접근 범위를 함수 내로 하고 싶지만 전역 변수의 특징이 필요할 때 쓰인다.
## 클래스의 정적 멤버 변수
정적 멤버 변수도 마찬가지로 한번의 선언 및 초기화된다. 일반적인 멤버 변수는 객체를 생성할때마다 자신만의 공간을 가지고 생성자를 호출하여 초기화되므로 차이가 있다.

```cpp
#include <iostream>
using namespace std;

class MyClass
{
public:
    static int num;
};
int MyClass::num = 10; // 초기화

int main(void)
{
    MyClass obj1, obj2;
    obj1.num = 10;

    cout << obj2.num << '\n'; // 10
}
```

정적 멤버 변수는 한번의 선언과 초기화를 가진다. 때문에 생성자에서 초기화할 수 없으며 전역 변수처럼 범위 지정 연산자와 함께 작성하여 초기화한다.
이를 통해 알 수 있듯, 정적 멤버 변수는 모든 객체가 접근하는 하나의 전역 변수와 같다.
## 정적 전역 변수
일반적인 전역 변수처럼 모든 곳에서 접근이 가능하며 static이 붙는 것 이 외에는 초기화 방법 또한 같다. 기능으로써의 차이는 정적 전역 변수는 해당 파일 내에서만 유효하다는 것이다. 라이브러리는 전역 변수와 함수를 가진다고 하였다. 이때 전역 변수로써 사용하고 싶지만 외부 코드에서 접근이 불가능하도록 하고 싶다면 정적 전역 변수를 사용한다.

```cpp
#include <iostream>
using namespace std;

static int num = 10;

int main(void)
{
    cout << num << '\n';

    return 0;
}
```