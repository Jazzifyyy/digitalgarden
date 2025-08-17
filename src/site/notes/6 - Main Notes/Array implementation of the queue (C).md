---
{"dg-publish":true,"permalink":"/6-main-notes/array-implementation-of-the-queue-c/","tags":["dsa","info"]}
---

```c
#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>

typedef structure {
	int arr[100];
	int front;
	int rear;
} Queue;

Queue* create() {
	
}

int main (void) {
	Queue* Q = create();
	int choice, value;

	while (1) {
		printf("\nMenu:\n");
		printf("1. isEmpty\n");
		printf("2. isFull\n");
		printf("3. enqueue\n");
		printf("4. dequeue\n");
		printf("5. peek\n");
		printf("6. size\n");
		printf("7. exit\n");
		printf("Enter choice: ");
		if (scanf("%d", &choice) != 1) {
		// invalid input
			int c;
			while ((c = getchar() != '\n' && c != EOF)) { }
			printf("Invalid input. Try again. \n");
			continue;
		}
		switch (choice) {
			case 1:
				printf(isEmpty(Q) ? "Queue is empty. \n": 
				"Queue is not empty");
			case 2:
				printf(isFull(Q) ? "Queue is full. \n":                      "Queue is not full.\n");
                break;
            case 3:
	            printf("Enter integer to enqueue: ");
	            if (scanf("%d", &value) != 1) {
                    int c;
                    while ((c = getchar()) != '\n' && c!=EOF) { }
                    printf("Invalid number.\n");
                } else {
                    enqueue(Q, value);
                }
                break;
            case 4:
	            dequeue(Q);
	            break;
	        case 5: 
		        peek(Q);
		        break;
		    case 6:
			    print(size(Q));
			    break;
			case 7:
				free(Q);
				printf("Exiting.\n");
				return 0;
			default: 
				printf("Invalid choice. Pick 1-7. \n"); 
		}
	}
	return 0;
}
```
