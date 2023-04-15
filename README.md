# CppLecture
- C++은 객체 지향 프로그래밍 언어로, C라는 언어의 확장판이다.
- C++은 C의 모든 기능을 포함하며 객체 지향이라는 패러다임과 제네릭 프로그래밍 기능을 추가하였다.
- `제네릭 프로그래밍`: 특정 자료형에 얽매이지 않고 여러 자료형을 가질 수 있어 재사용성을 높인 프로그램 방식, C++에서는 Template 기능이 있다.
## 용어
- `패러다임`: 프로그래밍 언어에서 패러다임이란 접근 방식이나 관점을 말한다. 예를 들어 어떠한 패러다임은 문제를 해결하는데 이러한 방식으로 해결하겠다는 것을 말한다.
- `소스코드`: 개발자가 작성한 프로그래밍 언어 코드를 말한다. 원시코드라고도 하며 엄격한 문법을 가지고 컴퓨터는 이를 해석하여 실행한다.
- `오브젝트코드`: 소스코드를 번역하여 만들어진 결과물을 말한다. 목적코드라고도 하며 컴파일러가 소스코드를 번역하면 목적코드라는 이진코드로 이루어진 파일이 생성된다. 여기서 주의할게 목적코드라고 해서 바로 실행될 수 있는 형태가 아니다. 어떠한 목적코드는 유지보수를 위해 여러개의 파일로 나누어 처리하여 만들어진 한 기능을 담당하는 일부 코드일 수 있다. 이를 이해하기 위해선 [컴파일 과정](./CompileProcess/)을 참고하자.
- `기계어`: 컴퓨터가 이해하고 실행할 수 있는 2진수로 쓰인 언어이다.
- `어셈블리어`: 기계어와 일대일 대응되는 프로그래밍 언어이다. 기계어는 사람이 읽을 수 없기에 어셈블리어로 변환하여 작업한다.
- `빌드`: 소스코드를 실행될 수 있는 프로그램으로 만드는 과정을 말한다.
- `런타임`: 프로그램이 실행되고 있는 동안의 실시간을 말한다.
# [기본 구문](./BasicSyntax/Syntax/)
1. [식별자](./BasicSyntax/Syntax/Identifier.md)
2. [변수와 함수의 의미](./BasicSyntax/Syntax/VariableAndFunction.md)
3. [연산자](./BasicSyntax/Syntax/Operator.md)
4. [기본 자료형과 변수](./BasicSyntax/Syntax/PrimaryDataType.md)
5. [파생 자료형](./BasicSyntax/Syntax/DerivedDataType.md)
6. [사용자 정의 자료형](./BasicSyntax/Syntax/UserDefinedDataType.md)
7. [배열과 포인터](./BasicSyntax/Syntax/ArrayAndPointer.md)
8. [메인 함수](./BasicSyntax/Syntax/MainFunction.md)
9. [C++ 기본 코드 예제](./BasicSyntax/Example/CppExample.md)
10. [조건문](./BasicSyntax/Syntax/IfConditionalStatements.md)
11. [반복문](./BasicSyntax/Syntax/LoopStatements.md)
12. [지역 변수와 전역 변수](./BasicSyntax/Syntax/LocalAndGlobalVariables.md)
13. [전처리기](./BasicSyntax/Syntax/Preprocessor.md)
14. [전처리기 예제](./BasicSyntax/Example/PreprocessorExample.md)
15. [이름 공간과 입출력](./BasicSyntax/Syntax/NamespaceAndIOstream.md)
# [OOP](./BasicSyntax/OOP/)
1. [객체](./BasicSyntax/OOP/ObjectOriented.md)
2. [생성자 종류](./BasicSyntax/OOP/Constructors.md)
3. [객체 지향의 특징](./BasicSyntax/OOP/CharacteristicsOfOOP.md)
4. [상속](./BasicSyntax/OOP/Inheritance.md)
# [키워드](./BasicSyntax/Keyword/)
1. [const와 static](./BasicSyntax/Keyword/ConstAndStatic.md)
2. [동적 할당과 new](./BasicSyntax/Keyword/Malloc.md)
3. [인라인 함수](./BasicSyntax/Keyword/Inline.md)
# 패러다임의 종류
## 절차지향
- 프로그램에서 수행할 명령을 순차적으로 처리하는 방식을 말하며 C언어가 대표적이다.
## 객체지향
- 객체를 중심으로 프로그램을 구성하는 것을 말한다. 필요한 데이터를 마치 하나의 객체처럼 추상화시켜 상호작용을 통해 프로그램을 구성한다. C++과 Java등이 대표적이다.
## 함수형 프로그래밍
- 자료처리에 수학적 함수의 사용을 강조하고 데이터의 가변성을 최대한 멀리하는 패러다임이다.
## 논리형 프로그래밍
- 논리규칙을 기반으로 프로그램을 구성하는 패러다임이다.
## 명령형 프로그래밍
- 컴퓨터가 수행할 명령을 나열하여 프로그램을 구성하는 패러다임이다.
## 병렬/분산 프로그래밍
- 작업을 여러개로 나누어 분산시켜 처리하는 패러다임이다.