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
![image](https://github.com/user-attachments/assets/b49bef69-2594-4bce-953b-396181b637d9)



cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/ff701cf4-0996-41d3-9fa1-41b26c60dce1)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/user-attachments/assets/70d04c12-6ec8-4b42-886e-998f569e41ed)

comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/c40a6b2a-29d5-4f65-bbc4-bb2b54d87284)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/81a6fa28-88bf-4088-a28b-ff60f193434e)


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


![image](https://github.com/user-attachments/assets/7d9caae8-c4bd-415c-913c-7676693a0d7f)



cut -d "|" -f 1 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/1af86af3-6909-4e96-80db-62a8f64efbcb)


cut -d "|" -f 2 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/9b446483-0a93-4c77-959b-0b1d1eba3960)

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

![image](https://github.com/user-attachments/assets/eb9f0614-8999-46f8-a6e8-86f335e7f6aa)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b10f434d-b984-4d9a-9bd1-48567c3f68f5)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b43f2bfd-498b-4a6d-bf3d-27b69aaf89d6)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/a965cd19-0199-4b02-a674-3c20cdaf1202)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/061abd62-d264-4f56-91f1-84f04335dd12)




grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/7814615d-217d-42ac-82e2-0260dcc3efda)


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
![image](https://github.com/user-attachments/assets/a86e8d55-f46f-45e1-82bd-8987a5b0bcfe)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a8a77b56-ceda-41e3-bccd-b9b7b682ebc1)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e16d8901-0757-449a-8b34-c44b4dbed997)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d0eb640e-3ae1-4e7e-b5ad-f513ceda800b)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ef793af8-f0ba-4c00-b197-75e872f303c5)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0d829e53-243d-4627-b87d-b4acfb89f95b)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/49956ad4-e3ef-4f06-a061-9714dafafe1d)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0df84486-779f-40b4-9038-dd5a1f24bb8c)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/36201d89-d0f4-486f-9f27-16572f0a96b9)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/243c47b3-4669-4dfe-9552-ac75dd54c66f)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/6e8e40c3-3e8e-4814-9349-85e5f228552f)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/fa705af3-e818-4b1a-ad56-88363b245f57)


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
![image](https://github.com/user-attachments/assets/2c1b403f-6024-4a38-965e-ec2ca09ae5e0)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/978ee233-a932-4873-a062-24a98078a601)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5268a5cc-e1fc-4d26-83b1-80ce991912c7)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c6bfb936-5b84-4465-a573-9adab229f68f)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/06f07433-5a4a-447f-98c3-129239c22cab)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5314edea-a091-4e03-a8cc-f161876250a3)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/10b9eb14-6576-4d22-aa41-0d58a0b09220)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4e3125bb-5d83-43b4-93cc-2cb50c12ab66)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/2ea2a50d-5e43-4ce7-bb85-d123802f7004)


seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/e264554e-4c99-4928-8117-a684c9227984)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/79e18ac2-ad6c-4110-9801-984cae7a3fe6)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/4d633300-7412-421e-9c31-66151bfc7211)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/f7cc71c9-53a6-4b3b-9d81-7dc7bb72de95)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/8d311e9e-a76e-4dbf-bd0d-5035c079528e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2ac15367-3ce7-49c9-859e-ed055b651d2d)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/68623511-b5f8-4d9d-884f-80230d6e280c)



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

![image](https://github.com/user-attachments/assets/58feeb5b-014a-4f76-83f1-4acb55c18294)


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


![image](https://github.com/user-attachments/assets/dcdaed4b-72f8-4e25-b36d-2cd38a5975d6)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/ee4d67b7-5893-4665-b372-fc01ce0cca25)

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

![image](https://github.com/user-attachments/assets/ceaadd91-812a-433f-9a24-4dc3bbef497e)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/2e39a6f9-5615-4054-8720-e8ed4e1ba87a)



#Backup commands
tar -cvf backup.tar *
## OUTPUT


![image](https://github.com/user-attachments/assets/a4397379-46d0-4703-9c09-f9af2d7c7e77)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/9d86e844-aa26-499d-9043-5990df2544fb)

gzip backup.tar

ls .gz
up.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/38b3adda-566d-4499-bc42-44d5457076ad)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


![image](https://github.com/user-attachments/assets/ab282b8f-3f36-43e9-8489-8291c929f2cb)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/45f75a6d-2afb-4152-bf6d-59b0072cdc64)


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

![image](https://github.com/user-attachments/assets/3cea144e-a943-492c-a0ce-9c5a0aeb243a)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/34aa6edf-2f00-4143-a223-c1739d81ad4d)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/040c2d7d-4e92-4164-bf3d-911d47f32f03)
 
abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/35c4a8c4-8619-4319-bba7-7a8464f8a019)


 
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

![image](https://github.com/user-attachments/assets/8d47570f-47d2-42b3-a086-093d196cd427)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/201400b8-2c5e-4ce6-9377-7b05daf9d577)


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

![image](https://github.com/user-attachments/assets/9da115c6-3a3d-4016-8d33-88adaf279ed8)

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


![image](https://github.com/user-attachments/assets/8fa17756-e7cf-489e-aa0d-bf42537beaac)


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

![image](https://github.com/user-attachments/assets/b5378a05-6098-48d8-9d07-5cc79e85205d)

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

![image](https://github.com/user-attachments/assets/cef417d9-c3bb-4bea-9e54-a95ec4e4a9dd)

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


![image](https://github.com/user-attachments/assets/98da33f6-6498-4fae-bfa7-9e4fbd2aab94)

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

![image](https://github.com/user-attachments/assets/26247a36-373e-489a-b3da-09c9fa2c0881)

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

 ![image](https://github.com/user-attachments/assets/05c42f50-8477-4dcc-9cf1-4575e14c9331)

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
 

 ![image](https://github.com/user-attachments/assets/a86a90ae-4ea0-4790-afdb-3b24aed40744)

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
 

 ![image](https://github.com/user-attachments/assets/8b85e133-98b9-4201-abff-24c0b30cb903)

 
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
 

![image](https://github.com/user-attachments/assets/12dee9f0-3b06-4988-8dbc-3626ebcc8ee8)


 
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86) 
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
  ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)

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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
 
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86) 
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

 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)


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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
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
 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86) 
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

 ![image](https://github.com/user-attachments/assets/127b5b58-8d8c-4839-b0de-747d51326a86)
# RESULT:
The Commands are executed successfully.
