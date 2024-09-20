# DSA-
#include<stdio.h>
#define MAX 5

int queue[MAX];
int front=-1,rear=-1;

int isFull(){
    return (rear+1)%MAX==front;
}

int isEmpty(){
    return front==-1;
}

void enqueue(int element){
    if(isFull()){
        printf("Queue is full\n");
        return;
    }
    if(front==-1){
        front=0;
    }
    rear=(rear+1)%MAX;
    queue[rear]=element;
    printf("Inserted %d\n",element);
}

int dequeue(){
    if(isEmpty()){
        printf("Queue is empty\n");
        return -1;
    }
    int element=queue[front];
    if(front==rear){
        front=-1;
        rear=-1;
    }else{
        front=(front+1)%MAX;
    }
    printf("Removed%d\n",element);
    return element;
}
void display(){
    if(isEmpty()){
        printf("Queue is empty\n");
        return;
    }
    printf("Queue elements:");
    int i=front;
    while(i!=rear){
        printf("%d",queue[i]);
        i=(i+1)%MAX;
    }
    printf("%d\n",queue[rear]);
}
int main(){
    dequeue();
    enqueue(10);
    enqueue(20);
    enqueue(30);
    enqueue(40);
    enqueue(50);
    display();
    
    dequeue();
    enqueue(60);
    display();
    
    return 0;
}
