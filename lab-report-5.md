mv command 

- mv file1 file2 <br>
This command renames file1 to file2. If file2 already exists, the command overwrites it. In this case, the original file2 is lost. This might be useful when, for example, in java
if the file name doesnt match the class name, and you need to rename the file. In the first example below, written_2/non-fiction/OUP/Berk/chABC.txt does not exist, and the mv command renamed 
ch2.txt in written_2/non-fiction/OUP/Berk/ to chABC.txt. In the second example, written_2/travel_guides/berlitz1/WhatToIbiza.txt already exists, and the command overwrites this file.  

```
mv written_2/non-fiction/OUP/Berk/ch2.txt written_2/non-fiction/OUP/Berk/chABC.txt
ls written_2/non-fiction/OUP/Berk | grep chABC.txt
chABC.txt
 
mv written_2/travel_guides/berlitz1/HistoryHongKong.txt written_2/travel_guides/berlitz1/WhatToIbiza.txt
ls | grep HistoryHongKong.txt #shows that this file doesnt exist anymore
ls | grep WhatToIbiza.txt    
WhatToIbiza.txt
```
  
- mv -i file1 file2 <br>
This command renames file1 to file2. However, this time the command prompts the user for confirmation before overwriting the file if it exists. This is useful when you are not sure
if file2 exists, and you dont wanna lose all contents of the file after running this command. 

```
mv -i written_2/non-fiction/OUP/Berk/CH4.txt written_2/non-fiction/OUP/Berk/ch7.txt 
overwrite written_2/non-fiction/OUP/Berk/ch7.txt? (y/n [n]) y
ls written_2/non-fiction/OUP/Berk | grep ch4.txt  
ls written_2/non-fiction/OUP/Berk | grep ch7.txt
ch7.txt
  
mv -i written_2/travel_guides/berlitz2/Algarve-History.txt written_2/travel_guides/berlitz2/Algarve-Intro.txt
overwrite written_2/travel_guides/berlitz2/Algarve-Intro.txt? (y/n [n]) y
ls written_2/travel_guides/berlitz2 | grep Algarve-History.txt
ls written_2/travel_guides/berlitz2 | grep Algarve-Intro.txt
Algarve-Intro.txt
```
  
- mv file1 directory <br>
This command moves file1 to directory. This command is useful when you are trying to set up a directory structure, and you realise that there is a file in the wrong directory, and you want 
to move it.

```
mv written_2/travel_guides/berlitz2/Amsterdam-Intro.txt written_2
ls written_2 
Amsterdam-Intro.txt     non-fiction             travel_guides
  
mv written_2/travel_guides/berlitz1/HandRHawaii.txt written_2/travel_guides
ls written_2/travel_guides
HandRHawaii.txt berlitz1        berlitz2
```
- mv -v file1 file2 <br>
This command renames file1 to file2. This command is useful because it lets you know which files or directories are being renamed. 
  
```
mv -v written_2/travel_guides/berlitz1/HistoryLasVegas.txt written_2/travel_guides/berlitz1/HistoryLasVegasRenamed.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt -> written_2/travel_guides/berlitz1/HistoryLasVegasRenamed.txt

mv -v written_2/travel_guides/berlitz2/Bahamas-history.txt written_2/travel_guides/berlitz2/Bahamas-HistoryRenamed.txt
written_2/travel_guides/berlitz2/Bahamas-history.txt -> written_2/travel_guides/berlitz2/Bahamas-HistoryRenamed.txt
```
Sources <br>
I used the "man" command on the terminal to find command-line options for the mv command. In addition, I used chat gpt to understand how the command-line option works, what it does, and the specific way that it can be used. For example, I typed "man mv" on the terminal to get the different command-line options for the find command. On chatgpt, I typed "What does the mv -v command do" and then "can you give me some examples of its usage". I followed a similar process for all the commands mentioned above.
