# Data-Structures-and-Algorithms 1
 
# Author
**Matthias Bartolo 0436103L**

## Preview:
<p align='center'>
  <img src="https://github.com/mbar0075/Data-Structures-and-Algorithms1/assets/103250564/d203bd9f-12ba-4e43-966b-cef00ff0e02b" style="display: block; margin: 0 auto; width: 70%; height: auto;"></br>
</p>

## Description of Task:
In this project, various programming tasks were undertaken to explore and implement different algorithms and data structures. These tasks cover a range of topics including **sorting algorithms**, **array operations**, **mathematical computations**, and **data structure manipulation**. The aim of this project was to showcase the understanding and application of these concepts. The following tasks were completed as part of this project:

1. Creation and Sorting of Integer Arrays: Two integer arrays, A and B, were created with a minimum size of 256 elements and unequal sizes. The arrays were populated with randomly generated integers ranging from 0 to 1024. Array A was sorted using Shell Sort, while array B was sorted using Quick Sort.

```python
def QuickSort(mylist,first,last):
    #Recursive Case where first pointer is smaller than last pointer
    if first<last:
        #Finding pivot element such that elements are smaller on the left and greater on the right
        pivotPos=partition(mylist,first,last);
        #Sorting left sublist
        QuickSort(mylist,first,pivotPos-1);
        #Sorting right sublist
        QuickSort(mylist,pivotPos+1,last);
```

2. Merging of Sorted Arrays: The sorted arrays A and B were efficiently merged into a new array, C, with a size equal to the sum of the sizes of A and B. The merging process was performed in linear time, ensuring optimal performance.

3. Identification of Extreme Points in an Array: An algorithm was devised to identify the extreme points in an array, A, consisting of n elements. Extreme points were defined as elements that met specific criteria in relation to their adjacent elements. The algorithm accurately identified and printed the extreme points of the array. If no extreme points were found, the algorithm outputted "SORTED". The question of whether an array has no extreme points if and only if it is sorted was carefully examined and discussed.

```python
def extreme(array):
    check =0;#Boolean variable to check if array is sorted
    #Traversing through array
    for i in range(1,len(array)-1):
        #Checking extreme points and setting boolean variable to 1 to indicate not sorted
        if(array[i-1]<array[i])and(array[i]>array[i+1]):
            print(array[i]);
            check=1;
        if(array[i-1]>array[i])and(array[i]<array[i+1]):
            print(array[i]);
            check=1;
    
    #If condition to check if list is sorted based on boolean variable
    if check==0:
        print("SORTED")
```

4. Finding 2-Pairs of Integers: A program was developed to find all 2-pairs of integers in a given list of integers. These pairs were characterized by having the same product but being distinct from each other. The range of integers in the list was specified as 1 to 1024. The program efficiently identified and reported all such 2-pairs.

5. Evaluation of RPN Arithmetic Expressions: A program was created to evaluate arithmetic expressions in Reverse Polish Notation (RPN) format using an Abstract Data Type (ADT) Stack. During the evaluation process, the contents of the stack were displayed, providing insights into the step-by-step computation of the expressions. The program supported the operators of addition, subtraction, multiplication, and division.

6. Primality Checking and the Sieve of Eratosthenes: A Boolean function was implemented to determine whether a given number is prime. Additionally, the Sieve of Eratosthenes algorithm was applied to efficiently identify prime numbers by eliminating multiples of prime numbers as candidates. The implementation included optimizations to improve computational efficiency.

7. Incremental Construction of Binary Search Trees: A program was designed to accept a random sequence of integers as input and incrementally build and display a Binary Search Tree (BST). The program emphasized simplicity and did not include balancing the BST, focusing on the fundamental concepts of BST construction.

8. Approximation of Square Roots: A program was developed to approximate the square root of a given number, n, using an iterative numerical method such as the Newton-Raphson Method. The program provided an efficient and accurate approximation of square roots.

9. Identification of Repeated Integers: A program was created to find all integers in an array that are repeated more than once. Special attention was given to devising a fast and memory-efficient approach for this task, ensuring optimal performance even for large arrays.

10. Recursive Determination of the Largest Integer: A recursive function was implemented to determine the largest number in a given list of integers. The function employed a recursive approach to systematically compare and identify the largest integer.

```python
#Parameters include List, largest element and counter to hold the index of the current element
def Largest(mylist,max,counter):
    #Base Case
    if counter==-1 :
        return max;
    #Recursive Case
    else :
        #if the max is smaller than current element
        #then max is set to be the current element
        if max<mylist[counter]:
            max=mylist[counter];
        #Calling recursive case and decrementing counter(index)
        return Largest(mylist,max,counter-1);
```

11. Computation of Trigonometric Functions: A function was developed to compute cosine or sine by considering the first n terms of the appropriate series expansion, such as the Maclaurin series. This allowed for accurate and efficient calculation of these trigonometric functions.

12. Calculation of Fibonacci Sequence Sum: A function was implemented to calculate the sum of the first n numbers in the Fibonacci sequence. The Fibonacci sequence, starting with the numbers 1 and 1, was utilized to perform the summation.

```python
def Fibonacci(n):
    #Declaring and initialising variables:
    
    returnsum=0;#Variable to hold the sum of n numbers
    sum=0;#Temporary variable to perform addition of num1 and num2
    num1=1;#num1 to hold the first term in sequence
    num2=1;#num2 to hold the second term in sequence
    count=0;#Counter to be used for looping
    
    #Looping if count<n
    while count<n :
        #Adding the contents of num1 to returnsum
        returnsum=returnsum+num1;
        
        #Finding the next term in the Fibonacci Sequence and incrementing count
        sum=num1+num2;
        num1=num2;
        num2=sum;
        count=count+1;
    
    #Returning the sum of n numbers
    return returnsum;
```

## Deliverables:
The repository includes:<br />
1.Matthias Bartolo DataStructures Coursework 2022-checkpoint.ipynb: Assignment Code<br />
2.Matthias Bartolo DSA Coursework2022.pdf: Assignment Documentation/Report
