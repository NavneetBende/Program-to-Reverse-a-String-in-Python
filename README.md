What are strings and how to reverse a string?
The string is an immutable sequence data type. It is a sequence of Unicode characters wrapped inside a single, double or triple quote. The task is to write a program to reverse the given string.
Example :

Input : Hello world
Output: dlrow olleH
Reversing a String in python language
Program to Reverse a String using Python
There are three approaches to reverse a string variable in python.

Using string slicing.
Using reversed() function.
Using Brute force.
Reversing a String Python Program
Method 1: Reversing a String using String slicing
Python code.
Run
#using slicing:
string = "Hello world"
print(string[::-1])
Output
Hello world
dlrow olleH
Explanation

The slicing function accepts three variables in the format

[start:stop:step]
The start holds the starting index of the string, the stop holds the last-1 element’s index, step holds the value of the number of steps while iteration.

In the code, string[::-1], when we pass -1 as the step and the empty start and end take 0 and len(string)-1 by default. This reverses the string with step 1 in the reverse direction.

Method 2: Reversing a String using reversed() function
Python code
Run
string = "Hello world"
print(''.join(list(reversed(string))))
Output
Hello world
dlrow olleH
Explanation.
The reversed() takes string values and returns the reversed string.

reversed(string)
In the above code, we take string using input() function. input() function returns a list, which is stored in the string variable. We pass the list string in reversed() function which returns a list of reversed string elements. The string list is then converted to a string variable using .join() function.

Method 3: Reversing a string using brute force approach
Python code
Run
#using brute force:
string = "Hello world"
output = ''
for i in range(len(string)-1,1,-1):
  output+=string[i]
output+=string[i-1]
output+=string[i-2]
print(output)
Output
Hello world
dlrow olleH
Explanation
In the above code, we use brute force approach, the algorithm is as follows:

Take string as input using input() function.
Initialise an empty string output.
Run a loop from last to first with step size as 1.
Append the element to the output string using ‘+’ operator.
Print the output using print() function.
The range() function in the for loop, accepts three variables,

range(start,stop,step)
We are iterating the whole string from the end hence, reversing the whole string.
