# Git CheatSheet

## Aim of this Repository
Using Git and GitHub for the first time can be **very very disturbing and overwhelming**.
I still remember sweating like hell when I first had to use GitHub. I was so scared to "break" something, lose my code, erase my colleagues' work... It was not funny at all.
But as soon as you understand how GitHub works, you will see the power it!


## Table of contents
1. [Set up the user information](#title1)
2. [Initialize your project](#title2)
3. [Start saving your code and your changes](#title3)


## Description
To better understand how to use GitHub, let's imagine that we see **2 trees**:

Tree 1  | Tree 2
------------- | -------------
on your computer  | on your GitHub

You can work on your computer (Tree 1), your code will be "locally" changed. Nobody will be able to see your work... except you because your files are saved on your computer.

Now, let's imagine that you are working on a great app and that you want to share your code with some friends. How would you do that? Send your project via WeTransfer? Send it in an e-mail? Oh God, no no no nooooooo!!! You will use GitHub!

What you will need to do is **to send a copy of your code from your computer (Tree 1) to GitHub (Tree 2)**.
So, I hope it's pretty clear for you now.

But why _A TREE_ as an analogy? Simply because you can create _A BRANCH_ to work on, both on your computer (Tree 1) and on GitHub (Tree 2). A branch is a copy of your project on which you will work on a specific functionality. While you will work on developing a new functionality, another team member will also be able to work on another task.


With GitHub, you will not only be able to work with others, share your code and get theirs, but also save all your projects and retrieve them on from any computer. So cool, isn't it?


## Install Git on your computer
- [ ] Download Git on your computer <https://git-scm.com/downloads>.
- [ ] Open a terminal (on VS Code or from your computer).
/!\ You don't need to be in any special directory to write the following commands (1. Set up user information). Thanks to the keyword **global**, the configuration will be applied "globally" in your computer.


## Main commands

### 1. Set up the user information <a name="title1"></a>

- Set up your name:
    - /!\ Replace only the values _yourFirstName yourLastName_ and keep the double quotes!
```
git config --global user.name "yourFirstName yourLastName"
```

- Set up your email address:
    - /!\ Replace only the value _yourEmailAddress_ and keep the double quotes!
```
git config --global user.email "yourEmailAddress"
```

- You can check the set up with:
```
git config --list
```

### 2. Initialize your project <a name="title2"></a>

- Go inside your project you are working on with:
```
cd nameOfYourDirectory
```

- Initialize Git in your project
```
git init
```

Have a look in your project, a hidden files named _.git_ will appear.
If you don't see it, make sure you did the command in the right directory and make sure hidden files are shown:
* You are a Mac user? Open your Finder and press simultaneously: **Command + Shift + . (period)**.
* You are PC user? Type on Google keywords like "Show hidden files Windows/...".


### 3. Start saving your code and your changes <a name="title3"></a>
- Create a branch
If you are working alone on your projects, you don't necessarily need to create a branch (= a copy of your project). But if you want to, create a branch by typing:
```
git branch nameOfYourBranch
```




