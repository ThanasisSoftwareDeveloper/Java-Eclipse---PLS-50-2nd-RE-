# Java-Eclipse---PLS50-2ndRE

1st Topic (Edit File with URLs)

A programmer wants to extract from a text file (the file mySources.src is given with the
exercise) containing web page addresses, the addresses of the websites without further
specification such as specific pages within the website or other queries. That is, if a line in
the file contains the address www.w3schools.com/quiztest/quiztest.asp?qtest=JAVA then
the developer wants to export the section www.w3schools.com
Write a URLsVisited class which is intended to read from a file containing web site
addresses one by one the lines and isolate the nodes they contain. It will store them in an
ArrayList structure and print them to the screen. It will then identify the unique nodes and
print them on the screen after an appropriate message.
The class will contain the following members:
A private one-dimensional ArrayList of alphanumerics named myURLs.
A constructor which will take as argument the name of a text file (containing web page
addresses). The constructor will read, line-by-line, the contents of the file, separate the
parts of each web page address, and store the node address it contains in the ArrayList
myURLs.
A public method named removeDuplicates that will have no argument. This will first
remove the duplicate elements from the ArrayList myURLs and then sort it. 
A public method printAll that will print all elements contained in the ArrayList myURLS.
To test your class, create a second class named URLsVisitedApp that will contain the main
method and which will accept from the user the name of the file containing the addresses
of the web pages (as an example, the file mySources.src is given along with the exercise).
For your convenience, you can provide the entire path along with the file name from the
keyboard.
The URLsVisitedApp class will additionally contain a fileAnalyzer method that will take as
an argument the name of the file given by the user. This will implement the following: 
It will create a URLsVisited object with this file as an argument.
It will call the printAll instance of method in order to print all the addresses of the nodes
contained in the file.
It will call the removeDuplicates instance of method to find the unique addresses of the 
nodes and sort them.
It will again call the printAll instance of method to print the unique addresses of the nodes 
contained in the file.
An example of running the program if the mySources.src file (which for the purposes of 
this example is assumed to be in the C:\Users\George\Downloads\urlfind\sources\ folder) 
is used as input is shown below:


Which filename do you want to analyze? 
C:\Users\George\Downloads\urlfind\sources\mySources.src
The file analyzed is:  C:\Users\George\Downloads\urlfind\sources\mySources.src

The Web sites visited are:
www.test.gr
www.politico.eu
www.java67.com
en.wikipedia.org
www.cnn.gr
www.politico.eu
www.investopedia.com
en.wikipedia.org
www.cnn.gr
www.ceicdata.com
en.wikipedia.org

The unique Web sites visited are:
en.wikipedia.org
www.ceicdata.com
www.cnn.gr
www.investopedia.com
www.java67.com
www.politico.eu
www.test.gr


An example of running the program if a file name that does not exist is used as input is the following:

Which filename do you want to analyze? 
myResources.src
The file analyzed is:
myResources.src

java.io.FileNotFoundException: myResources.src (The system cannot find the file specified)
Could not find the file myResources.src. Please insert a valid path and filename

Note: In order to read from a file you can use the commands you will find in example 9.2 of your book  or the Scanner class. You will need to do mandatory exception handling with a
try ... catch ... statement.

----------------------------------------------

2nd Topic (Edit Files with URLs with Options Menu)

Write a class named URLsVisitedMenu that contains the main() method. The program will use the URLsVisited class of Topic 1. It will display the menu of options on the screen as follows:

1. Input the name of the file containing URLs you want to analyze
2. Input the path of the directory containing the files you to want to analyze for URLs
3. Exit
Which is your choice?

The menu will be displayed by calling a menu() method contained in the URLsVisitedMenu class, which will read and return the user's selection. This can only be 1, 2 or 3 and only then will the menu return, 
otherwise it will display the options again. The case where the user enters something other than the numbers 1, 2 or 3 can be handled through a combination of exception handling and a do... while iteration structure (make sure your program handles the case of unintended user input such as a String or a double number through exception handling).
The URLsVisitedMenu class will also contain the fileAnalyzer method as you constructed for Topic 1 with the same functionality.
The program will be executed iteratively (and here you can use do... while) until the user gives the 3 that terminates it.
If the user chooses 1, the program:
It will request and read from the keyboard the path and name of a file (as a single String) whose contents will be parsed to find the nodes it contains.
It will then call the fileAnalyzer method with the String containing the path and file given as an argument.
This method will print on the screen first the nodes contained in the input file and then the unique nodes sorted.
