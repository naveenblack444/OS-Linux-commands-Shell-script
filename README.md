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

<img width="1501" height="385" alt="image" src="https://github.com/user-attachments/assets/b8fd907e-a0cf-4a09-9569-576993978052" />


cat < file2
## OUTPUT
<img width="1504" height="261" alt="image" src="https://github.com/user-attachments/assets/b662d3ac-a041-4ebe-9d2e-8f3fd603d651" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1489" height="115" alt="image" src="https://github.com/user-attachments/assets/36adf05b-eb7c-478c-a8c6-52745968e4da" />

comm file1 file2
 ## OUTPUT
<img width="1501" height="341" alt="image" src="https://github.com/user-attachments/assets/c4587026-da36-462a-b761-b85b33ec44f1" />

 
diff file1 file2
## OUTPUT
<img width="1491" height="407" alt="image" src="https://github.com/user-attachments/assets/ceba94be-bcfc-45b9-bcb9-7eb0b8db238b" />


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

<img width="716" height="149" alt="image" src="https://github.com/user-attachments/assets/1a31efe0-6207-4b48-892d-29bd12e67a05" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="904" height="183" alt="image" src="https://github.com/user-attachments/assets/d9ccf12d-fab7-4d1f-8ea1-1b195b8f0b8b" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="942" height="179" alt="image" src="https://github.com/user-attachments/assets/66609b44-856d-481a-b555-1139138e9d1e" />


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

<img width="601" height="127" alt="Screenshot 2026-10-24 134817" src="https://github.com/user-attachments/assets/afa2aa4a-1982-44cf-a0c3-1a90d93c126d" />


grep hello newfile 
## OUTPUT

<img width="660" height="95" alt="Screenshot 2026-10-24 134936" src="https://github.com/user-attachments/assets/cc64a981-d9b8-49e6-9b85-cf2c90442f98" />



grep -v hello newfile 
## OUTPUT

<img width="783" height="97" alt="Screenshot 2026-10-24 135025" src="https://github.com/user-attachments/assets/50ca807a-55a2-41f9-b340-d1b36f73aa9c" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="807" height="127" alt="image" src="https://github.com/user-attachments/assets/44f8bb40-6303-4b4f-b951-da0f785e73c4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="687" height="92" alt="image" src="https://github.com/user-attachments/assets/2144e665-4488-46a9-8ffc-9555709e74ff" />



grep -R ubuntu /etc
## OUTPUT

<img width="1236" height="705" alt="image" src="https://github.com/user-attachments/assets/9b4a3dad-e966-4eb2-bb93-b477073c0698" />


grep -w -n world newfile   
## OUTPUT
<img width="843" height="132" alt="image" src="https://github.com/user-attachments/assets/0e3fdf26-45ee-4d53-acb2-1802cf29761d" />


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

<img width="820" height="130" alt="image" src="https://github.com/user-attachments/assets/2fd10e5a-22e9-4428-ae1f-a01819c6ba66" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="800" height="136" alt="image" src="https://github.com/user-attachments/assets/024db737-12f5-41b1-9e52-81602d30d305" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT




egrep '(^hello)' newfile 
## OUTPUT

<img width="796" height="102" alt="image" src="https://github.com/user-attachments/assets/a0648c37-c88b-4839-a073-a592fd3941ba" />


egrep '(world$)' newfile 
## OUTPUT

<img width="675" height="101" alt="image" src="https://github.com/user-attachments/assets/ce78a033-204e-4cdd-a4b7-97528e109b06" />


egrep '(World$)' newfile 
## OUTPUT

<img width="770" height="155" alt="image" src="https://github.com/user-attachments/assets/13054fc1-caa1-4ed9-b709-39252eef66c3" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="770" height="155" alt="image" src="https://github.com/user-attachments/assets/89429a08-6835-450f-a9f2-4f399c61dbd1" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="790" height="97" alt="image" src="https://github.com/user-attachments/assets/59c24b9f-71b6-4c42-9f51-6ce7f63f2014" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="947" height="92" alt="image" src="https://github.com/user-attachments/assets/002ff67e-5dfe-4a1f-b134-6f2d6ff76787" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="787" height="97" alt="image" src="https://github.com/user-attachments/assets/d06a5ff9-9844-40db-9fe3-dac992ddb9ea" />


egrep l{2} newfile
## OUTPUT

<img width="852" height="125" alt="image" src="https://github.com/user-attachments/assets/27ad9f1d-7440-4bf8-b15a-307b74dfe2ce" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="818" height="161" alt="image" src="https://github.com/user-attachments/assets/cc18eb39-c458-4ba1-a8d4-20d4c4b09b25" />


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

<img width="821" height="406" alt="image" src="https://github.com/user-attachments/assets/740e00c7-1697-4411-b216-40213642084b" />


sed -n -e '$p' file23
## OUTPUT

<img width="773" height="92" alt="image" src="https://github.com/user-attachments/assets/2b6d6875-eb3b-4ae6-aafb-281024419b52" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="892" height="310" alt="image" src="https://github.com/user-attachments/assets/81f3f4ab-3fb8-4337-bfc0-4867177f9fe6" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="896" height="318" alt="image" src="https://github.com/user-attachments/assets/2f0c2bd1-80fe-409b-ba88-c80d47def7d1" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="885" height="318" alt="image" src="https://github.com/user-attachments/assets/4f47f6b4-4a6c-4e38-a51f-be197ea40884" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="977" height="230" alt="image" src="https://github.com/user-attachments/assets/8363e799-1ff0-41cd-bf77-139aa8a8a81a" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="968" height="160" alt="image" src="https://github.com/user-attachments/assets/9ae16f8c-bf92-4788-acc7-bff295811212" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="850" height="120" alt="image" src="https://github.com/user-attachments/assets/2d0e0db4-e7cc-40c3-988a-9603e179783f" />


seq 10 
## OUTPUT

<img width="881" height="382" alt="image" src="https://github.com/user-attachments/assets/72cf9214-9156-4ccf-880b-520789df268c" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="797" height="163" alt="image" src="https://github.com/user-attachments/assets/37d779fb-5ab2-4f10-8e2c-5b0f56699d15" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="845" height="161" alt="image" src="https://github.com/user-attachments/assets/ca3aabba-c54b-40e7-a099-b32e59ffe7b8" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="910" height="187" alt="image" src="https://github.com/user-attachments/assets/60d48f56-32be-4983-a47d-7aa2593e0c6c" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="688" height="155" alt="image" src="https://github.com/user-attachments/assets/690d00bd-c7f7-4910-a8e3-f4f3a8209a90" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="760" height="155" alt="image" src="https://github.com/user-attachments/assets/6e31d63f-0ad1-4872-9b1a-e5e440429450" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="835" height="163" alt="image" src="https://github.com/user-attachments/assets/8ea2b79b-8804-4102-89a8-18c66a0941e4" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="866" height="155" alt="image" src="https://github.com/user-attachments/assets/63acf83c-531e-40eb-bb40-706b36f6cce8" />



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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
