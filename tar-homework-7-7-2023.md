1. Create file ABC and put it in tar file (Tushar.tar)
Create file user.info put it in Tushar.tar
In Tushar.tar, they will have to be both the files, ABC and user.info

```
touch abc.txt
ls
tar -cf tushar.tar abc.txt 
tar -tf tushar.tar 
touch user.info
ls
tar -cf tushar.tar user.info
tar -tf tushar.tar 
tar -cf tushar.tar abc.txt user.info
tar -tf tushar.tar 
```

2. From tar file, delete 1 or 2 files

```
tar --delete -f tushar.tar user.info
tar -tf tushar.tar
```

3. Create tar file -> Extract all the content from tar file.
Extract tar file in backup folder (Do not use move or copy command)

```
tar -xf tushar.tar -C backup/
```