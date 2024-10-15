Data Structures is about how data can be stored in different structures.
Algorithms is about how to solve different problems, often by searching through and manipulating data structures.
Theory about Data Structures and Algorithms (DSA) helps us to use large amounts of data to solve problems efficiently.

what are Data Structures?
A data structure is a way to store data.
We structure data in different ways depending on what data we have, and what we want to do with it.
Data structures give us the possibility to manage large amounts of data efficiently for uses such as large databases and internet indexing services.

Data structures are essential ingredients in creating fast and powerful algorithms. They help in managing and organizing data, reduce complexity, and increase efficiency.

***********In Computer Science there are two different kinds of data structures.**********

-----Primitive Data Structures are basic data structures provided by programming languages to represent single values, such as integers, floating-point numbers, characters, and booleans.

------Abstract Data Structures are higher-level data structures that are built using primitive data types and provide more complex and specialized operations. Some common examples of abstract data structures include arrays, linked lists, stacks, queues, trees, and graphs.

What are Algorithms?
An algorithm is a set of step-by-step instructions to solve a given problem or achieve a specific goal.
Algorithm examples:

Finding the fastest route in a GPS navigation system
Navigating an airplane or a car (cruise control)
Finding what users search for (search engine)
Sorting, for example sorting movies by rating
The algorithms we will look at in this tutorial are designed to solve specific problems, and are often made to work on specific data structures. For example, the 'Bubble Sort' algorithm is designed to sort values, and is made to work on arrays.


Term	            Description
Algorithm	      A set of step-by-step instructions to solve a specific problem.
Data Structure	  A way of organizing data so it can be used efficiently. Common data structures include arrays, linked lists, and binary trees.
Time Complexity  	A measure of the amount of time an algorithm takes to run, depending on the amount of data the algorithm is working on.
Space Complexity	A measure of the amount of memory an algorithm uses, depending on the amount of data the algorithm is working on.
Big O Notation	    A mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. Used in this tutorial to describe the time complexity of an algorithm.
Recursion	       A programming technique where a function calls itself.
Divide and Conquer	 A  method of solving complex problems by breaking them into smaller, more manageable sub-problems, solving the sub-problems, and combining the solutions. Recursion is often used when using this method in an algorithm.
Brute Force	       A simple and straight forward way an algorithm can work by simply trying all possible solutions and then choosing the best one.

***********Fibonacci Numbers**********

The Fibonacci numbers are very useful for introducing algorithms, so before we continue, here is a short introduction to Fibonacci numbers.

The Fibonacci numbers are named after a 13th century Italian mathematician known as Fibonacci.

The two first Fibonacci numbers are 0 and 1, and the next Fibonacci number is always the sum of the two previous numbers, so we get 0, 1, 1, 2, 3, 5, 8, 13, 21, ...


The Fibonacci Number Algorithm
To generate a Fibonacci number, all we need to do is to add the two previous Fibonacci numbers.

The Fibonacci numbers is a good way of demonstrating what an algorithm is. We know the principle of how to find the next number, so we can write an algorithm to create as many Fibonacci numbers as possible.

Below is the algorithm to create the 20 first Fibonacci numbers.

#### Loops vs Recursion
To show the difference between loops and recursion, we will implement solutions to find Fibonacci numbers in three different ways:

An implementation of the Fibonacci algorithm above using a for loop.
An implementation of the Fibonacci algorithm above using recursion.
Finding the 
n
th Fibonacci number using recursion.
1. Implementation Using a For Loop
It can be a good idea to list what the code must contain or do before programming it:

Two variables to hold the previous two Fibonacci numbers
A for loop that runs 18 times
Create new Fibonacci numbers by adding the two previous ones
Print the new Fibonacci number
Update the variables that hold the previous two fibonacci numbers
Using the list above, it is easier to write the program:

Example
prev2 = 0
prev1 = 1

print(prev2)
print(prev1)
for fibo in range(18):
    newFibo = prev1 + prev2
    print(newFibo)
    prev2 = prev1
    prev1 = newFibo
2. Implementation Using Recursion
Recursion is when a function calls itself.

To implement the Fibonacci algorithm we need most of the same things as in the code example above, but we need to replace the for loop with recursion.

To replace the for loop with recursion, we need to encapsulate much of the code in a function, and we need the function to call itself to create a new Fibonacci number as long as the produced number of Fibonacci numbers is below, or equal to, 19.

Our code looks like this:

Example
print(0)
print(1)
count = 2

def fibonacci(prev1, prev2):
    global count
    if count <= 19:
        newFibo = prev1 + prev2
        print(newFibo)
        prev2 = prev1
        prev1 = newFibo
        count += 1
        fibonacci(prev1, prev2)
    else:
        return

fibonacci(1,0)
3. Finding The 
n
th Fibonacci Number Using Recursion
To find the 
n
th Fibonacci number we can write code based on the mathematic formula for Fibonacci number 
n
:

F
(
n
)
=
F
(
n
−
1
)
+
F
(
n
−
2
)

This just means that for example the 10th Fibonacci number is the sum of the 9th and 8th Fibonacci numbers.

Note: This formula uses a 0-based index. This means that to generate the 20th Fibonacci number, we must write 
F
(
19
)
.

When using this concept with recursion, we can let the function call itself as long as 
n
 is less than, or equal to, 1. If 
n
≤
1
 it means that the code execution has reached one of the first two Fibonacci numbers 1 or 0.

The code looks like this:

Example
def F(n):
    if n <= 1:
        return n
    else:
        return F(n - 1) + F(n - 2)

print(F(19))
Notice that this recursive method calls itself two times, not just one. This makes a huge difference in how the program will actually run on our computer. The number of calculations will explode when we increase the number of the Fibonacci number we want. To be more precise, the number of function calls will double every time we increase the Fibonacci number we want by one.