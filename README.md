# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![ss1](https://github.com/user-attachments/assets/b4b494a8-013f-4065-990a-56afedfe012c)


cat < file2
## OUTPUT
![ss2](https://github.com/user-attachments/assets/5d638997-8de0-4f32-bab6-a984058226fd)


# Comparing Files
cmp file1 file2
## OUTPUT
![ss3](https://github.com/user-attachments/assets/c12de008-f24a-4761-9f23-a7cd1dbf7443)

comm file1 file2
 ## OUTPUT
![ss4](https://github.com/user-attachments/assets/b97574b6-e8a7-4335-b655-d7fb7fd6fa2c)

 
diff file1 file2
## OUTPUT
![ss5](https://github.com/user-attachments/assets/99467b3b-e62f-49ee-91cd-c7266d3ddf8b)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![ss6](https://github.com/user-attachments/assets/59f09cf8-c542-407a-acc7-21888053fd82)



cut -d "|" -f 1 file22
## OUTPUT

![ss7](https://github.com/user-attachments/assets/ef254853-efc7-40c0-86e0-1c7509be37cb)


cut -d "|" -f 2 file22
## OUTPUT

![ss8](https://github.com/user-attachments/assets/a3d26868-f1c8-48f9-9068-f2a99398ec31)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![ss9](https://github.com/user-attachments/assets/c830c802-9081-4bdb-916e-d0a1da2935df)


grep hello newfile 
## OUTPUT

![ss10](https://github.com/user-attachments/assets/0246931d-9454-4566-80f2-57e42882db9f)



grep -v hello newfile 
## OUTPUT

![ss11](https://github.com/user-attachments/assets/a3a8336e-bd84-4349-b533-a80a740076bf)


cat newfile | grep -i "hello"
## OUTPUT

![ss12](https://github.com/user-attachments/assets/96181003-9863-4dea-91c4-6186f6c4e574)


cat newfile | grep -i -c "hello"
## OUTPUT

![ss13](https://github.com/user-attachments/assets/75e0655c-a285-4851-bc50-f6de81a8f797)


grep -R ubuntu /etc
## OUTPUT

![ss14](https://github.com/user-attachments/assets/728a6bbd-99f5-4f2c-87b4-845dfcb11682)


grep -w -n world newfile   
## OUTPUT
![ss15](https://github.com/user-attachments/assets/d4a1867d-fce2-41f0-b44f-035f0c72d426)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![ss16](https://github.com/user-attachments/assets/062fff8e-c5c1-4cdc-93ab-56fa1d3bbace)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![ss17](https://github.com/user-attachments/assets/3d6a8e7f-69a0-496e-896e-4c7cfb756969)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![ss18](https://github.com/user-attachments/assets/799365d9-b77b-4b30-b3ae-8a5ba82594be)



egrep '(^hello)' newfile 
## OUTPUT

![ss19](https://github.com/user-attachments/assets/7da282ef-7739-410a-bbb5-80942be1643a)


egrep '(world$)' newfile 
## OUTPUT

![ss20](https://github.com/user-attachments/assets/fcfc746c-0e9d-4733-bce3-3bdfa2263c8c)


egrep '(World$)' newfile 
## OUTPUT
![ss21](https://github.com/user-attachments/assets/e643e9c9-4eb4-41a0-9764-400fd0d2d68f)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![ss22](https://github.com/user-attachments/assets/c4690bad-4d57-4791-b656-52c371e24d65)


egrep '[1-9]' newfile 
## OUTPUT

![ss23](https://github.com/user-attachments/assets/af67e939-03b7-4d9e-a7df-79ca9c3d3376)


egrep 'Linux.*world' newfile 
## OUTPUT
![ss24](https://github.com/user-attachments/assets/cc4de019-a04d-464d-bc9e-84fc5b5dd8d9)


egrep 'Linux.*World' newfile 
## OUTPUT
![ss25](https://github.com/user-attachments/assets/0b31a9a8-70c9-4a43-8b58-2586bce5c220)


egrep l{2} newfile
## OUTPUT
![ss26](https://github.com/user-attachments/assets/a1502cf6-aed9-49bb-a9ac-eebada8967ab)



egrep 's{1,2}' newfile
## OUTPUT 
![ss27](https://github.com/user-attachments/assets/c65402da-d7fe-4995-9f2c-9d4c4cfe8360)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![ss28](https://github.com/user-attachments/assets/f852938c-0afa-4155-a4dc-9452effce041)



sed -n -e '$p' file23
## OUTPUT
![ss29](https://github.com/user-attachments/assets/9a1f5c12-8f96-4d34-af50-f7ed66e7dea0)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![ss30](https://github.com/user-attachments/assets/6368e8bf-146f-4d9d-93b0-f7661c55d8e5)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![ss31](https://github.com/user-attachments/assets/ce83e590-695f-4988-ba51-3c19ca7e9e61)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![ss32](https://github.com/user-attachments/assets/49d50555-0caf-4152-b4f6-a3f11963a114)



sed -n -e '1,5p' file23
## OUTPUT
![ss33](https://github.com/user-attachments/assets/b66ce381-5c65-4655-a92c-5fe31d1a42b6)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![ss34](https://github.com/user-attachments/assets/06b6c0ef-7d76-4f92-8662-f879826c3b16)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![ss35](https://github.com/user-attachments/assets/d4ac6abb-87f0-4c58-9c96-4d04ef5b92ed)



seq 10 
## OUTPUT

![ss36](https://github.com/user-attachments/assets/a00028d4-7336-42b8-af98-da42b6cc51a1)


seq 10 | sed -n '4,6p'
## OUTPUT
![ss37](https://github.com/user-attachments/assets/fbf15239-0b32-45a4-9f5f-4c7c910147bd)



seq 10 | sed -n '2,~4p'
## OUTPUT

![ss38](https://github.com/user-attachments/assets/c3d0aadd-23de-4d4a-b726-f3933ef1dd7c)


seq 3 | sed '2a hello'
## OUTPUT

![ss39](https://github.com/user-attachments/assets/b93e7555-5525-4bb1-899a-4bb49df1e61a)


seq 2 | sed '2i hello'
## OUTPUT
![ss40](https://github.com/user-attachments/assets/ff4dee72-ec67-4f0b-93b2-d44926cbb401)


seq 10 | sed '2,9c hello'
## OUTPUT
![ss41](https://github.com/user-attachments/assets/da743669-6e75-49cd-90b7-ed55d9656566)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![ss42](https://github.com/user-attachments/assets/6da4f0b7-b8bf-4eb7-8af3-b26bd18776ca)



sed -n '2,4{s/$/*/;p}' file23
![ss43](https://github.com/user-attachments/assets/015747b2-0487-40af-9acc-0d33d243359c)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![ss44](https://github.com/user-attachments/assets/6ce28910-c07d-43e8-91f6-999f0d1f2dff)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![ss45](https://github.com/user-attachments/assets/129d9c57-6c7e-4fdd-b7bc-4d414a75946b)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![ss46](https://github.com/user-attachments/assets/a5c67e30-9bf8-46c7-82e2-43e2284e08a1)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![ss47](https://github.com/user-attachments/assets/1829c02a-5313-4a94-a7dd-0d6ceafcfe97)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![ss48](https://github.com/user-attachments/assets/7392998d-dfe3-4a77-801b-95c00cf6abc8)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![ss49 a](https://github.com/user-attachments/assets/c47ee04e-93ed-45f1-9f7a-c83fc9a3acae)
![ss49 b](https://github.com/user-attachments/assets/3b3cd906-e076-4bdb-b53c-45f88778162a)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT
![ss50](https://github.com/user-attachments/assets/f69fdbcc-ddae-46be-806a-4164b1f259e4)

gzip backup.tar

ls .gz
## OUTPUT
![ss51](https://github.com/user-attachments/assets/0586d90d-69e4-4497-9b0f-037c1b6bc10e)

gunzip backup.tar.gz
## OUTPUT
![ss52](https://github.com/user-attachments/assets/7efdfa51-cb25-4ed5-8ba5-c36192dfb83a)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![ss53](https://github.com/user-attachments/assets/eca378c2-ee7e-4639-a747-18d04c61353f)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![ss54](https://github.com/user-attachments/assets/086a86bd-95b7-443e-871b-55e7bdd5adb9)

![ss54 b](https://github.com/user-attachments/assets/0de79786-901a-4fd1-a695-5e27394e158b)

 
ls file1
## OUTPUT
![ss55](https://github.com/user-attachments/assets/44e3c9a2-9135-40bc-892a-30e956b97280)

echo $?
## OUTPUT 
![ss56](https://github.com/user-attachments/assets/3f99ddca-dbec-4790-aa73-b736e2d6640a)

./one
bash: ./one: Permission denied

# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![ss57](https://github.com/user-attachments/assets/d7683187-460d-420d-99b1-79f4aeceee10)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![ss58](https://github.com/user-attachments/assets/14b359af-21c6-408e-b929-4982b360ddf9)



# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![ss59](https://github.com/user-attachments/assets/4ad9ac14-7829-4527-9015-740f30892645)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![ss60](https://github.com/user-attachments/assets/49ae3763-dd88-4696-9569-4dab71dba165)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![ss61](https://github.com/user-attachments/assets/9db6c9d5-4c3f-40e6-851f-0adc49866bfe)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![ss62](https://github.com/user-attachments/assets/76589d17-4220-4970-9dc5-4ffa4f944c4b)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![ss63](https://github.com/user-attachments/assets/6177a31b-9a21-4dd0-bb2e-840204650570)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![ss64](https://github.com/user-attachments/assets/406b8016-bf45-42ee-b087-9367932ba827)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
![ss65](https://github.com/user-attachments/assets/b837e421-9452-4619-bedd-bc2b49f1def3)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
![ss66](https://github.com/user-attachments/assets/730296f0-f2e7-4176-a6fe-210b8cd3cfc3)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
![ss67](https://github.com/user-attachments/assets/8cb06f8a-2bc0-4bd1-8045-2ee37c517a92)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```


 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
![ss68](https://github.com/user-attachments/assets/db409e2f-4b3a-4f0c-ac11-01b501bf0cf0)
$ ./forin2.sh 
![ss69](https://github.com/user-attachments/assets/85e27987-c67a-4df6-b249-be9817e10359)
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![ss71](https://github.com/user-attachments/assets/2ec892bf-30df-44ea-b9c3-20c414cf395f)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![ss72](https://github.com/user-attachments/assets/e2fe48d7-760b-47e7-ba54-bd3e4dc1ff4b)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![ss73](https://github.com/user-attachments/assets/5b609472-6fef-4b2e-b133-efa4037cf333)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![ss74](https://github.com/user-attachments/assets/1f772220-e96a-4067-a382-d00aa9813df6)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![ss75](https://github.com/user-attachments/assets/70d8355b-ae6b-4b7e-883e-cb4892dd5432)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![ss76](https://github.com/user-attachments/assets/ea0fd3b6-3ed0-4ba0-8215-2be77f3583ec)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![ss77](https://github.com/user-attachments/assets/720cf2d4-5070-4ade-84c7-0a06e1055f9a)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![ss78](https://github.com/user-attachments/assets/0efdd03d-1264-48cb-b72e-774e064eaf85)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh ![ss79](https://github.com/user-attachments/assets/b4c1fedb-5c8f-470e-bbdd-f03b5e3be60d)


 
 ./funcex.sh 1 2 ![ss80](https://github.com/user-attachments/assets/eec19e9d-5dc5-438b-b19e-5082fae8dc50)


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![ss81](https://github.com/user-attachments/assets/43851081-3958-4071-a226-e583c5ca19bf)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![ss82](https://github.com/user-attachments/assets/f670a589-d812-423b-8a3b-928d12802756)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![ss83](https://github.com/user-attachments/assets/901767b2-e3d4-42ea-98a3-2ba116e3dddd)

 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![ss84](https://github.com/user-attachments/assets/c6e47203-4d07-49ee-8312-8d5a3bf4d34f)


# RESULT:
The Commands are executed successfully.
