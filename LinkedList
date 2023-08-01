#include <stdio.h>
#include <stdlib.h>
#define STACK_SIZE 10
struct node {
       int data;
       struct node *next;
};

typedef struct{
        int cnt;
        struct node *top;
}stack;


void initialize (stack *stk){
     stk->cnt=0;
     stk->top=NULL;
}

void push (stack *stk, int x) {
     if(stk->cnt==STACK_SIZE){
     printf("Stack is full.\n"); 
     }else{
           struct node *temp=(struct node*)malloc(sizeof(struct node)); //malloc fonksiyonu bu sekilde yazilir.
           temp->data=x;
           temp->next=stk->top;
           stk->cnt++;
           stk->top=temp;
           }
     }

int pop(stack *stk){
    if (stk->cnt==0){
        printf("Stack is empty");
        return 0;
    }else{
          int data=stk->top->data;
          struct node *temp=stk->top;
          stk->top=stk->top->next;
          free(temp);
          stk->cnt--;
          return data;
    }
}

main(){
       stack s;
       initialize(&s);
       push(&s, 3);
       push(&s, 2);
       push(&s, 10);
       push(&s, 40);
       printf("%d\n", pop(&s));
       printf("%d\n", pop(&s));
       printf("%d\n", pop(&s));
       printf("%d\n", pop(&s));
}
