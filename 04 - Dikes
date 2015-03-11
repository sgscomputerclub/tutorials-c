# 04 - Dikes

This rather cryptically named chapter covers the C build system. if you have only ever used interpreted languages, such as Python, Javascript, and Ruby, the concept of a build system will probably seem a bit alien and unecessary. You needn't fear, however, as we will be covering everything about it in this chapter.

## What you're used to
If you have come from Python and the like you are probably used to writing your code and then running it directly, i.e. running `python program.py`. This, however conveniant, is not very good for distributing applications and also runs programs very slowly. C, and many other languages, opted for the less conveniant, but faster and more easily distributed version, called compiling. Python's method is called interpreting.

### Interpreting
Interpreting is the process of a program reading your code and then executing what you say to do. For example, when you write in Python:
```python
x = 10
y = 15
z = x * y
```
Python reads the first line, creates a variable called `x` containing the value `10`. Then it reads the next line, creates a value named `y` contaning the value `15`. Finally it reads the final line, creates a variable called `z` containg the product of `x` and `y`.

As you might guess this is quite slow to run, as there lots of checks and reading that Python has to do with every line, such that it can actually multiply `x` and `y` together. For example it has to be able to tell that this is incorrect code:
```python
x = "a string"
y = "another string"
z = x * y
```

### Compiling
