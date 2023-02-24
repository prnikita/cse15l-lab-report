-name <br>
This command is used to search for files with a specified name in a directory. It might be useful when you know the name of a file, but have no idea where it is stored on your computer. It can also be used as a fast way to access a file and the file path. 
```
find written_2/travel_guides/berlitz1 -name "HistoryEgypt.txt"
written_2/travel_guides/berlitz1/HistoryEgypt.txt

find written_2/non-fiction/OUP/Castro -name "chA.txt"
written_2/non-fiction/OUP/Castro/chA.txt
```

-size <br>
This command is used to search for files of a specified size. You can also search for files that are bigger than or smaller than a specified size. In case, for example, you wanna eradicate all files in a directory that are too big, "find -size" can be used to access all of those files. Note that in the first example below, the head command has been used to only display the first ten lines of the output. 
```
find written_2 -name "*.txt" -size -1M > find_size.txt
head -n 10 find_size.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt

find written_2/non-fiction/OUP/Castro -name "*.txt" -size -1M
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chP.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chM.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chO.txt
```

-iname <br>
This command is used to search for files with a specified name in a case insensitive manner. In case you named a file with both capital letters and small letters, but now you are unsure of the exact name, you can still find the file using the "-iname" command as it ignores the case while searching for the file.  
```
find written_2/non-fiction/OUP/Castro -iname "cha.txt"
written_2/non-fiction/OUP/Castro/chA.txt

find written_2/travel_guides/berlitz1 -iname "historydublin.txt"
written_2/travel_guides/berlitz1/HistoryDublin.txt
```

-type <br>
This command is used to search for files of a specific type. For example 'f' can be used to search for files, while 'd' can be used to search for directories. In case, you are only looking for the directories in the specific location, you can use "-d", and similarly if you are only searching for files in a specific location, you can use "-f".
```
find written_2 -type f -name "ch*.txt"
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt
written_2/non-fiction/OUP/Kauffman/ch3.txt
written_2/non-fiction/OUP/Kauffman/ch1.txt
written_2/non-fiction/OUP/Kauffman/ch4.txt
written_2/non-fiction/OUP/Kauffman/ch5.txt
written_2/non-fiction/OUP/Kauffman/ch7.txt
written_2/non-fiction/OUP/Kauffman/ch6.txt
written_2/non-fiction/OUP/Kauffman/ch8.txt
written_2/non-fiction/OUP/Kauffman/ch9.txt
written_2/non-fiction/OUP/Kauffman/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
written_2/non-fiction/OUP/Fletcher/ch6.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chP.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chM.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chO.txt

find written_2 -type d 
written_2
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Rybczynski
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Castro
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```

Sources <br>
I used the "man" command on the terminal to find command-line options for the find command. In addition, I used chat gpt to understand how the command-line option works, what it does, and the specific way that it can be used. I typed "man find" on the terminal to get the different command-line options for the find command. On chatgpt, I typed "What does the find -name command do" and then "can you give me some examples of its usage". I followed a similar process for all the commands mentioned above. 
