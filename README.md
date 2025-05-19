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
![image](https://github.com/user-attachments/assets/ab56b509-94aa-42b2-8a3a-d56c73e2d3f9)

cat < file2

## OUTPUT
![image](https://github.com/user-attachments/assets/5921a2fd-c11a-4c3a-844f-03c162573671)

# Comparing Files
cmp file1 file2

## OUTPUT
![image](https://github.com/user-attachments/assets/63dc6be0-4a25-4719-b91a-7772a793779c)

comm file1 file2

## OUTPUT
![image](https://github.com/user-attachments/assets/38ce96f3-8170-4cc3-ae62-1dd17905dafe)

diff file1 file2

## OUTPUT
![image](https://github.com/user-attachments/assets/00499cf4-b772-4836-93d9-ed1c6aa621a3)

## Filters
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
![image](https://github.com/user-attachments/assets/9e016e51-2a76-4d72-9fa9-224615598ef9)

cut -d "|" -f 1 file22

## OUTPUT
![image](https://github.com/user-attachments/assets/a31a5fc9-6d7a-427f-9b2d-2e8602215e11)

cut -d "|" -f 2 file22

## OUTPUT
![image](https://github.com/user-attachments/assets/1b9b6e13-20d0-4a7e-8ea0-edafd448b904)

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
![image](https://github.com/user-attachments/assets/0c9fdef0-7b27-4a1e-a30e-e2468b636c07)

grep hello newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/45203f13-5661-4084-b96c-743da7a08a9d)

grep -v hello newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/9e25294c-e6fe-4702-a355-0265f08551a5)

cat newfile | grep -i "hello"

## OUTPUT
![image](https://github.com/user-attachments/assets/ba65d428-7d1c-40a1-bbfc-9188f12ce843)

cat newfile | grep -i -c "hello"

## OUTPUT
![image](https://github.com/user-attachments/assets/3e90846f-edb1-4646-a897-9f21203bbfdd)

grep -R ubuntu /etc

## OUTPUT
![image](https://github.com/user-attachments/assets/234dcc4b-c134-430c-bcf8-5afbd4b8dd2c)

grep -w -n world newfile  

## OUTPUT
![image](https://github.com/user-attachments/assets/948798da-102f-463a-bac4-aaf0d74c0b77)

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
![image](https://github.com/user-attachments/assets/299b22ae-cb26-4f4b-9e6a-6fcfb2eb5db6)

egrep -w '(H|h)ello' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/936010b4-eb51-4711-a577-90b7186c6b35)

egrep -w '(H|h)ell[a-z]' newfile

## OUTPUT
![image](https://github.com/user-attachments/assets/6662efc1-f94c-49c2-9bcf-3494542e4b07)

egrep '(^hello)' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/97d59239-69a4-451e-8e0e-2f84111d07c7)

egrep '(world$)' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/fe67db8b-0a53-43f6-b9bb-474b4a87ed92)

egrep '(World$)' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/63ba11bc-9621-471c-9dcb-3654022b0a8c)

egrep '((W|w)orld$)' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/e5d94c34-ed3e-4682-9a1d-38444684c828)

egrep '[1-9]' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/e9ed5bec-902b-4afe-9993-d1f832315d16)

egrep 'Linux.*world' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/359a6a43-c3c8-4c68-b7af-301849715454)

egrep 'Linux.*World' newfile 

## OUTPUT
![image](https://github.com/user-attachments/assets/ae927069-76b8-45a0-a45d-b20b6143dc30)

egrep l{2} newfile

## OUTPUT
![image](https://github.com/user-attachments/assets/87141120-0bc3-4831-9fda-e347c27aee80)

egrep 's{1,2}' newfile

## OUTPUT 
![image](https://github.com/user-attachments/assets/08192cf4-76ae-47d7-ae53-cd065e36eefa)

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
![image](https://github.com/user-attachments/assets/1ded43b7-3349-431b-994b-8c3338354a15)

sed -n -e '$p' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/dd38e99f-cb1f-47a6-979d-eb4eff63c05d)

sed  -e 's/Ram/Sita/' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/f8b6f7db-488b-4a03-b8fa-4ad260624989)

sed  -e '2s/Ram/Sita/' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/c284ca91-d15f-4313-a0ac-ce82edd20966)

sed  '/tom/s/5000/6000/' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/8a6a6a42-7f24-484b-a269-382e5be1bccb)

sed -n -e '1,5p' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/dfa7b6b2-b864-4b0d-88fd-edf2ea40290d)

sed -n -e '2,/Joe/p' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/d01f34ad-9a05-47b3-a45c-53fb8914c6d1)

sed -n -e '/tom/,/Joe/p' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/887fe0ca-de51-474f-a064-1c642d8af40d)

seq 10 

## OUTPUT
![image](https://github.com/user-attachments/assets/bdc80571-718d-4abd-a182-66ff5f816ac7)

seq 10 | sed -n '4,6p'

## OUTPUT
![image](https://github.com/user-attachments/assets/5be9fad8-2f06-4966-9990-c2e1d2b20590)

seq 10 | sed -n '2,~4p'

## OUTPUT
![image](https://github.com/user-attachments/assets/4b6ad2fd-8814-4b96-86e9-3b548075f837)

seq 3 | sed '2a hello'

## OUTPUT
![image](https://github.com/user-attachments/assets/440dd90d-7149-4fa9-99f4-dd1d28632fd3)

seq 2 | sed '2i hello'

## OUTPUT
![image](https://github.com/user-attachments/assets/c697a869-c2a1-490e-8eda-6f9a4a5e3c6b)

seq 10 | sed '2,9c hello'

## OUTPUT
![image](https://github.com/user-attachments/assets/a80847c1-d907-464e-91ea-7684e5d389f8)

sed -n '2,4{s/^/$/;p}' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/c8bb730b-79f5-44a1-8468-1104adf2e36c)

sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/eb9c618b-f832-487e-b157-a6012496da6e)

## Sorting File content
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
![image](https://github.com/user-attachments/assets/29512c44-77eb-4bdd-9af9-8ad1beb043ac)

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
![image](https://github.com/user-attachments/assets/c5cd7f50-222d-4945-92e7-1b191ad4f322)

## Using tr command

cat file23 | tr [:lower:] [:upper:]

## OUTPUT
![image](https://github.com/user-attachments/assets/dd856ac0-a30f-4315-b408-b65e2fd51d4c)

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
![image](https://github.com/user-attachments/assets/5b199877-a703-4173-a347-2366abc959f5)

cat urllist.txt | tr -d ' ' | tr -s '.'

## OUTPUT
![image](https://github.com/user-attachments/assets/dc9d76d3-3c79-441f-9609-72db39e67daa)

#Backup commands

tar -cvf backup.tar *

## OUTPUT
![image](https://github.com/user-attachments/assets/3fcc56a6-1692-442f-89d9-558d1737b4e1)

mkdir backupdir
mv backup.tar backupdir
cd backupdir
tar -tvf backup.tar

## OUTPUT
![image](https://github.com/user-attachments/assets/d2d50501-5832-4507-b115-285e85e682f7)
![image](https://github.com/user-attachments/assets/d8a624d8-29c1-468b-bb32-890dd78ff62f)

tar -xvf backup.tar

## OUTPUT
![image](https://github.com/user-attachments/assets/90a547dc-6661-4a8a-a2b2-b5afde191b00)

gzip backup.tar
ls .gz

## OUTPUT
![image](https://github.com/user-attachments/assets/77ad4f80-32cf-4ad0-9d6b-828c5ee12a3d)

gunzip backup.tar.gz

## OUTPUT
![image](https://github.com/user-attachments/assets/8bd09212-3431-4f7a-9404-9c6ad6c1ac97)

## Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/5f7e7264-6a8d-4483-a532-527ee4d64b3a)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt

## OUTPUT
![image](https://github.com/user-attachments/assets/4350f478-eb93-4d56-9787-fb4d14f65fe7)

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
![image](https://github.com/user-attachments/assets/a691e873-82d3-438d-afec-32fabb16a87a)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/bb9ae618-9849-4b6c-a69e-ffae15090bb9)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/0be6d10e-8fdd-416a-bfdf-f3f5eacccc60)

./one
bash: ./one: Permission denied
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/36404f2d-57c5-4f86-be2e-703f467c739c)

abcd
echo $?
## OUTPUT
![image](https://github.com/user-attachments/assets/7e771701-63f4-4020-8f13-fe2c624af0f2)

## mis-using string comparisons

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
## OUTPUT
![image](https://github.com/user-attachments/assets/daef97bc-99d0-4b8a-8dc1-856b402d8aa9)

chmod 755 strcomp.sh
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/61db6e62-81c9-41f0-a8f2-4200075c1aad)

## check file ownership
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
![image](https://github.com/user-attachments/assets/2666f066-062c-4312-a1fe-d32705da5dc5)

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
![image](https://github.com/user-attachments/assets/857d8c28-e157-4869-8128-315439920159)

## using numeric test comparisons
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
## OUTPUT
![image](https://github.com/user-attachments/assets/9915fed4-35e6-4842-857a-539707a29648)

## check if a file
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
## OUTPUT
![image](https://github.com/user-attachments/assets/86bf7203-338c-485c-8467-ed0e95c7fdeb)

## looking for a possible value using elif
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
![image](https://github.com/user-attachments/assets/c48a83d4-55fb-4ca9-af20-81bcd73014c9)

## testing compound comparisons
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
![image](https://github.com/user-attachments/assets/c116fbf3-d5d4-479d-a407-1f59ca7172ca)

## using the case command
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
## OUTPUT
![image](https://github.com/user-attachments/assets/c1ca90bf-5c24-4ad0-b32d-7f0d578013a6)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/73090d45-8f91-4515-9e27-9acfbe087708)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/4da6539b-728b-408a-bc15-68a162d2ed7c)

cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/803f0ed1-50ef-41cb-819e-a3a8515483aa)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/7434ccb0-5951-4995-bcae-e418ce645387)

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
$ ./forin2.sh 

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
![image](https://github.com/user-attachments/assets/013a2988-d9a2-4b8b-ac29-34203bb631f7)

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
![image](https://github.com/user-attachments/assets/239b8abb-45b5-4726-a5f8-7ef23a4ec394)

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
![image](https://github.com/user-attachments/assets/f4bcf253-b2ab-479f-ba6f-b6dfc8eea199)

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
![image](https://github.com/user-attachments/assets/669eb80c-46c0-4768-ba71-3b74616e2524)

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
![image](https://github.com/user-attachments/assets/b14a936e-56aa-4f8d-8387-05014185f85a)

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
![image](https://github.com/user-attachments/assets/a908f9b8-ff8b-436b-b96f-1b2e8becce72)

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
![image](https://github.com/user-attachments/assets/e5e610af-fe45-4d60-801f-bcf08f41387d)

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
![image](https://github.com/user-attachments/assets/ea624506-cce3-4368-b4f3-73c7907df9c4)

cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
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
![image](https://github.com/user-attachments/assets/0da4edcb-051b-4b66-b4c6-7975a4bb163a)

./funcex.sh 
./funcex.sh 1 2
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
![image](https://github.com/user-attachments/assets/ec40e244-5754-4d87-8381-5a21fd35d9b6)

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
![image](https://github.com/user-attachments/assets/e4d725a7-cd88-4f46-bccf-c7b17d7c43af)

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
![image](https://github.com/user-attachments/assets/da47b744-dc1e-4e46-9a04-ea739c65ce12)

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
![image](https://github.com/user-attachments/assets/6ca9bc56-d203-4eb3-9444-57674765c4d7)

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
![image](https://github.com/user-attachments/assets/0c627e55-5192-4d97-884c-d98f3bade188)

# RESULT:
The Commands are executed successfully.
