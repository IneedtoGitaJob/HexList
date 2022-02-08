#include <stdio.h>
#include <stdlib.h>
#include <string.h>

struct Node{
int data;

struct Node* next0;
struct Node* next1;
struct Node* next2;
struct Node* next3;
struct Node* next4;
struct Node* next5;
struct Node* next6;
struct Node* next7;
struct Node* next8;
struct Node* next9;
struct Node* nextA;
struct Node* nextB;
struct Node* nextC;
struct Node* nextD;
struct Node* nextE;
struct Node* nextF;
}Node;

//Inserts a Value into the array
void Insert(struct Node* Head, int val);
//Helper function Sets all next pointers of a newly created array to NULL
void Point_To_NULL(struct Node* Head);
//returns 1 if the value is in the list else returns 0
int Search(struct Node* HeadPoint, int val);
//Helper function Used to traverse through the List
struct Node* Traverse(struct Node* current, char value);

//Starter function
int main (){

int New_val;
FILE* f = fopen("obagna.txt","r");
FILE* f2 = fopen("obagna2.txt","r");
if(f == NULL){
    return 0;
}

struct Node* Head = (struct Node*)malloc(sizeof(Node));
Head->data = -1;
Point_To_NULL(Head);

while(fscanf(f,"%d",&New_val)!=EOF){
Insert(Head,New_val);
}
struct Node* HeadPoint = Head;
int cal = 0;
while(fscanf(f2,"%d",&New_val)!=EOF){
cal = Search(HeadPoint, New_val);
printf("\n%d\n",cal);
}

return 1;
}

//Inserts a Value into the array
void Insert(struct Node* Head, int val)
{
//Inputs the hex value of a number into the array
char Hexed_val[9];
sprintf(Hexed_val, "%x", val);
printf("Hex:%s ",Hexed_val);
printf("Val:%d ",val);
struct Node* current = Head;
struct Node* prev = Head;

//Int i will be our iteration value because values in the array are stored in the opposite direction in which they should be read we start at the last full cell and iterate down
int i = strlen(Hexed_val);
printf("Len:%d \n",i);
//Iterate until an empty node is found or we have run out of hexed values
while(current != NULL && i > 0)
{
    prev = current;
    current = Traverse(current, Hexed_val[i-1]);
    i--;
}


//Insert into an empty node
if(current == NULL){

//Create Node to be inserted
struct Node* temp = (struct Node*)malloc(sizeof(struct Node));
if(temp == NULL)
{
printf("Memory error");
exit(0);
}

temp->data = val;
Point_To_NULL(temp);



//Link the rest of the tree to the new node
switch(Hexed_val[i])
{
case '0':
prev->next0 = temp;
break;
case '1':
prev->next1 = temp;
break;
case '2':
prev->next2 = temp;
break;
case '3':
prev->next3 = temp;
break;
case '4':
prev->next4 = temp;
break;
case '5':
prev->next5 = temp;
break;
case '6':
prev->next6 = temp;
break;
case '7':
prev->next7 = temp;
break;
case '8':
prev->next8 = temp;
break;
case '9':
prev->next9 = temp;
break;
case 'a':
prev->nextA = temp;
break;
case 'b':
prev->nextB = temp;
break;
case 'c':
prev->nextC = temp;
break;
case 'd':
prev->nextD = temp;
break;
case 'e':
prev->nextE = temp;
break;
case 'f':
prev->nextF = temp;
break;
}


}

//Insert into a Full Node
else{
    //If we find a duplicate val we do not input it
    if(current->data == val)
    {
    printf("duplicate value ignored");
    return;
    }
    //Insert Behind
        int val2 = current->data;
            current->data = val;
Insert(Head, val2);


}

}

//Sets all next pointers of a newly created array to NULL
void Point_To_NULL(struct Node* Head){
Head->next0=NULL;
Head->next1=NULL;
Head->next2=NULL;
Head->next3=NULL;
Head->next4=NULL;
Head->next5=NULL;
Head->next6=NULL;
Head->next7=NULL;
Head->next8=NULL;
Head->next9=NULL;
Head->nextA=NULL;
Head->nextB=NULL;
Head->nextC=NULL;
Head->nextD=NULL;
Head->nextE=NULL;
Head->nextF=NULL;
}

//Searches for a specific val
int Search(struct Node* HeadPoint, int val){
char Hexed_val[9];
sprintf(Hexed_val, "%x", val);
struct Node* current = HeadPoint;

int x = strlen(Hexed_val);

while(x >0)
{
current = Traverse(current, Hexed_val[x-1]);
x--;
if(current != NULL){
if(current->data == val){return 1;}
}
else{
    return 0;
}
}

return 0;
}

//Used to traverse through the List
struct Node* Traverse(struct Node* current, char value){
switch(value){
case '0':
    return current->next0;
break;
case '1':
    return current->next1;
break;
case '2':
    return current->next2;
break;
case '3':
    return current->next3;
break;
case '4':
    return current->next4;
break;
case '5':
    return current->next5;
break;
case '6':
    return current->next6;
break;
case '7':
    return current->next7;
break;
case '8':
    return current->next8;
break;
case '9':
    return current->next9;
break;
case 'a':
    return current->nextA;
break;
case 'b':
    return current->nextB;
break;
case 'c':
    return current->nextC;
break;
case 'd':
    return current->nextD;
break;
case 'e':
    return current->nextE;
break;
case 'f':
    return current->nextF;
break;
}
}


