# AO
BASIC ARITHMETIC OPERATOR
#include <stdio.h>

void add();
void subtract();
void multiply();
void divide();

int main() {
    int choice;

    while (1) {
        printf("\nSimple Calculator\n");
        printf("1. Add\n");
        printf("2. Subtract\n");
        printf("3. Multiply\n");
        printf("4. Divide\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1: add(); break;
            case 2: subtract(); break;
            case 3: multiply(); break;
            case 4: divide(); break;
            case 5: return 0;
            default: printf("Invalid choice\n");
        }
    }

    return 0;
}

void add() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("Result: %d\n", a + b);
}

void subtract() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("Result: %d\n", a - b);
}

void multiply() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("Result: %d\n", a * b);
}

void divide() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    if (b == 0) {
        printf("Error! Division by zero.\n");
    } else {
        printf("Result: %.2f\n", (float)a / b);
    }
}
