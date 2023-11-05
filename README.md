# Java-Eclipse---PLS50-2ndRE

---------------------------------------------------------------------------------------------------
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

--------------------------------------------------------------------------------------------------------------------------------------

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

If the user selects 2, the program:
It will request and read from the keyboard the path in which the files to be analyzed are contained to find the nodes they contain.
It will check if the path exists and then read the contents of the input folder (the file names) into a string table named filenames.
For each element of the filenames table it will call the fileAnalyzer method. This will again print to the screen first the nodes contained in the input file and then the unique nodes sorted.
If the user selects 3, the program
It will terminate
You can use a switch command, if you wish, to execute the appropriate code on each user selection. An example of running the program in the case where the user selects "2" is given below:
1. Input the name of the file containing URLs you want to analyze
2. Input the path of the directory containing the files you to want to analyze for URLs
3. Exit
Which is your choice?
2
Which directory's files do you want to analyze? 
C:\Users\George\Downloads\urlfind\sources
The filename under analysis is: GeorgeSources.src
The Web sites visited are:
www.realsimple.com
www.caroleking.com
www.realsimple.com
www.billboard.com
www.realsimple.com
www.caroleking.com
www.billboard.com

The unique Web sites visited are:
www.billboard.com
www.caroleking.com
www.realsimple.com


The filename under analysis is: mySources.src
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


1. Input the name of the file containing URLs you want to analyze
2. Input the path of the directory containing the files you to want to analyze for URLs
3. Exit
Which is your choice?

-------------------------------------------------------------------------------------------------
3rd Topic (Supermarket Sales)

A Supermarket chain wants to record for its stores the sales of the products they sell. The Supermarket chain has stores in different cities and they all sell the same products. For the purpose of this exercise, write a class called SupermarketSales that contains as members:
A two-dimensional public table named sales and with data decimal numbers (double). Each row of the table will store the sales (in euros) of a store in the supermarket chain for all products.
Two public integers katastimata and products where respectively the number of stores owned by the supermarket chain and the number of products offered by the chain will be stored. The number of stores corresponds to the number of rows in the sales table and the number of products in the columns of the table respectively. 
A manufacturer that takes as an argument a two-dimensional table. It will check if the contents of the table are valid product sales values (>=0). If they are not, it will display an error message and the program will terminate (you can use the System.exit method). If the data is valid, it will assign this table to sales, and store in katastimata the number of rows in the table and in products the number of columns. 

A public method getKatastimataSales that will traverse the table and calculate for each store the sum of sales and display it on the screen.
A public method getProductSales that will traverse the table, and calculate for each product the sum of sales as well as the average sales per store and display it on the screen.
A public method getSupermarketSales that will traverse the table, and calculate the sum of the supermarket chain sales and the average sales per store and display it on the screen. Figure 2(c)
To test your class, write a program that creates an object of the class by passing the table for the sales of three stores and four products, according to the data shown in Figure 1. The program containing main will be in a second class called MainProgramSupermarket, and will call the methods created appropriately. In Figure 2 you can see sample execution in BlueJ.

---------------------------------------------------------------------------------------------------------
4th Topic (Class extension - Supermarket sales on file)

Extend the SupermarketSales class by creating a subclass called SupermarketSalesToFile. The subclass will include functionality to save the sales results to a text file on disk, rather than displaying them on the screen. 
In the SupermarketSalesToFile subclass you will add:
A class-level (static) field of alphanumeric type named supermarketname, which will store the name of the supermarket chain.
A private alphanumeric field named poli, which will store the City in which there is a store or stores.
A constructor which will take a two-dimensional array as an argument and use the hyperclass constructor (using super) with the same parameter for initialization. You do not need to declare katastimata and products again as they are inherited from the superclass.
A public static void method named setSupermarketName which will take as an argument an alphanumeric which is the name of the Supermarket chain and store it in the static variable. 
A public void method named setPoli which will take as an argument an alphanumeric which is the city and store it in the variable «poli».
A public String method named getPoli that returns the city . 
In addition, override the getKatastimataSales method so that it calculates the results (sum of sales per store) but instead of the screen, stores them in a text file on disk named <katastima>.txt where <katastima> is the name of the corresponding store, e.g. athina.txt or thessaloniki.txt, patra.txt etc. A sample of the file format can be seen in Figure 3.
To test your class, write a program (in a second class named MainProgram4) that creates two SupermarketSalesToFile objects with the sales of 3 stores in the city of athina and 2 stores in the city of patra respectively and saves the results in two separate files. The sales are for 4 products for each store and you can set random values you want in your respective sales variables. There is no need for the user to enter them from the keyboard. 
Your program will first call the static method setSupermarketName() to set the name of the supermarket to "Sklavenitis". Note, that this method can be called directly, without having previously created an object, so the call will be made with the class name, i.e. SupermarketSalesToFile.setSupermarketName("Sklavenitis").

It will then create the two objects of the class, one for each poli, and assign the appropriate values to the poli field of each object.
Finally, it will call the getkatastimataSales method of the two objects to store the results in the corresponding files.

Contact
-------
Feature requests, comments and requests for clarification should all be sent to the author at thanasis20007@gmail.com. I will try to respond quickly to all requests, so feel free to email me!
