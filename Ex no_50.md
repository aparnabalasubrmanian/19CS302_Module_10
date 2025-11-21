
# EX 50 C function to delete a node from a Doubly Linked List at the beginning of the list.
## DATE: 1.11.25
## AIM:
To write a C function to delete a node from a Doubly Linked List at the beginning of the list.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a function to perform all basic operations. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End.   

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
void display() 
{ 
struct Node *temp; 
temp=head; 
 
 
while(temp!=NULL) 
{ 
printf("%.2f ",temp->data); 
temp=temp->next; 
} 
 
} 
 
 SAVEETHA ENGINEERING COLLEGE  
void insert(float data) 
{ 
struct Node *n=(struct Node*)malloc(sizeof(struct Node)); 
struct Node *temp; 
if(head==NULL) 
{ 
head=n; 
n->data=data; 
n->next=NULL; 
n->prev=NULL; 
temp=head; 
} 
else 
{ 
while(temp->next!=NULL) 
{ 
temp=temp->next; 
} 
n->data=data; 
n->next=NULL; 
n->prev=temp; 
temp->next=n; 
} 
 
 
 
} 
void search(float data) 
{ 
struct Node *temp; 
temp=head; 
int i=0,f=0; 
 
while(temp!=NULL) 
{ 
if(temp->data==data) 
{ 
printf("item %.2f found at location %d\n",data,i+1);  
i++; 
temp=temp->next; 
} 
if(f==0) 
{ 
printf("Item not found\n"); 
} 
} 
void delete() 
{ 
struct Node *p; 
p=head; 
if(p==NULL) 
{ 
printf("UNDERFLOW \n"); 
} 
else if(head->next==NULL) 
{ 
head=NULL; 
free(head); 
printf("Node deleted\n"); 
} 
else 
{ 
p=head; 
head=head->next; 
head->prev=NULL; 
printf("Node deleted\n"); 
} 
 
}
```

## Output:
![image](https://github.com/user-attachments/assets/f6186ab1-5325-4a0c-9be1-96ef08646704)


## Result:
Thus the program was executed and the output was verified successfully.
