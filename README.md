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
<img width="301" height="146" alt="Screenshot from 2026-01-30 10-06-46" src="https://github.com/user-attachments/assets/17f96028-fbc2-488f-bd7d-569042123b28" />

cat < file2
## OUTPUT
<img width="257" height="152" alt="Screenshot from 2026-01-30 13-49-29" src="https://github.com/user-attachments/assets/25e36a29-4625-44d4-9d88-0a2b507e0423" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="364" height="50" alt="image" src="https://github.com/user-attachments/assets/fac142d4-77b7-4278-93c1-e1beab28de10" />

comm file1 file2
 ## OUTPUT
<img width="402" height="311" alt="Screenshot from 2026-01-30 14-19-40" src="https://github.com/user-attachments/assets/e13b6c57-838f-4952-89ef-035af2b4161d" />

 
diff file1 file2
## OUTPUT
<img width="400" height="266" alt="image" src="https://github.com/user-attachments/assets/3f07b519-b3d2-4ce0-b486-5eb818cb53a5" />


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
<img width="399" height="67" alt="image" src="https://github.com/user-attachments/assets/55fc4fc5-e7e1-4de4-a0b2-06b047d743cf" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="495" height="165" alt="image" src="https://github.com/user-attachments/assets/83a1cbe0-12b5-429e-8533-ccab4edcf295" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="497" height="128" alt="image" src="https://github.com/user-attachments/assets/5bb6d257-34a8-43fa-9cf6-0b763c8078f2" />


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
<img width="1074" height="90" alt="image" src="https://github.com/user-attachments/assets/344c0177-a7d8-4c7a-a1cc-8aa227e43497" />



grep hello newfile 
## OUTPUT

<img width="1097" height="90" alt="image" src="https://github.com/user-attachments/assets/2e4859de-c44a-4c84-9b45-e23124311121" />



grep -v hello newfile 
## OUTPUT
<img width="1148" height="82" alt="{6337A6C4-8315-4E50-BE17-9CB4F451392A}" src="https://github.com/user-attachments/assets/012d3c30-d52b-4b86-bd19-ce6f506240f2" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="1053" height="151" alt="image" src="https://github.com/user-attachments/assets/fcef76da-03e4-4e09-aea0-e2a706bad44e" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="742" height="103" alt="{9B92D462-CA0E-4469-84B3-307244E4B41B}" src="https://github.com/user-attachments/assets/778a5409-e78b-433b-ba4e-ee9adfa6139a" />




grep -R ubuntu /etc
## OUTPUT
<img width="743" height="741" alt="{E2C11F20-5FA6-4A8D-9E18-FEA6B5BBFD20}" src="https://github.com/user-attachments/assets/2828df95-1801-436d-a56b-176441d0f75c" />



grep -w -n world newfile   
## OUTPUT
<img width="943" height="101" alt="image" src="https://github.com/user-attachments/assets/9a26712d-9d76-4805-831c-4dca151a2647" />


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
<img width="740" height="106" alt="image" src="https://github.com/user-attachments/assets/97d1bc7b-d6e7-4fa1-81ca-1802e929bd98" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="740" height="106" alt="image" src="https://github.com/user-attachments/assets/61b74975-ecac-40cc-b747-ea2b79dd6d4f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="600" height="89" alt="image" src="https://github.com/user-attachments/assets/d06617db-7b3c-4ec9-bf5f-37c2a67df157" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="587" height="47" alt="image" src="https://github.com/user-attachments/assets/8ba4ca90-07bb-4ddc-8587-46f5b2aad3fa" />


egrep '(world$)' newfile 
## OUTPUT
<img width="586" height="68" alt="image" src="https://github.com/user-attachments/assets/94e157d1-cf9f-4137-958c-d27fec316305" />



egrep '(World$)' newfile 
## OUTPUT
<img width="594" height="45" alt="image" src="https://github.com/user-attachments/assets/125e0b4a-c1ec-40a0-8558-3a3c30fd5a95" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="598" height="112" alt="image" src="https://github.com/user-attachments/assets/e46babbc-1ac6-4625-8ce2-23c75dd10c84" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="573" height="53" alt="image" src="https://github.com/user-attachments/assets/cd3cff2e-a63d-4e0b-b045-4d7dc7a5e23c" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="591" height="72" alt="image" src="https://github.com/user-attachments/assets/dc728037-ab66-4e6a-ba2d-ec484bb8da01" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="598" height="71" alt="image" src="https://github.com/user-attachments/assets/73130cd2-f2b5-4240-989c-83a66771e56e" />


egrep l{2} newfile
## OUTPUT

<img width="536" height="69" alt="image" src="https://github.com/user-attachments/assets/1f07946a-5c5a-42d6-ad87-6613b2286a63" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="569" height="86" alt="image" src="https://github.com/user-attachments/assets/01955d98-e489-4f49-b1a0-f473df1a2fb9" />


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

<img width="549" height="41" alt="image" src="https://github.com/user-attachments/assets/7582dfdc-5bcf-4c88-876e-989ca2ede2b8" />


sed -n -e '$p' file23
## OUTPUT

<img width="553" height="43" alt="image" src="https://github.com/user-attachments/assets/2a176bc3-d9c7-4d7e-a2fc-0ca338058b17" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="597" height="219" alt="image" src="https://github.com/user-attachments/assets/7a5f4c0a-557a-40d3-b694-5df74848b19c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="593" height="221" alt="image" src="https://github.com/user-attachments/assets/c64fde0c-c32c-4dec-8e61-5b6e92598561" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="596" height="220" alt="image" src="https://github.com/user-attachments/assets/f091704e-741d-4605-bce9-c67b387d70cd" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="571" height="134" alt="image" src="https://github.com/user-attachments/assets/72a0d016-b5dd-4046-9458-d22883cf7cfe" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="594" height="110" alt="image" src="https://github.com/user-attachments/assets/c5467783-2129-439b-aab7-284db648d93e" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="596" height="93" alt="image" src="https://github.com/user-attachments/assets/52fee354-59b4-47fb-9e3f-7c37227f79e0" />


seq 10 
## OUTPUT
<img width="407" height="245" alt="image" src="https://github.com/user-attachments/assets/35330981-82ad-4f18-ad19-58f928e4ebfb" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="575" height="91" alt="image" src="https://github.com/user-attachments/assets/27e97a21-6bf7-430c-a6c1-3668eb6c30ee" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="559" height="90" alt="image" src="https://github.com/user-attachments/assets/60008e50-0ec1-41bb-a178-7c37f3c4ceba" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="568" height="117" alt="image" src="https://github.com/user-attachments/assets/57acbe23-699c-45e3-bd41-373696876089" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="559" height="92" alt="image" src="https://github.com/user-attachments/assets/3f13aab4-2378-4286-9632-3b2090bcd9d1" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="583" height="90" alt="image" src="https://github.com/user-attachments/assets/67a0df4b-daf4-4fce-822b-27cdbb7a0406" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="595" height="111" alt="image" src="https://github.com/user-attachments/assets/ca3e399d-249c-4425-a52d-8e59e1886e00" />



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
<img width="458" height="134" alt="image" src="https://github.com/user-attachments/assets/62ef5a4c-240e-4ad8-b81a-59dc01ea1c0a" />


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

<img width="454" height="136" alt="image" src="https://github.com/user-attachments/assets/485a6467-8474-463e-8cab-d20f0a99737e" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="602" height="223" alt="image" src="https://github.com/user-attachments/assets/51fe5f4f-7018-4f12-9abf-00facca036b4" />

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


<img width="586" height="113" alt="image" src="https://github.com/user-attachments/assets/f802b599-e2e5-4794-a760-1744c7ddba5b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="593" height="118" alt="image" src="https://github.com/user-attachments/assets/5a363f57-4ea3-4605-9570-b75ec48c28e9" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="558" height="200" alt="image" src="https://github.com/user-attachments/assets/705d0a98-68f6-40d1-ae3e-3f15bb5573b5" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="598" height="226" alt="image" src="https://github.com/user-attachments/assets/6d845993-9202-4648-a10b-2706708b561a" />


tar -xvf backup.tar
## OUTPUT
<img width="591" height="220" alt="image" src="https://github.com/user-attachments/assets/0d8bfae1-506d-4396-b9c8-1f806987e58a" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="560" height="48" alt="image" src="https://github.com/user-attachments/assets/3734293a-9ba9-4467-b8ff-73e39cf24124" />

gunzip backup.tar.gz
## OUTPUT
<img width="606" height="113" alt="image" src="https://github.com/user-attachments/assets/5432e4a7-62e7-49b2-84a4-ba2c0ddcfa8e" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="593" height="92" alt="image" src="https://github.com/user-attachments/assets/49cbb9b4-9170-4988-b6cb-05b9255c1209" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="526" height="87" alt="image" src="https://github.com/user-attachments/assets/1c0c60c5-d186-4f89-a846-1c27abfbf37e" />


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
<img width="598" height="353" alt="image" src="https://github.com/user-attachments/assets/7d48503a-18e4-4a76-ab77-a90270ab37ab" />


 
ls file1
## OUTPUT
<img width="434" height="48" alt="image" src="https://github.com/user-attachments/assets/feba4519-83b6-45cb-ae2e-e502b2eceeb3" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="411" height="44" alt="image" src="https://github.com/user-attachments/assets/879c40e7-3802-4287-b8af-0c14f7e7e12e" />

abcd
 
echo $?
 ## OUTPUT

<img width="427" height="43" alt="image" src="https://github.com/user-attachments/assets/6148cf38-84d0-42d9-99d2-c97a2a4b4d1b" />

 
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
<img width="546" height="162" alt="image" src="https://github.com/user-attachments/assets/ee49d6f0-d195-48c2-900d-c74f228c04d0" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="565" height="91" alt="image" src="https://github.com/user-attachments/assets/44f5d411-786c-48c7-b749-dbd664f2526d" />


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
<img width="565" height="91" alt="image" src="https://github.com/user-attachments/assets/14ee023a-e94f-48ff-96c7-4b18921e1d8b" />

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

<img width="548" height="135" alt="image" src="https://github.com/user-attachments/assets/40598305-0f91-494f-9842-ae0356d8f6bd" />


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
<img width="554" height="110" alt="image" src="https://github.com/user-attachments/assets/c8bc4f40-10db-493d-8d02-954af0633c67" />

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
<img width="567" height="90" alt="image" src="https://github.com/user-attachments/assets/b6a03ede-18d1-4137-accd-c87c663e477c" />


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
<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/67ec577e-c039-46a9-b8df-e78ffe67d3dd" />

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
<img width="562" height="153" alt="image" src="https://github.com/user-attachments/assets/6a6c9084-1996-49c8-92f3-b9dd240b6bf3" />

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
<img width="572" height="155" alt="image" src="https://github.com/user-attachments/assets/4a820037-a32a-491b-a0b9-734d2be98792" />

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
<img width="565" height="305" alt="image" src="https://github.com/user-attachments/assets/482c052b-e647-4db2-9a57-677e75c70ec9" />

 
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
<img width="583" height="179" alt="image" src="https://github.com/user-attachments/assets/3637f545-bd0f-46fe-bd14-7b111b281162" />

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
 <img width="583" height="179" alt="image" src="https://github.com/user-attachments/assets/b07b2a4f-89af-4e85-90c6-8f4f924ab531" />

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
<img width="544" height="93" alt="image" src="https://github.com/user-attachments/assets/95fa1e5c-18ef-4034-b4ab-f369dbf1f335" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="548" height="91" alt="image" src="https://github.com/user-attachments/assets/3c7e6b69-bb7f-47f7-8cb7-988f4e71cee0" />


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
<img width="546" height="71" alt="image" src="https://github.com/user-attachments/assets/0568d62d-33a1-4914-9c83-049eb7915fe4" />

 
 ./funcex.sh 1 2
<img width="519" height="47" alt="image" src="https://github.com/user-attachments/assets/fed72fcf-e63f-48e7-93a7-04713ac8694c" />

 
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
 <img width="570" height="93" alt="image" src="https://github.com/user-attachments/assets/d62aeebc-328c-4946-baed-36ece16507e1" />

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
<img width="571" height="110" alt="image" src="https://github.com/user-attachments/assets/2017fa33-0e95-4609-be31-66a8d88f708c" />

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
 
 <img width="568" height="329" alt="image" src="https://github.com/user-attachments/assets/6c0edda0-a69d-47fa-998a-ba71b4ac14a5" />

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
 ![Uploading image.png…]()

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
<img width="1056" height="208" alt="{743F218B-3E79-48B8-B53C-C2B30F45950A}" src="https://github.com/user-attachments/assets/a131c1f5-289a-4676-8038-bcaffded81b8" />


# RESULT:
The Commands are executed successfully.
