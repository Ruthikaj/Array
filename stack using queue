Let's perform a dry run of the MyQueue class code, explaining what happens at each line.
class MyQueue {
public:
    stack<int> input, output; // Declare two stacks: input for enqueue and output for dequeue.
    MyQueue() { // Constructor for MyQueue
        // Initializes an empty queue with two stacks.
    }
    void push(int x) { // Method to add an element to the queue
        input.push(x); // Push the new element onto the input stack.
    }
    int pop() { // Method to remove the front element from the queue
        int popped_ele; // Variable to store the popped element.
        if(output.empty() == false) { // Check if the output stack has elements.
            popped_ele = output.top(); // Get the top element from output (front of the queue).
            output.pop(); // Remove the top element from the output stack.
        }
        else { // If output stack is empty
            while(!input.empty()) { // Transfer all elements from input to output
                output.push(input.top()); // Push the top element of input to output.
                input.pop(); // Remove the top element from input.
            }
            popped_ele = output.top(); // Now get the top element from output (front of the queue).
            output.pop(); // Remove the top element from the output stack.
        }
        return popped_ele; // Return the popped element.
    }
    int peek() { // Method to check the front element of the queue without removing it
        int top_element; // Variable to store the top element.
        if(output.empty() == false) { // Check if the output stack has elements.
            top_element = output.top(); // Get the top element from output (front of the queue).
            // output.pop(); // Do not remove it, just peek.
        }
        else { // If output stack is empty
            while(!input.empty()) { // Transfer all elements from input to output
                output.push(input.top()); // Push the top element of input to output.
                input.pop(); // Remove the top element from input.
            }
            top_element = output.top(); // Get the top element from output (front of the queue).
            // output.pop(); // Do not remove it, just peek.
        }
        return top_element; // Return the front element.
    }
    bool empty() { // Method to check if the queue is empty
        return output.empty() && input.empty(); // Return true if both stacks are empty.
    }
};
/**
 */

Summary of Operations

Push Operation (push(int x)): Elements are pushed onto the input stack. This operation runs in O(1) time.
Pop Operation (pop()):
If output is not empty, it pops the top element directly.
If output is empty, it transfers all elements from input to output (reversing their order) and then pops the top element from output. This operation can take O(n) time in the worst case when transferring elements.

Peek Operation (peek()):
Similar to pop(), but it only retrieves the top element without removing it. It also can take O(n) time in the worst case when transferring elements.

Empty Operation (empty()): Checks if both stacks are empty, which is an O(1) operation.

This implementation effectively simulates a queue using two stacks, maintaining the FIFO (First-In-First-Out) behavior of a queue.
