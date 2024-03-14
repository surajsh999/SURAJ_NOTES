


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
-r, --recursive  

grip -i "mailbox_register" file.txt  
grep -inc "rsvp" file.txt  
grep -in "rsvp" file.txt  
grep -v "rsvp" file.txt  
grep -vc "rsvp" file.txt  
grep -o "rsvp" file.txt  
grep 08:51:06.*mailbox allocated file.txt  
grep "start.*end" file.txt  
grep -ir "info" /kani  
grep -irn "info" /kani  
grep -e "start" -e "end" file1.txt  

sed
---

sed 's/mailbox_create/newword/g' file.txt  
sed -n '1,10p' file.txt  
sed '1,10d' file.txt  

-i	sed -ibak 's/On/Off/' php.ini	 Backup and modify input file directly  
-E	sed -E 's/[0-9]+//g'             input-file	Use extended regular expressions                                                      
-n	sed -n '3 p' config.conf       	Suppress default pattern space printing                                                           
-f	sed -f script.sed config.conf	Execute sed script file                                                                           
-e	sed -e 'command1' -e 'command2' input-file	Execute multiple sed commands                                                         
																																	  
#### Substitute/Replace                                                                                                                  
																																	  
sed 's/pattern/replace_string/' file.txt       # Replace 'pattern' with 'replace_string' in file.txt                                  
sed 's/pattern/replace_string/g' file.txt      # Replace all occurrences of 'pattern' with 'replace_string' in file.txt               
sed 's/pattern/replace_string/2' file.txt      # Replace the 2nd occurrence of 'pattern' with 'replace_string' in file.txt            
sed 's/pattern/&_&/' file.txt                  # Duplicate 'pattern' and insert '_' in between (pattern_pattern)                      
																																	  
#### In-place editing                                                                                                                    
																																	  
sed -i 's/pattern/replace_string/g' file.txt   # Replace all occurrences of 'pattern' with 'replace_string' in-place                   
sed -i 's/pattern/replace_string/3g' file.txt  # Replace only the 3rd occurrence of 'pattern' with 'replace_string' in-place           
																																	   
#### Delete lines                                                                                                                         
																																	   
sed '/pattern/d' file.txt                      # Delete lines matching 'pattern'                                                       
sed '/^$/d' file.txt                           # Delete blank lines                                                                    
																																	   
#### Insert/Append lines                                                                                                                  
																																	   
sed '3r file_to_read' file.txt                 # Read contents of file_to_read and insert after line 3                                 
sed '3i new_line' file.txt                     # Insert 'new_line' after line 3                                                        
sed '3a new_line' file.txt                     # Append 'new_line' after line 3                                                        
																																	   
#### Print lines                                                                                                                          
																																	   
sed -n '/pattern/p' file.txt                   # Print lines matching 'pattern'                                                        
sed -n '3,5p' file.txt                         # Print lines 3 to 5                                                                    
sed -n '3p;4q' file.txt                        # Print line 3 and quit after line 4                                                    
																																	   
#### Transform cases                                                                                                                      
																																	   
sed 's/\w+/\L&/g' file.txt                     # Lowercase all words                                                                   
sed 's/\w+/\U&/g' file.txt                     # Uppercase all words                                                                   
sed 's/.*/\L&/; s/\<./\U&/g' file.txt          # Capitalize first letter of each word                                                  
																																	   
#### Using regular expressions                                                                                                            
																																	   
sed 's/[^a-zA-Z]//g' file.txt                  # Remove all non-alphabetic characters                                                  
sed 's/\(hello\)\(world\)/\2\1/g' file.txt     # Swap 'hello' and 'world'     

