1. If we want to keep a function private to the file in which it was created we use the keyword static.
```c
#include "other.h"

static int secretNumber()
{
    return 2;
}

int favNum(){
    return secretNumber();
}
```
2. The header file for the src file other should not contain any mentiuon of secretNumber(), Main will not be able to access it.
