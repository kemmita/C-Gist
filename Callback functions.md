```c
#include <stdio.h>

int sumSq(int a, int b)
{
    return (a*a) + (b*b);
}

int sum(int a, int b)
{
    return a + b;
}

void printNumberValue(int (*funcPtr)(int,int), int a, int b)
{
    printf("%d", funcPtr(a,b));
}

int main()
{
    printNumberValue(&sum, 2, 3);

    return 0;
}

#include <stdio.h>
#include <malloc.h>

int sumSq(int a, int b)
{
    return (a*a) + (b*b);
}

int sum(int a, int b)
{
    return a + b;
}

void printNumberValue(int (*funcPtr)(int,int), int a, int b)
{
    printf("%d", funcPtr(a,b));
}

int main()
{
    printNumberValue(&sum, 2, 3);

    return 0;
}

```
