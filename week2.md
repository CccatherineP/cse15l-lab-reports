1. the first thing we need to do is to download Github desktop to our own computer, and also make sure we have JAVA JDK installed too<br />
2. from the Github desktop, we can go on the repository page, there is a "code" button; you can click on that and choose "Open With Github Desktop", 
then we can open the file we want to open.<br />
3. The next step is to build and run the server on our own computers:<br />
1) enter these two commands in the terminal:<br /> ⤇ javac Server.java NumberServer.java<br />⤇ java NumberServer 4000<br />Then we would be able to see 
this as the output "Server Started! Visit http://localhost:4000"<br />
2) When we go to the link it provides, we can do some tricks<br />
The screen we first saw it's going to be like this<br />![0](https://user-images.githubusercontent.com/122485099/213314216-915e6f08-e4c8-4287-b498-e1846437a479.jpg)<br />
Then we can type "/increment" after 4000 in the url, and return, which we can see the following happens<br />
![increment](https://user-images.githubusercontent.com/122485099/213314462-4d6b01c8-bd8a-480f-b0c2-184ec3eef41d.jpg)
<br />
Next, when we delete the "/increment" we just wrote and enter it, we can see this: <br />

![add_2](https://user-images.githubusercontent.com/122485099/213314622-dfacc74b-6fb6-410e-822d-36cd2037bea4.jpg)
<br />
Here is another trick, which is to enter "/add?count=10", which 10 can be any number that you want to enter, and we can see this next<br />
![add](https://user-images.githubusercontent.com/122485099/213314838-2b640a04-19e5-446d-b236-492fb9eb45d9.jpg)<br />
4. The next thing we want to do is to run the server on the remote computer, which contains the things we learned during the last lab. <br />
  1) we first need to connect our own computer to the server like what we did the last lab session<br />
  2) then we type git clone <your-repository-url-for-your-fork> in our command
  3) when we type java NumberServer 4000, we can change 4000 into any number that we want to, in order not to have the same url with others <br />
  4) let your partner to see if they can access this url on their computer!<br />![run on other server](https://user-images.githubusercontent.com/122485099/213316105-215b0860-7b3a-4b47-bd33-35db164b24ae.jpg)

  

