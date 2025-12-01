
# EX 48 C functions to perform all basic operations in Doubly Linked List.
## DATE: 1.11.25
## AIM:
To write a C functions to perform all basic operations in Doubly Linked List.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a function to search an element in the double linked list.. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End
   
## Program:
```
/*
Developed by: Aparna RB
RegisterNumber:  212222220005
*/
struct Node
{
    char data; 
    struct Node *next;
    struct Node *prev;
}*head;
void display()
{
    struct Node *ptr;
    ptr=head;
    while(ptr!=NULL)
    {
        printf("%c\n",ptr->data);
        ptr=ptr->next;
    }
}
void insert(char data)
{
    struct Node *ptr;
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    if(head==NULL)
    {
        head=n;
        head->data=data;
        n->next=NULL;
        return;
    }
    ptr=head;
    while(ptr->next!=NULL)
    {
        ptr=ptr->next;
    }
    n->data=data;
    n->next=NULL;
    ptr->next=n;
}
void search(char data)
{
    struct Node *ptr;
    char item=data;
    int i=0,flag;
    ptr = head;
    while (ptr!=NULL)
    {
        if(ptr->data == item)
        {
            printf("item %c found at location %d\n",item,i+1);
            flag=0;
        }
        i++;
        ptr = ptr -> next;
    }
    if(flag!=0)
    {
        printf("Item not found\n");
    }
}
void delete()
{
    struct Node *ptr;
    
    if(head==NULL)
    {
        printf("UNDERFLOW");
        
    }
    else if(head->next==NULL)
    {
        head=NULL;
        free(head);
        printf("Node deleted\n");
    }
    else
    {
        ptr=head;
        head=ptr->next;
        free(ptr);
        printf("Node deleted\n");
    }
}
```

## Output:
<img width="699" height="789" alt="image" src="https://github.com/user-attachments/assets/569910e9-08a6-4160-909e-858b0fb380b1" />



## Result:
Thus the program was executed and the output was verified successfully.
