# 3 - I know you know

Hello again! Welcome back to the C tutorial! I hope the last chapter wasn't too much to handle all in one hit. Don't worry, though, because this chapter goes back to stuff you knew even before you started the first chapter: Python.

I mentioned at the start of the first chapter that this tutorial is aimed at Pythonesta's - that is, someone who is competent using Python. However, you only really need a beginner-moderate competency in Python to understand it. In this chapter, we will be looking at some features in Python and their equivalents (or lack therof) in C.

## Function

A function is a method for reusing code, like a formula in Science. In Python, defining a function looks like this:

```python
def add(first, second):
    return first + second
```
And to use this function:

````python
x = add(1, 2)
print(add(3, 4))
if add(5, 6) == 12:
    # math is broken :(
for i in range(0, add(7, 8)):
    # run 15 times
```

In C, using functions is relatively similar:

```c
int add(int first, int second) {
    return first + second;
}
```
and to use this function:

```c
int x = add(1, 2);
printf("%d\n", add(3, 4));
if (add(5, 6) == 12) {
    // math is broken :(
}
for (int i = 0; i < add(7, 8); i++) {
    // run 15 times
}
```

The first difference you will notice is that to define the function `add` we used `int`, rather than a more logical `def`, `define`, `fn`, or `function`. This is because, in C, you must specify the type of variable that you will return. Common types include:

Type | Definition | Keyword
--------|--------------|------------
Integer | Whole number | `int`
Floating point | Decimal number | `float`
Character | Single letter | `char`

There are many more, such as `short`, `unsigned long long`, `signed short int`, `long double`, and `unsigned long long int`, however they are significantly more complicated and we will cover later.

The second defference is the use of curly braces. This actually very similar to Python, just with the characters changed. Just replace the colon with a curly brace and add a closing brace at the end and you have valid C. Note, however, that while in Python this would be illegal:
```python
def add(first, second):
return first + second
```
this is valid C:
```c
int add(int first, int second) {
return first + second;
}
```
However, you should still puta tab at the start of the line, as it makes your code much easier to read.

Next, you''ll notice that before the function parameters whe put the type they must be, int this case `int`. This is because every variable must have a type, including, in this example, `first` and `last`, which are of type `int`. That means that, while in Python you could say `first = "First"` if you wanted to, that would be an error while compiling your program in C. You will also notice this is the same in the second example, where it says `int x = add(1, 2);` rather than just `x = add(1, 2)`.

You are probably confused by the line `printf("%d\n", add(3, 4));`. This can be broken into two parts which will make it much easier for you to understand. First, `printf("\n");`. We saw this earlier. In this case, it simply prints a new line character, represented by `\n`. The second half is actually a feature that was copied into Python called string interpolation, which we will cover at a different point in this chapter.

Next, the `for` loop. This works differently than in Python. We will cover this in another section.
