1. We need to create a user whose identity is 5000.
Add it in grpup with 'sales' name.
Expire user account in 3 days.
Add user in sales group.

```
sudo useradd -m -u 5000 rajdeep
id rajdeep
sudo groupadd sales
sudo usermod -a -G sales rajdeep
id rajdeep
sudo useradd -e 2023-07-26 rajdeep
sudo chage -l rajdeep
```

2. Create group with name "marketing" & "HR"
Add yash user in marketing and check if user is added in it and same check in HR.
yash should be part of HR and marketing group.

```
sudo groupadd marketing
sudo groupadd HR
tail -2 /etc/group
sudo usermod -a -G marketing yash
id yash
sudo usermod -a -G HR yash
id yash
```

3. Whenever by default we create a file we should get permission rwx-r-rw

```
umask 0031
```

4. Create 3 files in such a place that when we create any new user it should automatically be copied in created user's folder.

```
cd /etc/skel
ls
touch filea.txt fileb.txt filec.txt
sudo touch filea.txt fileb.txt filec.txt
ls
sudo useradd -m pooja
ls -lah /home/pooja
```

5. date command should be called every 5 minutes and it should come in 1 file automatically.

```
vi date.sh

# Inside date.sh

#!/bin/bash

while true; do
    date
    sleep 10
done

# Change file permissions

chmod +x date.sh

# Execute the script

./date.sh
```