
# EX 46 C function to traverse the linked list and display it in the following format.
## DATE: 1.11.25
## AIM:
To write a C function to traverse the linked list and display it in the following format.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a function to insert a node in a linked list. 
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
struct Node{ 
char data; 
struct Node *next; 
}*head; 
 
 
void insert(char data) 
{ 
struct Node *n=(struct Node*)malloc(sizeof(struct Node)); 
struct Node*temp; 
if(head==NULL) 
{ 
head=n; 
n->data=data; 
n->next=NULL; 
temp=head; 
return; 
} 
 
}  
else 
{ 
while(temp->next!=NULL) 
{ 
temp=temp->next; 
} 
n->next=NULL; 
n->data=data; 
temp->next=n; 
} 
}
```

## Output:
![image](https://github.com/user-attachments/assets/35063d17-0a43-4cb8-bc4f-63a05b22e6df)


## Result:
Thus the program was executed and the output was verified successfully.
