
# EX 49 C function to search an element in the doubly linked list.
## DATE: 1/11/25
## AIM:
To write a C function to search an element in the doubly linked list.

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
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void search(float data)
{
    struct Node *ptr;
    ptr=head;
    float item=data;
    int i=0,temp;
    while(ptr!=NULL)
    {
        if(ptr->data==item)
        {
            printf("item %.2f found at location %d",item,i+1);
            temp=0;
        }
        i++;
        ptr=ptr->next;
    }
    if(temp!=0)
    {
        printf("Item not found");
    }
}

## Output:
![image](https://github.com/user-attachments/assets/f88735dd-ab41-4d79-8334-1db4eae38a63)


## Result:
Thus the program was executed and the output was verified successfully.
