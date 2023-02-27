# File-Operatioins-in-python

Date 05/09/2022
basic file programs in python

Python 3.10.0 (tags/v3.10.0:b494f59, Oct  4 2021, 19:00:18) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.
f = open("abc123",'w')
f.write("This is abc123 text file\n it soon working great")
47
f.write("Come in harry great have a sweet day")
36
f.close()
f = open("abc123",'r')
kalyan = f.read()
kalyan
'This is abc123 text file\n it soon working greatCome in harry great have a sweet day'
pandu = f.read()
pandu
''
f.close()
f.open('abc123','r')
Traceback (most recent call last):
  File "<pyshell#10>", line 1, in <module>
    f.open('abc123','r')
AttributeError: '_io.TextIOWrapper' object has no attribute 'open'
f=open('abc123','r')
pandu = f.read()
pandu
'This is abc123 text file\n it soon working greatCome in harry great have a sweet day'
a = f.read()
a
''
f.readable()
True
f.writable()
False
f.open()
Traceback (most recent call last):
  File "<pyshell#18>", line 1, in <module>
    f.open()
AttributeError: '_io.TextIOWrapper' object has no attribute 'open'
f.close
<built-in method close of _io.TextIOWrapper object at 0x000002095B4CE9B0>
f.closed
False
f.mode
'r'
f.close()
f.mode
'r'
f.closed
True
l=['kalyan','pandu','reddy','asam']
f = open('abc123','a')
f.write('again content')
13
f.writelines(l)
f.close()
f = open('abc123','r')
data = f.read()
data
'This is abc123 text file\n it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
f.seek(0)
0
da = f.read()
da
'This is abc123 text file\n it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
a = f.read()
a
''
f.seek(0)
0
abc = f.read()
abc
'This is abc123 text file\n it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
f.seek(0)
0
a = f.read(10)
a
'This is ab'
abc
'This is abc123 text file\n it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
b = f.read()
b
'c123 text file\n it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
f.seek(0)
0
c = f.readline()
c
'This is abc123 text file\n'
line2 = f.readline()
line2
' it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam'
f.seek(0)
0
d = f.readlines()
for line in d:
    print(line,end='')

This is abc123 text file
 it soon working greatCome in harry great have a sweet dayagain contentkalyanpandureddyasam
f.close()
f.closed
True
with open('abc1' ,'w') as f:
    f.write("Asam kalyan\n reddy")
    f.write("Everything is going fine\n and ping you later")
    f.write("Come a gain ang grow")

    
18
44
20
with open('abc1' , 'r') af k:
    
SyntaxError: invalid syntax. Perhaps you forgot a comma?
with open('abc1' ,'r') as f:
    f.readline()
    f.read(10)
    f.readlines()

    
'Asam kalyan\n'
' reddyEver'
['ything is going fine\n', ' and ping you laterCome a gain ang grow']
f.closed()
Traceback (most recent call last):
  File "<pyshell#70>", line 1, in <module>
    f.closed()
TypeError: 'bool' object is not callable
f.closed
True
with open('abc1' ,'r') as k:
    k.readline()
    k.read(10)
    k.readlines()

    
'Asam kalyan\n'
' reddyEver'
['ything is going fine\n', ' and ping you laterCome a gain ang grow']
with open('abc1' ,'r') as k:
    k.read(6)
    k.tell()
    k.read(5)
    k.tell()
    k.readline()
    k.tell()
    k.seek(0)
    k.tell()
    k.readlines()
    k.tell()

    
'Asam k'
6
'alyan'
11
'\n'
13
0
0
['Asam kalyan\n', ' reddyEverything is going fine\n', ' and ping you laterCome a gain ang grow']
84
with open('abc1' ,'r') as k:
    k.read(6)
    k.tell()
    k.read(5)
    k.tell()
    k.readline()
    k.tell()
    k.seek(0)
    k.tell()
    k.readlines()
    k.tell()
    k.seek(40)
    k.tell()

    
'Asam k'
6
'alyan'
11
'\n'
13
0
0
['Asam kalyan\n', ' reddyEverything is going fine\n', ' and ping you laterCome a gain ang grow']
84
40
40
data = 'all students are marvelous....!'
f = open('abc14','w')
f.write(data)
31
with open('abc14','r+') as f:
    text = f.read()
    text
    f.seek(17)
    f.write('Gemss')
    f.tell()
    f.read()
    f.tell()

    
'all students are marvelous....!'
17
5
22
'lous....!'
31
with open('abc14','r+') as f:
    text = f.read()
    text
    f.seek(17)
    f.write('Gemss')
    f.tell()
    f.read()
    f.tell()
    f.read()

    
'all students are Gemsslous....!'
17
5
22
'lous....!'
31
''
















import os
os.path.isfile('abc14')
True
os.path.isfile('abc123')
True
os.path.isfile('kalyanredy')
False
s = "This is very crazy about\n the files how\n they behave\n...ok"
f.closed
True
f = open('abc12','w+')
da = f.read()
da
''
f.seek(0)
0
da = f.read()
da
''

      
s '    '
SyntaxError: invalid syntax
s = '   '
s
'   '
s = "This is very crazy about\n the files how\n they behave\n...ok"
f.closed
False
f.writelines(s)
d = f.read()
d
''
f.seek(0)
0
d = f.read()
d
'This is very crazy about\n the files how\n they behave\n...ok'
f.writelines(s)
f.seek(0)
0
d1 = f.read()
d1
'This is very crazy about\n the files how\n they behave\n...okThis is very crazy about\n the files how\n they behave\n...ok'



_______________________________________________________________________________________________________


import csv  #Comma Seperated Value
with open("emp.csv",'w',newline='') as f:
    w = csv.writer(f)    #returns csv writer object
    w.writerow(["ENO","ENAME", "ESAL","EADD"])  #Writing into the file
    n = int(input("Enter no. of Employess: "))
    for i in range(n):
        eno = input("Enter Employee number: ")
        ename = input("Enter Employee name: ")
        esal = input("Enter Employee salary: ")
        eadd = input("Enter Employee address: ")
        w.writerow([eno,ename,esal,eadd])
print("Successfully all Employee details written successfullly..\n")

f = open('emp.csv','r')
r = csv.reader(f) #returns the csv reader object 
data = list(r)
for line in data:
    for word in line:
        print(word,"\t",end="")
    print()

f.close()


o/p:

Enter no. of Employess: 2
Enter Employee number: 1
Enter Employee name: ka
Enter Employee salary: 10
Enter Employee address: ap
Enter Employee number: 2
Enter Employee name: pa
Enter Employee salary: 20
Enter Employee address: ka
Successfully all Employee details written successfullly..

ENO     ENAME   ESAL    EADD 
1       ka      10      ap 
2       pa      20      ka 

______________________________________________________________________________________________


Working with zip files


from zipfile import* 
#ZipFile Z and F must be captial
f = ZipFile('kalyan75','w',ZIP_DEFLATED)#ZIP_DEFAULTED  used to create the zip file
#f.write("asam pavan klayn reddy\n how \n are \n you doing")
#f.write("Yaa \n come on Mr. it a great \n time soon ")
f.write('kalyan143')

f.close()
print("Successfully zip file created")

f = ZipFile('kalyan75','r',ZIP_STORED)
names = f.namelist()
for name in names:
    print('File name: ',name)
    print("The content of the file is : ")
    f1 = open(name,'r')
    print(f1.read())
    print()
f.close()



o/p:

Successfully zip file created
File name:  kalyan143
The content of the file is :
Eno,Ename,Eage,Esal

1,pa,22,1

2,ra,23,100



PS D:\Ka_VS_CoDe\K@ly@N> 

___________________________________________________________________________

to know the status of a file

import os

s = os.stat('ka1.c')
print(s)


o/p:
os.stat_result(st_mode=33206, st_ino=1688849860284938, st_dev=3893993624, st_nlink=1, st_uid=0, st_gid=0,
 st_size=1995, st_atime=1662479034, st_mtime=1647686528, st_ctime=1641020251)







