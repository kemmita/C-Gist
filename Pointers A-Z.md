1. Basics
```c
#include <stdio.h>
int main()
{
    // Define var of int
    int number = 99;
    // Create pointer
    int* pNumber = &number;
    // access the value stored at the location the pointer is pointing to
    printf("%d", *pNumber);
    // change value of var using pointer
    *pNumber = 22;
    printf("%d", number);
    return 0;
}
```
2. Check if pointer is null
```c
#include <stdio.h>
void myFunc(const int* num){
    // Check if pointer is null    
    if(!*num)
        printf("%d", *num);
}
int main()
{
    int a = 10;
    myFunc(&a);
    return 0;
}
```
3. 
