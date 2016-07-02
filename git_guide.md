## Git Guide

Below are the steps that I take to check the health, create/delete branches, push and pull down changes from Github. This stuff can definitely be tricky but you will be amazed at how much of it becomes habit as you do it more and more.

__Where in the World is Carmen Sandiego (errrr… what folder are you in)?__

It important that you are in the right application (code project) folder on your local machine.

Open Terminal and then navigate to the right folder:

    $ cd code/<app name>

or

    $ cd address-bloc

Anytime you need to check where you are, run:

    $ pwd

Anytime you need to see what is in your current folder:

    $ ls

anytime you want to start over and go back to the base folder, run:

    $ cd

To open Atom on a code project folder (aka the one you are currently in), run:

    $ atom .

To see which branch you are on:

    $ git branch

There is a * next to the one you are on. All of them are listed.

To checkout to a new branch:

    $ git checkout -b <new branch name>

To checkout (move) to a branch that already exists

    $ git checkout <existing branch name, like master>

To delete a branch:

     $ git branch -D <existing branch name>

__Pushing and Pulling with Github Remotes__

_Push_

When you are in your app folder, check that you have a remote setup for Github by running

    $ git remote -v

You should see something like:

    origin	git@github.com:Brit200313/alliance.git (fetch)
    origin	git@github.com:Brit200313/alliance.git (push)

this means that when I

    $ git status
    $ git add .
    $ git commit -m ’Some really smart commit message’
    $ git push origin <current branch name I am on>

I will be able to push code to Github successfully.

Do you not see anything when you run “git remote -v”? Do you have the repo created on Github? If you are missing the remote, run this:

    $ git remote add origin https://github.com/kraniasar/<repo name>.git

_Pull_

Once I start collaborating with you on your code, I will push code up that you will then need to pull down (fact: keeping your local copy of code and your Github copy of code as close to the same as possible is an art and something you will be practicing a lot).

So if I updated your “master” branch of your repo, you would then:

    $ git pull origin master

You will see changes come down.

_MERGE CONFLICTS_

When you pull and you see MERGE CONFLICTS, this means that I adjusted a file in a different way than how you changed it locally. No biggie! It just means that you need to open the file in Atom that it is complaining about.

Remove any line from the file that looks like:

     <<<<<<< HEAD

Adjust the code so that between the two branches, the code is right. Go ahead and commit the fixed file (you may have several) back to Github:

    $ git status
    $ git add .
    $ git commit -m ’Some really smart commit message’
    $ git push origin <current branch name I am on>

__The Ultimate Guide to Checking Out Branches and Pushing to Github__

I included some of these skills above but I wanted to make it uber clear.

    $ cd <my app folder>
    $ git branch
    	Which branch? Look for the *
    $ git pull origin <branch name I’m on so my local copy is updated>
    $ git checkout -b <new branch name>
    	Make some codez in Atom and save them.
    $ git status
	Are the files listed that are changed correct?
    $ git add .
    $ git commit -m’ Another smart commit message.’
    $ git push
    	You will get a message like this:

   	fatal: The current branch hello has no upstream branch.
           To push the current branch and set the remote as upstream, use

           git push --set-upstream origin hello

    $ git push --set-upstream origin hello
    $ git checkout master
    $ git branch -D <branch I just pushed from, like “hello”>

Hint: You almost never delete the “master” branch.

### Bloc Specific

__Checkpoint - Starting with Master branch__

    $ git checkout -b checkpoint-number
    ---complete work---
    $ git push origin checkpoint-number
    $ git checkout master
    $ git merge checkpoint-number
    $ git push origin master

__Assignment - Starting with Master branch__

    $ git checkout -b assignment-number
    ---complete work---
    $ git push origin assignment-number

Do not merge assignments back in Master.
