#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

int search(struct Node *head, int key) {
    int pos = 1;
    struct Node *temp = head;

    while (temp != NULL) {
        if (temp->data == key)
            return pos;
        temp = temp->next;
        pos++;
    }
    return -1;
}

int main() {
    struct Node *head = NULL, *newNode, *temp;
    int choice = 1, key;

    while (choice) {
        newNode = (struct Node*)malloc(sizeof(struct Node));
        printf("Enter data: ");
        scanf("%d", &newNode->data);
        newNode->next = NULL;

        if (head == NULL)
            head = newNode;
        else {
            temp = head;
            while (temp->next != NULL)
                temp = temp->next;
            temp->next = newNode;
        }

        printf("Do you want to continue (1/0)? ");
        scanf("%d", &choice);
    }

    printf("Enter value to search: ");
    scanf("%d", &key);

    int result = search(head, key);
    if (result == -1)
        printf("Value not found in the list\n");
    else
        printf("Value found at position %d\n", result);

    return 0;
}
