## Linux commands

**username of current user**
```
whoami
```


**ls**
list files and dir
```
ls 
ls -a
ls -l
```

**tree directory**
```
tree
tree > file.txt
```

**print working directory**
```
pwd
```


**rm: remove file(s)**
```
rm <filename>
rm <filename1> <filename2> ..
```


**remove non empty dir:**
```
rm -r <non-empty dir name>
```


**remove empty dir:**
```
rmdir <empty dir name>
```

**cd: change directory**
/       : root
..      : parent
../..   : multilevel
~       : start from home
```
cd /
cd ..
cd ../..
cd ~
```

**touch:make files**
```
touch <name_filename>
```

**mkdir: make directory**
```
mkdir <dirname>
mkdir <dirname1> <dirname2> ..
```

**mv: move folder**
```
mv <filename> <destination folder name>
mv input.txt test/
```


**pip freeze**
shows all the pip installed packages
```
pip freeze
pip freeze > requirements.txt
```


**sudo**
```
sudo apt install 
sudo apt update
sudo apt upgrade
sudo apt autoremove
sudo apt autoclean
```

**copy**
```
cp <filename1> <name2>
```


**cat**
prints content of a file
```
cat <filename>
cat <filename1> <filename2> ..
```


**echo**
prints argument back on terminal
```
echo “This is test”
```

**>**
```
ls > output.txt
pip freeze > requirement.txt
```

**<**
copies left to right

```
clear
```
clears temimal

```
code .
```
Opens current directory in vs code

```
python
```
opens python shell

```
mysql
```
open mysql shell

```
exit
```
close terminal
