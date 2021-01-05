```c
#include <stdio.h>
#include <stdlib.h>
int main() {
    //Explicitly declare the zie of an array
    int x[100];
    //Here we use the {} to explicitly declare the array.
    int r [] = {'a', 'b', 'c'};
    //Here we can dynamically declare an array based on a users input.
    int n;
    printf("Please enter the number of bodies that will be stored: \n");
    scanf("%d", &n);
    int b[n];
    for (int i = 1; i <= n; ++i) {
        printf("Please enter the age of dead body %d \n", i);
        scanf("%d", &b[i]);
    }
    return 0;
}
```
