# fundamentalDataAnalysis-Task

# Task 1 - count

October 5th, 2020: Write a Python function called counts that takes a list as input and returns a dictionary of unique items in the list as keys and the number of times each item appears as values. So, the input ['A', 'A', 'B', 'C', 'A'] should have output {'A': 3, 'B': 1, 'C': 1} . Your code should not depend on any module from the standard library1 or otherwise. You should research the task first and include a description with references of your algorithm in the notebook.

# Solution

The Task started by defined what is List and Dictionary in python. I defined the List as a collection which is ordered and chaneable while Dictionary is a collection which id unordered and indexed.

I explained the overview of the Task is to use List as input and Dictionary as output without the code depending on any module from the standard python library or otherwise as was instructed in the Task

I started the code by creating List and Dictionary, I loop through the List, using dictionary get method() to return the value for a given key which was set as a default and return the list in a dictionary
  
#####  #create list

list = [ 'A', 'A', 'B', 'C', 'A']

#### #create dictionary

dict = {}

##### #loop through the list
for i in list:
    
   #### #using dict get method()
    
    dict[i] = dict.get(i,0)+1 

print(dict)


# Task - 2 Dicerolls

November 2nd, 2020: Write a Python function called dicerolls that simulates rolling dice. Your function should take two parameters: the number of dice k and the number of times to roll the dice n. The function should simulate randomly rolling k dice n times, keeping track of each total face value. It should then return a dictionary with the number of times each possible total face value occurred. So, calling the function as diceroll(k=2, n=1000) should return a dictionary like: {2:19,3:50,4:82,5:112,6:135,7:174,8:133,9:114,10:75,11:70,12:36} You can use any module from the Python standard library you wish and you should include a description with references of your algorithm in the notebook.

# Solution
The solution to Task -2 started by defined python function. It is a block of code which only runs when it is called and can pass data, known as parameter, into a function, then return data as a result.

The code started by importing python library called numpy. I define the functions by declaring the data, loop through the times(100), using random.ranint method to return the selected number range specified(2,12), pass the data to return the result.

#### import python library called numpy
import numpy as np

#### #define function by declaring the data or arguments

def roll_dice(rolls, sides):
   
   k = 2
    
   n =100
 
 #### #loop through the dice roll range  
    
    dice = {i:0 for i in range(2, 13)} 
   
   #### #loop through the times 
    
    for n in range(rolls):
   
   #### #method of returning the selected specified number range
        
        dice[np.random.randint(k, sides)] += 1
    
  #### #return the selected number range  
    
    return(dice)

#### passing the data or arguments

roll_dice (100,  13) 


# Task 3 - Numpy.Random.Binomial


The numpy.random.binomial function can be used to
simulate flipping a coin with a 50/50 chance of heads or tails. Interestingly, if a
coin is flipped many times then the number of heads is well approximated by a
bell-shaped curve. For instance, if we flip a coin 100 times in a row the chance of
getting 50 heads is relatively high, the chances of getting 0 or 100 heads is relatively
low, and the chances of getting any other number of heads decreases as you move
away from 50 in either direction towards 0 or 100. Write some python code that
simulates flipping a coin 100 times. Then run this code 1,000 times, keeping track
of the number of heads in each of the 1,000 simulations. Select an appropriate
plot to depict the resulting list of 1,000 numbers, showing that it roughly follows
a bell-shaped curve. You should explain your work in a Markdown cell above the
code.

# Solution

I started writing the code by first, import standard python libraries called matplotlib for visualization of the result and numpy for working with arrays. I define the number of each probability trials, I use numpy.ramdom.biomial distribution method for the result of flipping the coin 100 times and tested it 1000 times and finally I use histogram plot to visualized the result.

#### #import libraries

import matplotlib.pyplot as plt

import numpy as np

#### #number of each probability trials

n, p = 100, .5

#### #result of flipping coin 100 time was tested 1000 time. 

s = np.random.binomial(n, p, 1000)
s
#### #using histogram plot to visualized the result

plt.hist(s) # using histogram plot to visualized the result
