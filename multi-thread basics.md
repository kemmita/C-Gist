```c
#include <pthread.h>
#include <stdio.h>

typedef struct apiCall{
    char * request;
    char * response;
} apiCall;

void* http_request(void *ptr)
{
    apiCall *call = (apiCall *) ptr;
    printf("%s \n", call->request);
    call->response = "got this response";
    return NULL;
}

int main()
{
    apiCall callOne = {.request = "go get my data"};
    // Declare new thread
    pthread_t printThread;
    // Create new thread, last var is how you pass arguments to the function that is defined in the thread, in this case we are using the
    // http_request function i created above.
    pthread_create(&printThread, NULL, http_request, (void*) &callOne);
    // wait for thread to complete
    pthread_join(printThread, NULL);
    // print value that was assigned in other thread process on line 13
    printf("%s", callOne.response);
    return 0;
}
```
