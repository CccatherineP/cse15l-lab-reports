I choose `grep` as the command and found 4 interesting command-line options or alternate ways to use the command I chose<br />
# 1. `grep -r -l`
This option is used to find the file that contains certain word and listed them all out in the output, this is useful when you want to see the exact file
and their location<br />
Example 1: 
```
grep -r -l "Bali" written_2/
written_2/travel_guides/berlitz1/HandRHawaii.txt
written_2/travel_guides/berlitz2/Bali-History.txt
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
```
![-r -l_1](https://user-images.githubusercontent.com/122485099/218333749-d92c2590-8868-4375-a637-0a8973e081e3.jpg)
Here, I try to find the files that contain "Bali" and list them in the output, that's also what the command `grep -r -l "Bali" written_2/` does. <br />
Example 2:
```
grep -r -l "Milan" written_2/
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryIstanbul.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/IntroItaly.txt
written_2/travel_guides/berlitz1/WhatToItaly.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
```
![image](https://user-images.githubusercontent.com/122485099/218333873-9b155b31-11b8-4c26-9849-d26c1f66dd54.png)
Here, I try to find the files that contain "Milan" and list them in the output, that's also what the command `grep -r -l "Milan" written_2/` does. <br />

# 2. `grep -c`
This option is used to count the number of occurrences of a pattern in the specified file(s), this is useful when you want to count the number of a specific word in a file<br />
Example 1: 
```
grep -c "extremity" written_2/travel_guides/berlitz2/Algarve-History.txt
1
```
![image](https://user-images.githubusercontent.com/122485099/218334673-abdf5ac1-e73f-45a3-8b33-b69ec7f8bb33.png)

Here, I try to count how many times that the word "extremity" exists in the Algarve-History.txt, by using the command `grep -c "extremity" written_2/travel_guides/berlitz2/Algarve-History.txt
`, I was able to count the "extremity" word in the text <br />

Example 2:
```
grep -c "is" written_2/travel_guides/berlitz2/Algarve-History.txt
33
```
![image](https://user-images.githubusercontent.com/122485099/218334748-74e295da-24b3-409f-8685-8735cc528a60.png)
Here, I try to count how many times that the word "is" exists in the Algarve-History.txt, by using the command `grep -c "is" written_2/travel_guides/berlitz2/Algarve-History.txt
`, I was able to count the "is" word in the text <br />

# 3. `grep -i`
This option is used to make the search case-insensitive, which list the lines that contain the word (case doesn't matter), this is useful since we cannot predict 
where the word is going to be in the line, so case-insensitive makes it easier<br />
Example 1:
```
grep -i "PM" written_2/travel_guides/berlitz1/HandRLosAngeles.txt
numbers. Check-out time is generally noon or 1pm, with check-in usually
available from 2pm to 3pm. All hotels accept major credit cards.
```
![image](https://user-images.githubusercontent.com/122485099/218334895-fec24d7b-422a-49db-914a-2eb5b49a00d1.png)
Here, when I type the word "PM" in capitalized letter, but command `grep -i "PM" written_2/travel_guides/berlitz1/HandRLosAngeles.txt` can still help me find the line(s) that contain the word, no matter the case. 
<br />
Example 2:
```
grep -i "june" written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
high season (late June–mid Sept) or during school holidays (one week in
```

![-i_2](https://user-images.githubusercontent.com/122485099/218335146-40338a34-62b5-4a32-84dc-a372342d1df8.jpg)

Here, when I type the word "june" in capitalized letter, but command `grep -i "june" written_2/travel_guides/berlitz1/HandRLakeDistrict.txt` can still help me find the line(s) that contain the word, no matter the case. 
<br />


# 4. `grep -v`
This option is used to invert the match and display lines that do not contain the word, this is useful when you don't want to contain the information 
that you don't want<br />
Example 1:
```
grep -v "to" written_2/travel_guides/berlitz1/HandRIbiza.txt
Recommended Hotels
The establishments listed below offer a cross-section of
local restaurants, and should convince you that not everything on the
island comes with chips (french fries).
offfical government rating system.
As a basic guide, the symbols we use indicate what you can
✪less than 5,000 ptas.
✪✪5,000–8,000 ptas.
✪✪✪more than 8,000 ptas.
```
![image](https://user-images.githubusercontent.com/122485099/218335717-390e33c3-b041-4a58-a3c1-adee8263404c.png)
Here, I want to see the lines in the file that do not contain the word "to", and by using the command `grep -v "to" written_2/travel_guides/berlitz1/HandRIbiza.txt`
, I was able to get the output.<br />

Example 2:
```
grep -v "0" written_2/travel_guides/berlitz1/HandRIstanbul.txt
Recommended Hotels
Finding accommodation in Istanbul is rarely a problem, as
the city has recently seen a boom in the hotel business. However, if
you want a room in a particular hotel, it is best to book, especially
during July and August. The main hotel areas are Laleli, Aksaray, and
Sultanahmet in the Old City, and around Taksim Square in Beyo‘lu.
Intense competition among the middle-range hotels means that you can
often bargain for a lower rate, especially if you plan to stay for more
than two nights.
As a basic guide we have used the symbols below to indicate
prices for a double room with bath, including breakfast:
```
Here, I want to see the lines in the file that do not contain the word "0", and by using the command `grep -v "0" written_2/travel_guides/berlitz1/HandRIstanbul.txt`
, I was able to get the output.<br />
![image](https://user-images.githubusercontent.com/122485099/218336181-fcd27992-361e-4827-af5c-2bb74c95d2d9.png)<br />
*I found all the information by asking ChatGPT



















