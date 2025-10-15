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
<img width="472" height="123" alt="Screenshot from 2025-10-15 15-28-55" src="https://github.com/user-attachments/assets/98ebe739-e27a-4e6d-989f-07695a2bdc5c" />



cat < file2
## OUTPUT
<img width="478" height="138" alt="Screenshot from 2025-10-15 15-29-26" src="https://github.com/user-attachments/assets/18d2f30c-1756-4f2c-845a-4332252b84dd" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="481" height="53" alt="Screenshot from 2025-10-15 15-30-02" src="https://github.com/user-attachments/assets/96fe82f2-2dce-4ec0-8a9c-40e66c1835ec" />

comm file1 file2
 ## OUTPUT
<img width="541" height="179" alt="Screenshot from 2025-10-15 15-30-27" src="https://github.com/user-attachments/assets/a0280169-1a8b-4a3b-b97f-1ecc12f22f3f" />

 
diff file1 file2
## OUTPUT
<img width="540" height="220" alt="Screenshot from 2025-10-15 15-31-38" src="https://github.com/user-attachments/assets/7d7270a1-b7f2-4a0f-840d-e582534c9709" />


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
<img width="533" height="96" alt="Screenshot from 2025-10-15 15-34-46" src="https://github.com/user-attachments/assets/5142faae-3fa8-4a14-90fd-d585205897ff" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="498" height="241" alt="Screenshot from 2025-10-15 18-57-50" src="https://github.com/user-attachments/assets/0ff072a9-545f-4764-8f1a-74464ae8736d" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="509" height="250" alt="Screenshot from 2025-10-15 18-58-37" src="https://github.com/user-attachments/assets/786b9ed1-d294-4392-805e-86b62e020d00" />


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
<img width="522" height="71" alt="Screenshot from 2025-10-15 15-36-39" src="https://github.com/user-attachments/assets/0bd303d0-7c37-404d-8ee1-263bbb3e8bbd" />



grep hello newfile 
## OUTPUT
<img width="522" height="71" alt="Screenshot from 2025-10-15 15-37-05" src="https://github.com/user-attachments/assets/95fe0573-3df9-4174-b9ad-509e76f84c63" />




grep -v hello newfile 
## OUTPUT
<img width="508" height="162" alt="Screenshot from 2025-10-15 18-59-08" src="https://github.com/user-attachments/assets/ac37f88b-a831-48ec-89fe-4af05c636412" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="522" height="71" alt="Screenshot from 2025-10-15 15-38-48" src="https://github.com/user-attachments/assets/a164108c-b694-48d3-b546-5c380464278e" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="522" height="71" alt="Screenshot from 2025-10-15 15-38-08" src="https://github.com/user-attachments/assets/df14c5b5-8fe5-4ac0-9b3a-dc50756df31e" />


grep -R ubuntu /etc
## OUTPUT
<img width="1304" height="644" alt="Screenshot from 2025-10-15 18-59-56" src="https://github.com/user-attachments/assets/50d30d15-f335-4984-b4cd-a4a2777eaeb7" />

grep -w -n world newfile   
## OUTPUT
<img width="632" height="91" alt="Screenshot from 2025-10-15 15-42-22" src="https://github.com/user-attachments/assets/733ac185-7361-43c8-a5de-75af7ac07ea2" />


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
<img width="659" height="90" alt="Screenshot from 2025-10-15 15-45-02" src="https://github.com/user-attachments/assets/683aa9a6-d76d-4db0-ab46-2f5deaf6261f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="754" height="98" alt="Screenshot from 2025-10-15 19-01-16" src="https://github.com/user-attachments/assets/c5336828-572a-4571-b293-1f9c3f7a63af" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="659" height="90" alt="Screenshot from 2025-10-15 15-45-49" src="https://github.com/user-attachments/assets/e867c511-3295-4831-99e6-e5869dc69be2" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="659" height="73" alt="Screenshot from 2025-10-15 15-46-40" src="https://github.com/user-attachments/assets/4b508eb8-c734-4722-a195-8d4ef96e317c" />

egrep '(world$)' newfile 
## OUTPUT

<img width="659" height="93" alt="Screenshot from 2025-10-15 15-47-49" src="https://github.com/user-attachments/assets/fe3fee02-df37-4ab3-b7b8-b2e6af97cdc4" />


egrep '(World$)' newfile 
## OUTPUT
<img width="754" height="98" alt="Screenshot from 2025-10-15 19-01-58" src="https://github.com/user-attachments/assets/3e6b6878-4213-4c5b-9807-d7d6d36b82bf" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="659" height="115" alt="Screenshot from 2025-10-15 15-48-27" src="https://github.com/user-attachments/assets/1f5b1516-6ec6-4e76-aee2-4d59fc201724" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="670" height="72" alt="Screenshot from 2025-10-15 15-49-03" src="https://github.com/user-attachments/assets/00c94ef1-4010-40d3-94ba-1df674bce235" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="670" height="72" alt="Screenshot from 2025-10-15 15-49-30" src="https://github.com/user-attachments/assets/21a3782b-1ce7-4e51-8cc2-9bd78a82e81f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="670" height="72" alt="Screenshot from 2025-10-15 15-49-54" src="https://github.com/user-attachments/assets/a467c988-1679-4d23-ba34-448ccf7e43f8" />


egrep l{2} newfile
## OUTPUT

<img width="670" height="90" alt="Screenshot from 2025-10-15 15-50-59" src="https://github.com/user-attachments/assets/cb3d4a76-c1d2-4964-a1de-1bbb3f27061f" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="670" height="113" alt="Screenshot from 2025-10-15 15-51-21" src="https://github.com/user-attachments/assets/66ef5340-a8f2-4c05-9916-6710cbb7a138" />


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

<img width="670" height="79" alt="Screenshot from 2025-10-15 15-59-25" src="https://github.com/user-attachments/assets/070a86f7-8959-4533-b669-e7353dcd5bf6" />


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="670" height="271" alt="Screenshot from 2025-10-15 16-01-23" src="https://github.com/user-attachments/assets/d5493440-4049-4118-ab41-9742bcf89c18" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="670" height="271" alt="Screenshot from 2025-10-15 16-02-32" src="https://github.com/user-attachments/assets/91968252-b55b-4c98-b4cd-0847a803aa5b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="670" height="271" alt="Screenshot from 2025-10-15 16-03-34" src="https://github.com/user-attachments/assets/1d79d2f5-1248-45d0-88ec-6691d06201e8" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="670" height="163" alt="Screenshot from 2025-10-15 16-04-02" src="https://github.com/user-attachments/assets/339b1e0e-bb29-4174-a0c9-0397ac459862" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="670" height="123" alt="Screenshot from 2025-10-15 16-04-41" src="https://github.com/user-attachments/assets/aef00d23-93e8-444a-9757-fb710fcd81a6" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="670" height="92" alt="Screenshot from 2025-10-15 16-05-41" src="https://github.com/user-attachments/assets/67489ff0-fd7c-4d2e-9eac-aac0e32453c8" />


seq 10 
## OUTPUT

<img width="670" height="268" alt="Screenshot from 2025-10-15 16-06-02" src="https://github.com/user-attachments/assets/b73f7d67-7a87-4b74-86e9-a60f5abc9c38" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="670" height="117" alt="Screenshot from 2025-10-15 16-06-34" src="https://github.com/user-attachments/assets/05d76dd2-2417-469a-817a-3afd35c868dd" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="670" height="117" alt="Screenshot from 2025-10-15 16-07-37" src="https://github.com/user-attachments/assets/a578459f-fb8b-4085-b391-c6701c0f4bf4" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="670" height="139" alt="Screenshot from 2025-10-15 16-08-05" src="https://github.com/user-attachments/assets/a977cd6b-303f-4596-9f2a-2772f54eaa4f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="670" height="121" alt="Screenshot from 2025-10-15 16-10-49" src="https://github.com/user-attachments/assets/e1dc1ee6-b692-48af-b851-54af95b37525" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="670" height="121" alt="Screenshot from 2025-10-15 16-11-22" src="https://github.com/user-attachments/assets/47ec7e8d-2a90-41b4-bc14-d55b22f782b8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="670" height="121" alt="Screenshot from 2025-10-15 16-12-33" src="https://github.com/user-attachments/assets/f9c5ce52-8693-4904-9d54-666ea1533724" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="670" height="121" alt="Screenshot from 2025-10-15 16-13-57" src="https://github.com/user-attachments/assets/c40d645f-cdeb-405f-be4b-0a282aa5eea5" />


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
<img width="670" height="156" alt="Screenshot from 2025-10-15 16-18-56" src="https://github.com/user-attachments/assets/5ebb9625-a016-4d6e-a9b6-99db4fe95477" />


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
<img width="670" height="156" alt="Screenshot from 2025-10-15 16-19-55" src="https://github.com/user-attachments/assets/3827d338-93e5-4945-8a55-16ce5c1c9221" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="670" height="267" alt="Screenshot from 2025-10-15 16-21-16" src="https://github.com/user-attachments/assets/45fdeea9-21e1-4003-95db-4143f902aa7b" />

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
<img width="452" height="129" alt="Screenshot from 2025-10-15 17-53-09" src="https://github.com/user-attachments/assets/d42ea069-a190-4c33-8f5b-fb4bb16b1515" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="548" height="122" alt="Screenshot from 2025-10-15 17-54-03" src="https://github.com/user-attachments/assets/44b98d80-384b-4b81-8944-ec007c3877a9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="698" height="881" alt="Screenshot from 2025-10-15 17-55-11" src="https://github.com/user-attachments/assets/884d9bdc-589c-4bc7-b6f2-1dbb180471d4" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1135" height="864" alt="Screenshot from 2025-10-15 18-14-03" src="https://github.com/user-attachments/assets/d6fada4f-7d42-4153-8cac-5da70afc464d" />


tar -xvf backup.tar
## OUTPUT
<img width="805" height="864" alt="Screenshot from 2025-10-15 18-10-51" src="https://github.com/user-attachments/assets/d7ddde35-08d8-4684-9126-098a71fcbf2a" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="309" height="83" alt="Screenshot from 2025-10-15 18-18-15" src="https://github.com/user-attachments/assets/eed5311f-1b5a-4e90-a512-6695ad895d79" />

gunzip backup.tar.gz
## OUTPUT
<img width="741" height="141" alt="Screenshot from 2025-10-15 18-19-03" src="https://github.com/user-attachments/assets/805b8181-1bde-4fca-abb1-dc6bc6f4ab89" />

 
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
<img width="504" height="234" alt="Screenshot from 2025-10-15 18-28-37" src="https://github.com/user-attachments/assets/0728d8b5-e3e0-49e8-b5bb-ba2d17ac4cd9" />


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

 <img width="998" height="731" alt="Screenshot from 2025-10-15 18-34-14" src="https://github.com/user-attachments/assets/d91589e0-636d-4e3d-a334-0fd9aa302683" />

ls file1
## OUTPUT
<img width="494" height="75" alt="Screenshot from 2025-10-15 18-34-40" src="https://github.com/user-attachments/assets/ec60116d-b82b-448a-9aaa-e6bb1d820f89" />

echo $?
## OUTPUT
<img width="494" height="75" alt="Screenshot from 2025-10-15 18-34-50" src="https://github.com/user-attachments/assets/821a64cb-77fd-4b36-891f-dfecbde2ae7b" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="494" height="250" alt="Screenshot from 2025-10-15 18-35-32" src="https://github.com/user-attachments/assets/616b5073-47c2-4e2d-9664-96e034600335" />

 
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

<img width="494" height="228" alt="Screenshot from 2025-10-15 18-37-18" src="https://github.com/user-attachments/assets/b422d3bc-b457-4d9f-81a8-afe1e301a174" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="494" height="228" alt="Screenshot from 2025-10-15 18-40-38" src="https://github.com/user-attachments/assets/cd39db49-2dcf-4e33-ae9d-99f5a447c4ca" />

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
