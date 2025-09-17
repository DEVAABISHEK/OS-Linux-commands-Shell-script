# EX 1 : OS-Linux-commands-Shell-scripting
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
<img width="358" height="158" alt="image" src="https://github.com/user-attachments/assets/b0ef8edd-899b-4949-90f1-0fcc37d9419a" />




cat < file2
## OUTPUT
<img width="418" height="175" alt="image" src="https://github.com/user-attachments/assets/f9357305-3d3a-40ed-bf4b-fb95b695bafe" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="473" height="80" alt="image" src="https://github.com/user-attachments/assets/8a02869c-c258-441f-8b2a-51db38b38901" />

 
comm file1 file2
 ## OUTPUT
 <img width="490" height="232" alt="image" src="https://github.com/user-attachments/assets/17b8abb4-c08c-4cd3-928a-df6b0d9420b1" />


 
diff file1 file2
## OUTPUT
<img width="551" height="302" alt="image" src="https://github.com/user-attachments/assets/2e2de233-f9df-4a5e-9973-68302c07ffa6" />



# Filters

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
<img width="422" height="103" alt="image" src="https://github.com/user-attachments/assets/d4e31eb0-16e9-4d1a-9371-8364e8663b47" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="380" height="135" alt="image" src="https://github.com/user-attachments/assets/211424c7-f412-4380-87c1-302f5cd01ed6" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="407" height="127" alt="image" src="https://github.com/user-attachments/assets/f725b186-a2a5-4544-b689-b16e0f356a4f" />



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
<img width="412" height="82" alt="image" src="https://github.com/user-attachments/assets/f4daf2e3-8954-4525-ae35-e0ed96623212" />




grep hello newfile 
## OUTPUT
<img width="321" height="78" alt="image" src="https://github.com/user-attachments/assets/848d0eda-052d-4f44-9d79-3e281934cfcf" />





grep -v hello newfile 
## OUTPUT
<img width="382" height="77" alt="image" src="https://github.com/user-attachments/assets/6c2034ce-421d-42d5-a425-9a916e3afa30" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="436" height="100" alt="image" src="https://github.com/user-attachments/assets/d5701cae-ec62-41f7-9efa-f6c6f601a8e2" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="445" height="77" alt="image" src="https://github.com/user-attachments/assets/afef6c1a-183f-4ff2-b228-b5fa705601a1" />





grep -R ubuntu /etc
## OUTPUT
<img width="1392" height="448" alt="image" src="https://github.com/user-attachments/assets/62c985cc-30ae-411b-8073-5a61345afe25" />




grep -w -n world newfile   
## OUTPUT
<img width="402" height="98" alt="image" src="https://github.com/user-attachments/assets/95834c18-a002-402c-acb2-ed61adcaa75b" />



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
<img width="455" height="105" alt="image" src="https://github.com/user-attachments/assets/20cdd7d6-30ca-4416-9790-ff2ae9d82c7a" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="397" height="101" alt="image" src="https://github.com/user-attachments/assets/9f36ac3f-ae5e-4d35-8381-50539a4c3972" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="429" height="104" alt="image" src="https://github.com/user-attachments/assets/ac6a9264-f38a-41a5-9d14-4f44b1f6f114" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="361" height="76" alt="image" src="https://github.com/user-attachments/assets/05cc2163-3353-4f91-a221-086fd16f91d4" />




egrep '(world$)' newfile 
## OUTPUT
<img width="367" height="97" alt="image" src="https://github.com/user-attachments/assets/00cffea1-67bc-4c32-ac09-7b944ec0dfc7" />




egrep '(World$)' newfile 
## OUTPUT
<img width="342" height="76" alt="image" src="https://github.com/user-attachments/assets/10aec547-ef56-488a-ace9-331a02450f5e" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="420" height="115" alt="image" src="https://github.com/user-attachments/assets/87d068e7-796d-4918-adda-a01668f5e4f8" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="321" height="76" alt="image" src="https://github.com/user-attachments/assets/58202628-f999-4979-a457-3e85752328b4" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="377" height="73" alt="image" src="https://github.com/user-attachments/assets/3efd3fa6-f549-4678-acd0-21180303836a" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="386" height="76" alt="image" src="https://github.com/user-attachments/assets/7d79acc8-f3b7-45b0-bc5f-d81c912ae031" />



egrep l{2} newfile
## OUTPUT
<img width="312" height="95" alt="image" src="https://github.com/user-attachments/assets/10d56911-d500-4146-ba37-6cebe206ef47" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="342" height="122" alt="image" src="https://github.com/user-attachments/assets/8453aa6f-e22c-4943-b046-8770ab7b8a52" />



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
<img width="358" height="78" alt="image" src="https://github.com/user-attachments/assets/fd2ebc7e-f40c-4486-a628-fa5bd5fcdc14" />




sed -n -e '$p' file23
## OUTPUT
<img width="659" height="326" alt="image" src="https://github.com/user-attachments/assets/972d621c-c4dd-49b9-8d6c-d6482477a67b" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="420" height="250" alt="image" src="https://github.com/user-attachments/assets/888e7005-5830-44d0-a978-c931e36bf8c5" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="401" height="251" alt="image" src="https://github.com/user-attachments/assets/87c93e9d-0e21-48aa-8b87-535a97dd4920" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="426" height="251" alt="image" src="https://github.com/user-attachments/assets/46b27ab1-916a-43bd-8340-5a1b64346844" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="366" height="177" alt="image" src="https://github.com/user-attachments/assets/c9ec9264-5073-4834-b33b-7085ca538cae" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="372" height="127" alt="image" src="https://github.com/user-attachments/assets/537e499d-97ef-4714-82fe-af76032b9463" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="412" height="97" alt="image" src="https://github.com/user-attachments/assets/9a0418f5-affe-4ec2-a939-25ad1b0cd875" />




seq 10 
## OUTPUT
<img width="283" height="305" alt="image" src="https://github.com/user-attachments/assets/e90ac850-45d6-4d35-a8ec-b335fbf744ca" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="337" height="117" alt="image" src="https://github.com/user-attachments/assets/c8db7541-18bb-480a-9eac-e1a4243e8044" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="385" height="128" alt="image" src="https://github.com/user-attachments/assets/eedc91c3-9892-49f3-a7dc-2879f5669d7c" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="346" height="150" alt="image" src="https://github.com/user-attachments/assets/347094e4-bcb3-4a22-860a-4b077342614d" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="320" height="127" alt="image" src="https://github.com/user-attachments/assets/c4f3e9bc-282c-49c3-9796-970ccc3945ec" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="350" height="121" alt="image" src="https://github.com/user-attachments/assets/8157599d-7f8d-46b6-80b5-c61428f6f988" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="396" height="128" alt="image" src="https://github.com/user-attachments/assets/edd4a6a4-1ffe-4fd2-b6ea-d4917870b952" />




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="417" height="117" alt="image" src="https://github.com/user-attachments/assets/aee58ec7-3b65-4f80-a6b8-23dd18581074" />



# Sorting File content
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
<img width="382" height="182" alt="image" src="https://github.com/user-attachments/assets/ce984592-e38b-446d-8a39-3d131960a12b" />



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
<img width="348" height="175" alt="image" src="https://github.com/user-attachments/assets/c4a568e9-7bfd-4ad1-92eb-3bb36383b5a6" />




# Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="463" height="252" alt="image" src="https://github.com/user-attachments/assets/1d01e708-3642-4d9d-82b1-452893988973" />


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
 <img width="371" height="120" alt="image" src="https://github.com/user-attachments/assets/42c9767e-273b-46c5-8276-00534207057f" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="468" height="127" alt="image" src="https://github.com/user-attachments/assets/a4c710d5-5858-427c-99b2-6c1e024f87db" />




# Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="457" height="801" alt="image" src="https://github.com/user-attachments/assets/5b9fd13d-aac0-4945-9828-340c92e9f646" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="808" height="803" alt="image" src="https://github.com/user-attachments/assets/9582a99f-a57e-4dcf-a692-04fba52ebf49" />



tar -xvf backup.tar
## OUTPUT
<img width="790" height="796" alt="image" src="https://github.com/user-attachments/assets/4365e025-2570-482b-ba6a-e107ad1ead6c" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="447" height="75" alt="image" src="https://github.com/user-attachments/assets/3456a815-39ec-49fe-835b-e4e681a6ffe8" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="1433" height="147" alt="image" src="https://github.com/user-attachments/assets/f8ed4a30-ac4e-4db6-a3f0-080a6798766f" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="408" height="130" alt="image" src="https://github.com/user-attachments/assets/69790336-4602-424c-93b4-3dd3a55c9d7a" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="346" height="122" alt="image" src="https://github.com/user-attachments/assets/9741d651-9edf-4a70-a5b9-4a4c804bf40e" />



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
<img width="727" height="450" alt="image" src="https://github.com/user-attachments/assets/3331d870-87e5-4154-b25c-0220ddfaf751" />


 
ls file1
## OUTPUT
<img width="335" height="82" alt="image" src="https://github.com/user-attachments/assets/55590744-924c-45a5-b882-c452093d1d8a" />


echo $?
## OUTPUT 
<img width="282" height="71" alt="image" src="https://github.com/user-attachments/assets/3d41e11d-fd81-42bf-8ec6-00031b8c88f8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="438" height="151" alt="image" src="https://github.com/user-attachments/assets/f6be1ca0-b34d-4208-942d-8a4c13f3e621" />

 
abcd
 
echo $?
 ## OUTPUT
 <img width="366" height="157" alt="image" src="https://github.com/user-attachments/assets/966900f0-f5cb-4d7b-b713-55f50d970809" />



 
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
<img width="411" height="267" alt="image" src="https://github.com/user-attachments/assets/760b1f96-4893-45df-81e8-125e257374f6" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="623" height="148" alt="image" src="https://github.com/user-attachments/assets/c092b37e-d5a9-4401-9861-0cdfd4341e73" />



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
<img width="552" height="77" alt="image" src="https://github.com/user-attachments/assets/5776bbfe-2632-4c4b-b26a-fbe7d3fbcc2b" />



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
<img width="518" height="176" alt="image" src="https://github.com/user-attachments/assets/99741558-3ecb-4050-94df-dd35649fc40f" />




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
<img width="398" height="97" alt="image" src="https://github.com/user-attachments/assets/cc839e09-0da9-4eb3-893e-b0d13bf09835" />


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
<img width="455" height="130" alt="image" src="https://github.com/user-attachments/assets/780d566b-c5bb-4854-9c33-fec653a0e69a" />


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
<img width="370" height="80" alt="image" src="https://github.com/user-attachments/assets/bdde5546-d0c1-42b7-90b6-00cd065d1ce3" />



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
<img width="407" height="76" alt="image" src="https://github.com/user-attachments/assets/43e2ced1-f4ae-4b0e-b10d-7095f3f1fbcc" />


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
<img width="372" height="82" alt="image" src="https://github.com/user-attachments/assets/b5cbd5c1-feae-4fa5-81df-f5c6ae1641c4" />

 
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
<img width="300" height="306" alt="image" src="https://github.com/user-attachments/assets/7c870325-1f82-4672-88f6-48a0d905cf7e" />

 
 
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
$ ./untiltest.sh
## OUTPUT
<img width="277" height="152" alt="image" src="https://github.com/user-attachments/assets/75c9672c-db0a-4a45-bfe1-3cb97d846110" />

 
 
 
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
<img width="330" height="203" alt="image" src="https://github.com/user-attachments/assets/364f11b2-6db4-47fb-8a17-0cd327628d91" />

 
 
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
## OUTPUT
<img width="306" height="151" alt="image" src="https://github.com/user-attachments/assets/f7e529ec-b97c-449e-9575-f2040f1e8a46" />

 
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
<img width="341" height="228" alt="image" src="https://github.com/user-attachments/assets/67e29d24-2f55-4e78-a0a9-835d2c1c564d" />



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
<img width="473" height="177" alt="image" src="https://github.com/user-attachments/assets/369c431c-ee6c-4a2b-9b74-c5126106a68a" />


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
<img width="336" height="205" alt="image" src="https://github.com/user-attachments/assets/c026938d-ae21-4ed5-905f-2378c302d8fd" />


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
 <img width="533" height="348" alt="image" src="https://github.com/user-attachments/assets/9e1cf5fd-27b7-4978-8c11-75d4065e29b8" />


 
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
<img width="308" height="130" alt="image" src="https://github.com/user-attachments/assets/e2eec7ba-ba70-421c-b978-3fe98e5f67a0" />



 
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
<img width="308" height="185" alt="image" src="https://github.com/user-attachments/assets/a6337c53-f116-4a18-a881-b3f2c5115f6b" />

 
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
<img width="391" height="100" alt="image" src="https://github.com/user-attachments/assets/7a061ba4-8969-4407-8744-dc77ffe7c3f4" />



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
<img width="410" height="106" alt="image" src="https://github.com/user-attachments/assets/94ffa8af-04f9-4cf0-9b23-f6087b17dac2" />





 
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
<img width="312" height="81" alt="image" src="https://github.com/user-attachments/assets/ee4d3fea-dd5b-44f5-9889-26ff194c78dd" />



 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="502" height="602" alt="image" src="https://github.com/user-attachments/assets/ed2b2d76-e75f-4966-ac42-b53ef4620f36" />


 
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
<img width="502" height="602" alt="image" src="https://github.com/user-attachments/assets/3b7f0738-f4fd-4ec5-9702-9ae0261adbe9" />


 
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
 ./argshift.sh 1 2 3
## OUTPUT
<img width="502" height="602" alt="image" src="https://github.com/user-attachments/assets/43b28686-b03f-42ea-941c-24c2c8bd47b1" />


 
 
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
<img width="361" height="367" alt="image" src="https://github.com/user-attachments/assets/1cc4b8c5-9c66-48ae-8a16-1be4aa603032" />

 
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
<img width="325" height="252" alt="image" src="https://github.com/user-attachments/assets/b660b1ff-a31c-49b1-ab5c-593e46dbbe6e" />



# RESULT:
The Commands are executed successfully.
