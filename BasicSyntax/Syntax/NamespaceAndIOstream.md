# 이름 공간
`라이브러리`란 `변수와 함수의 집합`이라 말하였다. 변수와 함수는 모두 고유의 식별자를 가져야 한다. 하지만 만약에 이러한 `식별자가 동일하여 구분되지 못한다면 이름 공간을 사용해야 한다.` 이름 공간이란 말 그대로 `공간에 이름이 주어지는 기능`이다. 전역에 존재하는 식별자는 지역을 포함한 또 다른 모든 식별자들을 신경써야 하지만, 이름 공간을 사용하면 `외부와 상관없이 이름 공간 내에서 원하는 식별자를 사용`할 수 있다는 장점이 있다. `단, 이름 공간 내에서도 같은 식별자가 존재해서는 안 된다.`

```cpp
// 이름 공간 선언
namespace MyNamespace
{
    int num; // 이름 공간 내에 선언된 전역 변수


    // 이름 공간 내에 선언 및 정의된 함수
    int add(int a, int b)
    {
        return a + b;
    }
}
```

이름 공간 내에서도 `함수 외부에 변수를 선언`하면 `전역 변수`이다. 이름 공간은 각자의 공간을 사용하여 `식별자를 확장하는 기능`만 할 뿐, 변수나 함수로서의 기능은 그대로다. 또한 이름 공간 내에 또 다른 이름 공간을 선언할 수 있다.

```cpp
namespace A
{
    // 이름 공간 내에 이름 공간 선언
    namespace B
    {
        int num; // 다른 이름 공간을 사용하기에 선언이 가능하다. 마찬가지로 이것도 전역 변수와 같다.
    }

    int num;


    int add(int a, int b)
    {
        return a + b;
    }
}
```

해당 변수들과 함수에 접근하는 코드는 아래와 같다.

```cpp
A::B::num = 10;
A::num = 5;
A::add(A::B::num, A::num);
```

`::`라는 범위 지정 연산자를 사용하는데, 이 연산자는 이름 공간내에 존재하는 요소에 접근할 수 있도록 한다.
## using
이름 공간이 따로 필요하지 않는 경우라면 using이라는 키워드로 범위 지정 연산자를 생략할 수 있다. using은 선언된 이후에 유효하다.

```cpp
namespace A
{
    namespace B
    {
        int num;
    }

    int num;


    int add(int a, int b)
    {
        return a + b;
    }
}

int main(void)
{
    // 함수 내에서 using을 했으므로 해당 지역에서만 유효하다.
    using namespace A;
    num = 10; // A::num = 10
    B::num = 5;

    add(num, B::num);
    return 0;
}
```

```cpp
namespace A
{
    namespace B
    {
        int num;
    }

    int num;


    int add(int a, int b)
    {
        return a + b;
    }
}

// 전역에서 using을 했으므로 전역에서 유효하다.
using namespace A;

int main(void)
{
    num = 10; // A::num = 10
    B::num = 5;

    add(num, B::num);
    return 0;
}
```

```cpp
namespace A
{
    namespace B
    {
        int num;
    }

    int num;


    int add(int a, int b)
    {
        return a + b;
    }
}

int main(void)
{
    // A의 이름 공간에 포함된 add라는 함수만 이름 공간을 생략할 수 있다.
    using A::add;
    A::num = 10;
    A::B::num = 5;

    add(A::num, A::B::num);
    return 0;
}
```

## 별명
이름 공간에 또 다른 이름을 부여한다.

```cpp
namespace A
{
    namespace B
    {
        int num;
    }

    int num;


    int add(int a, int b)
    {
        return a + b;
    }
}

int main(void)
{
    // A::B에 포함된 요소들은 또 다른 이름인 AB로 접근될 수 있다.
    namespace AB = A::B;
    A::num = 10;
    AB::num = 5;

    A::add(A::num, AB::num);
    return 0;
}
```

# 입출력
C++의 입출력 라이브러리로는 `cstdio`, `iostream`이 있다. C++은 기존 C의 확장이므로 `stdio.h` 또한 포함할 수 있다. 이 라이브러리들은 표준 라이브러리에 속하는데
표준 라이브러리란 개발자가 자주 사용하고 개발 환경에 기본으로 포함되어지는 것들을 말한다. 알고리즘에서 쓰이는 여러 자료 구조들도 C++에서 표준 라이브러리로 존재한다.

```cpp
#include <iostream>

int main(void)
{
    int num = 10;

    // std라는 이름 공간에 포함된 cout으로 num을 출력한다.
    std::cout << num; // 10

    return 0;
}
```

`cout`은 무언가를 출력할 수 있다. 이때 무언가를 출력하려면 비트 연산자인 `<<`를 사용한다.

```cpp
std::cout << num << str << '\n';
```

입력은 아래와 같이 받는다.

```cpp
#include <iostream>

int main(void)
{
    int num;

    // std라는 이름 공간에 포함된 cin으로 입력받아 num에 할당한다.
    std::cin >> num;

    return 0;
}
```

`cin`은 무언가를 입력받을 수 있다. 이때 무언가를 입력받고 변수에 할당하려면 비트 연산자인 `>>`를 사용한다.
위 코드를 실행하면 입력을 받을 때까지 프로그램이 멈추는 것을 확인할 수 있다. 이처럼 `작업을 완료하기 전까지 프로그램이 멈추는 것을 Blocking이라 한다.`
엄밀히 말하자면 프로그램이 아닌 쓰레드가 멈추는 것이지만 이는 프로그램 구조에서 다루겠다. 반대로 `해당 작업을 완료할 수 없어 바로 다음 작업으로 넘어가는 것을 Non-Blocking이라 한다.`