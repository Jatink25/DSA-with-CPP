Approach to the question:
while implementing a queue using two stack. the approach is simple to just push in queue is to push the number to stack1
(say st1.push(x))

for pop and peek: first push the element of first stack to the second stack. so that the top element of the second stack is the first number that is pushed in the first stack . due to which it actually implementing the process of first in first out.
 ```cpp
        if(st2.empty()){
            while(!st1.empty()){
                   st2.push(st1.top());
                   st1.pop();   
            }
        }  
```

and return the appropriate values.

for isempty function just check, if both stacks are empty then the queue is empty else it is not.