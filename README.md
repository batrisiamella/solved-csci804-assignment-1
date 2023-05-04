Download Link: https://assignmentchef.com/product/solved-csci804-assignment-1
<br>
This assignment aims to establish a basic familiarity with C++ classes. The assignment introduces increasingly object-based, C++ style of solution to a problem.




<strong>General Requirements</strong>

<ul>

 <li>You should observe the common principles of OO programming when you design your classes.</li>

 <li>You should make proper documentation and implementation comments in your codes where they are necessary.</li>

 <li>Logical structures and statements are properly used for specific purposes.</li>

</ul>




<strong>Objectives</strong>

On completion of these tasks you should be able to:

<ul>

 <li>code and run C++ programs using the development environment.</li>

 <li>make effective use of the on-line documentation system that supports the development environment.</li>

 <li>code programs using C++ in a hybrid style (procedural code using instances of simple classes) and in a more object-based style.</li>

 <li>manipulate string data.</li>

</ul>




<strong>Tasks: </strong>

In this assignment, you will design and implement classes that handle real estate properties inspections by using the following UML diagrams (ID means unique identifier).




Define a class <strong>Agent </strong>in a file <strong>Agent.h</strong> and implement constructors / destructor (if necessary), member functions in a file <strong>Agent.cpp</strong>.

Define a class <strong>Property</strong> in a file <strong>Property.h</strong> and implement constructors / destructor (if necessary), member functions in a file <strong>Property.cpp</strong>.

Define a class <strong>Buyer</strong> in a file <strong>Buyer.h</strong> and implement constructors / destructor (if necessary), member functions in a file <strong>Buyer.cpp</strong>.

Define a class <strong>Inspection</strong> in a file <strong>Inspection.h</strong> and implement constructors / destructor (if necessary), member functions in a file <strong>Inspection.cpp</strong>. Define and implement the functions <strong>addNewBooking()</strong>, <strong>searchBookings()</strong> and <strong>saveBookings()</strong> in this class to perform “book a new inspection”, “search inspection bookings” and “save inspection bookings”.

The types of data members are up to you.

<strong>Hint:</strong> <strong>The class Inspection may composite the classes (arrays) Agents, Properties and Buyers.</strong>

Implement <strong>main()</strong> function <strong>and other necessary functions</strong> in a file <strong>realEstate.cpp.</strong> The program loads data from the text files which names should be passed into the main() function by <strong>the command line arguments</strong> when it starts. The program loads data into the dynamic memories (No STL allowed), and displays the records that loaded from the text files. For example,

Load agents’ records.

100; David Roman Volma; 0401123456

101; Bill Grace; 0403123321

102; Alice Brown; 0402111222 Load properties’ information.

1001; 5/10 Northfields Ave, North Wollongong, NSW 2500; Townhouse; 280000

1002; 3 Moore Street, Wollongong, NSW 2500; House; 450000 1003; 23/87 Norman Street, NSW 2500; Unit; 210000 Load buyers’ information.

Alice Smith; 1/2 Moore Street, Wollongong, NSW 2500; 0212345678

Bob Turyn; 23 Southland Road, Wollongong, NSW 2500; 0244123456




The text files <strong>agents.txt</strong>, <strong>properties.txt</strong> and <strong>buyers.txt</strong> for testing can be downloaded from elearning. See the section Testing for more details.

<strong>Hint: You may create dynamic arrays to store data above. Don’t forget to delete those arrays before the program end.  </strong>

<strong>Testing: </strong>

In the working directory on banshee, you can compile the program by g++ –o ass1 realEstate.cpp Agent.cpp Property.cpp Buyer.cpp Inspection.cpp Or to make it simple, you can compile the program by g++ –o ass1 *.cpp

To run the program, you should pass the files’ names to the main() by

./ass1 agents.txt properties.txt buyers.txt

<strong>Note: Do not define constant files’ names inside the source code. </strong>You can use bcheck to check if there is any memory leak by bcheck ./ass1 agents.txt properties.txt buyers.txt

Then the program displays the following menu and gets input choices in a loop until the input choice is 0 (zero):

<ol>

 <li>Book a new inspection.</li>

 <li>Search inspection bookings. Input choice (0-quit):</li>

</ol>

When the input choice is 1, the program will get inputs of a new booking and save the data into the dynamic memories. The function <strong>addNewBooking() </strong>in the class <strong>Inspection</strong> will be called to add a new booking in the memory. The inputs like following (<strong>Note: Data in</strong><strong> Red </strong><strong>means input from the keyboard.)</strong>:

Add a new inspection.

Agent number: 100 Buyer phone: 0212345555 No such a buyer.

Buyer phone: 0212345678

Property id: 100 No such a property.

Property id: 1001

Inspection date (day month year): 10 3 2013 Inspection time (hour minute): 10 0 Comments: good




Suppose we have more inspection bookings,  1. Book a new inspection.

<ol start="2">

 <li>Search inspection bookings. Input choice (0-quit): 1 Add a new inspection.</li>

</ol>

Agent number: 100

Buyer phone: 0212345678

Property id: 1002

Inspection date (day month year): 10 3 2013

Inspection time (hour minute): 10 30

Comments: very good

<ol>

 <li>Book a new inspection.</li>

 <li>Search inspection bookings.</li>

</ol>

Input choice (0-quit): 1 Add a new inspection.

Agent number: 101

Buyer phone: 0244123456

Property id: 1003

Inspection date (day month year): 11 3 2013

Inspection time (hour minute): 10 0 Comments: I want to see more houses 1. Book a new inspection.

<ol start="2">

 <li>Search inspection bookings. Input choice (0-quit): 2</li>

</ol>

When the input choice is 2, the program will get input of an agent’s number and find all inspections booked for him/her. The function <strong>searchBookings()</strong> in the class <strong>Inspection</strong> will be called to do the search.

Input agent number: 100

The agent: 100; David Roman Volma; 0401123456 has following inspections booked.

Property :1001; 5/10 Northfields Ave, North Wollongong, NSW 2500; Townhouse;

280000 by

Alice Smith; 1/2 Moore Street, Wollongong, NSW 2500; 0212345678 at

10/3/2013 10:0

Feedback: good

Property :1002; 3 Moore Street, Wollongong, NSW 2500; House; 450000 by

Alice Smith; 1/2 Moore Street, Wollongong, NSW 2500; 0212345678 at

10/3/2013 10:30

Feedback: very good




<ol>

 <li>Book a new inspection.</li>

 <li>Search inspection bookings.</li>

</ol>

Input choice (0-quit): 2

Input agent number: 101

The agent: 101; Bill Grace; 0403123321 has following inspections booked.

Property :1003; 23/87 Norman Street, NSW 2500; Unit; 210000 by

Bob Turyn; 23 Southland Road, Wollongong, NSW 2500; 0244123456 at

11/3/2013 10:0

Feedback: I want to see more houses

When the input choice is 0, the program will save the inspections’ information into a text file and quit.

<ol>

 <li>Book a new inspection.</li>

 <li>Search inspection bookings.</li>

</ol>

Input choice (0-quit): 0

Save file to: insp.txt

When we check the text file insp.txt, we can find the file contains the following information.

Agent: 100; David Roman Volma; 0401123456

Property: 1001; 5/10 Northfields Ave, North Wollongong, NSW 2500; Townhouse;

280000 be inspected by a buyer:

Alice Smith; 1/2 Moore Street, Wollongong, NSW 2500; 0212345678 at 10/3/2013 10:0

Feedback: good

Agent: 100; David Roman Volma; 0401123456

Property: 1002; 3 Moore Street, Wollongong, NSW 2500; House; 450000 be inspected by a buyer:

Alice Smith; 1/2 Moore Street, Wollongong, NSW 2500; 0212345678 at 10/3/2013 10:30 Feedback: very good

Agent: 101; Bill Grace; 0403123321

Property: 1003; 23/87 Norman Street, NSW 2500; Unit; 210000

be inspected by a buyer: Bob Turyn; 23 Southland Road, Wollongong, NSW 2500;

0244123456 at 11/3/2013 10:0

Feedback: I want to see more houses


