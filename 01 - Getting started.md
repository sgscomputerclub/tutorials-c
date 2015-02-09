Welcome! This guide will teach you how to write computer programs in the C programming languge.

First, a little background on C. C was created in 1973 by AT&T, the American equivalent of Telstra.
C is usually considered the fastest around, and usued to write almost everything: from video games to desktop
applications, to the operating systems themselves (i.e. Windows, Mac OS X, Linux, iOS, Android are all mostly
written in C). Many other languages are themselves written in C, such as Python (another language taught at Computer
Club). C is not the youngest language by any means, but it is still the most popular language currently in use,
narrowly edging out Java - a name you may be familiar with because of its frequent annoying updates.

So, now that you are up do date on the C gossip, let's get to learning the language!
Not so fast there, however, as with learning anything, you need the right tools. Unfortunately, when using C this
process changes depending on what operating system you are using. So, what I'm going to do is guide you through each
process, and you can pick whichever one is relevant to you, OK? OK! Here we go:

## Windows
Most of you are probably using Windows, and more still are probably using the school computers, where installing things
is frowned upon by the masters. Fear not! I have a solution. First thing's first, you need a compiler. A compiler is
something that turns what your write (called the "source code", because it's is where the program comes from, and it is
written in code) into the program. On Windows, programs end in ".exe". I am sure you have seen these around
somewhere. No? Have a look in C:\Windows\System32 - but don't touch anything! These are very important files, without
which your computer would not run. All the files marked "Executable" are programs. We are going to be making one of
these. So, the compiler we are going to be using is called "TCC" which stands for "Tiny C compiler". Pretty self
explanatory, isn't it? It is small enough that you can drop it in your account folder so that you can use from any
computer in the school. To download TCC, click
[this link](https://github.com/sgscomputerclub/C-tutorial/raw/master/files/tcc-0.9.26-win32-bin.zip).
You have to extract it (right click -> "Extract All") and then you will have a folder called TCC. Copy this folder to
your account folder (the one in BoysHome) and your done! You successfully installed the compiler.

There is one more step however, and that is to install "make". make (no caps) is a way of simplifying working with C.
It is only one file, so it barely counts as an installation. All you have to do is click
[this link](https://github.com/sgscomputerclub/C-tutorial/raw/master/files/make.exe). This will download "make.exe",
which you can put exactly where you copied the folder "TCC". And you're finsihed, for real this time!

Buuuut, not quite. There is just one more step, I promise. This is the last one. You need an editor, something to help
you write in the C language. I recommend Notepad++, as it is an existing recommendation of the Computer Club,
completely free, and not too shabby an editor.
[Here is a link](http://download.tuxfamily.org/notepadplus/6.7.3/npp.6.7.3.bin.zip), simply right click ->
"Extract All", and copy the resulting folder where you put "TCC" and "make.exe". That's it, your done. Completely for
real. All you need to do to start nodepad++ is open the folder and double click "notepad++.exe" (the ".exe" part
might not show up, but that's OK. That's just Windows trying to not scare off the none technical folk (like you and me
:P). So now go on to the next tutorial, located in the file "02 - Do you see the C?.md".

## Mac
A Mac user, eh? Fine by me, let's get started. The first thing you need to do is download a compiler. A compiler is
something that turns what your write (called the "source code", because it's is where the program comes from, and it is
written in code) into the program. On Mac programs generally do not have a ".something" (called a "file extension"),
unlike ".docx" (Word documents) or ".pptx" (Powerpoint presentation). There are hundreds, if not thousands of these,
litering your computer, all doing very important jobs (like allowing you to read this tutorial :P). Luckily, Apple
supplies a package that contains everything you need to start using C (the Windows users are not so lucky. Poor them.).
Simply open a Terminal window (use spotlight and search "Terminal". It is the black square icon. We will be using it
a lot, so it would be useful to drag it onto your dock) and type `xcode-select --install` then hit enter. A window will
come up, click "Install". And your done! Well, you still have to wait for a bit for it to download, but then your done.

Actually, wait, hold on, there's one more thing you need to install. An editor. It will help you write in the C
language. I recommed TextMate, as it is completely free and a pretty good editor.
[Here is a link](https://api.textmate.org/downloads/release). You might need to extract it, which you can do by double
clicking. You can drag the app to your Applications folder, and you're done! You are ready to go to the next tutorial,
located in "02 - Do you see the C?.md".
