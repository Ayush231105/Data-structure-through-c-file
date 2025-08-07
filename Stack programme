#include <stdio.h>
#include <stdlib.h>

#define MAX 100

int stack[MAX];
int top = -1;

void push();
void pop();
void peek();
void display();
int isFull();
int isEmpty();

int main() {
    int choice;

    printf("===== Stack Operations Menu =====\n");

    while (1) {
        printf("\n----------------------------------\n");
        printf("1. Push\n");
        printf("2. Pop\n");
        printf("3. Peek (Top Element)\n");
        printf("4. Display Stack\n");
        printf("5. Check if Stack is Full\n");
        printf("6. Check if Stack is Empty\n");
        printf("7. Exit\n");
        printf("----------------------------------\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
        case 1:
            push();
            break;
        case 2:
            pop();
            break;
        case 3:
            peek();
            break;
        case 4:
            display();
            break;
        case 5:
            if (isFull())
                printf("Stack is FULL\n");
            else
                printf("Stack is NOT full\n");
            break;
        case 6:
            if (isEmpty())
                printf("Stack is EMPTY\n");
            else
                printf("Stack is NOT empty\n");
            break;
        case 7:
            printf("Exiting program... Goodbye!\n");
            exit(0);
        default:
            printf("?? Invalid choice! Please try again.\n");
        }
    }

    return 0;
}

// Push operation
void push() {
    int item;
    if (isFull()) {
        printf("?? Stack Overflow! Cannot push element.\n");
        return;
    }
    printf("Enter the element to push: ");
    scanf("%d", &item);
    top++;
    stack[top] = item;
    printf("? %d pushed to stack.\n", item);
}

// Pop operation
void pop() {
    if (isEmpty()) {
        printf("?? Stack Underflow! Nothing to pop.\n");
        return;
    }
    printf("? %d popped from stack.\n", stack[top]);
    top--;
}

// Peek operation
void peek() {
    if (isEmpty()) {
        printf("?? Stack is empty. No top element.\n");
        return;
    }
    printf("?? Top element is: %d\n", stack[top]);
}

// Display stack
void display() {
	int i;
    if (isEmpty()) {
        printf("?? Stack is empty.\n");
        return;
    }
    printf("?? Stack elements from top to bottom:\n");
    for (i = top; i >= 0; i--) {
        printf("%d\n", stack[i]);
    }
}

// Check if stack is full
int isFull() {
    return top == MAX - 1;
}

// Check if stack is empty
int isEmpty() {
    return top == -1;
}
