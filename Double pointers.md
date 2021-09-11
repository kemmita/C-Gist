1. Creating a double pointer.
```c
#include <stdio.h>

int main()
{
    int i = 5;
    int *pnum = &i;
    int **ppnum = &pnum;

    // Below will retur the address of *pnum, the first pointer
    printf("%d", *ppnum);
    // Below will retur the int *pnum was pointing to
    printf("%d", **ppnum);
    return 0;
}
```
2. Why use a double pointer? We use a double pointer when passing a pointer to a function this we we modify the actual pointer and not a copy of the pointer sent.
```c
#include <stdio.h>
#include <malloc.h>

void foo(int **ptr) {
    int a = 5;
    // assign the address of a to the original pointer    
    *ptr = &a;
    // check address of original pointer and the value the original pointer was pointing to.
    printf("%u %d \n", &*ptr, **ptr);
}

int main()
{
    int *ptr;
    ptr = malloc(sizeof(int));
    *ptr = 10;
    // to pass a double pointer, simply use the address of the original pointer    
    foo(&ptr);
    // check address of original pointer and the value the original pointer was pointing to.
    printf("%u %d \n", &*ptr, **ptr);
    printf("%u %d", &ptr, *ptr);
    return 0;
}

```
