## first you need to create a ssh key
### 1.open your sourcetree and select "操作" then open terminal
### 2.create your ssh key

``` git command
$ cd ~/.ssh
# if not such directory, try to use 'mkdir .ssh'
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Owner/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Owner/.ssh/id_rsa.
Your public key has been saved in /c/Users/Owner/.ssh/id_rsa.pub.
The key fingerprint is:
# press enter 3 times
SHA256:svcwwlXyHMlBJbtf+uR4K+BZyGcOvGCfU+5K0SLqyXs Owner@DESKTOP-JCCBGFM
The key's randomart image is:
+---[RSA 3072]----+
|         .+..    |
|         . =     |
|        . *      |
|         = +     |
|      . So*.. .  |
|     . =o.*+=o   |
|      =.++.&o .  |
|     o +E=B +=.  |
|      =o  o+oo+. |
+----[SHA256]-----+

```

### 3.set your github's ssh key

open  **~/.ssh/id_rsa.pub** with editor and copy that contents .

paste to your github→setting→ssh→add 

### 4.clone your repository(first you need to create one at github.com)

``` git command
$ git clone git@github.com:kenkokuLife/testRepo.git
Cloning into 'testRepo'...
The authenticity of host 'github.com (13.114.40.48)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com,13.114.40.48' (RSA) to the list of known hosts.
warning: You appear to have cloned an empty repository.
# when your clone a empty repository
```

### 5.tell MINGW64 who youre

``` git command
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

### 6.create a test file

``` git command
$ dir
testRepo
# comfirm you cloned the repository
vi README.md
# create a markdown file and edit that(press i to edit and press shift+zz to save it)
$ cat README.md
this is test file...
# when your edit "this is test file..."
```

### 7.add your changes to index

``` git command
$ git add README.md
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   README.md
# cofirm index
```

### 8.start your first commit!

``` git command
$ git commit -m "first commit"
[master (root-commit) 2e643d0] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```

### 9.push your commit to reflect master data

``` git command
$ git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 227 bytes | 75.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:kenkokuLife/testRepo.git
 * [new branch]      master -> master
```

### 10.goto your github and to see the miracle

you did!

| [README.md](https://github.com/kenkokuLife/testRepo/blob/master/README.md) | [first commit](https://github.com/kenkokuLife/testRepo/commit/2e643d0223bf7f2531471bac0487c18d39a0d48a) | 31 minutes ago |
| ------------------------------------------------------------ | ------------------------------------------------------------ | -------------- |
|                                                              |                                                              |                |

## 



###  README.md



this is test file...

