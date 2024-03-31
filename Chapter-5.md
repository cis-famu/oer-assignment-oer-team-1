  //Understanding the Purpose of Functions//
-Explain what a function is and why functions are used in programming.-

A function in programming is a block of code. It's  like a recipe. It's a set of instructions that performs a specific task when you use it.
A function is sort of like a  mini-program inside a larger program. Functions help keep your code organized and easier to understand because 
they group related tasks together in one. Functions  also make it easier to reuse code, which means we don't have to write the same thing over 
and over again. It limits the redundancy. So, whenever we need to perform a particular task, we can just call the function instead of writing 
out all the instructions again.


-Describe the benefits of using functions (code reusability, modularity, abstraction)-

Code Reusability: With functions you are able to write a code one time and reuse that code as many times as you desire throughout your program. 
This ultimately saves you time and reduces the chances of small errors in your code.  


Modularity: Functions help by collapsing the program into smaller parts, that essentially is easier for the program to read. Each function can be
used to solve a certain problem or perform a certain task.You are also able to collaborate with your team on different functions.This makes your code
easy to read, organized, and simple. 

Abstraction: The functions don't reveal the details of how the codes work. However it isn't really needed. What's important is how the code works and 
how to use it properly. This makes your code simpler, easier to understand, and easier to maintain. When you modify the function you can do so without 
affecting the rest of your code.






//Function Syntax and Structure//
Define the key components of a function: return type, function name, parameters, function body, and return statement.
Differentiate between void and value returning functions.
Demonstrate the use of the return statement to return values from functions.
Identify function prototypes.

### Writing Basic Functions

This C++ program checks if a given integer is even or odd. It prompts the user to enter a number, then determines its parity using a basic
function called isEven(). If the number is even, it prints "even", otherwise "odd". This program demonstrates the simplicity of using
functions in C++ to solve basic arithmetic problems.

      #include <iostream>
      
      using namespace std;
      
      bool isEven(int n) {
        return (n % 2 == 0);
        }
      
      int main() {
          int num;
          cout << "Enter a number: ";
          cin >> num;
          if (isEven(num))
              cout << num << " is even." << endl;
              else
              cout << num << " is odd." << endl;
              return 0;
              }

This next program demonstrates a simple function to determine whether a given integer is positive, negative, or zero. The function
checkNumber() takes an integer as input and prints a corresponding message based on its sign. The main function prompts the user to enter a
number, calls the checkNumber() function, and outputs the result accordingly. This program showcases the use of functions and conditional
statements in C++ to analyze basic numeric values.
  
      #include <iostream>
      
      using namespace std;
      
      // Function to check if a number is positive, negative, or zero
      void checkNumber(int num) {
          if (num > 0)
              cout << num << " is positive." << endl;
          else if (num < 0)
              cout << num << " is negative." << endl;
          else
              cout << num << " is zero." << endl;
      }
      
      int main() {
          int num;
          cout << "Enter a number: ";
          cin >> num;
          checkNumber(num);
          return 0;
      }
___________________________________________________________________________________________________________________
//Calling Functions//
Call functions from within other functions or the main function, passing arguments correctly.
Understand the concept of passing arguments by value.
Understand the concept of passing arguments by reference.

//Function Overloading//

Function overloading is a feature that allows the programmer to use the same function to do different things. Normally something like this would be a problem however, when the function is used multiple times with different amounts or kinds of parameters each one can be used as if they were named entirely different functions. An example with notes can be seen below:

    #include <iostream>
    #include <string>

    using namespace std;

    int multiply(int x, int y){
      return  x * y;
    }

    // This statement works because it has more int arguments than the original
    int multiply(int x, int y, int z){ 
      return  x * y * z;
    }

    //----------------------------------------------------
    // This statement works because it the double argument
    // is not shared with the other multiply functions
    //----------------------------------------------------
    double multiply(double x, double y, double z){
      return  x * y * z;
    }

    int main(){

    // each of the cout functions list the  arguemts that correlate to one of the multiply fuctions
    cout << multiply (4,3) << endl;
    cout << multiply (4,3,2) << endl; 
    cout << multiply (4.2,3.5,2.9) << endl;

    return 0;

    }

However, issues may occur if the overloaded functions overlap your code will likely out put an 'ambigious' error because it is unclear to the compiler which of your overloaded funtion youre refrencing. An example can be seen below:

    #include <iostream>
    #include <string>

    using namespace std;

    int multiply(int x, int y){
      return  x * y;
    }

    int multiply(int x, int y, int z){ 
      return  x * y * z;
    }

    double multiply(double x, double y, double z){
      return  x * y * z;
    }

    int main(){

    cout << multiply (4,3) << endl;
    cout << multiply (4,3,2) << endl; 
    cout << multiply (4,3.5,2.9) << endl; //<------

    return 0;

    }

The compiler does not know which iteration of the multiply function to use because the arguments over lap the int (4) should be a double (4.0).

For practice copy and paste the code below into a shell and fill in the blanks:

    #include <iostream>
    #include <string>

    using namespace std;

    int add(int x, int y){
      return  x + y;
    }

    int add(______________){ 
      return  x + y + z;
    }

    int main(){

    cout << add (4,3) << endl;
    cout << add (________) << endl; 


    return 0;

    }

