# CppLecture
- C++은 객체 지향 프로그래밍 언어로, C라는 언어의 확장판이다.
- C++은 C의 모든 기능을 포함하며 객체 지향이라는 패러다임과 제네릭 프로그래밍 기능을 추가하였다.
## 용어
- **패러다임** : 프로그래밍 언어에서 패러다임이란 개발자에게 어떤 접근 방식이나 관점을 갖게 해주는 이론적인 틀을 말한다.
- **소스 코드** : 원시 코드(주로 고급 언어를 가르킴)라고도 하며, 개발자가 작성한 프로그래밍 언어 코드를 말한다. 바로 실행될 수 있는 형태가 아니기 때문에 소스 코드를 컴파일하는 과정을 거쳐야 한다.
- **오브젝트 코드** : 목적 코드(주로 저급 언어를 가르킴)라고도 하며, 소스 코드를 컴파일하여 만들어진 결과물을 말한다.
- **컴파일** : 어떤 언어로 쓰여진 코드를 또 다른 언어로 번역하는 것을 말한다. 이러한 컴파일 과정을 도와주는 프로그램을 컴파일러라고 한다.
- **빌드** : 전처리, 컴파일, 링킹, 테스팅, 패키징 등 컴파일뿐만 아니라 여러 기타 작업들을 포함한 것을 말한다. 그리고 이러한 빌드 과정을 도와주는 프로그램을 빌드 도구라고 한다.
- **런타임** : 프로그램이 실행되고 있는 동안의 실시간을 말한다.
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
