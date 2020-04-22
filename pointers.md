# Pointers in C and C++

```*``` &rarr; Operator to declare pointer or to reference a pointer of a variable, example: *ptr returns the value to which ptr is pointing to. Also to declare a pointer it should be declared as ```int *ptr```

```&``` &rarr; Operator to get the address of another variable, example: ```&val``` returns a pointer to ```val```.

Examples:
```C

int *ptr; // Declaring a pointer

int val = 1;

ptr = &val; // ptr now points to val

val2 = *ptr; // val2 now has the same value as val. In this case with *ptr we are obtaining the value contained on the variable ptr is pointing to.

```

```C++
#include <iostream>;
using namespace std;

int main(){
    int a[3];
    a[0] = 10;
    a[2] = 20;

    /*
    Arrays in C and C++ are, actually, a pointer that points to the first location to the array a[0]
    To access each location, you can use alternatively:
    a[0] == *a
    a[1] == *(a+1)
    a[2] == *(a+2)
    ...
    */

    *a += 1; // Equivalent to a[0] +=1
    printf("%d \n", a[0]); // Should print 11

    a[0] = *(a+2) // Equivalent to a[0] = a[0+2]
    printf("%d \n", a[0]); // Should print 20

}
```