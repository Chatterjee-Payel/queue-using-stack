# queue-using-stack
class Queue {
    stack<int> input, output;
public:

    void enqueue(int x) {
        input.push(x);
    }

    int dequeue() {
        int t=peek();
        output.pop();
        return t;
    }
    int peek()
    {
        if(output.empty())
        {
            while(input.size())
            {
                output.push(input.top());
                input.pop();
            }
        }
        return output.top();
        
    }
};
