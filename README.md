
# Coding Exercises

As a warmup for today, here are a few coding problems. Each problem is more difficult than the one before. 

You are not expected to complete all of these problems this morning. Feel free to 
use this notebook as a resource for flexing your coding muscles whenever you need a break from the math of Mod 2. If you complete all of the problems and would like more to solve, check out [Code Wars](https://www.codewars.com). 

For each section, a prompt is provided as well as an empty function. 

Fill in the code for that empty function and run the test cell to measure the success of your code.


```python
## Run this cell unchanged.

def assert_equals(pred,test):
    if pred == test:
        print('Success!')
    else:
        print('Fail')
```

# Array.diff

Your goal in this kata is to implement a difference function, which subtracts one list from another and returns the result.

It should remove all values from list a, which are present in list b.

```array_diff([1,2],[1]) == [2]```

If a value is present in b, all of its occurrences must be removed from the other:

```array_diff([1,2,2,2,3],[2]) == [1,3]```


```python
def array_diff(a, b):
    '''
    Your code here
    '''
```

Test your function below


```python
assert_equals(array_diff([1,2], [1]), [2]), 
assert_equals(array_diff([1,2,2], [1]), [2,2]) 
assert_equals(array_diff([1,2,2], [2]), [1]) 
assert_equals(array_diff([1,2,2], []), [1,2,2]) 
assert_equals(array_diff([], [1,2]), [])
```

    Success!
    Success!
    Success!
    Success!
    Success!


# Moving Zeros To The End

Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.

```move_zeros([false,1,0,1,2,0,1,3,"a"]) # returns[false,1,1,2,1,3,"a",0,0]```


```python
def move_zeros(array):
    '''
    Your code here
    '''
```

Test your function in the cell below


```python
assert_equals(move_zeros([1,2,0,1,0,1,0,3,0,1]),[ 1, 2, 1, 1, 3, 1, 0, 0, 0, 0 ])
assert_equals(move_zeros([9,0.0,0,9,1,2,0,1,0,1,0.0,3,0,1,9,0,0,0,0,9]),[9,9,1,2,1,1,3,1,9,9,0,0,0,0,0,0,0,0,0,0])
assert_equals(move_zeros(["a",0,0,"b","c","d",0,1,0,1,0,3,0,1,9,0,0,0,0,9]),["a","b","c","d",1,1,3,1,9,9,0,0,0,0,0,0,0,0,0,0])
assert_equals(move_zeros(["a",0,0,"b",None,"c","d",0,1,False,0,1,0,3,[],0,1,9,0,0,{},0,0,9]),["a","b",None,"c","d",1,False,1,3,[],1,9,{},9,0,0,0,0,0,0,0,0,0,0])
assert_equals(move_zeros([0,1,None,2,False,1,0]),[1,None,2,False,1,0,0])
assert_equals(move_zeros(["a","b"]),["a","b"])
assert_equals(move_zeros(["a"]),["a"])
assert_equals(move_zeros([0,0]),[0,0])
assert_equals(move_zeros([0]),[0])
assert_equals(move_zeros([False]),[False])
assert_equals(move_zeros([]),[])
```

    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!


# Highest and Lowest

You are given a string of space separated numbers, and have to return the highest and lowest number.

**Example:**

```high_and_low("1 2 3 4 5")  # return "5 1"```

```high_and_low("1 2 -3 4 5") # return "5 -3"```

```high_and_low("1 9 3 4 -5") # return "9 -5"```

**Notes:**

- All numbers are valid Int32, no need to validate them.
- There will always be at least one number in the input string.
- Output string must be two numbers separated by a single space, and highest number is first.


```python
def high_and_low(numbers): #z.
    '''
    Your code here
    '''
```

Test your function below


```python
assert_equals(high_and_low("4 5 29 54 4 0 -214 542 -64 1 -3 6 -6"), "542 -214")
assert_equals(high_and_low("200 6 -2 1000 -30 492 93 -21 9 38 123"), "1000 -30")
assert_equals(high_and_low("1 2 3 4 1 2 3 4 1 2 3 4 1 2 3 4"), "4 1")
assert_equals(high_and_low("10 9 8 7 6 5 4 3 2 1 0 -1 -2 -3 -4"), "10 -4")
assert_equals(high_and_low("338 218 9493823 4949237237 030173734"), "4949237237 218")
assert_equals(high_and_low("0001 0002 00004 00000006"), "6 1")
```

    Success!
    Success!
    Success!
    Success!
    Success!
    Success!


# First character that repeats

Find the first character that repeats in a String and return that character.

```first_dup('tweet') # returns 't'```

```first_dup('like') # returns None```

*This is not the same as finding the character that repeats first. In that case, an input of 'tweet' would yield 'e'.*


```python
def first_dup(s):
    '''
    Your code here
    '''
```

Test your function below


```python
assert_equals(first_dup('tweet'), 't')
assert_equals(first_dup('Ode to Joy'), ' ')
assert_equals(first_dup('ode to joy'), 'o')
assert_equals(first_dup('bar'), None)
assert_equals(first_dup('123123'), '1');
assert_equals(first_dup('!@#$!@#$'), '!');
assert_equals(first_dup('1a2b3a3c'), 'a');
```

    Success!
    Success!
    Success!
    Success!
    Success!
    Success!
    Success!


# Count letters in string

In this kata, you've to count lowercase letters in a given string and return the letter count in a hash with 'letter' as key and count as 'value'. The key must be 'symbol' instead of string in Ruby and 'char' instead of string in Crystal.

**Example:**

```letter_count('arithmetics') # returns {"a": 1, "c": 1, "e": 1, "h": 1, "i": 2, "m": 1, "r": 1, "s": 1, "t": 2}```


```python
def letter_count(s):
    '''
    Your code here
    '''
```

Test your function below


```python
assert_equals(letter_count("joelisverycool"), {'j': 1,'o': 3,'e': 2,'l': 2,'i': 1,'s': 1,'v': 1,'r': 1,'y': 1,'c': 1})
assert_equals(letter_count("activity"), {"a": 1, "c": 1, "i": 2, "t": 2, "v": 1, "y": 1})
assert_equals(letter_count("arithmetics"), {"a": 1, "c": 1, "e": 1, "h": 1, "i": 2, "m": 1, "r": 1, "s": 1, "t": 2})
assert_equals(letter_count("traveller"), {"a": 1, "e": 2, "l": 2, "r": 2, "t": 1, "v": 1})
assert_equals(letter_count("daydreamer"), {"a": 2, "d": 2, "e": 2, "m": 1, "r": 2, "y": 1})
```

    Success!
    Success!
    Success!
    Success!
    Success!


# Sum of Digits / Digital Root

In this kata, you must create a digital root function.

A digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. This is only applicable to the natural numbers.

**Here's how it works:**

```
digital_root(16)
=> 1 + 6
=> 7

digital_root(942)
=> 9 + 4 + 2
=> 15 ...
=> 1 + 5
=> 6

digital_root(132189)
=> 1 + 3 + 2 + 1 + 8 + 9
=> 24 ...
=> 2 + 4
=> 6

digital_root(493193)
=> 4 + 9 + 3 + 1 + 9 + 3
=> 29 ...
=> 2 + 9
=> 11 ...
=> 1 + 1
=> 2```


```python
def digital_root(n):
    '''
    Your code here
    '''
```

Test your function below


```python
assert_equals( digital_root(16), 7 )
assert_equals( digital_root(456), 6 )
assert_equals( digital_root(333), 9 )
assert_equals( digital_root(1039), 4 )
assert_equals( digital_root(20), 2 )
```

    Success!
    Success!
    Success!
    Success!
    Success!

