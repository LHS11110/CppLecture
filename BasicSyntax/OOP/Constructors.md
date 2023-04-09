# 기본 생성자
기본 생성자는 [객체](./ObjectOriented.md)에서 말했듯 매개변수가 없는 가장 기본적인 형태의 생성자이다.
# 매개변수가 있는 생성자
생성자에는 매개변수가 들어갈 수 있다.

```cpp
class MyClass
{
private:
    int num;
public:
    MyClass()
        : num(0)
    {

    }


    // 매개변수가 있는 생성자
    MyClass(int n)
        : num(n)
    {

    }
};
```

```cpp
MyClass obj(10); // 암시적 호출
MyClass obj = MyClass(10); // 명시적 호출
```
# 복사 생성자
객체의 값을 또 다른 객체에 복사하는 과정에 호출되는 생성자이다.

```cpp
MyClass obj1;

// 복사 생성자 호출
MyClass obj2 = obj1; // 대입 연산을 통한 호출
MyClass obj2(obj1);
```

```cpp
class MyClass
{
private:
    int num;
public:
    MyClass()
        : num(0)
    {

    }


    // 복사 생성자
    MyClass(const MyClass& obj)
        : num(obj.num)
    {

    }
};
```