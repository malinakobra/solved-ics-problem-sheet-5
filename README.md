Download Link: https://assignmentchef.com/product/solved-ics-problem-sheet-5
<br>
<table width="572">

 <tbody>

  <tr>

   <td width="456"><strong>Problem 5.1: </strong><em>base b numbers closed form</em></td>

   <td width="116"></td>

  </tr>

 </tbody>

</table>

Consider a base <em>b </em>number system (<em>b &gt; </em>1) with <em>n </em>digits and the number 1<em>…</em>1<em><sub>b </sub></em>(<em>n </em>times the digit 1).

<ol>

 <li>Define a sum formula that provides the value of the n-digit number 1<em>…</em>1<em><sub>b</sub></em>.</li>

 <li>Proof via induction that the value of the n-digit number 1<em>…</em>1<em><sub>b </sub></em>is given by the following closed form:</li>

</ol>

For example, the 4-digit base 5 number 1111<sub>5 </sub>has the value .

<strong>Problem 5.2: </strong><em>unicode and utf-8 encoding                                                                        </em>

The content of a file containing UTF-8 Unicode encoded text is given by the following sequence of bytes in hexadecimal notation:

48 65 6c 6c 6f 20 f0 9f 8c 8d 21 0a

<ol>

 <li>Write each byte in binary notation.</li>

 <li>Identify the unicode code points of the characters. What is the text stored in the file?</li>

 <li>Which line end convention is used? What are other popular line end conventions?</li>

</ol>

<strong>Problem 5.3: </strong><em>long years (haskell)                                                                                                                 </em>

According to the ISO8601 calendar, most years have 52 weeks, but some have 53 weeks. These are so called long years. There is a relatively simple way to calculate whether a given year <em>y </em>is a long year. The function <em>w</em>(<em>y</em>) determines with the helper function <em>p</em>(<em>y</em>) the number of weeks in the year <em>y</em>. (Note that the functions use integer division.)

otherwise

Implement a Haskell function isLongYear :: Int -&gt; Bool to determine whether a year is a long year. Use the isLongYear function to calculate all long years in the range 2000..2100.

Submit your Haskell code as a plain text file.

<strong>Problem 5.4: </strong><em>decimal to binary and binary to decimal (haskell)                                                  </em>

Implement a function to convert a decimal number into a binary notation and one function to convert from a binary notation back.

<ol>

 <li>Implement a function dtob :: Int -&gt; String that converts a non-negative integer number into a String (consisting of the characters ’0’ and ’1’) representing the integer number as a binary number. It is not necessary to handle negative integers in a meaningful way.</li>

 <li>Implement a function dtob :: String -&gt; Int that converts a String (consisting of the characters ’0’ and ’1’) representing a binary number into the corresponding non-negative integer number. It is not necessary to handle unexpected strings in a meaningful way.</li>

</ol>

Submit your Haskell code as a plain text file. Below is a template file with a few unit test cases.

1 module Main (main) where

2

3 import Test.HUnit

4

<ul>

 <li><em>— |The ‘dtob’ function converts a non-negative integer number into a</em></li>

 <li><em>— String providing a binary representation of the number.</em></li>

 <li>dtob :: Int -&gt; String</li>

 <li>dtob _ = undefined</li>

</ul>

9

10 <em>— |The ‘btod’ function converts a String representing a non-negative </em>11 <em>— integer number as a binary number into an integer number.</em>

<ul>

 <li>btod :: String -&gt; Int</li>

 <li>btod _ = undefined</li>

</ul>

14

<ul>

 <li><em>{-</em></li>

 <li><em>Below are some test cases.</em></li>

 <li><em>-}</em></li>

</ul>

18

<ul>

 <li>dtobTests = TestList [ dtob 0 ~?= “0”</li>

 <li>, dtob 1 ~?= “1”</li>

 <li>, dtob 2 ~?= “10”</li>

 <li>, dtob 127 ~?= “1111111”</li>

 <li>, dtob 12345 ~?= “11000000111001”</li>

 <li>]</li>

</ul>

25

<ul>

 <li>btodTests = TestList [ btod “0” ~?= 0</li>

 <li>, btod “1” ~?= 1</li>

 <li>, btod “10” ~?= 2</li>

 <li>, btod “1111111” ~?= 127</li>

 <li>, btod “11000000111001” ~?= 12345</li>

 <li>]</li>

</ul>

32

33 main = runTestTT $ TestList [ dtobTests, btodTests ]