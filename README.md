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

<img width="417" height="156" alt="Screenshot 2026-08-01 195912" src="https://github.com/user-attachments/assets/4cbe7450-228c-4888-b413-2a0fa236ad98" />


cat < file2
## OUTPUT

<img width="467" height="195" alt="image" src="https://github.com/user-attachments/assets/b5773944-d5d0-448e-b281-f39343e4687e" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="397" height="77" alt="image" src="https://github.com/user-attachments/assets/63f72ba3-dfe1-436f-b051-3eeba888aece" />

comm file1 file2
 ## OUTPUT

<img width="402" height="228" alt="image" src="https://github.com/user-attachments/assets/f6876a48-57c7-4ede-8fd3-76e1209cc9f6" />

 
diff file1 file2
## OUTPUT

<img width="382" height="282" alt="image" src="https://github.com/user-attachments/assets/0b68d0f1-ecf3-4e7e-9c32-8e4875d8ac66" />


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

<img width="388" height="107" alt="image" src="https://github.com/user-attachments/assets/de08cf68-035f-41d9-86a0-993097de3079" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="362" height="132" alt="image" src="https://github.com/user-attachments/assets/818fa7d2-a991-41ca-8184-589062da0f74" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="350" height="125" alt="image" src="https://github.com/user-attachments/assets/111880f9-b8b8-4329-8926-5906084f96f6" />


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

<img width="398" height="83" alt="image" src="https://github.com/user-attachments/assets/4cef5771-cdb7-424a-bdb4-a723951c5d33" />


grep hello newfile 
## OUTPUT

<img width="352" height="76" alt="image" src="https://github.com/user-attachments/assets/cfefe90a-377d-4603-a91c-d921916bec79" />



grep -v hello newfile 
## OUTPUT

<img width="352" height="72" alt="image" src="https://github.com/user-attachments/assets/36596f67-38ac-49e7-879a-422ed6375008" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="395" height="102" alt="image" src="https://github.com/user-attachments/assets/4c5b829c-9c05-4614-bb6f-897d3bae638a" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="440" height="80" alt="image" src="https://github.com/user-attachments/assets/9fa79bed-c730-4e0d-8b59-1a8f6ba75349" />



grep -R ubuntu /etc
## OUTPUT

<img width="822" height="537" alt="image" src="https://github.com/user-attachments/assets/92882edd-e6af-4a25-8a2e-c51ac3a1025a" />


grep -w -n world newfile   
## OUTPUT

<img width="397" height="102" alt="image" src="https://github.com/user-attachments/assets/ba0fb19a-43a6-4e82-8787-cb2407efa5ea" />


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

<img width="387" height="100" alt="image" src="https://github.com/user-attachments/assets/94e12a40-4b63-4a0a-ac29-44e3593ad23d" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="403" height="105" alt="image" src="https://github.com/user-attachments/assets/79cb70fc-0cb9-4316-87f8-c5ea58a362a8" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="415" height="103" alt="image" src="https://github.com/user-attachments/assets/0a470df2-6506-4c86-b0bb-5cc385e77847" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="342" height="82" alt="image" src="https://github.com/user-attachments/assets/fd4c1d3d-fb87-4f05-bd52-c33e0dc24e7e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="346" height="76" alt="image" src="https://github.com/user-attachments/assets/4ae6b6ba-ea81-45fa-820d-5b2992921a09" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="385" height="128" alt="image" src="https://github.com/user-attachments/assets/67005031-3856-418f-a7ac-31bb526824eb" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="333" height="75" alt="image" src="https://github.com/user-attachments/assets/a989a5ba-6c8b-4668-8a3a-c7581c272b6c" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="367" height="85" alt="image" src="https://github.com/user-attachments/assets/b1d2141c-052d-4a50-99bf-33b6fc43e61c" />


egrep l{2} newfile
## OUTPUT

<img width="371" height="100" alt="image" src="https://github.com/user-attachments/assets/8f586af7-1b51-4587-84d4-9174402156fb" />


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

<img width="412" height="72" alt="image" src="https://github.com/user-attachments/assets/85842bfe-3082-478a-9223-6b523d1ad967" />


sed -n -e '$p' file23
## OUTPUT

<img width="368" height="73" alt="image" src="https://github.com/user-attachments/assets/80f3a11d-7549-4d92-b583-d249d8e32acd" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="427" height="247" alt="image" src="https://github.com/user-attachments/assets/b8012491-adad-4371-b3ca-d8fc3895c82e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="390" height="247" alt="image" src="https://github.com/user-attachments/assets/2eb8cf61-02a4-448b-85d5-7b3f4b2aa21f" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="363" height="126" alt="image" src="https://github.com/user-attachments/assets/e44292ff-30ff-40fa-b70f-af815fe93dce" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="400" height="102" alt="image" src="https://github.com/user-attachments/assets/11a8ec97-8d51-4276-a062-854268dba212" />


seq 10 
## OUTPUT

<img width="340" height="302" alt="image" src="https://github.com/user-attachments/assets/8a46d6e7-6d64-4d90-9b24-fcb4c0c1c6da" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="350" height="125" alt="image" src="https://github.com/user-attachments/assets/09b00e44-47ad-4fba-b60d-e41ebd3509bb" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="367" height="150" alt="image" src="https://github.com/user-attachments/assets/52f40a71-82ee-4361-a34f-d31d78717a74" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="357" height="118" alt="image" src="https://github.com/user-attachments/assets/30f5c0be-47d3-4839-a2f3-9a9d744ae680" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="375" height="128" alt="image" src="https://github.com/user-attachments/assets/be58fdd2-7436-4600-9beb-b8d99414e3c7" />


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

<img width="416" height="172" alt="image" src="https://github.com/user-attachments/assets/65c3787e-bc5b-4c28-83fe-1a10252c1eae" />


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

<img width="400" height="171" alt="image" src="https://github.com/user-attachments/assets/f0c3c47b-6892-4401-826f-083d92758eba" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="431" height="247" alt="image" src="https://github.com/user-attachments/assets/3b6b4475-fe95-46f5-b19e-dbb5c39fa924" />


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

<img width="416" height="122" alt="image" src="https://github.com/user-attachments/assets/9b4a3174-d98c-45b7-900e-9a5d539677a5" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="477" height="128" alt="image" src="https://github.com/user-attachments/assets/7b2eaef8-5541-4acc-8fcc-672eaf9ede72" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="365" height="116" alt="image" src="https://github.com/user-attachments/assets/7b0eb8da-5cb8-4102-93ff-3c0f7b5abafe" />


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

<img width="398" height="275" alt="image" src="https://github.com/user-attachments/assets/2437e5ea-2694-4ffd-9e66-bd80194cfaa6" />

 
ls file1
## OUTPUT

<img width="382" height="278" alt="image" src="https://github.com/user-attachments/assets/3b31f6d1-b786-4395-a285-06adf299267c" />


echo $?
## OUTPUT 

<img width="373" height="271" alt="image" src="https://github.com/user-attachments/assets/df8e7873-a20d-4274-a255-264bd9b2bb5f" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="372" height="273" alt="image" src="https://github.com/user-attachments/assets/9ee03067-c65b-434a-9654-7ac482368fbe" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="347" height="278" alt="image" src="https://github.com/user-attachments/assets/aa932066-f44b-4a53-ab61-a0465c3c723f" />

 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="350" height="110" alt="image" src="https://github.com/user-attachments/assets/69943e71-8bac-4ba7-b17e-68db8873d633" />


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

<img width="467" height="102" alt="image" src="https://github.com/user-attachments/assets/1bae2742-28a9-43db-aa66-2f73956c91b3" />


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

<img width="465" height="97" alt="image" src="https://github.com/user-attachments/assets/243c6e2e-6e12-47bf-a3eb-605f2a08acb7" />


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

<img width="483" height="101" alt="image" src="https://github.com/user-attachments/assets/e073bc7b-0ff5-4dca-8fb5-8dc8e30b3fb6" />


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

<img width="352" height="71" alt="image" src="https://github.com/user-attachments/assets/a510aec7-55e3-4074-89ea-f8d369ce4d3c" />


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

<img width="441" height="72" alt="image" src="https://github.com/user-attachments/assets/0bccd93d-97f5-465e-98c1-0052748085ca" />


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

<img width="341" height="77" alt="image" src="https://github.com/user-attachments/assets/733f9c71-b5e2-4eea-8cb4-eeb16007b467" />

 
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
 
 <img width="350" height="166" alt="image" src="https://github.com/user-attachments/assets/0ea5e81d-031b-4d5d-8d24-a947c31f6e45" />

 
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
 
<img width="377" height="205" alt="image" src="https://github.com/user-attachments/assets/2120d2a1-64aa-446b-ac0c-155456264d4c" />
 
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

<img width="367" height="126" alt="image" src="https://github.com/user-attachments/assets/3159bf05-3468-4590-be7b-7a16426593fa" />

 
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

<img width="377" height="201" alt="image" src="https://github.com/user-attachments/assets/53941d5a-361a-4abb-93f7-bb63f3e37d65" />


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

<img width="346" height="172" alt="image" src="https://github.com/user-attachments/assets/57cea3a2-16e0-4338-998f-36dd29cbb791" />


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

<img width="365" height="180" alt="image" src="https://github.com/user-attachments/assets/a66609fc-1ab6-4349-968e-44c13e481e16" />


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

<img width="452" height="357" alt="image" src="https://github.com/user-attachments/assets/dacd58bc-082e-4040-851c-e92ea88eb1bd" />

 
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

<img width="421" height="100" alt="image" src="https://github.com/user-attachments/assets/8447acce-5561-403c-883a-31cd5af53a7f" />


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 
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

<img width="392" height="95" alt="image" src="https://github.com/user-attachments/assets/75e0f659-fdde-4180-afd5-97e145cd7b91" />

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

<img width="375" height="67" alt="image" src="https://github.com/user-attachments/assets/aa00db78-46df-42d5-8785-88dec02f09e8" />

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

<img width="405" height="125" alt="image" src="https://github.com/user-attachments/assets/c751fedd-34b3-44f8-81c7-287f89a1a6f6" />


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

<img width="365" height="122" alt="image" src="https://github.com/user-attachments/assets/21425438-33ba-4423-889e-4d0487a3f095" />

 
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

<img width="447" height="375" alt="image" src="https://github.com/user-attachments/assets/ffcf69a4-fa17-4d46-ad34-21c600a98ddf" />

 
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

<img width="397" height="125" alt="image" src="https://github.com/user-attachments/assets/c25e2a4f-b710-48ba-82fa-86317cfa1bcb" />



# RESULT:
The Commands are executed successfully.
