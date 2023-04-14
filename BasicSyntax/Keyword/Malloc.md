# 동적 메모리 할당
기존의 변수들은 개수가 정해져 있거나 개발자가 원하지 않음에도 알아서 메모리가 반환되기에 불편한 점이 있었다. 하지만 원하는 만큼 메모리를 직접 할당하고 직접 반환하는 형태로 메모리 공간을 다룰 수 있게 하는 것을 동적 메모리 할당이라고 한다. 동적 메모리 할당의 장점은 당연하게도 원하는 만큼 만들 수 있고 고유하며 원하는 시기에 다시 메모리 공간을 반환하여 자원을 낭비하지 않을 수 있다.
## new 키워드
동적 할당 키워드이며 기본 예제는 아래와 같다.

```cpp
#include <iostream>
using namespace std;

int main(void)
{
    int* ptr = new int; // 4바이트 정수형 동적 할당, new 키워드가 반환하는 값은 주소값이다.
    *ptr = 4;

    cout << *ptr << '\n';

    delete ptr; // 메모리 공간 해제

    return 0;
}
```

일반적인 자료형 뿐만 아니라 사용자 정의 자료형을 동적 할당할 수 있다.

```c++
#include <iostream>
using namespace std;

Class MyClass
{
    ...
};

int main(void)
{
    MyClass* ptr = new MyClass;
    *ptr = 4;

    delete ptr; // 메모리 공간 해제

    return 0;
}
```

배열의 크기 또한 고정된 정수형이 아닌 입력을 받아 원하는 크기만큼의 배열 또한 생성 가능하다.

```cpp
#include <iostream>
using namespace std;

int main(void)
{
    int len;

    cin >> len;

    int* ptr = new int[len]; // len의 크기를 가진 int형 배열 동적 할당

    delete[] ptr; // 배열 메모리 공간 해제

    return 0;
}
```

new 키워드는 힙(heap) 영역의 메모리 공간을 사용하여 할당하고 그 주소를 반환한다.
힙 공간에 할당된다면 다시 delete로 없애지 않는 이상 사라지지 않기에 꼭 delete로 필요없는 시기에 해제해줘야 한다.