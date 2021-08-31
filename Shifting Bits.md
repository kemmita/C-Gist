```c
#include <stdio.h>

int main()
{
    // an int is 32 bits and 3 would = 0000 0000 0000 0000 0000 0000 0000 0011
    int x = 3;
    // this would move all bits to the left by 1 so the result would be 0000 0000 0000 0000 0000 0000 0000 0110 and the int would then equal 6
    // to movie right just use >>
    int modifiedX = x << 1;
    printf("%d", modifiedX);
    return 0;
}

```
