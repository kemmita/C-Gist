```c
#include <stdio.h>
// create struct
struct purchase
{
    int month;
    int day;
    int year;
    char* productName;
};

// return struct from a function
struct purchase processPurchase(char* itemName){
    struct purchase purchaseToProcess = {12,12,204, itemName};
    return purchaseToProcess;
}

int main()
{
    char productName[100];
    printf("Enter product name: \n");
    scanf("%[^\n]",productName);
    char* pProdName = productName;
    struct purchase purchaseToDisplay = processPurchase(pProdName);
    printf("%s", purchaseToDisplay.productName);
    return 0;
}

```
