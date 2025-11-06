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

![WhatsApp Image 2025-09-03 at 4 27 33 PM](https://github.com/user-attachments/assets/15c2fd1b-dc2e-49b9-aa16-7d08197d17d4)


cat < file2
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM](https://github.com/user-attachments/assets/c5d75710-f7db-4ad3-83ae-778bf3f91c1c)


# Comparing Files
cmp file1 file2
comm file1 file2
## OUTPUT
<img width="749" height="221" alt="Screenshot 2025-09-06 165030" src="https://github.com/user-attachments/assets/2cc4c671-b64f-4e26-b8e8-32eb404397b8" />

diff file1 file2
## OUTPUT

<img width="670" height="267" alt="Screenshot 2025-09-06 165041" src="https://github.com/user-attachments/assets/08bce42b-9058-4586-a8d2-98dcbee64513" />

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

![WhatsApp Image 2025-09-03 at 4 27 33 PM (1)](https://github.com/user-attachments/assets/a46a7173-bdc8-4313-8d0a-581cbec9fd8d)



cut -d "|" -f 1 file22
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM (2)](https://github.com/user-attachments/assets/15fff899-5f2d-454c-8d67-773ee01a3e79)


cut -d "|" -f 2 file22
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM (3)](https://github.com/user-attachments/assets/40f1dd48-e8f1-4b09-b080-a0d8de9841e2)

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

![WhatsApp Image 2025-09-03 at 4 27 33 PM (4)](https://github.com/user-attachments/assets/36446524-7405-4fb6-9b14-21abc7bbd4d9)


grep hello newfile 
## OUTPUT


![WhatsApp Image 2025-09-03 at 4 27 33 PM (5)](https://github.com/user-attachments/assets/fcd762b2-9005-4edd-b766-e1e76c41f819)


grep -v hello newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM (5)](https://github.com/user-attachments/assets/19d805e2-a4fd-4263-8d00-00d77f83a837)


cat newfile | grep -i "hello"
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM (6)](https://github.com/user-attachments/assets/e14b6669-4237-42ee-82d2-c68ec3a05add)



cat newfile | grep -i -c "hello"
## OUTPUT


![WhatsApp Image 2025-09-03 at 4 27 33 PM (6)](https://github.com/user-attachments/assets/42d5bcb1-50ed-4103-aa63-7eed8bb994f6)


grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM](https://github.com/user-attachments/assets/b0b9f4ba-2794-43fe-8ed5-921bc513b289)


grep -w -n world newfile   
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 33 PM (7)](https://github.com/user-attachments/assets/01e1bb87-2de9-45f6-8af3-0c5722768fc8)

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

![WhatsApp Image 2025-09-03 at 4 27 36 PM (1)](https://github.com/user-attachments/assets/1efd2a4e-8d56-445f-a1c7-a3fb86e40353)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM (2)](https://github.com/user-attachments/assets/d57e981e-22e4-4bb3-a0f4-5b6ae098f9c7)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![WhatsApp Image 2025-09-03 at 4 27 36 PM (3)](https://github.com/user-attachments/assets/7f78e1a5-4192-413a-9a38-d840f7029e07)


egrep '(^hello)' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM (4)](https://github.com/user-attachments/assets/1ac2843e-2750-40f6-9b63-f2d104fd64b1)


egrep '(world$)' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM (5)](https://github.com/user-attachments/assets/91a4fe92-d397-433b-bfdc-5a5c932ba924)


egrep '(World$)' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM (5)](https://github.com/user-attachments/assets/697edc29-463f-4d38-b235-69d12455257a)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 36 PM (6)](https://github.com/user-attachments/assets/7cea2688-9882-4cfd-ae46-49c290659ce8)


egrep '[1-9]' newfile 
## OUTPUT

<img width="812" height="50" alt="Screenshot 2025-09-06 171324" src="https://github.com/user-attachments/assets/2be6fb81-394f-46a1-a153-d8448b703239" />


egrep 'Linux.*world' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM](https://github.com/user-attachments/assets/7b4339be-46f6-4ed7-87e6-c02dcd41cce7)

egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM](https://github.com/user-attachments/assets/a269dfa7-ecf9-4732-9758-ba690f654eb0)

egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (2)](https://github.com/user-attachments/assets/e54e6f05-ae93-4583-bee2-d4fcb1cb2ed3)


egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-09-03 at 4 27 37 PM (3)](https://github.com/user-attachments/assets/f7f3dff1-3875-4578-841b-664853df476d)


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

![WhatsApp Image 2025-09-03 at 4 27 37 PM (4)](https://github.com/user-attachments/assets/038da712-583c-4904-903d-d47ed3d6535d)


sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (5)](https://github.com/user-attachments/assets/3546ae37-024a-4b9d-8c56-6f90dc492e1d)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (6)](https://github.com/user-attachments/assets/499cbfdd-06a1-4377-95fb-4f64c42c2826)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="901" height="209" alt="Screenshot 2025-09-06 171429" src="https://github.com/user-attachments/assets/f9121c71-9417-4333-9ce8-bfd97ef1be3a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (7)](https://github.com/user-attachments/assets/48d22475-0451-480c-b761-f5209fd7c22d)


sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (8)](https://github.com/user-attachments/assets/6ba77a4c-de7f-4bcb-b7bb-2b9353de9d7b)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (9)](https://github.com/user-attachments/assets/154a5b4d-6ae5-4d3e-9624-4d181fd719fc)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (10)](https://github.com/user-attachments/assets/6ba99ada-de81-4f40-95ab-5dd0e0d29ecb)


seq 10 
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (11)](https://github.com/user-attachments/assets/71c270ae-ffd5-4d35-899a-14fa686a13e6)


seq 10 | sed -n '4,6p'
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (12)](https://github.com/user-attachments/assets/ed5a7340-300a-4e50-bdec-0f26f7841a01)


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="898" height="97" alt="Screenshot 2025-09-06 171512" src="https://github.com/user-attachments/assets/d04d2652-5ea6-4942-9421-199f727bc4aa" />


seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (13)](https://github.com/user-attachments/assets/68da43f1-1a69-4be8-bb0e-9d893295a86e)


seq 2 | sed '2i hello'
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (14)](https://github.com/user-attachments/assets/53beeb87-b34f-47e8-9a6d-042b12368446)


seq 10 | sed '2,9c hello'
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (15)](https://github.com/user-attachments/assets/2ec15b48-9c16-4280-9f80-507a18f58857)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (16)](https://github.com/user-attachments/assets/cbf74d4b-fc84-4ec7-892b-31455f75db81)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![WhatsApp Image 2025-09-03 at 4 27 37 PM (17)](https://github.com/user-attachments/assets/37e1f119-b062-4cee-9de0-650d1dd1bdae)


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="844" height="134" alt="Screenshot 2025-09-06 171750" src="https://github.com/user-attachments/assets/cff6256a-56a8-4995-9262-3dd3894e0635" />


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

<img width="799" height="86" alt="Screenshot 2025-09-06 172007" src="https://github.com/user-attachments/assets/a36741f6-ff1f-47cc-b4a7-a3bb481dd576" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="898" height="91" alt="Screenshot 2025-09-06 172050" src="https://github.com/user-attachments/assets/55b11f49-edb9-4aca-af77-170ad95501bc" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="904" height="207" alt="Screenshot 2025-09-06 172307" src="https://github.com/user-attachments/assets/1bed4825-c8e1-4fb3-b8d2-e41910f474d8" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="723" height="118" alt="Screenshot 2025-09-06 172411" src="https://github.com/user-attachments/assets/1675da42-b168-425a-b473-87d185d3b66a" />


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

<img width="810" height="867" alt="Screenshot 2025-09-06 172904" src="https://github.com/user-attachments/assets/ef505062-5da5-4ca6-a8e3-3fe6ad19a8d8" />

 
ls file1
## OUTPUT

<img width="810" height="867" alt="Screenshot 2025-09-06 172904" src="https://github.com/user-attachments/assets/85e290af-f254-4153-bf26-b98cbd1d8393" />


echo $?
## OUTPUT 

<img width="549" height="75" alt="Screenshot 2025-09-06 172957" src="https://github.com/user-attachments/assets/5879461a-3eaa-46a9-bf88-2c629b48f714" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="549" height="75" alt="Screenshot 2025-09-06 172957" src="https://github.com/user-attachments/assets/c70cfa0d-5a69-4dd7-9333-ec4f673a92e5" />

abcd
 
echo $?
 ## OUTPUT

<img width="594" height="80" alt="Screenshot 2025-09-06 173102" src="https://github.com/user-attachments/assets/12f6710c-1a28-42dd-82eb-3cad70c5315d" />

 
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
## OUTPUT

<img width="911" height="443" alt="Screenshot 2025-09-06 173144" src="https://github.com/user-attachments/assets/27dbadfc-8359-4c5c-9347-6a5866eabfae" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="775" height="139" alt="Screenshot 2025-09-06 173217" src="https://github.com/user-attachments/assets/af50e54c-d794-4eb6-a5de-db4b524fa659" />


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

<img width="852" height="350" alt="Screenshot 2025-09-06 173247" src="https://github.com/user-attachments/assets/2ccd8792-3815-4606-8a6c-1439e02b42a2" />


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

<img width="728" height="856" alt="Screenshot 2025-09-06 173344" src="https://github.com/user-attachments/assets/9bcbde1f-c98b-4770-8a4b-c59110eced7c" />


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
## OUTPUT

<img width="759" height="453" alt="Screenshot 2025-09-06 173456" src="https://github.com/user-attachments/assets/e30dd3ce-e7ad-4107-98ef-a91145d6e356" />


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
## OUTPUT

<img width="760" height="569" alt="Screenshot 2025-09-06 173532" src="https://github.com/user-attachments/assets/851d918a-fdc2-4826-8e8f-5989901fd67f" />


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

<img width="849" height="548" alt="Screenshot 2025-09-06 173601" src="https://github.com/user-attachments/assets/eab02498-1740-48e2-a54d-d65a5e2142b5" />


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

<img width="870" height="297" alt="Screenshot 2025-09-06 173639" src="https://github.com/user-attachments/assets/ba4e5b1c-4b81-4e0e-ad7b-960b60a7da27" />


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

## OUTPUT

<img width="713" height="354" alt="Screenshot 2025-09-06 173708" src="https://github.com/user-attachments/assets/414926ca-70e7-4f7f-a9e2-2769a1f6ece4" />

 
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

<img width="692" height="465" alt="Screenshot 2025-09-06 173943" src="https://github.com/user-attachments/assets/19971575-95ec-443f-aa94-97973491ac27" />

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

 <img width="642" height="314" alt="Screenshot 2025-09-06 174021" src="https://github.com/user-attachments/assets/0abd8c65-c275-450c-8e28-d742cc64e72d" />

 
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

<img width="760" height="406" alt="Screenshot 2025-09-06 174110" src="https://github.com/user-attachments/assets/2db6c81a-b145-4b32-b91d-7c24222c1e2e" />


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

<img width="794" height="368" alt="Screenshot 2025-09-06 174202" src="https://github.com/user-attachments/assets/a3d54332-d76e-4c0a-a067-a69be64d415f" />


cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
## OUTPUT

<img width="689" height="366" alt="Screenshot 2025-09-06 174306" src="https://github.com/user-attachments/assets/c130d607-1627-4ff5-8f57-b72a78f57071" />


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
## OUTPUT


<img width="690" height="365" alt="Screenshot 2025-09-06 174358" src="https://github.com/user-attachments/assets/d045df75-3dd3-4143-8576-e91fc57897c2" />

 
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

<img width="690" height="365" alt="Screenshot 2025-09-06 174358" src="https://github.com/user-attachments/assets/3e429ed6-a4f9-400e-af46-7544b8c2be93" />

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

<img width="656" height="353" alt="Screenshot 2025-09-06 174558" src="https://github.com/user-attachments/assets/0c17843c-f99f-4fe5-b494-f68b88f99d20" />


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

<img width="616" height="342" alt="Screenshot 2025-09-06 174630" src="https://github.com/user-attachments/assets/6d11c99f-ae83-44a6-bf9e-6ebcc0934d64" />


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

<img width="535" height="618" alt="Screenshot 2025-09-06 174716" src="https://github.com/user-attachments/assets/f6532c12-d3f8-48f6-a55b-4af90e9d3b0a" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT

<img width="842" height="438" alt="Screenshot 2025-09-06 174827" src="https://github.com/user-attachments/assets/1521f28b-6c7b-4eb2-ba7c-4cd0c11983a0" />

 
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

<img width="813" height="471" alt="Screenshot 2025-09-06 174917" src="https://github.com/user-attachments/assets/c03a6432-a215-4c26-a9ad-5c3c94de2ab0" />

 
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

<img width="523" height="265" alt="Screenshot 2025-09-06 174950" src="https://github.com/user-attachments/assets/74c1aba8-8d48-49c7-b8b5-dc42b8ccd735" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT

<img width="532" height="262" alt="Screenshot 2025-09-06 175020" src="https://github.com/user-attachments/assets/8b28279e-e613-42c2-9669-99c6c5b898b3" />



 
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

 ./funcex.sh 

 
 ./funcex.sh 1 2
 ## OUTPUT

<img width="615" height="381" alt="Screenshot 2025-09-06 175122" src="https://github.com/user-attachments/assets/356b3b8c-b123-4f24-9f9b-b59f599b61af" />

 
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

<img width="685" height="593" alt="Screenshot 2025-09-06 175151" src="https://github.com/user-attachments/assets/ae90edd9-d40a-41a1-a587-ee25706cbecf" />


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
$ ./argshift.sh 1 2 3
 ## OUTPUT

<img width="566" height="376" alt="Screenshot 2025-09-06 175248" src="https://github.com/user-attachments/assets/ce08479a-a5b6-4665-b690-529119fedecb" />

 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
 ./argshift.sh 1 2 3
```
## OUTPUT

  <img width="682" height="545" alt="Screenshot 2025-09-06 175541" src="https://github.com/user-attachments/assets/275b7485-8fec-4d7c-a887-084326539d75" />

 
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

<img width="617" height="908" alt="Screenshot 2025-09-06 175622" src="https://github.com/user-attachments/assets/a33fd5b3-c014-4c36-9b7b-91f87ca472fc" />

 
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

<img width="693" height="650" alt="Screenshot 2025-09-06 175658" src="https://github.com/user-attachments/assets/aef21498-c69b-4ec1-b9ef-eb80acfb2c39" />


# RESULT:
The Commands are executed successfully.
