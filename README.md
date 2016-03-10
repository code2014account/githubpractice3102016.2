```# githubpractice3102016.2

matt24ray:~/workspace $ git config --global user.name "Matt"
matt24ray:~/workspace $ git config --global user.email mwray@gmail.com
matt24ray:~/workspace $ git config --global color.ui true
matt24ray:~/workspace $ git config --global push.default simple
matt24ray:~/workspace $ cat ~/.gitconfig
[user]
        name = Matt
        email = mwray@gmail.com
[core]
    editor = nano
    whitespace = off
    excludesfile = ~/.gitignore
[advice]
    statusuoption = false
[color]
        ui = true
[push]
        default = simple
matt24ray:~/workspace $ cd ~
matt24ray:~ $ mkdir -p bloc/shopping_cart
matt24ray:~ $ cd bloc/shopping_cart
matt24ray:~/bloc/shopping_cart $ pwd
/home/ubuntu/bloc/shopping_cart
matt24ray:~/bloc/shopping_cart $ touch apple.txt
matt24ray:~/bloc/shopping_cart $ ls
apple.txt
matt24ray:~/bloc/shopping_cart $ git init .
Initialized empty Git repository in /home/ubuntu/bloc/shopping_cart/.git/
matt24ray:~/bloc/shopping_cart (master) $ ls -al
total 12
drwxr-xr-x 3 ubuntu ubuntu 4096 Mar 10 18:09 ./
drwxr-xr-x 3 ubuntu ubuntu 4096 Mar 10 18:09 ../
drwxr-xr-x 7 ubuntu ubuntu 4096 Mar 10 18:09 .git/
-rw-r--r-- 1 ubuntu ubuntu    0 Mar 10 18:09 apple.txt
matt24ray:~/bloc/shopping_cart (master) $ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        apple.txt

nothing added to commit but untracked files present (use "git add" to track)
matt24ray:~/bloc/shopping_cart (master) $ git add apple.txt
matt24ray:~/bloc/shopping_cart (master) $ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   apple.txt

matt24ray:~/bloc/shopping_cart (master) $ touch banana.txt
matt24ray:~/bloc/shopping_cart (master) $ ls
apple.txt  banana.txt
matt24ray:~/bloc/shopping_cart (master) $ git commit -m "Create the apple.txt file"
[master (root-commit) bd241dc] Create the apple.txt file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 apple.txt
matt24ray:~/bloc/shopping_cart (master) $ add banana.txt
bash: add: command not found
matt24ray:~/bloc/shopping_cart (master) $ git commit -m "Git Checkpoint Assignment."
On branch master
Untracked files:
        banana.txt

nothing added to commit but untracked files present
matt24ray:~/bloc/shopping_cart (master) $ touch banana.txt
matt24ray:~/bloc/shopping_cart (master) $ ls
matt24ray:~/bloc/shopping_cart (master) $ git commit -m "Git Assignment."
[master b077e1c] Git Assignment. 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 banana.txt
matt24ray:~/bloc/shopping_cart (master) $ git log
commit b077e1c1a608ef2eabae68df54161868db4e1086
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:13:27 2016 +0000

    Git Assignment.

:...skipping...
commit b077e1c1a608ef2eabae68df54161868db4e1086
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:13:27 2016 +0000

    Git Assignment.

commit bd241dc05e21159cdad8e32f39364e89248893f2
:...skipping...
commit b077e1c1a608ef2eabae68df54161868db4e1086
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:13:27 2016 +0000

    Git Assignment.

commit bd241dc05e21159cdad8e32f39364e89248893f2
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:10:38 2016 +0000
:...skipping...
commit b077e1c1a608ef2eabae68df54161868db4e1086
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:13:27 2016 +0000

    Git Assignment.

commit bd241dc05e21159cdad8e32f39364e89248893f2
Author: Matt <mwray@gmail.com>
Date:   Thu Mar 10 18:10:38 2016 +0000

    Create the apple.txt file
~
~
~
~
~
matt24ray:~/bloc/shopping_cart (master) $ ~
bash: /home/ubuntu: Is a directory
matt24ray:~/bloc/shopping_cart (master) $ cd ~
matt24ray:~ $ mkdir shopping_cart_assignment
matt24ray:~ $ git checkout master
fatal: Not a git repository (or any of the parent directories): .git
matt24ray:~ $ git init
Initialized empty Git repository in /home/ubuntu/.git/
matt24ray:~ (master) $ cd ~
matt24ray:~ (master) $ cd shopping_cart_assignment
matt24ray:~/shopping_cart_assignment (master) $ git checkout master
error: pathspec 'master' did not match any file(s) known to git.
matt24ray:~/shopping_cart_assignment (master) $ git checkout -b shopping_cart_assignment
Switched to a new branch 'shopping_cart_assignment'
matt24ray:~/shopping_cart_assignment (shopping_cart_assignment) $ cd ~
matt24ray:~ (shopping_cart_assignment) $ git rm apple.txt
fatal: pathspec 'apple.txt' did not match any files
matt24ray:~ (shopping_cart_assignment) $ cd ~
matt24ray:~ (shopping_cart_assignment) $ echo $HOME
/home/ubuntu
matt24ray:~ (shopping_cart_assignment) $ ..
matt24ray:/home $ ..
matt24ray:/ $ ..
matt24ray:/ $ git rm apple.txt
fatal: Not a git repository (or any of the parent directories): .git
matt24ray:/ $ cd bloc
bash: cd: bloc: No such file or directory
matt24ray:/ $ cd home
matt24ray:/home $ cd bloc
bash: cd: bloc: No such file or directory
matt24ray:/home $ cd bloc_shopping_cart
bash: cd: bloc_shopping_cart: No such file or directory
matt24ray:/home $ cd ~
matt24ray:~ (shopping_cart_assignment) $ cd bloc
matt24ray:~/bloc (shopping_cart_assignment) $ cd bloc/shopping_cart
bash: cd: bloc/shopping_cart: No such file or directory
matt24ray:~/bloc (shopping_cart_assignment) $ git remove apple.txt
git: 'remove' is not a git command. See 'git --help'.

Did you mean this?
        remote
matt24ray:~/bloc (shopping_cart_assignment) $ git rm apple.txtfatal: pathspec 'apple.txt' did not match any files
matt24ray:~/bloc (shopping_cart_assignment) $ ls
shopping_cart/
matt24ray:~/bloc (shopping_cart_assignment) $ ..
matt24ray:~ (shopping_cart_assignment) $ ..
matt24ray:/home $ cd bloc
bash: cd: bloc: No such file or directory
matt24ray:/home $ ..
matt24ray:/ $ ..
matt24ray:/ $ ..
matt24ray:/ $ echo $HOME
/home/ubuntu
matt24ray:/ $ cd bloc/shopping_cart
bash: cd: bloc/shopping_cart: No such file or directory
matt24ray:/ $ ..
matt24ray:/ $ cd home
matt24ray:/home $ ..
matt24ray:/ $ cd ~
matt24ray:~ (shopping_cart_assignment) $ cd bloc
matt24ray:~/bloc (shopping_cart_assignment) $ cd shopping_cartmatt24ray:~/bloc/shopping_cart (master) $ ls
apple.txt  banana.txt
matt24ray:~/bloc/shopping_cart (master) $ git rm apple.txt
rm 'apple.txt'
matt24ray:~/bloc/shopping_cart (master) $ touch lettuce.txt
matt24ray:~/bloc/shopping_cart (master) $ git diff > lettuce.txt
matt24ray:~/bloc/shopping_cart (master) $ git init
Reinitialized existing Git repository in /home/ubuntu/bloc/shopping_cart/.git/
matt24ray:~/bloc/shopping_cart (master) $ git add lettuce.txt
matt24ray:~/bloc/shopping_cart (master) $ git commit -m "Add lettuce.txt"
[master 4724344] Add lettuce.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename apple.txt => lettuce.txt (100%)
matt24ray:~/bloc/shopping_cart (master) $ cat lettuce.txt
matt24ray:~/bloc/shopping_cart (master) $ 
```
