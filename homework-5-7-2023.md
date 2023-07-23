Create a folder called desktop. Create 2 folders and 2 files inside it . Delete 1 file and 1 folder. Delete Desktop folder.

```
ls
mkdir desktop
ls
cd desktop
mkdir folder1 folder2
ls
touch file1 file2
ls
rm file2
ls
rmdir folder2
ls
cd ..
pwd
rm -rv desktop/
```

Create Regex folder, Create linux file in it Copy linux file in backup folder.

```
pwd
ls
mkdir regex backup
ls
cd regex/
touch linux
ls
cp linux /home/shrutic29933/backup/
ls
cd ../backup/
```

Create learning folder -> create regex folder -> Create file.txt
Copy that file in /home/shruti

```
ls
cd ..
pwd
mkdir learning
ls
cd learning/
mkdir regex
ls
cd regex/
touch data.txt
ls
cp data.txt /home/shrutic29933/
```

Create test folder -> move data.txt & paste in test folder.

```
pwd
mkdir test
ls
pwd
mv data.txt /home/shrutic29933/test/
ls
cd test/
ls
```


Create user folder -> Create 400 files -> Delete 100 files
Copy 101 to 300 from user folder to test folder
Delete files 301 to 305 (Need to get warning: Do you want to delete files)

```
cd ..
ls
pwd
mkdir user
ls
cd user/
touch file{001..400}.txt
ls
rm file{001..100}.txt
ls
history
pwd
cd user/
ls
cp file(101..300).txt /home/shrutic29933/test/
ls
cd ../test/
ls
cd ../user/
ls
cp file{101..300}.txt /home/shrutic29933/test/
ls /home/shrutic29933/test/
rm -I file{301..305}.txt
ls
```

Copy whole user folder in test folder. 

```
cd ..
pwd
cp -r /home/shrutic29933/user/ /home/shrutic29933/test/
ls /home/shrutic29933/test/
```

Create "document" folder in "user" folder. In document folder, Create two folders with name "Tushar" a "Aman". 
Without using cd command, create two files into Tushar folder. 
Without using cd command copy both the files in Aman folder. 
Delete one file from Tushar folder.

```
ls
pwd
cd user/
mkdir document
ls
cd document/
cd ..
cd document/
mkdir tushar aman
ls
touch /home/shrutic29933/user/document/tushar/file1.txt
touch /home/shrutic29933/user/document/tushar/file2.txt
ls
ls /home/shrutic29933/user/document/tushar/
cp /home/shrutic29933/user/document/tushar/file1.txt /home/shrutic29933/user/document/aman/
cp /home/shrutic29933/user/document/tushar/file2.txt  /home/shrutic29933/user/document/aman/
history 
ls /home/shrutic29933/user/document/aman/
rm /home/shrutic29933/user/document/tushar/file2.txt 
ls /home/shrutic29933/user/document/tushar/
```