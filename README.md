# Git CheatSheet

## Aim of this Repository
Using Git and GitHub for the first time can be **very very disturbing and overwhelming**.
I still remember sweating like hell when I first had to use GitHub... I was so scared to "break" something, lose my code, erase my colleagues' work... It was not funny at all.
But as soon as I started to understand how GitHub worked, I could see the power of it!

So I will share with you the very basics of Git and GitHub and will explain you how to use it. Hope this will be useful and helpful!
(I think it is pretty much the same with GitLab but I am not using it for now.)

*P.S.: this repo is an ongoing process and I will do my best update it.*

<hr>

## Table of contents
I. [Description](#desc)<br />
II. [Install Git on your computer](#git)<br />
III. [Main commands](#main-commands)<br />
  1. [Set up the user information](#title1)<br />
  2. [Initialize your project](#title2)<br />
  3. [Start saving your code and your changes](#title3)<br />
   3.1. [Working on a branch](#title3.1)<br />
   3.2. [Start saving your work on GitHub](#title3.2)<br />

IV. [VERY Useful commands](#useful-commands)<br />

<hr>

## I. Description <a name="desc"></a>
To better understand the use of Git & GitHub, let's imagine **2 trees**:

Tree 1  | Tree 2
------------- | -------------
on your computer  | on your GitHub

You can work on your computer (Tree 1), your code will be "locally" changed. Nobody will be able to see your work... except you because your files are saved on your computer.

Now, let's imagine that you are willing to work on a great app with some friends. How would you do share your code to your mates? Send your project via WeTransfer? Send it in an e-mail? Oh God, no no no nooooooo!!! You will use Git & GitHub!

What you will need to do is **to send a copy of your code from your computer (Tree 1) to GitHub (Tree 2)**.
So, I hope what I am writing is pretty clear for you.

But why _A TREE_ as an analogy? Simply because you can create _A BRANCH_ to work on, both on your computer (Tree 1) and on GitHub (Tree 2). A branch is **a copy of your project on which you will work on a specific functionality**. While you will be focused on developing a new functionality, another team member will also be able on another functionality on his computer.

GitHub will help you save all your codes, enable you to share it with your team mates and make sure everyone is on the same page and has the same code as you.
You will not only be able to work and collaborate with others, but also work on your own solo projects and retrieve the code of any project from any computer. So cool  =) , isn't it?

<hr>

## II. Install Git on your computer <a name="git"></a>
- [ ] Download Git on your computer <https://git-scm.com/downloads>.
- [ ] Open a terminal (on VS Code or from your computer).
/!\ You don't need to be in any special directory to write the following commands (1. Set up user information). Thanks to the keyword **global**, the configuration will be applied "globally" in your computer.

<hr>

## III. Main commands <a name="main-commands"></a>

### 1. Set up the user information <a name="title1"></a>

So, you are in your terminal, write the following commands.
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
    - /!\ Replace only the value _nameOfYourDirectory_.
```
cd nameOfYourDirectory
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
- Create a branch (OPTIONAL IF YOU ARE WORKING ALONE ON YOUR PROJECT. Otherwise, go directly [here](#title3.2).)<br />
If you are working alone on your project, you don't necessarily need to create a branch (= a copy of your project). But if you are working working with other people, that is essential! You will then do the following command:
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
What will happen here? It will make a copy of your project in this new branch. All the changes in your code will only affect this "copy"/"version" of the project.

Yay! You can now start working on your branch! Then, as soon as you are done with coding a feature, you can go the next part (3.2.).

ATTENTION ATTENTION ATTENTION: if you've just created a branch locally on your computer (Tree 1), it won't be reflected in your GitHub repository (Tree 2). Vice versa: creating a branch on GitHub (Tree 2) won't be reflected locally on your computer (Tree 1)! Your computer and GitHub are 2 separate trees.

#### 3.2. Start saving your work on GitHub <a name="title3.2"></a>

What you will do now is "copy" and "paste" your code in the hidden file _.git_.
You will **ALWAYS** have to follow those 2 steps, they are like *TWINS*:

##### STEP 1: either "copy" ALL your changes...

```
git add .
```

or (these 2 commands do the same))

```
git add *
```

##### STEP 1: ... or "copy" only ONE file
- /!\ Replace only the value _nameOfTheFile_.
```
git add nameOfTheFile
```

##### STEP 2: "paste" your changes
- /!\ Replace only the value between the double quotes.
```
git commit -m "description of your commit"
```
This command will "paste" the file.s with your work in the hidden file _.git_.

There are great content on Internet on how to write concise commits but I would say that it should be short and you should describe the main changes that you have done (ex.: "_CSS button formatted_").

Something I didn't know is that you can do as many commits as you wish the same day and do ONLY ONE push (see Step 3) at the end of the day. To do so, you will always follow the 2 steps above and type the following command (Step 3).

##### STEP 3: "paste"/push your work on GitHub

Now, you will push your code to your repository on GitHub. It means that you will save the latest version of your code on GitHub (Tree 2).<br />
You will need to decide where you want to push/save it: to your *master branch on GitHub* (the KING ONE) or *to a new branch on GitHub that you will create* or *to an existing branch on GitHub*?

ATTENTION ATTENTION ATTENTION: if you've just created a branch locally on your computer (Tree 1), it won't be reflected in your GitHub repository (Tree 2). Vice versa: creating a branch on GitHub (Tree 2) won't be reflected locally on your computer (Tree 1)! Your computer and GitHub are 2 separate trees.

###### Case 1: push to master
If you want to push/paste your code to the master branch of your repository GitHub (Tree 2), you will do so:
```
git push origin master
```
Have a look at your repository on GitHub in "Code" section and your commit should appear! *You can then keep on working calmly and peacefully with GitHub...*

If for some mysterious reasons, an error message appears on your terminal and tells you that you are "behind some commits"... *DO NOT PANIC!!!* It might be because your local code (before the last changes you made) is different from the code on your repository. So, you will need to get/pull the code first (= retrieve the last version of the code on GitHub)) with this command:

```
git pull origin master
```

Then, re-do the "git push" to the master like shown above.


###### Case 2: push to a new branch on GitHub (Tree 2)
If you want to push/paste your code (Tree 1) to a new branch on your repository GitHub (Tree 2), you will push NOT TO "MASTER" BUT to a new branch on GitHub (Tree 2), like this:
    - /!\ Use the same name as your local branch, this will make your life easier:
```
git push origin nameOfYourLocalBranch
```

You might need to push your code on a specific branch on GitHub (created by someone else for instance). You will then need to adjust the name of the branch in your command:
```
git push origin nameOfTheBranchOnGitHub
```

If an error message appears on your terminal and tells you that you are "behind some commits"... *DO NOT PANIC!!!* It might be because some of your colleagues pushed their codes since you last "pull request", meaning that your code is different from theirs. So, you will need to get/pull their code first (= retrieve the last version of the code on GitHub) with this command:

```
git pull origin master
```
or (if you need to retrieve the code from another branch on GitHub, replace the _nameOfTheBranch_)
```
git pull origin nameOfTheBranch
```

Then, re-do the git "push". Then, you should be fine!

The latest version of your code is now on GitHub. If you pushed your work on a branch on GitHub and if you or your team mates are happy with your code, you will need to *merge* it to the main code. You have 2 options.

###### Option 1: merge locally your branch

In your terminal, switch back to the master branch (Tree 1).
```
git checkout master
```

Then, merge the branch you were working on with the master:
```
git checkout nameOfYourBranch
```
And it's done!

If necessary, you can delete your branch by doing so:
```
git delete -d nameOfYourBranch
```

... and create a new branch: 
```
git branch nameOfMyNewBranch
```

And don't forget to go on your new branch to work on another feature!
```
git checkout nameOfMyNewBranch
```

###### Option 2: merge your branch on GitHub

Go on the repository on GitHub.
_(WORK IN PROGRESS)_


<hr>

## IV. VERY Useful commands <a name="useful-commands"></a>

_(WORK IN PROGRESS)_

### How to remove a GitHub link from my project?

- First, type this command to know the name you gave when you made the link with your GitHub repository (generally "origin").
```
git remote
```

- Then, type the following command and replace the word ```origin``` if another word came out after the command above.

```
git remote rm origin
```

### How to delete a branch locally (on your computer)?
- /!\ Replace only the value _nameOfYourBranch_.  
```
git branch -d nameOfYourBranch
```

### How to switch branches?
- /!\ Replace only the value _nameOfYourBranch_.  
```
git checkout nameOfYourBranch
```
