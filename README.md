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
<img width="449" height="171" alt="Screenshot 2025-08-24 183501" src="https://github.com/user-attachments/assets/8ea51023-ac81-4cc1-a857-5e52ecd0e49a" />



cat < file2
## OUTPUT
<img width="434" height="268" alt="Screenshot 2025-08-24 183508" src="https://github.com/user-attachments/assets/3cd1b026-fa8c-46d8-ae3d-dc798e4835bd" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="482" height="131" alt="Screenshot 2025-08-24 183532" src="https://github.com/user-attachments/assets/8d7ae438-58cf-47b8-99ac-07ac7d841154" />


comm file1 file2
 ## OUTPUT
 
<img width="552" height="410" alt="Screenshot 2025-08-24 183604" src="https://github.com/user-attachments/assets/9744efd3-354c-4929-a513-06a263d9e5da" />


 
diff file1 file2
## OUTPUT
<img width="456" height="327" alt="Screenshot 2025-08-24 183625" src="https://github.com/user-attachments/assets/a167f0a4-f7f6-476d-b1c3-750f072cfef8" />




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

<img width="506" height="462" alt="Screenshot 2025-08-24 183851" src="https://github.com/user-attachments/assets/b0db69ad-0a4a-4e0e-945c-efaa4f829d48" />



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world


grep hello newfile 
## OUTPUT

<img width="392" height="127" alt="Screenshot 2025-08-24 184138" src="https://github.com/user-attachments/assets/a6faa6ba-c74f-41d2-8c4c-6af652fe6b9a" />




grep -v hello newfile 
## OUTPUT
<img width="357" height="160" alt="Screenshot 2025-08-24 184156" src="https://github.com/user-attachments/assets/aaf4646d-de63-4cf3-b34c-a1ef3d138028" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="464" height="154" alt="Screenshot 2025-08-24 184603" src="https://github.com/user-attachments/assets/655bba1c-1567-4019-899c-1bf3a0e76bd1" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="508" height="127" alt="Screenshot 2025-08-24 184625" src="https://github.com/user-attachments/assets/c09f1244-5d4d-4713-9c32-496e08557f04" />



grep -R ubuntu /etc
## OUTPUT

<img width="835" height="454" alt="Screenshot 2025-08-24 184736" src="https://github.com/user-attachments/assets/43334717-600f-45ed-9ba5-2be971e8281d" />


grep -w -n world newfile   
## OUTPUT
<img width="537" height="160" alt="Screenshot 2025-08-24 184805" src="https://github.com/user-attachments/assets/1ffc040c-267d-40ce-aa86-c0e5f17f6657" />


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

<img width="569" height="157" alt="Screenshot 2025-08-24 184936" src="https://github.com/user-attachments/assets/f5da0f0e-93db-48f5-b2f1-252d4b558ddf" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="525" height="155" alt="Screenshot 2025-08-24 185020" src="https://github.com/user-attachments/assets/e76770df-0199-4dde-957d-41a72b9f9a5d" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="458" height="130" alt="Screenshot 2025-08-24 185049" src="https://github.com/user-attachments/assets/acf66ca9-cc76-4c49-aec7-b4d89645f8bf" />


egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="520" height="192" alt="Screenshot 2025-08-24 185200" src="https://github.com/user-attachments/assets/2f26cd61-65d8-43a5-91d0-afb8579b7c9c" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="436" height="132" alt="Screenshot 2025-08-24 185226" src="https://github.com/user-attachments/assets/1cc16d25-1f9f-4083-a37d-79ec114b01f4" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="468" height="134" alt="Screenshot 2025-08-24 185252" src="https://github.com/user-attachments/assets/7c0d2231-f6cf-4b38-bcb8-a75a765f32d3" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="435" height="136" alt="Screenshot 2025-08-24 185344" src="https://github.com/user-attachments/assets/ab1daf9e-39ce-4ce0-a9d3-73550bd64ec2" />

egrep l{2} newfile
## OUTPUT

<img width="427" height="147" alt="Screenshot 2025-08-24 185432" src="https://github.com/user-attachments/assets/76ab920d-961b-4fc9-86c4-1a0c041f31dd" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="433" height="181" alt="Screenshot 2025-08-24 185513" src="https://github.com/user-attachments/assets/8d1ce265-f5b8-47d2-88e1-22d06004618a" />


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

<img width="373" height="136" alt="Screenshot 2025-08-24 185602" src="https://github.com/user-attachments/assets/b9c16027-d1fa-4d15-8ac2-b3749fe98f79" />



sed -n -e '$p' file23
## OUTPUT

<img width="362" height="139" alt="Screenshot 2025-08-24 185700" src="https://github.com/user-attachments/assets/08686c2a-6a96-44bc-a7a3-feb45ec624c0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="526" height="333" alt="Screenshot 2025-08-24 185729" src="https://github.com/user-attachments/assets/43df96db-aab2-4c8e-8067-053166f9550f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="508" height="345" alt="Screenshot 2025-08-24 185946" src="https://github.com/user-attachments/assets/3fdef582-733a-4fe7-93ec-0fedfcff5b56" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="552" height="337" alt="Screenshot 2025-08-24 190015" src="https://github.com/user-attachments/assets/73910626-bf9c-4c74-a96a-f817900a17ad" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="481" height="233" alt="Screenshot 2025-08-24 190041" src="https://github.com/user-attachments/assets/445cb1b1-4963-4784-90e0-49a3e962834c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="430" height="182" alt="Screenshot 2025-08-24 190112" src="https://github.com/user-attachments/assets/89c2e722-ae1f-4eea-8b77-00ab0351f5cd" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="520" height="157" alt="Screenshot 2025-08-24 190142" src="https://github.com/user-attachments/assets/401d13c3-237c-455f-b56b-15f9164b5ff4" />


seq 10 
## OUTPUT

<img width="487" height="354" alt="Screenshot 2025-08-24 190157" src="https://github.com/user-attachments/assets/67666e55-cc44-4de7-89a7-3d2082f5e755" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="454" height="181" alt="Screenshot 2025-08-24 190223" src="https://github.com/user-attachments/assets/38e61506-86cf-4a52-84a7-a9ab6a8fb5ec" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="421" height="179" alt="Screenshot 2025-08-24 190248" src="https://github.com/user-attachments/assets/68648d87-27fc-4be7-840d-7ad2c0221853" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="476" height="202" alt="Screenshot 2025-08-24 190310" src="https://github.com/user-attachments/assets/d5c3e15d-8cab-4b3a-9c9c-b936cb08f998" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="431" height="184" alt="Screenshot 2025-08-24 190328" src="https://github.com/user-attachments/assets/09a8c301-0a4b-46d6-b544-23539737bcb6" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="460" height="181" alt="Screenshot 2025-08-24 190358" src="https://github.com/user-attachments/assets/ae0a9042-349f-4e50-9213-dddc8df838fc" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="463" height="186" alt="Screenshot 2025-08-24 190430" src="https://github.com/user-attachments/assets/21359deb-da6e-48df-8fc7-5f2e60b02cca" />


sed -n '2,4{s/$/*/;p}' file23

<img width="504" height="180" alt="Screenshot 2025-08-24 190502" src="https://github.com/user-attachments/assets/73f5a03a-d540-4586-9c25-cee6160fb004" />

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

<img width="437" height="235" alt="Screenshot 2025-08-24 190535" src="https://github.com/user-attachments/assets/a9ad5db7-d32d-40bb-9bb9-aa1db21ce151" />

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

<img width="355" height="180" alt="Screenshot 2025-08-25 205145" src="https://github.com/user-attachments/assets/856db4be-9033-4303-ab1f-7ecda2c7abf3" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="527" height="282" alt="Screenshot 2025-08-25 205152" src="https://github.com/user-attachments/assets/7f941ed8-56de-417a-8510-722dee2b1f70" />

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
<img width="476" height="163" alt="Screenshot 2025-08-25 205206" src="https://github.com/user-attachments/assets/60271695-294a-4f86-8055-3ea928fbe171" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="576" height="155" alt="Screenshot 2025-08-25 205214" src="https://github.com/user-attachments/assets/1b0acaa7-d93b-46a6-9db3-f16b01596dc1" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="620" height="430" alt="Screenshot 2025-08-25 205221" src="https://github.com/user-attachments/assets/2eb6fc76-2d91-49ae-ad3f-eb7e48927426" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="810" height="528" alt="Screenshot 2025-08-25 205312" src="https://github.com/user-attachments/assets/b2e6e220-d510-4922-a6e2-6dc7167dde99" />

tar -xvf backup.tar
## OUTPUT

<img width="697" height="430" alt="Screenshot 2025-08-25 205332" src="https://github.com/user-attachments/assets/c19e8a30-d501-4dd9-b3f2-019f7f49c735" />

gzip backup.tar

ls .gz
## OUTPUT
 
 <img width="489" height="183" alt="Screenshot 2025-08-25 205405" src="https://github.com/user-attachments/assets/c6e5a3d4-0a1d-4d5f-bf6e-38b16805bdbc" />

gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="625" height="220" alt="Screenshot 2025-08-25 205722" src="https://github.com/user-attachments/assets/1ae4aabe-c7e3-4e2b-90cb-52049b09422b" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="416" height="333" alt="Screenshot 2025-08-25 205850" src="https://github.com/user-attachments/assets/d229fbaa-5449-4fd3-8337-a2028b8835aa" />


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

 <img width="730" height="530" alt="Screenshot 2025-08-25 210030" src="https://github.com/user-attachments/assets/32d18c5b-07a4-4465-90e5-0ac9ea1f24ee" />

ls file1
## OUTPUT

<img width="389" height="137" alt="Screenshot 2025-08-25 210041" src="https://github.com/user-attachments/assets/3e6fc774-9d25-422e-ac3c-aeb809d193ab" />

echo $?
## OUTPUT 

<img width="378" height="128" alt="Screenshot 2025-08-25 210120" src="https://github.com/user-attachments/assets/ef7517de-ac89-4d05-b2d0-2d418183150c" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="407" height="134" alt="Screenshot 2025-08-25 210228" src="https://github.com/user-attachments/assets/f7586b02-6cc6-4c24-998d-f0445062c6c3" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="402" height="146" alt="Screenshot 2025-08-25 210247" src="https://github.com/user-attachments/assets/07444eb7-9e16-419d-a09f-7a9a5739ec15" />

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="821" height="232" alt="Screenshot 2025-08-25 210421" src="https://github.com/user-attachments/assets/46826c46-06fb-4a14-9016-1d444f225509" />

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

<img width="694" height="136" alt="Screenshot 2025-08-25 210709" src="https://github.com/user-attachments/assets/a802e5bb-3f8c-4ff5-847a-3f3a780b1fa8" />

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
<img width="689" height="134" alt="Screenshot 2025-08-25 211014" src="https://github.com/user-attachments/assets/4a2e4250-76cf-40bd-8363-f9460a09ec68" />



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

<img width="689" height="134" alt="Screenshot 2025-08-25 211014" src="https://github.com/user-attachments/assets/fc8a59f7-c516-4909-a0e1-72639d63701e" />

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

<img width="681" height="183" alt="Screenshot 2025-08-25 211134" src="https://github.com/user-attachments/assets/eb191c1d-3560-4aa9-a8c3-84601a50a42e" />

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

<img width="688" height="158" alt="Screenshot 2025-08-25 211308" src="https://github.com/user-attachments/assets/a10ed823-d791-4bbf-bb7b-09ec0219a83c" />


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

<img width="738" height="147" alt="Screenshot 2025-08-25 211529" src="https://github.com/user-attachments/assets/c6d8f70c-13a4-4d96-a7cf-94e20a4e9171" />


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

<img width="496" height="184" alt="Screenshot 2025-08-25 211639" src="https://github.com/user-attachments/assets/5cc33e1d-d853-4807-966f-f8dac033a0ee" />


 
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

 <img width="605" height="413" alt="Screenshot 2025-08-25 211929" src="https://github.com/user-attachments/assets/3662de8e-087f-435a-8376-3495cda61934" />

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
## OUTPUT 

 <img width="632" height="237" alt="Screenshot 2025-08-25 220738" src="https://github.com/user-attachments/assets/5cebc801-3b7a-4a4f-9d71-71f456acf152" />

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

<img width="599" height="264" alt="Screenshot 2025-08-25 220712" src="https://github.com/user-attachments/assets/dde78d6f-f7e0-430c-9c92-80a91aaf7d50" />

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

<img width="806" height="385" alt="Screenshot 2025-08-25 221149" src="https://github.com/user-attachments/assets/2b5d2447-b386-466d-a12a-c1afe7494483" />

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

<img width="481" height="276" alt="Screenshot 2025-08-25 221307" src="https://github.com/user-attachments/assets/68a23e83-51e8-4f7a-8636-80aa8aaea899" />


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

<img width="531" height="282" alt="Screenshot 2025-08-25 221423" src="https://github.com/user-attachments/assets/86b7af77-fcc1-4691-a5aa-166f7b56c741" />

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

<img width="468" height="462" alt="Screenshot 2025-08-25 221512" src="https://github.com/user-attachments/assets/d21b3020-c9b5-4284-91ca-109c38079b25" />

 
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

 <img width="791" height="224" alt="Screenshot 2025-08-25 221847" src="https://github.com/user-attachments/assets/ef19cb77-b5e1-47af-be13-98c7e4c9cac2" />

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
 
 <img width="760" height="287" alt="Screenshot 2025-08-25 222141" src="https://github.com/user-attachments/assets/a413a336-e0c4-47c0-965d-0a445e3263d3" />

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

<img width="535" height="206" alt="Screenshot 2025-08-25 222231" src="https://github.com/user-attachments/assets/91b96c2b-89ab-402a-b65c-78371d89e77b" />

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

 ./funcex.sh 
 
## OUTPUT

 <img width="472" height="256" alt="Screenshot 2025-08-25 222409" src="https://github.com/user-attachments/assets/b8ff1f3f-7750-48f9-89ff-42586f18ffc2" />

 ./funcex.sh 1 2

 ## OUTPUT

<img width="488" height="188" alt="Screenshot 2025-08-25 222612" src="https://github.com/user-attachments/assets/db63a801-06af-4f31-b28e-7cf3043883e0" />

 
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

 <img width="488" height="188" alt="Screenshot 2025-08-25 222612" src="https://github.com/user-attachments/assets/85a00d6b-34f9-433d-8d6a-a06352edc1ec" />

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
 
 <img width="466" height="258" alt="Screenshot 2025-08-25 222953" src="https://github.com/user-attachments/assets/d3d3f864-3170-4d0a-bf00-f18d6e7e996f" />

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
 
 <img width="660" height="430" alt="Screenshot 2025-08-25 223043" src="https://github.com/user-attachments/assets/5416f108-1a80-4d3f-9988-ede3b4077021" />

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

<img width="518" height="434" alt="Screenshot 2025-08-25 223138" src="https://github.com/user-attachments/assets/5cc82906-b47f-4ed1-a0b9-55d8b04b7def" />

# RESULT:
The Commands are executed successfully.
