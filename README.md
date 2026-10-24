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
<img width="726" height="115" alt="Screenshot 2026-10-23 234531" src="https://github.com/user-attachments/assets/2fbb3afa-44af-4500-bc36-627d800fe242" />


cat < file2
## OUTPUT
 <img width="720" height="135" alt="Screenshot 2026-10-23 234538" src="https://github.com/user-attachments/assets/2231492d-dc26-4030-b9d0-8c9edee03899" />



# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="735" height="47" alt="Screenshot 2026-10-23 234542" src="https://github.com/user-attachments/assets/404b25d7-9407-43c3-8c18-093a5d9fbb55" />
comm file1 file2
 ## OUTPUT
<img width="807" height="250" alt="image" src="https://github.com/user-attachments/assets/e2693c3c-335e-42fe-9b99-0432c0a09bdd" />



diff file1 file2
## OUTPUT

<img width="510" height="201" alt="image" src="https://github.com/user-attachments/assets/0e56b01c-f98f-482b-a3f4-5ee9edf43715" />


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
<img width="731" height="65" alt="Screenshot 2026-10-23 234604" src="https://github.com/user-attachments/assets/48054b4a-b7ab-4c31-866f-f5c7b0775d7c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="810" height="157" alt="image" src="https://github.com/user-attachments/assets/5e6bf12f-7f79-4a7f-9538-8a149748a61b" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="871" height="157" alt="image" src="https://github.com/user-attachments/assets/fe18d6f2-dd2f-487f-8631-8f75f1e64081" />



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
<img width="815" height="50" alt="image" src="https://github.com/user-attachments/assets/2e224f47-8791-43c4-897b-b9bba63bdadd" />



grep hello newfile 
## OUTPUT


<img width="952" height="57" alt="image" src="https://github.com/user-attachments/assets/02b2446c-2301-4886-8288-74616d063eaa" />



grep -v hello newfile 
## OUTPUT

<img width="926" height="110" alt="Screenshot 2026-10-23 234616" src="https://github.com/user-attachments/assets/35bf153d-1575-4699-87ce-9aed240a1723" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1020" height="72" alt="Screenshot 2026-10-23 234621" src="https://github.com/user-attachments/assets/144839e1-96e5-4816-9d04-dec1b5abfa61" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="970" height="48" alt="Screenshot 2026-10-23 234627" src="https://github.com/user-attachments/assets/6d09001a-d8c0-4fa2-87bd-47a9b2e87e87" />



grep -R ubuntu /etc
## OUTPUT

<img width="1676" height="938" alt="Screenshot 2026-10-23 234650" src="https://github.com/user-attachments/assets/ad12ee3e-66a5-4e8c-88ad-2341e0b1b4eb" />


grep -w -n world newfile   
## OUTPUT

<img width="913" height="95" alt="Screenshot 2026-10-23 234703" src="https://github.com/user-attachments/assets/a410ac18-420f-41b8-a355-6a1b148110f0" />

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
<img width="980" height="62" alt="Screenshot 2026-10-23 234745" src="https://github.com/user-attachments/assets/93150144-8a4b-418a-8f01-5fe0556b0e2f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="946" height="75" alt="image" src="https://github.com/user-attachments/assets/93381a7d-dd22-4f25-96b6-be4ba7c64a49" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="993" height="72" alt="Screenshot 2026-10-23 234749" src="https://github.com/user-attachments/assets/488e9d66-3c9a-4fd8-92af-3d9501e80ab3" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="847" height="41" alt="Screenshot 2026-10-23 234755" src="https://github.com/user-attachments/assets/04b81369-f96d-4626-95c4-4d64d2bf1a6a" />


egrep '(world$)' newfile 
## OUTPUT


<img width="948" height="70" alt="Screenshot 2026-10-23 234759" src="https://github.com/user-attachments/assets/80b3b784-ba60-4ea4-9cc1-106894b9548c" />



egrep '(World$)' newfile 
## OUTPUT

<img width="926" height="51" alt="Screenshot 2026-10-24 092524" src="https://github.com/user-attachments/assets/2b340807-39c1-43fd-90b0-b8f31b4f3ee8" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="980" height="93" alt="Screenshot 2026-10-23 234805" src="https://github.com/user-attachments/assets/8e5d6598-f0ce-4558-914c-3a80ea774513" />

<img width="937" height="55" alt="Screenshot 2026-10-23 234810" src="https://github.com/user-attachments/assets/a98e8530-ea2b-41a4-9371-6a5c8d9cc21e" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="937" height="55" alt="Screenshot 2026-10-23 234810" src="https://github.com/user-attachments/assets/a98e8530-ea2b-41a4-9371-6a5c8d9cc21e" />


<img width="975" height="40" alt="Screenshot 2026-10-23 234820" src="https://github.com/user-attachments/assets/317f37cc-19dd-4eec-8263-fc957b2caca4" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="975" height="40" alt="Screenshot 2026-10-23 234820" src="https://github.com/user-attachments/assets/317f37cc-19dd-4eec-8263-fc957b2caca4" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="975" height="40" alt="Screenshot 2026-10-23 234820" src="https://github.com/user-attachments/assets/317f37cc-19dd-4eec-8263-fc957b2caca4" />




egrep l{2} newfile
## OUTPUT

<img width="896" height="98" alt="Screenshot 2026-10-23 234828" src="https://github.com/user-attachments/assets/fa3db6c6-5cc5-45e2-a734-b197a7e17ec3" />

<img width="1051" height="201" alt="Screenshot 2026-10-23 234832" src="https://github.com/user-attachments/assets/f89d5e6e-c19e-4ac9-b03c-99edd1b24de6" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1051" height="201" alt="Screenshot 2026-10-23 234832" src="https://github.com/user-attachments/assets/f89d5e6e-c19e-4ac9-b03c-99edd1b24de6" />


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


<img width="861" height="42" alt="Screenshot 2026-10-23 234835" src="https://github.com/user-attachments/assets/29fcbec1-be03-402f-bd07-e2be0c6183ee" />


sed -n -e '$p' file23
## OUTPUT

<img width="837" height="46" alt="image" src="https://github.com/user-attachments/assets/fa332182-781f-4931-9a30-38383ed35fab" />


<img width="1090" height="205" alt="Screenshot 2026-10-23 234845" src="https://github.com/user-attachments/assets/2f94eeb8-fcc1-4372-bbc8-1337e61116cc" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT



<img width="1090" height="205" alt="Screenshot 2026-10-23 234845" src="https://github.com/user-attachments/assets/2f94eeb8-fcc1-4372-bbc8-1337e61116cc" />






sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1090" height="205" alt="Screenshot 2026-10-23 234845" src="https://github.com/user-attachments/assets/2f94eeb8-fcc1-4372-bbc8-1337e61116cc" />

<img width="907" height="145" alt="Screenshot 2026-10-23 234904" src="https://github.com/user-attachments/assets/728d3c19-7110-4a3b-ad20-271b7020d7c2" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1123" height="211" alt="Screenshot 2026-10-23 234857" src="https://github.com/user-attachments/assets/7245dd0e-f5cd-49b4-9e71-1afe642ec269" />

<img width="1020" height="95" alt="Screenshot 2026-10-23 234912" src="https://github.com/user-attachments/assets/f2dcbe26-0de7-442e-b3d0-f75899f43639" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="907" height="145" alt="Screenshot 2026-10-23 234904" src="https://github.com/user-attachments/assets/728d3c19-7110-4a3b-ad20-271b7020d7c2" />

<img width="986" height="73" alt="Screenshot 2026-10-23 234917" src="https://github.com/user-attachments/assets/2518fa80-7e50-48a4-8cd8-9c08febc751c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1020" height="95" alt="Screenshot 2026-10-23 234912" src="https://github.com/user-attachments/assets/f2dcbe26-0de7-442e-b3d0-f75899f43639" />

<img width="800" height="257" alt="Screenshot 2026-10-23 234925" src="https://github.com/user-attachments/assets/f765daf3-105a-4e05-8f5e-95502c254210" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="986" height="73" alt="Screenshot 2026-10-23 234917" src="https://github.com/user-attachments/assets/2518fa80-7e50-48a4-8cd8-9c08febc751c" />


<img width="953" height="86" alt="Screenshot 2026-10-23 234931" src="https://github.com/user-attachments/assets/f6064f5e-ff9a-4117-af8a-5ac578b6675b" />

seq 10 
## OUTPUT

<img width="800" height="257" alt="Screenshot 2026-10-23 234925" src="https://github.com/user-attachments/assets/f765daf3-105a-4e05-8f5e-95502c254210" />

<img width="950" height="117" alt="Screenshot 2026-10-23 234936" src="https://github.com/user-attachments/assets/fb032c4b-f66a-494e-ab38-5ab49d6658b8" />

seq 10 | sed -n '4,6p'
## OUTPUT


<img width="950" height="117" alt="Screenshot 2026-10-23 234936" src="https://github.com/user-attachments/assets/fb032c4b-f66a-494e-ab38-5ab49d6658b8" />

<img width="845" height="112" alt="Screenshot 2026-10-23 234941" src="https://github.com/user-attachments/assets/b3ae5345-12ea-4c4c-a55b-5f05a32a15f8" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="845" height="112" alt="Screenshot 2026-10-23 234941" src="https://github.com/user-attachments/assets/b3ae5345-12ea-4c4c-a55b-5f05a32a15f8" />

<img width="900" height="97" alt="Screenshot 2026-10-23 234946" src="https://github.com/user-attachments/assets/1f00f10c-a1ce-42cf-96d2-280c57a1a064" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="900" height="97" alt="Screenshot 2026-10-23 234946" src="https://github.com/user-attachments/assets/1f00f10c-a1ce-42cf-96d2-280c57a1a064" />

<img width="1015" height="90" alt="Screenshot 2026-10-23 234951" src="https://github.com/user-attachments/assets/6df99abe-a5dc-4bf5-a00c-58552a5af329" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1015" height="90" alt="Screenshot 2026-10-23 234951" src="https://github.com/user-attachments/assets/6df99abe-a5dc-4bf5-a00c-58552a5af329" />

<img width="1172" height="92" alt="Screenshot 2026-10-23 234955" src="https://github.com/user-attachments/assets/81c715ef-7cc8-41a2-b156-7d623faefd2b" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="990" height="85" alt="Screenshot 2026-10-23 234959" src="https://github.com/user-attachments/assets/081f27da-ef81-4551-a0ad-6ee501c95076" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="916" height="150" alt="Screenshot 2026-10-23 235003" src="https://github.com/user-attachments/assets/494892eb-fe66-4a01-adec-0396f9f50ac2" />


sed -n '2,4{s/$/*/;p}' file23


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


<img width="705" height="162" alt="Screenshot 2026-10-23 235013" src="https://github.com/user-attachments/assets/f432de50-8ddd-4f22-9b64-615e34c8fff5" />

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


<img width="805" height="157" alt="Screenshot 2026-10-23 235017" src="https://github.com/user-attachments/assets/58e8ae24-787f-4760-8c89-ff8a685e2767" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="1356" height="206" alt="Screenshot 2026-10-23 235023" src="https://github.com/user-attachments/assets/8283f778-7e05-4c17-9f51-c358bae4214d" />

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


<img width="856" height="95" alt="Screenshot 2026-10-23 235028" src="https://github.com/user-attachments/assets/3bbe3b9a-0638-4584-bfff-b967aabded67" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="895" height="102" alt="Screenshot 2026-10-23 235032" src="https://github.com/user-attachments/assets/e5e2a6fb-2828-466d-814b-8d7f4187f662" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT



<img width="935" height="120" alt="Screenshot 2026-10-23 235045" src="https://github.com/user-attachments/assets/aa2dcec0-b741-40e8-8b74-1155dd5f586d" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="983" height="497" alt="Screenshot 2026-10-23 235053" src="https://github.com/user-attachments/assets/d9e739fc-ff66-473e-9f09-ed453f83c590" />

tar -xvf backup.tar
## OUTPUT

<img width="1297" height="476" alt="Screenshot 2026-10-23 235100" src="https://github.com/user-attachments/assets/1f92d696-b351-471c-856a-c2e1f96da26c" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="1062" height="482" alt="Screenshot 2026-10-23 235106" src="https://github.com/user-attachments/assets/33697cfb-8af5-4245-9a33-3147daad0987" />

gunzip backup.tar.gz
## OUTPUT

<img width="1096" height="207" alt="Screenshot 2026-10-23 235121" src="https://github.com/user-attachments/assets/d130f5ca-483b-4693-a8cf-a58c9bbddc2c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="978" height="228" alt="Screenshot 2026-10-23 235132" src="https://github.com/user-attachments/assets/b4ed229c-0f9d-428e-a301-cff461a1a86b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


<img width="1095" height="332" alt="Screenshot 2026-10-23 235139" src="https://github.com/user-attachments/assets/3e8702cc-40b9-404b-9835-e8c5678328fb" />

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


 <img width="645" height="57" alt="Screenshot 2026-10-23 235143" src="https://github.com/user-attachments/assets/67e22305-fefc-4f71-bcd0-a7963ffeabf4" />

ls file1
## OUTPUT

<img width="758" height="47" alt="Screenshot 2026-10-23 235146" src="https://github.com/user-attachments/assets/7d0c1fba-5f01-45c9-b727-6582cda2305d" />

echo $?

## OUTPUT <img width="718" height="93" alt="Screenshot 2026-10-23 235150" src="https://github.com/user-attachments/assets/e70909db-4ded-473f-9915-60ecf18bae1e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="798" height="83" alt="Screenshot 2026-10-23 235156" src="https://github.com/user-attachments/assets/6aff9dad-6b32-40a4-a252-d64d11aa6b3c" />

abcd
 
echo $?
 ## OUTPUT

<img width="762" height="42" alt="Screenshot 2026-10-23 235202" src="https://github.com/user-attachments/assets/576ba3ac-515f-474a-9e0a-c7d6cf161c71" />


 
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


<img width="895" height="503" alt="Screenshot 2026-10-23 235213" src="https://github.com/user-attachments/assets/7f1bd3a6-2bb1-4484-897d-ef0d2fa14ec1" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="867" height="105" alt="Screenshot 2026-10-23 235223" src="https://github.com/user-attachments/assets/115bb905-43d0-4f8b-86c1-db4863152d04" />


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

<img width="1035" height="105" alt="Screenshot 2026-10-23 235228" src="https://github.com/user-attachments/assets/71ec0d23-0f71-48a4-b24c-5321809ea4f7" />

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


<img width="991" height="87" alt="Screenshot 2026-10-23 235232" src="https://github.com/user-attachments/assets/02306647-3cbe-4d52-9323-33073299101b" />


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

<img width="900" height="62" alt="Screenshot 2026-10-23 235236" src="https://github.com/user-attachments/assets/8ab7029c-6818-4383-aa94-773f5a6d0a45" />

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

<img width="858" height="73" alt="Screenshot 2026-10-23 235255" src="https://github.com/user-attachments/assets/373c80b2-a6a3-49ce-ad9b-3eae4b12166f" />

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

<img width="813" height="141" alt="Screenshot 2026-10-24 001735" src="https://github.com/user-attachments/assets/5a83a2cd-2db5-41fd-9aae-88be681eab27" />



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
<img width="793" height="178" alt="Screenshot 2026-10-24 001741" src="https://github.com/user-attachments/assets/84b34c3a-bdad-49a3-81d3-52d85354b408" />


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


<img width="790" height="117" alt="Screenshot 2026-10-24 001747" src="https://github.com/user-attachments/assets/29d8b72d-17fd-4e8b-8b01-7e4743e2955f" />
 
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
