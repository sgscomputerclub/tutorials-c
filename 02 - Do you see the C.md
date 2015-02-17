# 2 - Do you see the C?

Hello again! So nice to C you. Hehe, just a little joke to lighten the mood. It's only been about 10 seconds bu, so hopefully you've retained everything you read in the previous chapter. If you do not understand something, make sure you flip back to the first chapter and find out what it is. Or, if I've forgotten to include a definition of it - tell me! I want to know any mistakes - Google it, there have been many adventurers into C-land before you, one of them has surely run into your issue or lacked the same knowledge.

Anyway, I digress! We are going to start on writing our first C program. C programs are written in text files, like ".py" files except they end in ".c". So, open up your editor and press Ctrl+S (or Cmd+S on a Mac) and save the blank file as "something.c". This will help the editor enable syntax highlighting for C. I will be giving instructions based on the assumption that you have saved this file on your desktop.

The next step is to start writing code! I am going to supply you with a small piece of C code, that does little more than say "Hello World", but it will serve as a good validation that everything is setup correctly and show you what C programs look like. So, copy this snippet, character for character.

```c
#include <stdio.h>

int main() {
    printf("Hello World\n");
	return 0;
}
```

This may look cryptic right now, but after I explain what each line does you will understand much more.

```c
#include <stdio.h>
```

This line sort of like the equivalent of `import` in Python, but not quite. For now just think of it as `import`

```c
int main() {
```

This is an example of a function in C. In C, you have to declare what "type" the variable you are going to return is. the `main` function is like writing straight into a Python file. It's return type is `int` because it returns an integer indicating to the operating system whether it executed normally or crashed. A return code of `0` indicates that the program ran normally, while any other number means it crashed or other wise executed failed. Notice how the line ends in a brace? In C you delimit things with an opening and closing brace, instead of with a colon and indentation, like in Python. Please remember that all code, if it is not defining something like a function, struct or enum (you'll learn about all those) must go in the main function. This will be left out of future examples for brevity.

```c
printf("Hello World\n");
```

This is an example of a function call in C. This particular function has the same effect as `print("Hello World")` in Python. The `\n` causes it to make a new line afterwards, something `print()` in Python does for you. You will also notice that the line ends in a `;`. Unlike in Python, most lines (there are exceptions) need to be terminated with a semicolon.

```c
return 0;
```

This is an example of the return statement. It functions exactly like `return` in Python.

```c
}
```

This is the closing brace for the `main` function. It is like de-indenting in Python.

Unlike in Python, aside from global variables, every line of code must be inside a function. In fact, this the same in Python, just that any code not in a function is the equivalent of C's main function.

Now that you have typed that in and understand what each part of it does, save the file  and open the terminal. For Linux, Ctrl + Alt + T, for Mac it's the black app I showed you earlier, and type `cd Desktop`. For Windows, it's the "MSYS" application I showed you, type `cd "/C/Users/<your username here>/Desktop"`, replacing "<your username here>" with your username. Then, you should be able to type `gcc something.c -o something -std=c99`, but if you are on Windows type `gcc something.c -o something.exe -std=c99`. Now if you look on your desktop you will find a file named "something" or "something.exe". This is the program you made! If you double click it you may get no window or a flashing window. That is because our program runs very quickly then closes. The simple way to see the output of your program is to go back into the terminal and type `./something`. You will be greeted by your program, which "Hello World". Congratulations! You wrote your first C program, and hopefully understood the code behind it. In future In will gloss over details mentioned here, such as how to get to you desktop and when to add ".exe" on Windows. You are now ready to move on to the next chapter, which can be found in "03 - I know you know.md". Onwards!
