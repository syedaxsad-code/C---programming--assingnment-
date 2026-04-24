# C programming assignment-
1.QUESTION

Write a C program to find the maximum of three numbers without using logical operators.

CODE:
```c
#include <stdio.h>
int main() {
    int a, b, c, max;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    max = a;
    if (b > max)
        max = b;
    if (c > max)
        max = c;
    printf("Maximum number is: %d", max);
    return 0;
}
```
OUTPUT:
```
Enter three numbers: 10 25 15
Maximum number is: 25
```

2.QUESTION

  Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)

CODE:
```c
#include <stdio.h>
int main() {
    int year;
    printf("Enter a year: ");
    scanf("%d", &year);
    if (year % 400 == 0) {
        printf("%d is a century leap year", year);
    }
    else if (year % 100 == 0) {
        printf("%d is not a leap year", year);
    }
    else if (year % 4 == 0) {
        printf("%d is a non-century leap year", year);
    }
    else {
        printf("%d is not a leap year", year);
    }
    return 0;
}
```
OUTPUT:
```
Enter a year: 2024
2024 is a non-century leap year
```
3.QUESTION

Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.

CODE:
```c
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')) {
        printf("It is an alphabet\n");
        if (ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U'||
            ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u') {
            printf("It is a vowel");
        } else {
            printf("It is a consonant");
        }
    }
    else if (ch >= '0' && ch <= '9') {
        printf("It is a digit");
    }
    else {
        printf("It is a special character");
    }
    return 0;
}
```
OUTPUT:
```
Enter a character: a
It is an alphabet
It is a vowel
```

4.QUESTION

Write a C program for simple ATM simulation with operations Check
Balance, Deposit,  Withdraw,  Exit using 
switch and update balance accordingly.

CODE:
```c
#include <stdio.h>
int main() {
    int choice;
    float bal = 1000, amount;
    do {
        printf("\n1. Check Balance\n2. Deposit\n3. Withdraw\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch(choice) {
            case 1:
                printf("Balance: %.2f\n", bal);
                break;
            case 2:
                printf("Enter amount to deposit: ");
                scanf("%f", &amount);
                bal += amount;
                printf("Updated Balance: %.2f\n", bal);
                break;
            case 3:
                printf("Enter amount to withdraw: ");
                scanf("%f", &amount);
                if (amount <= bal) {
                    bal -= amount;
                    printf("Updated Balance: %.2f\n", bal);
                } else {
                    printf("Insufficient balance\n");
                }
                break;
            case 4:
                printf("Thank you!\n");
                break;
            default:
                printf("Invalid choice\n");
        }
    } while(choice != 4);
    return 0;
}
```
OUTPUT:
```
1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Enter your choice: 2
Enter amount to deposit: 500
Updated Balance: 1500.00

1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Enter your choice: 4
Thank you!
```

5.QUESTION

Write a C program for menu driven calculator using [switch statement]

CODE:
```c
#include <stdio.h>
int main() {
    int choice;
    float a, b;
    printf("Enter two numbers: ");
    scanf("%f %f", &a, &b);
    printf("\n1. Addition\n2. Subtraction\n3. Multiplication\n4. Division\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);
    switch(choice) {
        case 1:
            printf("Result = %.2f", a + b);
            break;
        case 2:
            printf("Result = %.2f", a - b);
            break;
        case 3:
            printf("Result = %.2f", a * b);
            break;
        case 4:
            if (b != 0)
                printf("Result = %.2f", a / b);
            else
                printf("Division by zero not allowed");
            break;
        default:
            printf("Invalid choice");
    }
    return 0;
}
```
OUTPUT:
```
Enter two numbers: 10 5

1. Addition
2. Subtraction
3. Multiplication
4. Division
Enter your choice: 1
Result = 15.00
```
