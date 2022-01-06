# Git CheatSheet

## Aim of this Repository
Using Git and GitHub for the first time can be **very very disturbing and overwhelming**.
I still remember sweating like hell when I first had to use GitHub... I was so scared to "break" something, lose my code, erase my colleagues' work... It was not funny at all.
But as soon as I started to understand how GitHub worked, I could see the power it!

So I will share with you the very basics of Git and GitHub and will explain you how to use it. Hope this will be useful!
(I think it is pretty much the same with GitLab but I am not using it for now.)


## Table of contents
I. [Description](#desc)
II. [Main commands](#main-commands)
    1. [Set up the user information](#title1)
    2. [Initialize your project](#title2)
    3. [Start saving your code and your changes](#title3)
III. [Useful commands](#useful-commands)


## Description <a name="desc"></a>
To better understand the use of Git & GitHub, let's imagine **2 trees**:

Tree 1  | Tree 2
------------- | -------------
on your computer  | on your GitHub

You can work on your computer (Tree 1), your code will be "locally" changed. Nobody will be able to see your work... except you because your files are saved on your computer.

Now, let's imagine that you are willing to work on a great app with some friends. How would you do share your code to your mates? Send your project via WeTransfer? Send it in an e-mail? Oh God, no no no nooooooo!!! You will use Git & GitHub!

What you will need to do is **to send a copy of your code from your computer (Tree 1) to GitHub (Tree 2)**.
So, I hope what I am writing is pretty clear for you.

But why _A TREE_ as an analogy? Simply because you can create _A BRANCH_ to work on, both on your computer (Tree 1) and on GitHub (Tree 2). A branch is **a copy of your project on which you will work on a specific functionality**. While you will be focused on developing a new functionality, another team member will also be able the same on his side.

GitHub will help you save all your codes, share it with your team mates and make sure everyone is on the same page and has the same code.
You will not only be able to work and collaborate with others but also work on your own solo projects and retrieve the code of any project from any computer. So cool  =) , isn't it?


## Install Git on your computer
- [ ] Download Git on your computer <https://git-scm.com/downloads>.
- [ ] Open a terminal (on VS Code or from your computer).
/!\ You don't need to be in any special directory to write the following commands (1. Set up user information). Thanks to the keyword **global**, the configuration will be applied "globally" in your computer.


## Main commands <a name="main-commands"></a>

### 1. Set up the user information <a name="title1"></a>

So you are in your terminal, write the following commands.
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

This set up will be very useful when it comes to team work. You will be able to know who has worked on what.

- You can check the set up with:
```
git config --list
```

### 2. Initialize your project <a name="title2"></a>

- Create a repository on GitHub.
    - Go on [GitHub]<https://github.com> and log in to your account or create a new account if you do not have one yet.
    - Create a new repository:
        - Choose a meaningful name for your repository.
        - Choose the visibility: public or private:
            - Public: your code will be public and everyone will be able to see your code.
            - Private: your code will only be visible by you.
    - When the repository is created, GitHub will display some steps to follow (that I will explain now). So don't close that window!

- Go inside the project you are working on with:
```
_cd_ nameOfYourDirectory
```
cd means _change directory_.

- Initialize Git in at the root of your project
```
git init
```

Have a look at your project, a hidden file named _.git_ just appeared.
If you don't see it, make sure you typed the command in the right directory and make sure hidden files are shown:
-> You are a Mac user? Open your Finder and press simultaneously: **Command + Shift + . (period)**.
-> You are PC user? Type on Google keywords like "Show hidden files Windows/...".

- Link your GitHub repository to your project
    - Go back on the repository you just created on GitHub.
    - Copy and paste in your terminal the command which looks like this one:

```
git remote add origin https://github.com/yourGitHubUsername/nameOfYourRepository.git
```

- Check that your project and your repository are well-connected
```
git remote
```
and the word "origin" must appear in your terminal because you named the link to your repository "origin" (see the previous previous command).

You are now all set to start using GitHub!


### 3. Start saving your code and your changes <a name="title3"></a>

#### 3.1. Working on a branch <a name="title3.1"></a>
- Create a branch (OPTIONAL IF YOU ARE WORKING ALONE ON YOUR PROJECT. Otherwise, go directly [here](#title3.2).)
If you are working alone on your projects, you don't necessarily need to create a branch (= a copy of your project). But if you are working working with other people, that is essential!
    - /!\ Replace only the value _nameOfYourBranch_ and keep the double quotes!
    - Pick a meaningful name like _logInlogOut_.
```
git branch nameOfYourBranch
```

- Go on your new branch:
    - /!\ Replace only the value _nameOfYourBranch_.
```
git checkout nameOfYourBranch
```
What will happen here? It will make a copy of your project in this new branch. All the changes in your code will only affect this "copy"/version of the project.

#### 3.2. Start saving your work on GitHub <a name="title3.2"></a>

What you will do now is "copy" and "paste" your code in the hidden file _.git_.
There are **ALWAYS** 2 steps that go together :
- STEP 1: either "copy" ALL your changes...
```
git add .
```

or

```
git add *
```
These 2 commands do the same. We can imagine that it takes a picture of your project as it is.

- STEP 1: ... or "copy" only ONE file
    - /!\ Replace only the value _nameOfTheFile_.
```
git add nameOfTheFile
```

- STEP 2: "paste" your changes
    - /!\ Replace only the value between the double quotes.
```
git commit -m "description of your commit"
```
This command will "paste" the file.s with your work in the hidden file _.git_.

There are some great content on Internet on how to write concise commits but I would say that it should be short and you should describe the main changes that you have done (ex.: "_CSS button formatted_").

Something I didn't know is that you can do many commits the same day and push everything to GitHub at the end of the day. To do so, you will always follow the 2 steps above and type the following command.

- STEP 3: 



## Useful commands <a name="useful-commands"></a>


- a. How to remove a GitHub link from my project?
    - First, type this command to know the name you gave when you made the link with your GitHub repository (generally "origin").
```
git remote
```

    - Then, type the following command and replace the word "origin" if another word came out after the command above.
    
```
git remote rm origin
```

- b. How to delete a branch locally (on your computer)?
    - /!\ Replace only the value _nameOfYourBranch_.  
```
git branch -d nameOfYourBranch
```

- c. How to switch from a branch to another?
    - /!\ Replace only the value _nameOfYourBranch_.  
```
git checkout nameOfYourBranch
```