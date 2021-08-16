```c
#include <stdio.h>

int main()
{
    // Create Matrix
    int matrix[3][2] = {{11,2},{4,6},{54,67}};
    // access matrix value 6
    printf("%d \n", matrix[1][1]);
    // loop through matrix
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 2; ++j) {
            printf("%d \n", matrix[i][j]);
        }
    }
}

```
