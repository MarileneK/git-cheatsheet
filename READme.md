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

You can work on your computer (Tree 1), your code will be "locally" changed. No one else would be able to see your work... except you because your files are saved on your computer.

Now, let's imagine that you are working on a great app and that you want to share your code with some friends. How would you do that? Send your project via WeTransfer? Send it in an e-mail? Oh God, no no no nooooooo!!! You will use GitHub!

What you will need to do is **to send a copy of your code from your computer (Tree 1) to GitHub (Tree 2)**.
So, I hope it's pretty clear for you now.

But why __A TREE__ as an analogy? Simply because you can create __BRANCHES__ to work on, both on your computer (Tree 1) and on GitHub (Tree 2). A branch is a copy of your project on which you will work on a specific functionality. 



## Set Up
- [ ] Download Git on your computer (https://git-scm.com/downloads).
- [ ] Open a terminal (on VS Code or from your computer).
- /!\ You don't need to be in any special directory to write the following commands (1. Set up user information). Thanks to the keyword **global**, the configuration will be applied "globally" in your computer.


## Main commands

1. Set up user information
### Set up your name
**git config --global user.name** "_yourFirstName yourLastName_"

### Set up your email address
**git config --global user.email** "_yourEmailAddress_"

# You can check the set up with:
**git config --list**

- [ ] Go inside your project with:
**cd** _nameOfYourDirectory_.

# Initialize Git in your project
**git init**



#



