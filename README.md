# Git & Github
### Version control
---
|Git|
|:---:|
|<img src="https://i.pinimg.com/originals/84/9d/ac/849dac53ec386861333e6f24be7ce33f.jpg" width="200" height="150">|
|Free and open source software|
|Distributed version control system|
|Accessible anywhere in the world|
|One of the most common version control version control system available|
|Can also version control images, documents, etc|

---

`SSH protocol` - A method for secure remote login from one computer to another.<br />
`Repository`- The folders of your project that are set up for version control.<br />
`Fork` - A copy of a Repository.<br />
`Pull request` - The process you use to request that someone reviews and approves your changes before they become final.<br />
`Working directory` - A Directory on your file system , include its files and subdirectories, that is associated with a git Repository.<br />

---

# Markdown Syntax

## **HEADING**

# H1 HEADING
## H2 HEADING
### H3 HEADING
#### H4 HEADING
##### H5 HEADING
###### H6 HEADING

---

### Emoji

:point_right:<br />

#### [Emoji Cheatsheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

#### [Emoji Cheatsheet](https://gist.github.com/rxaviers/7360908)

---

### Bullet point
- Always synchronize your branches before starting any work on your own
- Avoid having very large changes that modify a lot of different things
- when working on a big change, it makes sense to have a separate feature branch
- Regularly merge changes made on the master branch back onto the feature branch
- Have the latest version of the project in the master branch, and the stable version of the project on a separate branch
- You shouldn't rebase changes that have been pushed to remote repos

---

### Number points
1.

>"***You can verify the data you get back out is the exact same data you put in.***" <br />
> -Linus Torvalds

---

### Blockquote

<blockquote>

~~~
a

b

c

~~~

</blockquote>

~~~
This is good feature in Github
~~~

```Python
   def greeting(name):
       print("Hello, " + name)
   ```

   ```HTML
   <!DOCTYPE html>
   <html lang="en" dir="ltr">
     <head>
       <meta charset="utf-8">
       <title></title>
     </head>
     <body>
       <p> how are you doing</p>
     </body>
   </html>
   ```

   ```C
   #include<stdio.h>
   int main(){
     int a = 5;
     printf("how are you doing %d",a);
     return 0;
   }
   ```

   ```C++
   #include<iostream>
   int main(){
     int a = 5;
     cout<<"how are you doing "<<a<<endl;
     return 0;
   }
   ```

   ---

### Comments

[comment]: <> (This is a comment, it will not be included)
[comment]: <> (in  the output file unless you use it in)
[comment]: <> (a reference style link.)

[//]: <> (This is also a comment.)

[//]: # (This may be the most platform independent comment)


<!---just--->

---

### Buttons using \<kbd>Esc\<kbd>

<kbd>Esc</kbd>

<kbd>Enter</kbd>

---

### Links

[This is the official syntax page](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax)


[online markdown editor](https://dillinger.io/)


[Resources to learn Git](https://try.github.io/)

---

### some of .gitignore extension are :-

# Compiled source # <br />
################### <br />
*.com <br />
*.class <br />
*.dll <br />
*.exe <br />
*.o <br />
*.so <br />

# Packages # <br />
############ <br />
# it's better to unpack these files and commit the raw source <br />
# git has its own built in compression methods <br />
*.7z <br />
*.dmg <br />
*.gz <br />
*.iso <br />
*.jar <br />
*.rar <br />
*.tar <br />
*.zip <br />

# Logs and databases # <br />
###################### <br />
*.log <br />
*.sql <br />
*.sqlite <br />

# OS generated files # <br />
###################### <br />
.DS_Store <br />
.DS_Store? <br />
._* <br />
.Spotlight-V100 <br />
.Trashes <br />
ehthumbs.db <br />
Thumbs.db <br />

---

### Fix:  How to resolve error 403 in github <br />
i.e. on pushing to git returning error atom 403 fatal: HTTP request failed

To remove old git hub account credential go to control panel -> User account -> credential manager -> manage windows credential then select account to remove -> remove -> Yes

alternate: \$git remote set-url origin https://\<username>@github.com/\<username>(path)/\<repo>.git

replace \<username> with your github username, path to exact path to your
current working repository

---


Common hash functions include MD5, SHA-1, SHA-256, and SHA-512. These hash functions use complex mathematical algorithms. The hashed value is simply there for comparison. For example, after downloading a file, the user can verify the integrity of the file by comparing the hash values from the source with the one generated by any hash calculator.

---

# All git commands

* git --version <br />
* git --help <br />
* git config --global user.name "<USER_NAME>" <br />
* git config --global user.email "<USER_EMAIL>" <br />
* git config --list <br />
* git init <br />
* git checkout -b main <br />
* git status <br />
* git add . <br />
* git add -A <br />
* git commit <file_name> -m "<Comments>" <br />
* git commit -m "<Comments>" <file_name> <br />
* git commit -a -m "<comments>" <br />
* git log <br />
* git log --oneline --graph <br />
* git diff <br />
* git clone <path> <br />
* git pull <br />
* git request-pull -p origin/main . <br />
* git pull <remote_name> main <br />
* git init --bare <br />
* git symbolic-ref HEAD refs/heads/main <br />
* git branch --set-upstream-to origin/main <br />
* git diff origin -- <file_name> <br />
* git stash <br />
* git stash pop <br />
* zip -r Cats.zip Cats <br />
* download Cats.zip <br />
* git branch <branch_name> <br />
* git checkout <branch_name> <br />
* git checkout -b <branch_name> -> combination of git branch and git checkout <br />
* git merge --ff-only <branch_name> -> --ff-only means fast forward merge <br />
* git pull --rebase <br />

---

# Fix simple mistake

* rm <file_name> <br />
  * git checkout -- <file_name> <br />
* git rm <file_name> <br />
  * git reset HEAD <file_name> <br />
  * git checkout -- <file_name> <br />
* git revert --no-edit HEAD <br />
* git commit --amend --no-edit <br />
* git reset --hard HEAD^ <br />
  * --mixed -> resets index but not working tree <br />
  * --soft -> moves HEAD only, and it leaves both index and working tree unchanged. <br />
  * --hard -> reset changes both index and working tree to match specified commit <br />
<details>
<summary> To undo git reset --hard HEAD^ then perform below 2 steps </summary>

  * git reflog <br />
    * git reset --hard <discarded_commitid> <br />

</details>

---
