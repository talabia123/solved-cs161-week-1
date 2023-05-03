Download Link: https://assignmentchef.com/product/solved-cs161-week-1
<br>
In this assignment you’ll get some practice with some of the tools we’ll be using throughout the course.  These instructions will assume that you have followed the tutorials in the “Tools You Will Need” page.

Use a terminal emulator to log into the school server (flip).  Type ​<strong>ls</strong>​ to list the contents of the directory you’re in.  Type ​<strong>ls -l</strong>​ for more information about each file.  Create a new directory called “week1” by typing ​<strong>mkdir week1</strong>​.  Go into that directory by typing ​<strong>cd week1</strong>​ (you can get back out of it by typing ​<strong>cd ..</strong>​ which moves you up one level from your current directory).  Use vim (or emacs or nano) to make a file named animal.cpp. Type the following code into the file:

#include &lt;iostream&gt;

#include &lt;string&gt;




// a simple example program int main()

{ std::string faveAnimal;

std::cout &lt;&lt; “Please enter your favorite animal.” &lt;&lt; std::endl; std::cin &gt;&gt; faveAnimal;

std::cout &lt;&lt; “Your favorite animal is the ” &lt;&lt; faveAnimal; std::cout &lt;&lt; “.” &lt;&lt; std::endl;




return 0;

}

Add a comment block at the top as discussed in the Code Style Guidelines.  Now save the file.  Type ​<strong>ls</strong>​ to verify that this directory now contains a file named animal.cpp.  Next type ​<strong>g++ animal.cpp -o animal</strong>​.  This will compile your source file and create an executable file named “animal”.  The ​<strong>-o</strong>​ flag lets you choose a name for the executable file.  If you instead just type ​<strong>g++ animal.cpp</strong>​, the name of the executable file will be “a.out”.  It is important that you do not accidentally give your executable file the same name as the source file.  If you do that, then your executable file will replace your source file and your source file will be gone (and you will be sad).  Now type in ./​<strong>animal</strong>​.

The program should now ask you to enter the name of your favorite animal, and after you do, it will print out “Your favorite animal is the &lt;whatever you typed&gt;.”  Notice that this program only reads the first word of the input, so if the animal name contains any spaces, the full name won’t be printed out.