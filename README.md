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
<img width="521" height="217" alt="image" src="https://github.com/user-attachments/assets/4e9d4a31-4a6e-46ab-9337-56d2b30111cd" />



cat < file2
## OUTPUT
<img width="457" height="228" alt="image" src="https://github.com/user-attachments/assets/d669a622-410a-42f3-8ada-f49808d6703c" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="522" height="111" alt="image" src="https://github.com/user-attachments/assets/bb338511-e82e-4682-9f66-9c256549e295" />

comm file1 file2
 ## OUTPUT
<img width="672" height="360" alt="image" src="https://github.com/user-attachments/assets/827e503c-c3d9-4c49-a0e3-e60994c5b31e" />


 
diff file1 file2
## OUTPUT
<img width="561" height="390" alt="image" src="https://github.com/user-attachments/assets/cf02a982-2816-406f-988a-dd077c06054b" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
## OUTPUT
<img width="502" height="112" alt="image" src="https://github.com/user-attachments/assets/c9a856ea-13ab-4be5-8cf9-7af115470634" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
## OUTPUT
<img width="542" height="155" alt="image" src="https://github.com/user-attachments/assets/635fbded-5b90-4e83-83a1-462790d2ed9e" />


cut -c1-3 file11
## OUTPUT

<img width="510" height="125" alt="image" src="https://github.com/user-attachments/assets/2f973afd-4a8b-4d3e-b168-55c633cf0608" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="522" height="152" alt="image" src="https://github.com/user-attachments/assets/6150f750-1689-4ad9-b744-0e127da08e8b" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="140" alt="image" src="https://github.com/user-attachments/assets/962e0b79-e6ab-41e0-936c-4cfc65bf440f" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
## OUTPUT
 <img width="517" height="131" alt="image" src="https://github.com/user-attachments/assets/4afd9b3a-cf26-4107-a91e-93cc5f11c04a" />

grep Hello newfile 
## OUTPUT
<img width="395" height="88" alt="image" src="https://github.com/user-attachments/assets/66eaba6e-e7a5-4238-b6a9-6942eaaa4b06" />

grep hello newfile 
## OUTPUT
<img width="340" height="162" alt="image" src="https://github.com/user-attachments/assets/ac608bae-8602-440a-ad4d-d436ecd9d82b" />
grep -v hello newfile 
## OUTPUT
<img width="430" height="90" alt="image" src="https://github.com/user-attachments/assets/31dafa63-9334-423d-9d7c-ff4dabf2c30d" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="600" height="200" alt="image" src="https://github.com/user-attachments/assets/01b62522-8767-4235-b2ba-66ac1900bdcc" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="582" height="87" alt="image" src="https://github.com/user-attachments/assets/6e3718e7-0c02-4d60-9c80-f1bf719f5134" />

grep -R ubuntu /etc
## OUTPUT
<img width="992" height="692" alt="image" src="https://github.com/user-attachments/assets/99aa1062-3dc4-47e2-9687-a4c92fd2a596" />

grep -w -n world newfile   
## OUTPUT

<img width="517" height="160" alt="image" src="https://github.com/user-attachments/assets/7129b524-a678-4d28-8af3-d2e456326072" />

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
## OUTPUT
<img width="613" height="427" alt="image" src="https://github.com/user-attachments/assets/034c8a54-a6c4-4bc2-87c2-8f9b6083dd11" />

egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="552" height="157" alt="image" src="https://github.com/user-attachments/assets/579a0514-f8b8-45e7-badc-ad7c98f1cccc" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="752" height="182" alt="image" src="https://github.com/user-attachments/assets/9cb55c90-d94e-4e23-add6-7c65ddac63ac" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="558" height="126" alt="image" src="https://github.com/user-attachments/assets/648b485f-8428-414c-84a2-c0cfdbfc1e75" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="545" height="92" alt="image" src="https://github.com/user-attachments/assets/9fb1d10a-5269-4797-91e9-83d3609312c1" />


egrep '(world$)' newfile 
## OUTPUT
<img width="547" height="127" alt="image" src="https://github.com/user-attachments/assets/410f543e-fc60-40a0-9029-1c4eb136775e" />

egrep '(World$)' newfile 
## OUTPUT

<img width="582" height="90" alt="image" src="https://github.com/user-attachments/assets/eb4c8a39-cb69-4436-831d-fbadd718f38d" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="592" height="167" alt="image" src="https://github.com/user-attachments/assets/79f52d0c-03cf-428f-91f8-ec5f9ab0083c" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="625" height="98" alt="image" src="https://github.com/user-attachments/assets/27c8a883-831a-4f68-bf7d-5e4c760b9bf0" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="602" height="90" alt="image" src="https://github.com/user-attachments/assets/c7e02b0b-2d1b-4e14-ac05-6d1a6a22cbe7" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="627" height="102" alt="image" src="https://github.com/user-attachments/assets/538fc3c8-97f7-45ed-845b-5507a0f7bd6b" />

egrep l{2} newfile
## OUTPUT
<img width="563" height="122" alt="image" src="https://github.com/user-attachments/assets/6305d281-1bf0-42fa-a2c2-d5d7460c4380" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="521" height="147" alt="image" src="https://github.com/user-attachments/assets/6f9c7712-5716-4f40-9819-18e9ebb83d26" />

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
<img width="527" height="92" alt="image" src="https://github.com/user-attachments/assets/a8487009-0698-47ff-9a17-cb504bb90306" />



sed -n -e '$p' file23
## OUTPUT

<img width="610" height="95" alt="image" src="https://github.com/user-attachments/assets/b0f0418c-8e24-4d1c-b06d-f1cd0aa28530" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="651" height="313" alt="image" src="https://github.com/user-attachments/assets/10c57bc5-3d25-4511-a3b0-43782ea8be65" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="647" height="312" alt="image" src="https://github.com/user-attachments/assets/8825c793-6036-48b1-80e3-2e2b5590c576" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="732" height="313" alt="image" src="https://github.com/user-attachments/assets/0e400588-5501-4681-bd9b-72075e1e80c2" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="586" height="218" alt="image" src="https://github.com/user-attachments/assets/0480d98c-afb4-4dbf-b1c0-5d4ca98c27ef" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="612" height="160" alt="image" src="https://github.com/user-attachments/assets/7c0d6a6d-fad3-4b80-abac-8c71568f81db" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="587" height="127" alt="image" src="https://github.com/user-attachments/assets/e88c2c69-a0c7-4d39-883a-926fef8c1fbe" />


seq 10 
## OUTPUT

<img width="572" height="368" alt="image" src="https://github.com/user-attachments/assets/72a512fb-8a6f-4b57-864a-09eab64e27c9" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="507" height="150" alt="image" src="https://github.com/user-attachments/assets/d5b8b6f3-223c-4623-abba-36df5c0dc435" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="507" height="150" alt="image" src="https://github.com/user-attachments/assets/6137d033-999e-437e-828e-e7041f636f7a" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="627" height="185" alt="image" src="https://github.com/user-attachments/assets/748559d6-8d39-432f-800d-58fe5093d624" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="543" height="147" alt="image" src="https://github.com/user-attachments/assets/2ec442d6-fcdb-4330-8860-160a2186d59a" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="553" height="136" alt="image" src="https://github.com/user-attachments/assets/1e3a4b84-4111-4744-853b-f4241dfb9722" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="580" height="158" alt="image" src="https://github.com/user-attachments/assets/64587bdd-746b-451b-a8be-2d207fbf1278" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="617" height="163" alt="image" src="https://github.com/user-attachments/assets/c3a460d9-cd5c-4ed9-811b-d31b4634509b" />

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

<img width="661" height="440" alt="image" src="https://github.com/user-attachments/assets/6ef0635d-3087-485d-b776-4474a4a08635" />


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

<img width="830" height="455" alt="image" src="https://github.com/user-attachments/assets/78d6afd1-dfec-4190-acde-a2bb1bf8102f" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="655" height="306" alt="image" src="https://github.com/user-attachments/assets/e9019559-8c45-4968-b75e-2826c9fb8eae" />

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
## OUTPUT

<img width="585" height="313" alt="image" src="https://github.com/user-attachments/assets/2fd3e1d4-b5d2-4fc8-9d2c-d44abd8e0b59" />

cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="583" height="152" alt="image" src="https://github.com/user-attachments/assets/f9f8fcbc-4ba8-49ac-878a-3d9121458baf" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="681" height="156" alt="image" src="https://github.com/user-attachments/assets/3a0be761-f7e1-4309-83ca-caaac76b9415" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="745" height="776" alt="image" src="https://github.com/user-attachments/assets/82112ac4-6ddc-4015-b871-752b7bf5393a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="892" height="782" alt="image" src="https://github.com/user-attachments/assets/5a11c80e-9be3-4dd8-bdfa-9e7d1988bb15" />


tar -xvf backup.tar
## OUTPUT

<img width="795" height="743" alt="image" src="https://github.com/user-attachments/assets/642c29bb-9455-4b73-83e7-3a7dc2ebd4d1" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="590" height="132" alt="image" src="https://github.com/user-attachments/assets/05183965-9377-438e-9482-64a3ccfe5384" />

gunzip backup.tar.gz
## OUTPUT

<img width="488" height="97" alt="image" src="https://github.com/user-attachments/assets/70df623c-399d-4078-90af-f9adfca0ee24" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="723" height="167" alt="image" src="https://github.com/user-attachments/assets/9cdfe133-ede3-42e3-aaf5-5e3b338cd00c" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="731" height="140" alt="image" src="https://github.com/user-attachments/assets/95c9e7e7-c07d-4809-ac8c-338cef7f71e5" />


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

<img width="877" height="487" alt="image" src="https://github.com/user-attachments/assets/2f7011f0-5eb6-4a19-85cd-f84754ccbb6d" />

 
ls file1
## OUTPUT

<img width="322" height="77" alt="image" src="https://github.com/user-attachments/assets/38b9ad25-055d-45cf-a210-8dedbc99e301" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="301" height="77" alt="image" src="https://github.com/user-attachments/assets/26174825-d43a-4e29-8eff-7b8cd6339077" />

echo $?
## OUTPUT 
 <img width="396" height="73" alt="image" src="https://github.com/user-attachments/assets/91c93752-fb9b-422b-a1b3-f85bc28aedea" />

abcd
 
echo $?
 ## OUTPUT

<img width="391" height="75" alt="image" src="https://github.com/user-attachments/assets/1a6deaf2-3b39-4d51-9cd6-0fd1005e7a9c" />

 
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
<img width="456" height="281" alt="image" src="https://github.com/user-attachments/assets/4bd172d5-885e-4e35-ac23-1e26c225bd45" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="743" height="152" alt="image" src="https://github.com/user-attachments/assets/d7bb38b0-2df2-421c-8d1d-634f69fbd3fe" />


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
<img width="722" height="232" alt="image" src="https://github.com/user-attachments/assets/b56dda1b-87cb-47ac-91d5-f06300c7a661" />

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

<img width="675" height="268" alt="image" src="https://github.com/user-attachments/assets/a8fb452a-e147-4721-ae11-a783feebef68" />

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
<img width="672" height="182" alt="image" src="https://github.com/user-attachments/assets/262a5308-e6ab-4c36-ae64-46eef9734505" />

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
<img width="765" height="213" alt="image" src="https://github.com/user-attachments/assets/25735566-247e-437e-810c-a715e84dd482" />

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
<img width="771" height="162" alt="image" src="https://github.com/user-attachments/assets/daeae78a-0708-477b-abf8-fdcc441c313c" />


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
<img width="772" height="157" alt="image" src="https://github.com/user-attachments/assets/1799872c-95ee-45ae-ad44-6926cfab499e" />

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
<img width="390" height="128" alt="image" src="https://github.com/user-attachments/assets/4eb919c1-d2c7-4855-aac8-1057880bb58d" />

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
<img width="410" height="362" alt="image" src="https://github.com/user-attachments/assets/0dc983f6-a47d-4fd5-a272-c8d46d176462" />
 
 
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
<img width="566" height="181" alt="image" src="https://github.com/user-attachments/assets/d03d047d-f053-4ac3-94c9-fb1ca73ef8b9" />
 
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
 <img width="730" height="266" alt="image" src="https://github.com/user-attachments/assets/2ec27d8b-a3c9-4c04-b517-d0d0b68dde11" />

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
 <img width="716" height="237" alt="image" src="https://github.com/user-attachments/assets/bfc09ec6-6d22-4406-8a21-605c5792b6b7" />

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
 <img width="651" height="271" alt="image" src="https://github.com/user-attachments/assets/d83483dc-abb6-44ae-b341-9b8fe09406a3" />

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

<img width="397" height="242" alt="image" src="https://github.com/user-attachments/assets/ab023875-bad2-4e52-a2e4-df7853043682" />

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
<img width="247" height="180" alt="image" src="https://github.com/user-attachments/assets/7420274c-363e-4b71-81ec-0fdeb7efa76f" />

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
<img width="402" height="245" alt="image" src="https://github.com/user-attachments/assets/8ebad6cd-2f3f-4275-9b66-dde91cb9f232" />

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

 <img width="357" height="430" alt="image" src="https://github.com/user-attachments/assets/d8841623-c3b0-45f4-af6f-45ad29dbb2ce" />

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
 <img width="287" height="110" alt="image" src="https://github.com/user-attachments/assets/ee986bf0-c5ed-43ed-bba2-cd70535c3122" />

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
 <img width="357" height="196" alt="image" src="https://github.com/user-attachments/assets/92af8deb-43ed-4272-8f16-2787aa042042" />

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

<img width="423" height="105" alt="image" src="https://github.com/user-attachments/assets/b2605559-a849-4a06-9dbd-98155972d3a7" />

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
 <img width="427" height="113" alt="image" src="https://github.com/user-attachments/assets/4200d30b-151b-487f-8a02-6065cd17eabe" />

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

 <img width="351" height="87" alt="image" src="https://github.com/user-attachments/assets/a3dffbf7-3282-4f06-9bb8-d03ba89a856e" />

 ./funcex.sh 1 2
 
<img width="297" height="87" alt="image" src="https://github.com/user-attachments/assets/49442d71-cfd6-445e-9e79-1b3d512ba2d6" />

 
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


<img width="322" height="142" alt="image" src="https://github.com/user-attachments/assets/d5a4e1c5-bdc8-4ce4-8675-215f9246fd91" />


# RESULT:
The Commands are executed successfully.
