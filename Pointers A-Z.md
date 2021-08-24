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
3. Working with arrays
```c
#include <stdio.h>

int main()
{
    // initialize array
    int array[3] = {10,10,20};
    // create pointer for array, this will point to the address of the first element in the array
    int* ptrArr = array;
    // get length of each int in array is 4 bytes * 10 elements = 40 we will take that and divide by 4, the size of a single int
    const int arrayLength = sizeof(array) / sizeof(array[0]);
    // loop through array
    for (int i = 0; i < arrayLength; ++i) {
        printf("%d \n", *(ptrArr+i));
    }
    return 0;
}
```
