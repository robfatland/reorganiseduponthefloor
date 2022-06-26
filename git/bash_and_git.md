## A quick rundown on `bash`

`bash` is the Bourne Again Shell. A shell is a terminal where you type UNIX commands,
usually with arguments to specify what you want, and the shell goes and does that 
and gives you any feedback and leaves you with the prompt again. This command/response
pattern is interactive. The commands are actually programs that are part of the 
operating system. Which is UNIX. Or nowadays an improved version of UNIX called Linux.


Bourne was some chap who wrote a shell; and I think it was improved upon to a version
two which was called Bourne Again. Hence Bourne Again Shell. Hence `bash`. 


What about automatically running a lot of commands? Yes, we can do that. Edit a 
file called `go.script` and then save it. From the command line issue `source go.script`
and the shell will try and execute those commands in sequence.


There are three other things to mention. 


First, the directory structure is of course a big tree; and we start in our
home directory, something like `/users/kilroy` or `/home/kilroy`. Find out
where you are by printing the working directory: `pwd`. There is a little spring
attached to your back belt loop that goes to your home directory. So go
somewhere that is not your home directory by changing directory to somewhere
else: `cd somewhere/else`. Now say `pwd`. Now say `cd` and just hit `Enter`. 
Now say `pwd` and notice the little spring has pulled you back home. 


Second, you can list files with `ls` but you can list *all* the files with
`ls -al`. Do this in your home directory and notice there is a file called
`.bashrc`. Because it starts with a period it is considered a system file 
so it does not get listed by the vanilla `ls` command. This is a script file
that runs when you log in and configures things for you, including what your
prompt looks like. You can edit it and run it again to effect your changes
by saying `source .bashrc`. If you are interested in a bit of customizing
you can ask me about the `greenandblack` repo. But anyway sometimes these
'starts with a period' files are actually directories; and they can be 
surprisingly big. And *sometimes* they can even hold secret things like
github *login credentials*. So it is important to maintain a sense of discretion
when you copy a repo from GitHub to a local clone. Make sure nothing winds 
up in your repo directory that should not be there; because when you run 
`git push` to copy your changes back to your safe copy, there your credentials
will be in public view on GitHub. You would think that nobody will ever notice
because who goes around looking at billions of repos all the time. But the 
answer is: Bots do. And they scrape credentials and do whatever naughty things
they were programmed to do. So that's an introduction to the purpose and perils
of your home directory. 


Third, each file and each directory has an access permission string associated
with it. You will see this when you issue `ls -al`. There are three fields,
each consisting of three values. There is also a leading character that tells
you if a file is actually a directory. Here is an example:


```
-rwxrwxrwx 1 kilroy kilroy  2668 Apr 19 15:50 terraform.tf
drwxr-xr-x 1 kilroy kilroy  4096 May 16 19:16 miniconda3
```


The upper file permission field starts with `-`. This means it is a file. Then is 
has `rwx`, then `rwx` again, and then `rwx` again. The first one means that you,
the User have read/write/execute permissions on this file. The second trio refers
to people in the same user Group as you. The third trio refers to Others; anyone
using this computer. This is really a holdover from when systems were commonly shared
by larger groups of people. However it is good to know what this means; and you can
modify the permission string for any file you own using the change mode command, `chmod`.


By the way the lower file
begins with `d`. This means it is a directory. Notice that in this case the User can
read/write/execute; but both Group and Other users can only read and execute. They 
cannot write changes to this directory. 


## Editors


Many use `EMACS` or similar "light" versions of this popular editor. The pattern seems to be 
that they sacrifice a little bit of real-estate at the bottom of the screen to present a ctrl-key
menu for save/exit/etcetera options. This is one good path to having the means to edit text files.


Another approach is to learn the peculiar syntax of the `vi` editor. `vi` has been improved so 
now it is called `vim`. It has both an `<insert>` and an `<escape>` mode so one has to develop
a little mental bit for which one you are currently in. When in escape mode you can move your 
cursor around or issue terse little commands that appear at the bottom of the screen. This is 
the sort of thing you would learn to do in an afternoon on a "learn vi" interactive website. 


I was introduced to `vi` so that is what I use. I think it is pretty amusing although sometimes
the feature creep has made it look very cluttered; so I've put a little effort into retro-simplification.
Again that is in my `greenandblack` repo. 

## linux commands

- `cd` to change directory`
- `pwd` print working directory
- `chmod` change permissions
- `ls` list directory contents; `ls -al` for a comprehensive view
- `rm file` to delete `file`
- `rmdir dir` to delete a (necessarily empty) directory
- `less file` to view the contents of `file` interactively (remembering that less is more)
- `more file` as an older version of `less`
- `cp a b` to copy file `a` to a new file called `b`
- `cat file1 >> file2` copies the contents of file1 onto the end of file2
- `grep mohawk file1.txt` searches for the occurrence of string `mohawk` in `file1.txt`
    - You can also open the file in an editor and search for `mohawk`; a little more time consuming
- `df .` prints the volume of the file system
- `du -h -d1` prints the volume of each directory in the current directory
    - This is a great sanity check to see if any directories have grown monstrous huge
    - You can also use it to descend into a directory and sort out where specifically monsters live
- `history` lists your recent commands in chronological order, conveniently numbering them
- `!54` re-issues command number 54 from your history
- `!!` re-runs the last command you gave


By the way: Certain text files can be edited (with care). For example `.bashrc`. But other files
can be very prone to ***breaking*** when edited as they were not intended for editor-based
modification. A good example is an IPython or Jupyter notebook file (file extension `.ipynb`). 


## git


`git clone https://github.com/robfatland/greenandblack.git`

Issue this from (say) your home directory: The clone will appear as subdirectory `greenandblack`.
It is important to emphasize ...
