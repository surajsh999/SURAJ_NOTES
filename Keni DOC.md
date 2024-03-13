

11/mar
------

chmod chown ( permitions )
--------------------------

chmod
-----
Read - 4  
write - 2  
execute - 1  

read + write = 6  
read + write + execute = 7  

chmod 667 file.txt  
chmod 777 file.txt  

u - owner   
g - group  
o - user  

chmod u+x filename  
chmod u-x filename  
chmod g+x filename  
chmod o+x filename  

chown  
-----  

to change owner of a file or a directory  

chown root filename  
chown user:group file.txt  



vi (visual editor ) - vim (improved version)
--------------------------------------------

vi   

:wq   to write and quite  
:q   to quite  
:w   to write  
:w!  to forcefully write  


i - insert  
h - left   
l - right  
j - move down  
k - move up  
gg - beggining of the file  
G - bottom of the file  
0 - starting of the line  
$ - end of the line   

yy - copy of the line    
dd - delete the line     
p - paste  
:%d - to clear all data    

_________________

12/3
----

GREP
----

grep - global / regular expression search /and print  

used for searching and manipulating text patterns within files  

grep -i "unix" file.txt  
grep grep -on "rsvp" file.txt (-o only match)  

-o, --only-matching  
-i, --ignore-case  
-n, --line-number  
-c, --count  



sed
---
-i	sed -ibak 's/On/Off/' php.ini	 Backup and modify input file directly  
-E	sed -E 's/[0-9]+//g'             input-file	Use extended regular expressions  
-n	sed -n '3 p' config.conf       	Suppress default pattern space printing  
-f	sed -f script.sed config.conf	Execute sed script file  
-e	sed -e 'command1' -e 'command2' input-file	Execute multiple sed commands  






