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

<img width="371" height="78" alt="image" src="https://github.com/user-attachments/assets/a819c34f-bdd7-47f1-8ef9-3d7f4b1998b3" />


cat < file2
## OUTPUT

<img width="317" height="102" alt="image" src="https://github.com/user-attachments/assets/fa78ff63-f79e-4fe0-adc0-acc13b07d875" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="319" height="38" alt="image" src="https://github.com/user-attachments/assets/fe86cd67-b2af-43c4-8180-e72d1af27739" />
 

comm file1 file2
 ## OUTPUT
 
<img width="326" height="107" alt="image" src="https://github.com/user-attachments/assets/c5c9b296-cae1-451e-b60d-98115d703165" />

 
diff file1 file2
## OUTPUT

<img width="335" height="163" alt="image" src="https://github.com/user-attachments/assets/29a67542-e0ba-4195-85ff-1a5e590ce877" />


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

<img width="322" height="53" alt="image" src="https://github.com/user-attachments/assets/cdf04351-8102-4581-b174-9ebadcd12a98" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="320" height="62" alt="image" src="https://github.com/user-attachments/assets/3bd58a8f-8fca-46df-aca4-e4154254b123" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="317" height="63" alt="image" src="https://github.com/user-attachments/assets/945ba529-bcc0-44bc-a945-16944f2570f1" />


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

<img width="326" height="39" alt="image" src="https://github.com/user-attachments/assets/aee8b23b-c866-464b-b9f8-bef7d518e3b8" />


grep hello newfile 
## OUTPUT

<img width="326" height="41" alt="image" src="https://github.com/user-attachments/assets/322020b1-f8cb-4105-94d7-ef2069c31451" />

grep -v hello newfile 
## OUTPUT

<img width="317" height="41" alt="image" src="https://github.com/user-attachments/assets/305c2da2-b65c-46d2-a795-42678c4da7ad" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="314" height="53" alt="image" src="https://github.com/user-attachments/assets/a815dd38-ffed-424a-8ab6-b3434183b5f8" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="321" height="43" alt="image" src="https://github.com/user-attachments/assets/6e5aaba5-b1c9-4a7d-97fa-a587893ee972" />


grep -R ubuntu /etc
## OUTPUT

<img width="405" height="174" alt="image" src="https://github.com/user-attachments/assets/fd132470-eecc-435f-a2e9-295e372c938d" />

grep -w -n world newfile   
## OUTPUT

<img width="334" height="50" alt="image" src="https://github.com/user-attachments/assets/8e3d1230-f61c-40c6-b86b-28158b3ee6c6" />


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

<img width="317" height="55" alt="image" src="https://github.com/user-attachments/assets/bdf7920a-f5ce-447a-b973-379bbbc6ac6f" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="322" height="54" alt="image" src="https://github.com/user-attachments/assets/d5c85386-f231-46c9-9a86-1f60d83bf10f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="327" height="55" alt="image" src="https://github.com/user-attachments/assets/aa30f7df-ecf4-45d7-99e7-273f8d1798c2" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="314" height="38" alt="image" src="https://github.com/user-attachments/assets/46e8faef-faef-4ac6-be5a-1a971e9c69a9" />

egrep '(world$)' newfile 
## OUTPUT

<img width="332" height="47" alt="image" src="https://github.com/user-attachments/assets/8a11d070-cfc6-47ac-9215-8ca1af5588be" />

egrep '(World$)' newfile 
## OUTPUT

<img width="325" height="38" alt="image" src="https://github.com/user-attachments/assets/e4906cf4-26e0-433c-ae48-fab659b5b2f4" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="316" height="62" alt="image" src="https://github.com/user-attachments/assets/eef2e58b-32cf-4ee6-9dcc-05e58107a532" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="321" height="38" alt="image" src="https://github.com/user-attachments/assets/03922128-8110-4fa7-bd3e-fa65fcabd76e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="313" height="38" alt="image" src="https://github.com/user-attachments/assets/a4b079b8-3797-40c6-8eb6-f9c865f265f0" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="315" height="37" alt="image" src="https://github.com/user-attachments/assets/fef6db73-eec4-4ef6-b7e3-c69370130fcd" />


egrep l{2} newfile
## OUTPUT

<img width="351" height="50" alt="image" src="https://github.com/user-attachments/assets/8de8f9cd-3ba5-42f4-ab34-1e1f48c56920" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="325" height="66" alt="image" src="https://github.com/user-attachments/assets/cb1834b1-93b1-4bb1-91f0-90727109ba0e" />


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

<img width="319" height="37" alt="image" src="https://github.com/user-attachments/assets/d6ddc4dc-de0f-4663-a4f0-3ad7d63a6e37" />


sed -n -e '$p' file23
## OUTPUT

<img width="318" height="41" alt="image" src="https://github.com/user-attachments/assets/62d3ea60-72b6-4c7c-a70c-5653393291a7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="313" height="127" alt="image" src="https://github.com/user-attachments/assets/854dba01-0969-4f53-9f4b-104f4ec6143d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="326" height="125" alt="image" src="https://github.com/user-attachments/assets/0f5227be-69a4-4db0-88ce-e90b8ce91084" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="317" height="125" alt="image" src="https://github.com/user-attachments/assets/dfcf62de-0f68-4ad4-b751-039004fc4768" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="314" height="91" alt="image" src="https://github.com/user-attachments/assets/57c32c03-845e-4e8a-a0a4-48774b939c8c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="320" height="65" alt="image" src="https://github.com/user-attachments/assets/f91513e0-cf1a-4a28-9d5f-9eb3b815d8e4" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="341" height="52" alt="image" src="https://github.com/user-attachments/assets/85a30642-2b92-4632-a09f-c3dcf8e530ce" />


seq 10 
## OUTPUT

<img width="320" height="149" alt="image" src="https://github.com/user-attachments/assets/54a6c1b9-4d1b-4f11-afec-ed4efbd6b006" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="321" height="65" alt="image" src="https://github.com/user-attachments/assets/54af0890-ba63-415f-8c9b-882adf655670" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="352" height="61" alt="image" src="https://github.com/user-attachments/assets/0efe612d-b6a8-402b-b5f7-c0421f6bfd88" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="314" height="74" alt="image" src="https://github.com/user-attachments/assets/e272ec58-d6b6-4fe2-ba35-0eb37581413f" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="319" height="65" alt="image" src="https://github.com/user-attachments/assets/4e6ca002-9b8d-474e-9718-d1b29f34f2b6" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="319" height="62" alt="image" src="https://github.com/user-attachments/assets/2b79af83-0772-4c14-a10a-4d51956f594c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="322" height="62" alt="image" src="https://github.com/user-attachments/assets/22842330-7f81-403f-96a6-c862e6b686c9" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="314" height="62" alt="image" src="https://github.com/user-attachments/assets/a05938c0-888b-46f1-ac92-b5d49c3687b3" />


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

<img width="323" height="87" alt="image" src="https://github.com/user-attachments/assets/2505f1c6-4c8d-4513-a709-491779389528" />


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

<img width="327" height="86" alt="image" src="https://github.com/user-attachments/assets/10c39e2a-d348-47a9-8ea4-45baed19646f" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="336" height="130" alt="image" src="https://github.com/user-attachments/assets/8b16fc5c-1d31-4c59-8e37-275c72eb9399" />


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

<img width="332" height="62" alt="image" src="https://github.com/user-attachments/assets/62f31ec8-4db6-4ad3-8524-3d63737c6af2" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="326" height="64" alt="image" src="https://github.com/user-attachments/assets/f67fe47e-1520-4c92-a9fd-fbdcb077161c" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="236" height="287" alt="image" src="https://github.com/user-attachments/assets/8724bfd3-640e-4613-bf8d-2eaeee0fc071" />
<img width="251" height="286" alt="image" src="https://github.com/user-attachments/assets/6d5b56eb-8b43-448d-99a7-88798c5cb48f" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="393" height="305" alt="image" src="https://github.com/user-attachments/assets/fddb70c2-bcbb-4b87-aeaf-b8b3b123e173" />

tar -xvf backup.tar
## OUTPUT

<img width="359" height="299" alt="image" src="https://github.com/user-attachments/assets/37c7f0fd-e3cb-44c3-ac04-d94c996a27fc" />
<img width="263" height="295" alt="image" src="https://github.com/user-attachments/assets/fb1ca00b-ca72-47a2-ba4c-b807299c5e15" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="386" height="40" alt="image" src="https://github.com/user-attachments/assets/8929bdbe-2f85-4723-b03c-bf46895b583c" />

 gunzip backup.tar.gz
## OUTPUT

 <img width="374" height="28" alt="image" src="https://github.com/user-attachments/assets/df9a99a6-b5fc-4de4-b792-8fe009e36af4" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="368" height="38" alt="image" src="https://github.com/user-attachments/assets/caa2e7ed-3680-4828-bc14-723e29359e17" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="368" height="65" alt="image" src="https://github.com/user-attachments/assets/e3061bdd-e84c-4f33-84a6-ac50d2c52cac" />


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

<img width="376" height="188" alt="image" src="https://github.com/user-attachments/assets/7291c4d7-a6eb-4dd7-b077-9cd234f13ac9" />

 ls file1
## OUTPUT

<img width="364" height="40" alt="image" src="https://github.com/user-attachments/assets/35da1ab3-1289-4e60-83bf-0b113d292dd3" />


echo $?
## OUTPUT 

<img width="369" height="40" alt="image" src="https://github.com/user-attachments/assets/19c23366-8123-4d4b-a999-72886db3d5e9" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="380" height="99" alt="image" src="https://github.com/user-attachments/assets/58b36d05-a58e-44ec-960f-e424f7acf39d" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="365" height="76" alt="image" src="https://github.com/user-attachments/assets/2d2a5b64-48f1-462c-92e1-084eaf6fab0e" />

 
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

<img width="362" height="137" alt="image" src="https://github.com/user-attachments/assets/64c217db-b7c8-4c90-a2e1-27d586ab8bd1" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="367" height="81" alt="image" src="https://github.com/user-attachments/assets/93769563-3f69-4488-9399-790612ba9846" />


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

<img width="372" height="42" alt="image" src="https://github.com/user-attachments/assets/dd583a5e-03e3-4e71-9984-863f255702b3" />


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

<img width="362" height="65" alt="image" src="https://github.com/user-attachments/assets/e16df27d-b9f0-47f8-b8f7-b0bf3ebc0eab" />


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

<img width="314" height="56" alt="image" src="https://github.com/user-attachments/assets/46a9e4b5-07f6-4dfe-bc7e-20c7a7aec2f6" />


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

<img width="327" height="64" alt="image" src="https://github.com/user-attachments/assets/f9f4e39f-8a64-444f-87ba-52e95eb09635" />


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

<img width="364" height="44" alt="image" src="https://github.com/user-attachments/assets/396059d5-8af5-49dc-bdd2-19208771f26f" />

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

<img width="318" height="38" alt="image" src="https://github.com/user-attachments/assets/ed54809e-c0c2-4992-99e9-225cc01041f0" />


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

<img width="310" height="64" alt="image" src="https://github.com/user-attachments/assets/102ebc84-ca92-4f94-91b2-52400b254021" />


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

<img width="313" height="156" alt="image" src="https://github.com/user-attachments/assets/dc2f7db6-a1f3-46c7-b63f-b3b2df42797c" />
 
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
 
<img width="316" height="79" alt="image" src="https://github.com/user-attachments/assets/6a188b5a-37d8-440f-bdf9-3ca958811953" />

 
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
 
<img width="307" height="101" alt="image" src="https://github.com/user-attachments/assets/917ab906-9995-4702-8754-b40fd38bef9d" />

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

<img width="319" height="87" alt="image" src="https://github.com/user-attachments/assets/69419a82-4ac7-4f4c-b646-04993eee2842" />

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

<img width="309" height="100" alt="image" src="https://github.com/user-attachments/assets/f194455a-1d09-44a3-a48f-06952d966c47" />

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

<img width="313" height="113" alt="image" src="https://github.com/user-attachments/assets/7d0c98fb-0318-44c4-b0f2-6269c61c3a02" />

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

<img width="308" height="87" alt="image" src="https://github.com/user-attachments/assets/35902c86-d5f0-4d61-89ad-09572f6a5ff8" />

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

<img width="310" height="86" alt="image" src="https://github.com/user-attachments/assets/a41713ab-52b5-496e-a7c1-15c0ef9535e8" />

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

<img width="308" height="177" alt="image" src="https://github.com/user-attachments/assets/f82d3f6b-44b9-4dfb-9dcb-3abbce359727" />

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

<img width="310" height="64" alt="image" src="https://github.com/user-attachments/assets/e3bfd727-a6bd-4720-9096-5a855a032712" />

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

 <img width="317" height="94" alt="image" src="https://github.com/user-attachments/assets/a9500b5e-26da-4fac-a241-6ab46af0e343" />

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

<img width="317" height="53" alt="image" src="https://github.com/user-attachments/assets/a8ddf8f3-208c-4252-9f9e-ebdbe743ff0f" />

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

<img width="309" height="197" alt="image" src="https://github.com/user-attachments/assets/e7ada2ea-063a-4744-a51c-828d2ac71fae" />


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

<img width="309" height="197" alt="image" src="https://github.com/user-attachments/assets/e7ada2ea-063a-4744-a51c-828d2ac71fae" />

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

<img width="305" height="89" alt="image" src="https://github.com/user-attachments/assets/0f5c2d9e-36f2-4903-84ad-dd9bf7c65dbb" />

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

<img width="336" height="127" alt="image" src="https://github.com/user-attachments/assets/7bcd82ad-159f-458e-a088-4b565c7ab935" />


# RESULT:
The Commands are executed successfully.
