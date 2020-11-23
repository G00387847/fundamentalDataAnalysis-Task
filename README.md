# fundamentalDataAnalysis-Task

# Task 1 - count

October 5th, 2020: Write a Python function called counts that takes a list as input and returns a dictionary of unique items in the list as keys and the number of times each item appears as values. So, the input ['A', 'A', 'B', 'C', 'A'] should have output {'A': 3, 'B': 1, 'C': 1} . Your code should not depend on any module from the standard library1 or otherwise. You should research the task first and include a description with references of your algorithm in the notebook.

# Solution

The Task started by defined what is List and Dictionary in python. I defined the List as a collection which is ordered and chaneable while Dictionary is a collection which id unordered and indexed.

I explained the overview of the Task is to use List as input and Dictionary as output without the code depending on any module from the standard python library or otherwise as was instructed in the Task

I started the code by creating List and Dictionary, I loop through the List, using dictionary get method() to return the value for a given key which was set as a default and return the list in a dictionary
  
##### create list
list =  'A', 'A', 'B', 'C', 'A'
#### create dictionary
dict = {}
##### loop through the list
for i in list:
    dict[i] = dict.get(i,0)+1 ##### using dict get method()  
print(dict)


# Task - 2 Dicerolls

November 2nd, 2020: Write a Python function called dicerolls that simulates rolling dice. Your function should take two parameters: the number of dice k and the number of times to roll the dice n. The function should simulate randomly rolling k dice n times, keeping track of each total face value. It should then return a dictionary with the number of times each possible total face value occurred. So, calling the function as diceroll(k=2, n=1000) should return a dictionary like: {2:19,3:50,4:82,5:112,6:135,7:174,8:133,9:114,10:75,11:70,12:36} You can use any module from the Python standard library you wish and you should include a description with references of your algorithm in the notebook.

# Solution
The solution to Task -2 started by defined python function. It is a block of code which only runs when it is called and can pass data, known as parameter, into a function, then return data as a result.

The code started by importing python library called numpy. I define the functions by declaring the data, loop through the times(100), using random.ranint method to return the selected number range specified(2,12), pass the data to return the result.

