# 메인 함수
- 메인 함수는 C++이 시작될 때 호출되는 함수이다.
- 모든 실행 가능한 C++ 프로젝트에는 반환값과 매개변수가 정해진 main 함수가 필요하다.

## 매개변수
```cpp
int main(int argc, char* argv[])
{
    return 0;
}
```

- 위 코드가 메인 함수의 기본 형태이며 매개변수는 없어도 된다. ```void```
- ```argc```는 Argument Count를 의미한다. ```argv```는 Argument Vector로 main 함수에 전달되는 문자열을 담고 있다.
- 실제로 프로젝트에서는 이러한 매개변수를 이용한 입출력보단 cin이나 scanf와 같은 프로그램 런타임중 이뤄지는 입출력을 대부분 받는다.
- 여기서 주의할건 매개변수를 사용하지 않는게 아닌 main 함수의 인자를 통한 입출력을 잘 받지 않는다는 것이다.
- C++은 먼저 빌드를 해야하는데 빌드과정은 생략하고 실행파일의 이름이 ```main.out```인 경우 인자를 전달하는 방법은 아래와 같다.

```./main.out MyString1 MyString2 MyString3```

- 위 코드에서 argc와 argv에는 사용자가 입력하지 않아도 기본적으로 들어가는 값이 존재한다. 때문에 argc는 3이 아닌 4가 들어간다.
- argv의 0번째는 프로그램의 실행명이며 1번째부터 위 인자의 순서에 따라 저장된다.
- 인자는 띄어쓰기로 구분된다.

## 반환값
- main 함수의 반환타입은 항상 4바이트 정수형이다.
- main 함수의 반환값은 상태를 나타내는데 ```0```은 정상적인 종료를 의미한다.
- ```0```이 아닌 수를 반환하면 대부분 에러를 의미한다.