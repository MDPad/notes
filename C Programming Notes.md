---
Theme: "[[C]]"
---
## Video Reference

[Introduction to C Programming](https://www.youtube.com/watch?v=d971m08_5Zo&list=PLA0M1Bcd0w8w-mqVmBjt-2J8Z1gVmPZVz&index=1)

---

## Types by Size

### Hierarchy of Types

```plaintext
char <= short <= int <= long <= long long
float <= double <= long double
```

### Type Table

|**Type**|**Size (bytes)**|**Minimum**|**Maximum**|
|---|---|---|---|
|unsigned char|1|0|255|
|char|1|-128|127|
|signed char|1|-128|127|
|int|4|-2,147,483,648|2,147,483,647|
|unsigned int|4|0|4,294,967,295|
|short|2|-32,768|32,767|
|unsigned short|2|0|65,535|
|long|8|-9,223,372,036,854,775,808|9,223,372,036,854,775,807|
|unsigned long|8|0|18,446,744,073,709,551,615|
|long long|8|-9,223,372,036,854,775,808|9,223,372,036,854,775,807|
|unsigned long long|8|0|18,446,744,073,709,551,615|
|float|4|±3.4e−38|±3.4e+38|
|double|8|±1.7e−308|±1.7e+308|
|long double|16|Varies|Varies|

---

## Increment and Decrement Operations

- `a++`: Increments the value **after** assigning it.
- `++a`: Increments the value **before** assigning it.

---

## Math Operations Priority

|**Priority**|**Operator**|**Description**|
|---|---|---|
|1|`++`, `--`|Increment and Decrement|
|2|`*`, `/`, `%`|Multiplication, Division, Modulus|
|3|`+`, `-`|Addition and Subtraction|

---

## Example Code

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main(void)
{
    srand(time(NULL));

    int range = 10;

    int r_1 = rand() % range;      // [0; range)
    int r_2 = rand() % range - 5;  // [-5; range-5)
    int r_3 = rand() + rand();

    double range_float = (double)rand() / (double)RAND_MAX; // [0; 1]

    printf("%d, %d, %.2f\n", r_1, r_2, range_float);

    return 0;
}
```
