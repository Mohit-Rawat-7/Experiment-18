# Experiment-18

## AIM
To learn queue in c++.

## Poblem Statement
Write a program to dequeue & enqueue in c++.

# Theory 
A queue is a way to organize items so that the first one added is the first one to be removed, following a first-in, first-out (FIFO) order. You add items to the back of the queue and take them out from the front. Queues are commonly used in situations like waiting in line or processing tasks, and they work with basic functions like adding (enqueue) and removing (dequeue) items. They can be built using lists or special structures, and they allow for quick adding and removing of items.

## Program Codes
```javascript
// Mohit Singh Rawat
//23070123086
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Queue{
    int rear, front, ar[size];
    public:
    Queue(){
        rear = -1;
        front = -1;
        ar[0]=0;
    }
    void enqueue(int);
    int dequeue();
    void disp();
};
void Queue :: enqueue(int num){
    if (rear == (size+1)){
        cout<<"Queue is full"<<endl;
    }
    else{
        if(front == -1){
            ar[++front]=num;
            rear++;
        }
        else{
            ar[++rear]=num;
        }
    }

    }
int Queue ::dequeue(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Queue is empty"<<endl;
        return ERROR;
    }
    else{
        int val = ar[front++];
        return val;
    }
}
void Queue :: disp(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Quee=ue is empty"<<endl;
        return;
    }
    else{
        int i = front ;
        while (i!=(rear+1)){
            cout<<ar[i];
            i++;
        }
    }
}

int main(){
        Queue q1;
        q1.enqueue(4);
        q1.enqueue(8);
        q1.enqueue(3);
        q1.disp();
        int val = q1.dequeue();
        cout<<endl<<"Deleted element: "<<val<<endl;
        q1.disp();

}
```

## Program Output
 <img width="324" alt="image" src="https://github.com/user-attachments/assets/4d3afe48-cba6-413f-86a6-69d105727db3">

## Conclusion 
In conclusion, queues are vital data structures that manage information in a first-in, first-out (FIFO) order. They are widely used in applications like task management and network handling, providing simple operations for adding and removing items to keep processes organized and efficient.

