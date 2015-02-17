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

## Loops

Looping is a very important feature of a language that allows you to do the same thing, often with a slight change, over and over again. If you haven't encountered looping before, imagine it's like rolling down a hill. You spin and spin, over and over, doing the same thing but hitting different bumps in the hill the further down you go.

However, it's very easy to go wrong when using loops, since you are not just doing that thing wrong once, but hundreds, thousands, or potentially infinite times. Kind of like if you landed on your head every time you spun while going down the hill: once is sore; twice, you will probably have a headache; three times and BOOM! a concussion.

In Python, there are only two types of loop - the `for` loop and the `while` loop. Most of the time you will probably use the former. Here are some quick examples, in case you have a bad memory (like me):

```python
for number in [1,5,2,4,8]:
    print(number) # prints each number in the list on a separate line

for number in range(0, 100):
    print(number) # prints 0 to 99 on a separate line

while True:
    print("This will print over and over, never ending")

number = 14
while number % 2 == 0: # checks if the number is divisible by two every iteration
    if number > 50:
        break # exits loop completely
    
    if number % 12 == 0:
        number += 4
        continue # skips to next iteration of loop
    
    number += 2
```

Hopefully that jogged any memories that were eluding you has to how loops in general work. Now, here is the same code, implemented in C:

```c
int numbers[5] = {1, 5, 2, 4, 8};
for (int i = 0; i < 5; i++) {
    printf("%d\n", numbers[i]); // prints each number in the list on a separate line
}

for (int i = 0; i < 100; i++) {
    printf("%d\n", i); // prints 0 to 99 on a separate line
}

while (1) { // same meaning as while True
    printf("This will print over and over, never ending\n");
}

for (;;) {
    printf("Infinite loops can also be written like this, they exactly the same thing");
}

int number = 14;
while (number % 2 == 0) {
    if (number > 50) {
        break;
    }

    if (number % 12 == 0) {
        number += 4;
        continue;
    }
    
    number += 2;
}

int number = 14;
do {
    if (number > 50) {
        break;
    }

    if (number % 12 == 0) {
        number += 4;
        continue;
    }
    
    number += 2;
} while (number % 2 == 0); // this is the same as the previous example, except that the code is run once before the
                              looping condition (the code in the while part and the middle section of for loops) is
                              checked
````

That's a lot of C code! Well, let's take things slowly. First, the things that stay the same between Python and C include `while` loops, `continue` and `break`. Actually, that's quite a lot of similarity. The only real differences are `for` loops and `do`-`while` loops. `do`-`while` loops are deceptively complex. The difference between them and regular `while` loops is that the code in the body - between the curly braces - is run once before checking if it should run at all. To illustrate this, two examples:

```c
while (0) { // same meaning as while False
    printf("This will never be printed, simply skipped over\n");
}

do {
    printf("This will be printed once, since the condition is checked after the first run of the body\n");
} while (0); // also remember that unlike a regular while loop, a do-while loop must be terminated with a semicolon
```

This can lead to some interesting situations if you replace `while` loops with `do`-`while` loops without thinking. Most of the time a `while` loop is what you'll use. However, the most common tye of loop is a `for` loop, and these work very differently in C and Python. In Python, a `for` loop is very literal. An example:

```python
for i in [23,3,4,4,2]:
    print(i)
```

This translates as "for each element in `[23,3,4,4,2]` run this code with the element represented as `i`". In C, a for loop is actually far more flexible, but also far more difficult to use. If you re-write that code snippet in C, you get this:

```c
int numbers[5] = {23,3,4,4,2};
for (int i = 0; i < 5; i++) {
    printf("%d\n", numbers[i]);
}
```

This translates to the code:

```c
int numbers[5] = {23,3,4,4,2};
int i = 0;
while (i < 5) {
    printf("%d\n", numbers[i]);
    i++
}
```

It does not translate well to English, as it is simply a wrapper around a while loop - in fact, that is exactly how the compiler treats. Both those statements mean exactly the same thing.
