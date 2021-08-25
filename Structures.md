1. Basics
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
2. Structs and pointers
```c
#include <stdio.h>
// Create struct
struct node
{
    int x;
    int y;
    int z;
};

// This is how you define a pointer of type node struct as the return type
struct node * alterNode(struct node* node)
{
    // alter pointer struct elements and return
    node->x = node->x * node->x;
    return node;
}

int main()
{
    // Define struct node
    struct node node = {10,2,3};
    // Define struct node pointer to have the value of the updated struct returned from the function above.
    struct node* pnode = alterNode(&node);
    // Verify struct was updated
    printf("%d", node.x);
    return 0;
}

```
