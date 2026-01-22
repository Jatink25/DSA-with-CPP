## implementing stack using queue
- There are two methods : 
    -with single queue
    -with two queues

## using two queue
**Approach**
- push element to q2;
- push element by element of q1 to q2(if q1 is not empty) while poping the elements from q1
- swap the elements of q1 and q2.
    ```cpp
     void push(int x) {
        q2.push(x);
        while(!q1.empty()){
            q2.push(q1.front());
            q1.pop();
        }
        swap(q1,q2);
    }
    ```
- for pop and top operation, use q1.pop() and q1.front()

## using single queue:
- push element in the queue
- rotate the elements by again pushing the top of the queue(for size-1 times) in the same queue while poping from queue
 ```cpp
    void push(int x) {
        int size = q.size();
        q.push(x);
        for(int i = 0;i<size;i++){
            q.push(q.front());
            q.pop();
        }
    }
```
- for pop and top operation, use q.pop() and q.front()