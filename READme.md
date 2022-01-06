# Git CheatSheet

## Aim of this Repository
Using Git and GitHub for the first time can be **very very disturbing and overwhelming**.
I still remember sweating like hell when I first had to use GitHub. I was so scared to "break" something, lose my code, erase my colleagues' work... It was not funny at all.
But as soon as you understand how GitHub works, you will see the power it!


## Description
To better understand how to use GitHub, let's imagine that we see **2 trees**:

    Tree 1       |      Tree 2
-----------------|-----------------
on your computer |  on your GitHub

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

You can work on your computer (Tree 1), your code will be "locally" changed. Nobody will be able to see your work... except you because your files are saved on your computer.

Now, let's imagine that you are working on a great app and that you want to share your code with some friends. How would you do that? Send your project via WeTransfer? Send it in an e-mail? Oh God, no no no nooooooo!!! You will use GitHub!

What you will need to do is **to send a copy of your code from your computer (Tree 1) to GitHub (Tree 2)**.
So, I hope it's pretty clear for you now.

But why _A TREE_ as an analogy? Simply because you can create _BRANCHES_ to work on, both on your computer (Tree 1) and on GitHub (Tree 2). A branch is a copy of your project on which you will work on a specific functionality. 


With GitHub, you will not only be able to work with others, share your code and get theirs, but also save all your projects and retrieve them on from any computer. So cool, isn't it?



## Set Up
- [ ] Download Git on your computer (https://git-scm.com/downloads).
- [ ] Open a terminal (on VS Code or from your computer).
- /!\ You don't need to be in any special directory to write the following commands (1. Set up user information). Thanks to the keyword **global**, the configuration will be applied "globally" in your computer.


## Main commands

1. Set up user information
### Set up your name
**git config --global user.name** "_yourFirstName yourLastName_"

/!\ Replace only the values _yourFirstName yourLastName_ and keep the double quotes!

### Set up your email address
**git config --global user.email** "_yourEmailAddress_"

/!\ Replace only the value _yourEmailAddress_ and keep the double quotes!

### You can check the set up with:
**git config --list**

2. Initialize your project
### Go inside your project with:
**cd** _nameOfYourDirectory_

### Initialize Git in your project
**git init**

Have a look in your project, a hidden files named _.git._ will appear.
If you don't see it, it is probably because you need to "show" them.
* You are a Mac user? Open your Finder and press simultaneously: Command + Shift + . (period) 
* You are PC user? 




#



