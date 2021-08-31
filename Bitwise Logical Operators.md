```c
#include <stdio.h>

int main()
{
    // Binary = 0000000000011001
    short int x = 25;
    // Binary = 0000000001001101
    short int y = 77;
    // "Binary And" Find where both bits equal 1 so it would be Binary = 0000000000001001 and that would equal 9, z will be 9
    short int z = x & y;
    printf("%d \n", z);
    // "Binary |" Find where one bit equals 1 so it would be Binary = 0000000001011101 and that would equal 93, z will be 93
    short int t = x | y;
    printf("%d \n", t);
    // "Binary ^" Find where one bit equals 1 but for the other byte that place must be 0 so it would be Binary = 0000000001010100 and that would equal 84, z will be 84
    short int k = x ^ y;
    printf("%d", k);
    return 0;
}
```
