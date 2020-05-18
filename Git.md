## Git Cheet Sheet

**Git: configurations**
```git
git config --global user.name "firstname lastname"
git config --global user.email "your-email@email-provider.com"
git config --global color.ut true
git config --list
```


**Git: start a repository**
```git
git init
git status
```


**Git: staging files**
```git
git add <filename>
git add <filename1> <filename2> <filename3>
git add .
git add *
git add -all
git add -A
git rm --cached <filename>
git reset <filename>
```


**Git: committing to a repository**
```git
git commit -m "<message comment here>"
git reset --soft HEAD^
git commit --amend -m <enter message>
```


**Git: pulling and pushing from and to repository**
```git
git remote add origin <link>
git push -u origin master
git clone <clone>
git pull
```