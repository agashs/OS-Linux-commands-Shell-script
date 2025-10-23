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
<img width="614" height="156" alt="i1" src="https://github.com/user-attachments/assets/07978dde-44ed-4013-a785-fb18530d2311" />



cat < file2
## OUTPUT

<img width="631" height="185" alt="i2" src="https://github.com/user-attachments/assets/2a715588-06e9-4b06-9e0d-a0fb39f5661e" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="661" height="76" alt="i3" src="https://github.com/user-attachments/assets/15ec1ddb-f303-4069-a8c7-757a709e0fe2" />

comm file1 file2
 ## OUTPUT
<img width="685" height="224" alt="i4" src="https://github.com/user-attachments/assets/c44b0320-2c3c-4d2b-8cca-ce7a95491753" />

 
diff file1 file2
## OUTPUT
<img width="667" height="278" alt="i5" src="https://github.com/user-attachments/assets/592223f0-a4fa-477d-af15-147a75c94c68" />


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

<img width="632" height="117" alt="i6" src="https://github.com/user-attachments/assets/ecf28c06-4b7b-43f9-91d2-271f25428a81" />



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
 
grep Hello newfile 
## OUTPUT

<img width="638" height="101" alt="i7" src="https://github.com/user-attachments/assets/e246225e-e504-412c-a1ad-34fc20759e02" />


grep hello newfile 
## OUTPUT

<img width="611" height="74" alt="i8" src="https://github.com/user-attachments/assets/75a1109d-0478-47f2-95d6-d5451ceab54b" />



grep -v hello newfile 
## OUTPUT

<img width="626" height="82" alt="i9" src="https://github.com/user-attachments/assets/33dffbcf-ea76-4ff6-9baa-6d7f6c8e93c4" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="710" height="104" alt="i10" src="https://github.com/user-attachments/assets/b77ffd83-7b58-4185-8472-1a21d5a24aa9" />




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="675" height="81" alt="i11" src="https://github.com/user-attachments/assets/08d240bc-f5c4-47d8-aa81-01a89d19eb89" />

grep -R ubuntu /etc
## OUTPUT

<img width="801" height="574" alt="i12" src="https://github.com/user-attachments/assets/9bb26e44-dacd-4d85-8296-15f15bbaf824" />


grep -w -n world newfile   
## OUTPUT
<img width="649" height="100" alt="i13" src="https://github.com/user-attachments/assets/7e80ac9a-b428-4710-85f2-f1832c97218e" />


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

<img width="673" height="105" alt="i14" src="https://github.com/user-attachments/assets/3c497695-d2e6-4292-a2d9-976c429639b3" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="695" height="104" alt="i15" src="https://github.com/user-attachments/assets/f64eaed5-dfd2-4085-ac07-ef9391a224f3" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="650" height="94" alt="i16" src="https://github.com/user-attachments/assets/232a0f35-ca11-44c7-b2d4-50b4e0e79e4e" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="697" height="77" alt="i17" src="https://github.com/user-attachments/assets/bb723309-edd8-4f4e-b6e7-a808ac330c3d" />



egrep '(world$)' newfile 
## OUTPUT

<img width="649" height="103" alt="i18" src="https://github.com/user-attachments/assets/9d6a02e6-fe21-4b50-a9af-b3d052ea3cfa" />


egrep '(World$)' newfile 
## OUTPUT
<img width="651" height="77" alt="i19" src="https://github.com/user-attachments/assets/0e00cab4-878f-413d-a170-0f36c343d84a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="667" height="127" alt="i20" src="https://github.com/user-attachments/assets/81802fc5-ee0a-4d63-90ae-0552ac19d38e" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="667" height="79" alt="i21" src="https://github.com/user-attachments/assets/cf9d2274-e5a4-4ed0-a24c-1423ef068bb7" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="651" height="76" alt="i22" src="https://github.com/user-attachments/assets/4212aef5-fce6-4325-b87f-1ca8dbf23b89" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="666" height="81" alt="i23" src="https://github.com/user-attachments/assets/da2b8f39-f317-47c1-9492-004a668384f7" />


egrep l{2} newfile
## OUTPUT

<img width="670" height="102" alt="i24" src="https://github.com/user-attachments/assets/9df6bed5-539d-45ca-bb19-30d645fb4ba8" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="731" height="133" alt="i25" src="https://github.com/user-attachments/assets/63e793eb-4ea0-4539-b32c-36c1f91ad995" />


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

<img width="617" height="84" alt="i26" src="https://github.com/user-attachments/assets/864157bc-1e80-4c29-abd5-620e29eeea1d" />


sed -n -e '$p' file23
## OUTPUT

<img width="611" height="87" alt="i27" src="https://github.com/user-attachments/assets/18e9ed7d-fa13-4c10-83a2-d059025d46fa" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="642" height="257" alt="i28" src="https://github.com/user-attachments/assets/faf0cdad-9dce-4663-afd3-f8dc25b2fcde" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="676" height="249" alt="i29" src="https://github.com/user-attachments/assets/11246547-3a49-4d89-971a-a879622455fc" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="644" height="259" alt="i30" src="https://github.com/user-attachments/assets/0b721d8a-7322-461d-85da-5c388c146264" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="700" height="180" alt="i31" src="https://github.com/user-attachments/assets/22fa9591-86dd-48ee-b662-b0eb0be4e307" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="669" height="131" alt="i32" src="https://github.com/user-attachments/assets/5929ea3d-1ec5-458e-9b0b-a1b13aec1381" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="676" height="104" alt="i33" src="https://github.com/user-attachments/assets/4e6a8bcd-057b-4dc7-a874-f8fa6eef921f" />


seq 10 
## OUTPUT

<img width="683" height="313" alt="i34" src="https://github.com/user-attachments/assets/7ae504aa-38fc-42f1-b45c-a91175a4ed84" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="641" height="130" alt="i35" src="https://github.com/user-attachments/assets/704807c9-2eb5-4e78-ad52-4a2d95919128" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="655" height="130" alt="i36" src="https://github.com/user-attachments/assets/a02704c8-821a-4b42-8c44-778fe79af39a" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="731" height="153" alt="i37" src="https://github.com/user-attachments/assets/4b0626f9-4753-42c6-baed-5dfdf91a6b5f" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="641" height="132" alt="i38" src="https://github.com/user-attachments/assets/8b74860b-f6fe-445e-82e0-15a0184f4b39" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="707" height="128" alt="i39" src="https://github.com/user-attachments/assets/2630b88b-eece-4566-9e0f-979c84d3df0c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="732" height="128" alt="i40" src="https://github.com/user-attachments/assets/b4389225-4296-40ab-b538-17a7539f6c74" />



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

<img width="665" height="125" alt="i41" src="https://github.com/user-attachments/assets/24f8e27b-c3c7-489b-9d09-839e90165237" />

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

<img width="676" height="205" alt="i42" src="https://github.com/user-attachments/assets/936353c9-af8e-4cc4-b09b-e0bb14cea013" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="640" height="180" alt="i43" src="https://github.com/user-attachments/assets/2c13be20-be3a-4597-9b74-61ac46c88d04" />

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
