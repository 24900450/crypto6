# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
1.Start the program and import the required libraries.<br>
2.Seed the random number generator using the current time(i.e) rand(time(0));<br>
3.Get the number of randon number to generate.<br>
4.Pass the value for number of iterations and print the numbers.<br>
5.End the program.

# PROGRAM:
```c
 #include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int count, min, max;

    printf("Enter number of random numbers: ");
    scanf("%d", &count);
    printf("Enter min value: ");
    scanf("%d", &min);
    printf("Enter max value: ");
    scanf("%d", &max);

    if (min > max) {
        printf("Error: min cannot be greater than max.\n");
        return 1;
    }

    srand((unsigned int)time(NULL)); // seed with current time

    printf("Pseudorandom numbers:\n");
    for (int i = 0; i < count; i++) {
        int random_number = rand() % (max - min + 1) + min;
        printf("%d\n", random_number);
    }

    return 0;
}
```
# OUTPUT:
<img width="664" height="376" alt="image" src="https://github.com/user-attachments/assets/94add36b-063a-47c2-b508-aad108aa58c6" />

# RESULT:
Implementation of Pseudorandom Number Generation Using Standard library is completed successfully.
