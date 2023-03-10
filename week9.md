# Lab Report 5
I really like lab report 3, so I choose to explore more on this one. This time, I choose `find` as the command and found 4 interesting command-line options or alternate ways to use the command I chose
## 1. `find -type`
The `-type` option allows you to specify the type of file you want to search for, such as directories (d) or files (f). This is useful when you are trying to figure out what directories are inside the file<br />
Example 1: 
```
find ./written_2 -type d
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2
```
![find -type](https://user-images.githubusercontent.com/122485099/224428058-0df159f4-2781-4b56-bee6-0d21d682b8bf.jpg)

Here, I want to find all directories inside `./written_2`, that's what `find ./written_2 -type d` does in this case. <br />

Example 2: 
```
find ./written_2/non-fiction/OUP/Fletcher -type f
./written_2/non-fiction/OUP/Fletcher/ch1.txt
./written_2/non-fiction/OUP/Fletcher/ch10.txt
./written_2/non-fiction/OUP/Fletcher/ch2.txt
./written_2/non-fiction/OUP/Fletcher/ch5.txt
./written_2/non-fiction/OUP/Fletcher/ch6.txt
./written_2/non-fiction/OUP/Fletcher/ch9.txt
```
![f](https://user-images.githubusercontent.com/122485099/224436544-057a5158-b55a-42db-a67a-ef796f5ad09f.jpg)
Here, I want to find all files inside `./written_2/non-fiction/OUP/Fletcher`, that's what `find ./written_2/non-fiction/OUP/Fletcher -type f` does in this case. <br />

## 2. `find -printf`
The `-printf` option allows you to specify the output format for the files found by find. This is useful if you want to see more information of the files being printed out by the command. <br />
Example 1: 
```
find ./written_2/non-fiction/OUP/Berk -type f -printf '%f %s\n'
CH4.txt 103491
ch1.txt 92355
ch2.txt 102942
ch7.txt 66887
```
![-printf](https://user-images.githubusercontent.com/122485099/224432151-e2da0ddd-6396-4019-ac28-8e957801c333.jpg)
Here, I want to print the filename and size of all files inside `./written_2/non-fiction/OUP/Berk`, that's what `find ./written_2/non-fiction/OUP/Berk -type f -printf '%f %s\n'` does in this case. <br />
Example 2: 
```
find ./written_2/non-fiction/OUP/Castro -type f -printf '%f %s\n'
chA.txt 35675
chB.txt 32819
chC.txt 23635
chL.txt 24476
chM.txt 55410
chN.txt 9182
chO.txt 8349
chP.txt 41470
chQ.txt 8274
chR.txt 33420
chV.txt 19909
chW.txt 6724
chY.txt 5424
chZ.txt 5431
```
![-printf2](https://user-images.githubusercontent.com/122485099/224432306-b7e1bafe-79e5-4dce-9d1d-8bbeabe11d34.jpg)
Here, I want to print the filename and size of all files inside `./written_2/non-fiction/OUP/Castro`, that's what `find ./written_2/non-fiction/OUP/Castro -type f -printf '%f %s\n'` does in this case. <br />

## 3. `find -size`
The `-size` option allows you to search for files of a specific size. This is useful if you want to find the larger files or smaller files. <br />
Example 1: 
```
find ./written_2 -size +100k
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
```
![-size](https://user-images.githubusercontent.com/122485099/224433082-6a025341-f89c-42e4-af4f-50fab777253c.jpg)
Here, I want to find the files that are larger than 100KB inside `./written_2`, that's what the command `find ./written_2 -size +100k` does in this case. <br />
Example 2: 
```
find ./written_2 -size -5k 
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1/HandRHongKong.txt
./written_2/travel_guides/berlitz1/HandRIbiza.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt
./written_2/travel_guides/berlitz1/HandRJerusalem.txt
./written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
./written_2/travel_guides/berlitz1/HandRLasVegas.txt
./written_2/travel_guides/berlitz1/HandRLisbon.txt
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt
./written_2/travel_guides/berlitz1/HandRMadeira.txt
./written_2/travel_guides/berlitz1/HandRMallorca.txt
./written_2/travel_guides/berlitz1/WhatToFrance.txt
./written_2/travel_guides/berlitz1/WhatToHawaii.txt
./written_2/travel_guides/berlitz1/WhereToHawaii.txt
```
![-size2](https://user-images.githubusercontent.com/122485099/224433711-acf42104-340d-4cee-8809-202407766617.jpg)

Here, I want to find the files that are smaller than 5KB inside `./written_2`, that's what the command `find ./written_2 -size -5k` does in this case. <br />

## 4. `find -prune`
The `-prune` option allows you to exclude specific directories (or files) from the search. This is useful when you want to exlude certain directories from the search. <br />
Example 1: 
```
find ./written_2/non-fiction -path ./written_2/non-fiction/OUP/Berk -prune -o -type d -print
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
```
![p1](https://user-images.githubusercontent.com/122485099/224435652-d61deaff-edd9-49d2-9a86-18c33ce3b66f.jpg)
Here, I want to find the directories from `non-fiction` but exclude `Berk`, that's what the command `find ./written_2/non-fiction -path ./written_2/non-fiction/OUP/Berk -prune -o -type d -print` does in this case. <br />

Example 2: 
```
find ./written_2/non-fiction -path ./written_2/non-fiction/OUP/Castro -prune -o -type d -print
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
```
![p2](https://user-images.githubusercontent.com/122485099/224436219-bab5a1cc-82ab-4506-9b46-3f75cfd957af.jpg)
Here, I want to find the directories from `non-fiction` but exclude `Castro`, that's what the command `find ./written_2/non-fiction -path ./written_2/non-fiction/OUP/Castro -prune -o -type d -print` does in this case. <br />
*I found all the information by asking ChatGPT







