```c
#include <stdio.h>
#include <stdbool.h>

int main()
{
    // Float
    float dolarAmoun = 234.239;
    printf("%.3f \n", dolarAmoun);
    // Double
    double ingredientWeight = 230.542222444e+11;
    printf("%f \n", ingredientWeight);
    // Boolean
    bool isMaried = true;
    printf("%d \n", isMaried);
    // Int
    int num = 1232345242;
    printf("%d \n", num);
    // Char
    char val = 'c';
    printf("%c \n", val);
    // Short
    short smallNumber = -11122;
    printf("%d \n", smallNumber);
    // Long
    long int bigNumber = 121344453;
    printf("%ld \n", bigNumber);
    // Enum
    enum states {MN = 0, WI = 1, MI = 2};
    enum states myState = MN;
    printf("%d \n", myState);
    return 0;
}
```
