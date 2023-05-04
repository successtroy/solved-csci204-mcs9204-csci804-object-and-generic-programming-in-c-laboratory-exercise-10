Download Link: https://assignmentchef.com/product/solved-csci204-mcs9204-csci804-object-and-generic-programming-in-c-laboratory-exercise-10
<br>
<strong>Task One: Palindrome (0.5 Marks) </strong>




A palindrome is a sequence of characters, numbers or words that have the property of reading the same in either direction (backwards or forwards). In a palindrome white space and punctuation have no significance (they are typically ignored).




Examples of palindromes are in the table below.

<strong>121</strong>  – A numeric sequence

<strong>GACTTCAG</strong> – A DNA Sequence

<strong>Sator Arepo tenet opera rotas.</strong> – A latin phrase for: <em>The farmer by his labour keeps the wheels to the plough. </em>

As you can see in the last example, white space and capitalization are ignored. <strong><em>You are to write a program that takes in a sequence and works out if it is/ isn’t a palindrome</em></strong>. We are going to do this in two different ways.

<strong> </strong>

Write a C++ program that reads a string/sequence from standard input till EOF. The string/sequence, including all white space, punctuation and newline characters should be read in character-by-character and stored into a vector. The vector should hold objects of type char. When the sequence is finished being read in create two iterators. One iterator points to the beginning and the other the end of the vector.




By using these iterators you can work out if the sequence is the same in both forward and reverse directions. Remember that you should ignore case, punctuation and white space characters. If the sequence is a palindrome, you should print it out in both forward and reverse directions and indicate it is a palindrome. Otherwise display an error message.




Save your code as <strong>task1Main.cpp</strong>. You can compile the program by

$g++ -o palindrome task1Main.cpp

Run the program like

$./palindrome &lt; exp1.txt

“GACTtCAaG” is a palindrome




$./palindrome &lt; exp2.txt

“A Toyota! Race fast, safe car! A Toyota!” is a palindrome




$./palindrome &lt; exp3.txt

“A nut for one jar of tuna.” is not a palindrome

<strong> </strong>

<h1>Task 2: Maps (0.5 Marks)</h1>




The Australian Tax Office (ATO) is currently rewriting a piece of software. As part of the process the ATO needs to migrate a text file, which contains an integer as unique identifier (also known as a tax file number), and a string (a persons full name which can contain white space characters) per line. Each tax file number is ‘normally’ associated with one name.




The file may look something like this:




654342 Fred E Smith

213233 Joe Blow

212221 Sarah T Brown

897654 Jamie Shotton

874356 Richard G Lyn




Assume the appropriate headers are included; the file stream ins is opened for input and a map is created using the declaration,




map&lt;int, string&gt; taxrecord()




Assume the following typedefs exist.




typedef map&lt;int, string&gt;::iterator mapit;

typedef map&lt;int, string&gt; maptype;




<ul>

 <li>Write a function with the prototype</li>

</ul>

void populatemap(maptype&amp; taxrecords, ifstream&amp; ins);




Where the map taxrecords, is passed by reference and key/ data pairs are read from the stream ins one by one and inserted into the map. You should report any duplicate insertions into the map with an error message.




<ul>

 <li>Write a function with the prototype</li>

</ul>

mapit findrecord(maptype&amp; taxrecords, int key);




Where the map taxrecords is passed by reference and an integer key, key, is passed. The function should attempt to find the key value in the map. If such a value is found, the function should return an iterator pointing to the matched pair, otherwise the value of the return value should be




taxrecords.end().




<strong>atoMap.cpp</strong> is a sketch of the program including a main() function to define and populate the taxrecord map  and test the two function defined in (a) and (b).










Complete the code atoMap.cpp. Compile and test is as follows:




$g++ -o atoMap atoMap.cpp




$./atoMap &lt; ato.txt




The total number of records is 5

Find the person whose TFN is 212221

212221 -&gt; Sarah T Brown




Find the person whose TFN is 212221

Not find





