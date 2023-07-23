1. Create a file 100 Mb in current user and fine out all the files whose size is more than 50Mb.

```
dd if=/dev/zero of=test file bs=1M count=100
dd if=/dev/zero of=outputfile bs=1M count=150
find /home/shrutic29933/ -type f -size + 50M
```


2. Find out all the files create by the current user in /home/<user_location>

```
find /home/shrutic29933/ -user shrutic29933 
find /home/shrutic29933/ -user shrutic29933 -maxdepth 1
```

3. Find only the files which has been created just within the last 10 minutes

```
find /home/shrutic29933/ -cmin 10
```

4. Find all the files only which are created by the current user and copy it inside the backup folder created in current user.

```
find /home/shrutic29933/ -user shrutic29933  | xargs cp -t backup
cd backup/
ls
```