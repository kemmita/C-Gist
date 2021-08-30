```c
#include <stdio.h>
#include <math.h>

int convertBinaryToDecimal(long long n){
   int number = 0, i = 0, currentNumber = 0;
    
    // while n is not null
    while (n != 0)
    {
        // get bit farthest to the right;
        currentNumber = n % 10;
        // drop bit from right by moving one place to the left
        n = n / 10;
        // take the 2 to the power of the current itteration number * the current bit
        number += currentNumber*pow(2, i);
        i++;
    }
    return number;
}


int main()
{
    printf("%d", convertBinaryToDecimal(1011));
    return 0;
}

```
