```c
#include <stdio.h>

FILE* getFile(char* path)
{
    FILE* pfile = fopen(path, "r");
    if(pfile == NULL)
        printf("Cant open file");
    return pfile;
}

void readFile(FILE* pFile)
{
    int c;
    while ((c = fgetc(pFile)) != EOF)
    {
        printf("%c", c);
    }
    fclose(pFile);
    pFile = NULL;
}

int main()
{
    FILE* pFile = getFile("C:dest.txt");
    readFile(pFile);
    return 0;
}

```
