Download Link: https://assignmentchef.com/product/solved-cs2040s-homework-guess-the-number
<br>
<strong>Problem 0. Guessing Game </strong>Let’s play a game! We’ve written up a program on the server that randomly selects a number between 0 to 1000 (inclusive). Then, it will ask your program to make a guess, which is going to be done by calling the public int guess() function. Your program will then have to return a number that is its guess. Then, the server will either terminate or respond. The details for what happens are listed below.

<ul>

 <li>If your program’s guess was too low, then the server will call your program’s public void update(int answer) method with <em>answer </em>= −1.</li>

 <li>If your program’s guess was too high, then the server will call your program’s public void update(int answer) method with <em>answer </em>= 1.</li>

</ul>

There will be at most 10 rounds of such interaction. If your program manages to guess the number correctly within the 10 rounds, then the server will terminate with acceptance. Else. the server will terminate with rejection.

Here is an example execution between a <strong>possible </strong>program<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> and the server (whose mystery number is 123):

<ol>

 <li>Server calls public int guess() and obtains 0</li>

 <li>Server calls public void update(-1) because 0 <em>&lt; </em>123</li>

 <li>Server calls public int guess() and obtains 200</li>

 <li>Server calls public void update(1) because 200 <em>&gt; </em>123</li>

 <li>Server calls public int guess() and obtains 124</li>

 <li>Server calls public void update(1) because 124 <em>&gt; </em>123</li>

 <li>Server calls public int guess() and obtains 123</li>

 <li>Server terminates and accepts.</li>

</ol>

In the above execution, the program only used 4 guesses. If the program uses 10 guesses and still does not get the right value the server will terminate and reject instead. Implement public int guess() and public void update(int answer) to solve this problem. As a mildly important note: your program will probably need some way of remembering past responses. In this scenario making use of instance variables to store your state would be useful.

<a href="#_ftnref1" name="_ftn1">[1]</a> your program needn’t execute like the one below