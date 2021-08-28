# The command line

You may not have worked with the command line before, but if you continue in computational research, it's destined to be something you spend a lot of time with. And probably - something you'll eventually enjoy using!

## Getting started on the command line

### Using the command line on a Mac

On a Mac, you have very few steps before you're up and running on the command line! All you need to do is to open up `Terminal`. This is a program on MacOS that communicates directly with the computer, so that you can send commands and run programs.

<div class="panel panel-primary">
  <div class="panel-heading">
    <h3 class="panel-title">Terminal Emulators</h3>
  </div>
  <div class="panel-body">
    A terminal emulator is an application that provides text-based commands to the computer, without some graphical user interface (GUI). In the case of your Mac, the terminal emulator takes the place of the clean graphics of the ribbon at the bottom of your screen and the icons arranged on your desktop. Rather than a double click starting a program, you explicitly send the command of what to do to the machine! 
  </div>
</div>

### Using the command line on Windows

In Windows, you can run commands through the **Command Prompt**, which you may have used before. You can access the command prompt using the `Run` application by typing "cmd", or through any search bar via typing "cmd" or "Command Prompt".

However, you'll probably come to an impasse pretty quickly when using the Command Prompt as a terminal emulator. It doesn't have a lot of the features that a program like `Terminal` does, so you'll probably want to download something to make your life easier. One great option for that is `Cmder`, with a download available [here](https://github.com/cmderdev/cmder/releases/download/v1.3.11/cmder.zip), although you might be able to get by with `Powershell` as loaded on your Windows machine.

### Logging on to Poseidon or another HPC system

Once you're using the terminal emulator of your choice, you can start directly executing commands, sending them to your computer without further middlemen. One of the commands you'll probably run the most often on your local computer is `ssh`. `ssh` is typically referred to as "Secure Shell" (though acronyms can be a bit ambiguous in computer science - my favorite example of this is *GNU*, the most famous example of a **recursive acronym**...look it up!). 

What `ssh` is doing is establishing a secure connection to a computer located somewhere else. You can think of `ssh` as a virtual administrator that allows you a pass into a computer that isn't your own. Once you're in, you can run commands on this _new_ computer the same way that you do so locally.

If you're part of the Alexander Lab, you'll be `ssh`-ing into `Poseidon`, the nautically-named compute cluster, which may also be so named due to the undue influence of **P**hysical **O**ceanographers. You can log into `Poseidon` using:

```
ssh <your-username>@poseidon-l1.whoi.edu
```

After the "l", you can place either a 1 or a 2. This just corresponds to the fact that we have two different login nodes ("login-1" and "login-2"). Because I do some work in interactive sessions, it makes it easiest for me to always log in to the same login node. In general, this doesn't matter so much. 

#### Using `vim`

Because the next exercise will involve a little bit of text editing, we'll take a second to talk about `vim`, one of the most popular command-line text editors (and our tool of choice!). It turns out that while the original tool, `vi`, stands for "Visual Improved", `vim` is also a bit of a recursive acronym, standing for "vi improved". 

There is a **lot** that you can do with `vim`. To start out with, we'll just talk about how to open and save.

To open a text file:

```
vim <textfilename.extension>
```

Which will take over your terminal with the canvas of the newly opened document. The document you specify *needn't exist previously* (you can create brand-new documents this way), and it can have *any extension* (including ones that you've never heard of). 

Once you are inside the document, you can type a colon (`Shift+;`) to tell `vim` that you wish to change modes. After you type the colon, your cursor should show up at the bottom of the panel. Next, you can type "i" for `INSERT`. This will change you to editing mode. 

<div class="panel panel-primary">
  <div class="panel-heading">
    <h3 class="panel-title">Exercise: Writing a Document with Vim</h3>
  </div>
  <div class="panel-body">
      Try out <code>vim</code> by creating a document called <code>test.txt</code> in your current working directory. Type a sentence in the document, then close it out.<br>
      When you type and enter <code>ls</code> after editing the document, what do you see? What about with the <code>-l</code> flag?
  </div>
</div>


#### Editing your `bash_profile`

Before you log in, you might want to do something immediately that can be super handy. We can *alias* a command to tell our shell to run a longer command in place of the shorter one that we enter. These aliased commands can be stored in our `bash_profile`. 


### Commands that you'll use most often

Working on the command line is most useful for opening and parsing files quickly and easily. For that reason, we provide a list below of a few of the commands you'll use most frequently when working with the command line. With the exception of the last command on this list, this set of commands is also an excellent group of commands to practice with.

- `ls` - print out the contents of the current directory.
- `cd` - change directories.
- `pwd` - print the current working directory.
- `mkdir` - make a new directory.
- `cp` - copy files between two locations.
- `mv` - move or rename a file or folder.
- `rm` - **warning**: doing this is _permanent_. There is no "Recycle Bin" or "Trash". This removes a file or folder.

<div class="panel panel-primary">
  <div class="panel-heading">
    <h3 class="panel-title">Command Line Flags & Arguments</h3>
  </div>
  <div class="panel-body">
      Every command has some set of <b>flags</b> that you can use in order to achieve the output you're looking for. Among the most useful flags is <code>--help</code> on Linux, which shows you all of the flags that are available for a command.<br>
      As opposed to flags, <i>arguments</i> are inputs that the command expects when you run it. These may be either optional or required, but you'll offer these to the command without any subheading. For example, the <code>cp</code> command <i>requires</i> that you give it two pieces of information, every time you run the command. It needs <i>what you want to copy</i> and <i>where you want to copy it to</i>. If you leave these details out, you'll get an <b>error</b>. The arguments to a command are separated ("delimited") by <b>spaces</b>.
  </div>
</div>

The key connection to make 
