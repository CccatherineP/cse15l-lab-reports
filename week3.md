# Part 1
In this part, we are asked to write a web server called `StringServer` 
that supports the path and behavior described below. It should keep track of a single string that 
gets added to by incoming requests. The requests should look like this: <br />
`/add-message?s=<string>` <br />
where you can replacee "<string>" with any string that you want: <br />
  it will print out `Hello` if you add `/add-message?s=Hello` after the original url<br />
  if you change `Hello` into other word, such as `World`, the page will show
  ```
  Hello
  World
  ```
  1) Here is my code for `StringServer`<br />
![StringServer_code](https://user-images.githubusercontent.com/122485099/215002895-0cd26e1c-51fe-4a8c-8d65-c69a611f56fe.jpg)<br />
  2) Here is the screenshot of entering `/add-message?s=Hello`<br />
  ![Hello](https://user-images.githubusercontent.com/122485099/215003579-b472a3eb-a2cd-4cca-bd64-59e0d6d19040.jpg)<br />
  * In this screenshot, the method `handleRequest` is being called
  * The argument `String str` has been passed down through the method. For the values, I have `new URI("http://localhost:4000/add-message?s=Hello")`
  and the string str `"Hello"`
  * The value of URI changed from `"http://localhost:4000"` into `"http://localhost:4000/add-message?s=Hello"`, string str changes from `null` into `"Hello"`
  3) Here is the screenshot when I change "Hello" to "World" <br />
  ![World](https://user-images.githubusercontent.com/122485099/215003637-97316ccf-6d66-44e6-9876-38e3420f081f.jpg)
  * In this screenshot, the method `handleRequest` is being called
  * The argument `String str` has been passed down through the method. For the values, I have `new URI("http://localhost:4000/add-message?s=World")`
  and the string str `"Hello\nWorld"`
  * The value of URI changed from `"http://localhost:4000/add-message?s=Hello"` into `"http://localhost:4000/add-message?s=World"`, string str changes from `"Hello` into `"Hello\nWorld"`<br />
	
# Part 2
  In lab3, we did some debugging and used JUnit to test the code we have. I want to choose the bug in method `reverseInPlace` <br />
  * First, when I wrote the JUnite test as: 
  ```
  @Test 
	public void testReverseInPlace() {
    int[] input1 = { 3, 4 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 4, 3 }, input1);
	}
  ```
  I got the error when I use the input `{ 3, 4 }`
  * Second, when I wrote the JUnite test as: 
  ```
  @Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
  ```
  The input doesn't induce any failure when I use the input `{ 3 }`
  * Here is the screenshot when I run the JUnit test<br />
![reverseInPlace](https://user-images.githubusercontent.com/122485099/215007896-60364615-f8d3-49ea-b25e-409dba84cbc0.jpg)<br />
  * Before the bug is being fixed, the code is:
  ```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < (arr.length); i += 1) {
      arr[i] = arr[arr.length-i-1];
    }
  }
  ```
  After the bug is being fixed, the code is:
  ```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < (arr.length/2); i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length-i-1];
      arr[arr.length - i - 1]=temp;
    }
  }
  ```
  * `revesrseInPlace` from the `ArrayExamples.java` itself contains a bug, the purpose of the program is try to swap places with each other not 
  just one place that swap places. The first bug would be inside the for loop parameters, here we find that the arr.length isn’t divided by 2, 
  this causes a bug because the system read that we are trying to move the whole array but actually we are trying to swap just half of the array. 
  The second bug is we need a temporary variable, here `temp` to store the array element of `i`. After we store it to the temporary variable we can 
  start the swapping process, which is already correct from the beginning. Now lastly, we need to be able to swap each other, so, 
  create another swapping process and then you will store it to the `temp` variable so the `temp` variable will change its values. 
  
# Part 3
  I would say that I learned a lot from the week2's lab, I never create any web server with the code and able to do all these tricks with adding contents 
  at the url. During the lab, codes for creating url were provided, so all we did is to try if the tricks work. Later, we were asked to create our own
  web server, that is also very interesting for me, which made me to look more closely at the codes written for catching and returning things we need for our 
  web server. I also learned a lot from week3's lab, but I already know most of them from my CSE12 class, so I would say that I learned more from the 
  previous week's lab. 
  

