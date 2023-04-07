# 기본 예제
```cpp
#ifndef _PROJECT_
#define _PROJECT_
#include <iostream>

#define NUM 0

int main(void)
{
#if NUM == 0
    int num = 0;
#elif NUM == 1
    int num = 1;
#elif NUM == 2
    int num = 2;
#else
    int num = 100;
#endif

    return 0;
}
#endif
```