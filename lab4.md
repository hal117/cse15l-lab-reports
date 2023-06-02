# Lab Report 4 by: Harrison Le
---

In today's lab, we had to see how fast we could edit and compile a file through the terminal using vim. There were a couple of steps to do this and many different ways to speed
up the process. The first thing we are going to have to do is generate an ssh key for our ieng6 accounts so that we won't need to enter our password.

---
## Step 1: Logging into remote account and generating SSH Keys
1. The first step is to generate an ssh key using  `ssh cs15lsp23xx@ieng6.ucsd.edu` and then `<enter>`.
2. Then copy the path that is provided after the line "your public key has been saved in".
3. Once you have this saved, log out of the remote account and enter the line of code 
`scp <path to your public SSH key> cs15lsp23xx@ieng6.ucsd.edu:~/.ssh/authorized_keys`

You can now able to log into your remote account without typing your password making the process faster and more efficient.

---
## Step 2: Cloning fork of the repository
After you are successfully logged in, type out

`git clone https://github.com/hal117/lab7.git <Enter>`

This clones the entire repository into your remote account. You should then see something like this.
![Image](lab4gitclone.png)

1. Type out `ls` to check whether lab7 has been successfully clones. This will list all the directories to be able to check if lab7 is there
2. If you see lab7, then change directories into it by typing out `cd lab7 <Enter>`.

---
## Step 3: Run the tests demonstrating they fail
Once you have successfully changed directories, you will run J-unit tests to demonstrate that there are tests being failed by typing out `bash test.sh <Enter>`. You should see 
something like this.

![Image](lab4test.png)

---
## Step 4: Editing the code to fix the failing test

After seeing the errors, we are going to have to fix the code through vim, a text editor program. In the terminal type out `vim ListExamples.java <Enter>` to open the file up in vim.
Once inside Vim here are the exact keys that I pressed.

`$ /index1 <Enter> n n n n n n n n n l l l l l r 2 <Esc> :wq`

`/index1` searches for index1 and clicking `n` will search for each occurence one by one so that we are able to get to the error. 

`l` this key moves the cursor to the right once, we do this to arrive at the point where the bug exists.

`r 2` will replace the index that the cursor is on with 2. (This fixes the bug the most efficiently).

`Esc` puts you into normal mode and `:wq` saves and exits the changes you mode. 

Each of these keystrokes make it easier to navigate through the code and make the changes necessary to fix the bugs within our code. 

Original code would look like this

![Image](lab4codefail.png)

After the fix it would look like this

![Image](lab4codesuccess.png)

---
## Step 5: Running the test to demonstrate they succeed

After fixing the code run a J-unit test to determine success by typing out `bash test.sh <Enter>`.

You should get an image that looks like this 

![Image](lab4bashtestsuccess.png)

---
## Step 6: Commit and push the changes to Github

To commit the changes, you type out `git add ListExamples.java<Enter>` Then `git commit -m Done! <Enter>`.

![Image](Changescommited.png)

Finally, push the resulting changes to your repository by typing out `git push origin` and then log in to your github and enter your password.

And there you go you are all set and have successfuly edited, compiled a file, and push the changes to your github repository!
