Identify input and output streams

A sequence of bytes that make up a set of characters is called a stream from the source (input) to a destination (output). Input streams come from a device into the computer, output streams come from the computer to some destination. To use input/output streams and devices C++ programs must have #include <iostream> in the header file. Allowing the programmer to use “cin” for 
input streams and “cout” for output streams.
________________________________________________________________________________________________________________________________

Read data from the standard input device
The standard input device is a keyboard and mouse used to control most operations of a computer. To read info from a keyboard specifically, the programmer must use “#include <iostream>” in the header file as explained above. Then within the code the function “cin” can be read from a keyboard.

Fix the code below

        #include <fstream>
        #include <iostream>
        #include <string>
        using namespace std;

        int main()
        {
           string name = "";
           cout << "Enter Name here:    ";
           // ENTER MISSING CODE HERE//
           cout << "My name is " << name << "." << endl;
        }

The missing line is:
	
 	cin >> name;
________________________________________________________________________________________________________________________________
Describe input stream functions get, ignore, putback, and peek

A function, also called a subprogram, is a set of instructions. Predefined functions, are a wealth of functions that are written. A very useful function, pow, called the power function, can be used to calcu;ate x^y in a program. 


Get
Sometimes you need to process the entire input, including whitespace characters, such as blanks and the newline character. The variable cin can access the stream function get, which is used to read character data. The get function inputs the very next character, including whitespace characters. 

						cin.get(varChar);
      
	You can effectively use the get function as follows:
1. cin.get(ch1);
2. cin.get(ch2);
3. cin>>num;
   
Ignore
When you want to process only partial data, you can use the stream function ignore to discard a portion of the input.

						cin.ignore(intExp, chExp);
      
In the above statement, intExp is an integer expression yielding an integer value. For an example, the number is 50, this means the program will ignore the next 50 characters. When the function ignore is used without any arguments, then it only skips the very next character. 

Putback & Peek
Suppose you are processing data that is a mixture of numbers and characters and you want the numbers to be read as numbers. Putback lets you put the last character extracted from the input stream by the get function back into the input stream. 

						istreamVar.putback(ch);

Peek looks into the input stream and tells you what the next character is without removing it from the input stream. 

						ch=istreamVar.peek();
      
Review Questions:
True/False: The get function inputs the very next character, including whitespace characters, from the input stream and stores it in the memory location indicated by its argument. 
  Fill in the blank: The syntax for putback is _______
 Which of the following statements are input stream functions?
Get
Ignore
Putback 
Peek
All of the above 
  
True  2. istreamVar.putback(ch)  3. (e) All of the above 
________________________________________________________________________________________________________________________________
Write data to the standard output device

_____________________________________________________________________________________________________________________________________
## Use manipulators in a program to format output

Chapter 2 discusses how important it is for programmers to generate the output they desire in their programs. It explains using the << operator and endl to display results on the screen. However, output isn't just about showing results it's also about formatting them correctly. For instance, sometimes you need to show numbers with a specific number of decimal places, like in a paycheck. Other times, you might need to align numbers in columns or fill empty spaces with certain characters. This section teaches you about different functions and manipulators to format your output exactly how you want it.

### Setprecision Manipulator:

The manipulator setprecision is employed to manage the output of floating-point numbers. Typically, floating-point numbers are displayed in scientific notation by default. Certain integrated development environments (IDEs) may default to showing floating-point numbers with a maximum of six decimal places. However, in scenarios like printing an employee's paycheck, the desired output typically requires only two decimal places. To achieve this, the setprecision manipulator is utilized to adjust the precision to 2 for printing floating-point output with two decimal places.

To use this manipulator the header file iomanip will need to be included in your code for example:

				           #include <iomanip>				

You will use the setprecision manipulator with cout and << for example:


				             cout << setprecision(2);
		 
Where the number 2 would occupy the intend number of decimal places.

### Fixed:

To have more control over the display of floating-point numbers, additional manipulators can be utilized. When aiming to output floating-point numbers in a fixed decimal format, the manipulator fixed is employed. The subsequent statement demonstrates setting the output of floating-point numbers in a fixed decimal format on the standard output device:

			                      cout << fixed;

Once the preceding statement is executed, all floating-point numbers will be presented in the fixed decimal format until the manipulator fixed is deactivated. You can deactivate the fixed manipulator by employing the stream member function unsetf. For instance, to disable the fixed manipulator on the standard output device, you would use the following statement:

				             cout.unsetf(ios::fixed);


### showpoint: 

If the decimal portion of a decimal number happens to be zero, instructing the computer to display the number in a fixed decimal format may result in the decimal point and the decimal part not being shown. To ensure that the output includes the decimal point and any trailing zeros, the manipulator showpoint is utilized. The subsequent statement demonstrates setting the output of decimal numbers to display the decimal point and any trailing zeros on the standard output device:

			                      cout << showpoint;
If you want your output in a fixed decimal format use:

			                      cout << fixed << showpint;

    

### set w:

The setw manipulator is employed to display the value of an expression within a specified number of columns, where the expression can be either a string or a number. Using setw(n) outputs the next expression in n columns with right justification. If, for instance, you set the number of columns to 6 but the output only needs three columns, the initial three columns remain empty. Moreover, if the specified number of columns is less than the actual columns needed for the output, the output automatically extends to the required number of columns without truncation. You can use this with cout and <<, for instance

				             cout << setw(3) << x << endl;
This statment would output 'x' into 3 coloums. In order to use this manipulator you would have to include the header file iomanip, similar to the setprecision manipulator.



### setfill:

Remember that with setw, if the specified number of columns is more than needed for the expression, the output aligns to the right, and the extra columns on the left get filled with spaces. By using setfill, you can make the output stream variables fill those extra columns with a character other than a space. The correct syntax is:

				             ostreamVar << setfill(ch);

Where 'ch' is the character and ostreamVar is the output stream variable.


### left and right Manipulators:

Remember, if the specified number of columns in the setw tool is more than what the next expression needs, it's usually right-justified. However, if you want the output to be left-justified instead, you can use the left manipulator. For example :

				             ostreamVar << left;
		 
You can use the same syntax with right, or you can disable this manipulator by using unsetf. The correct syntax is: 

					ostreamVar.unsetf(ios::left); 

_____________________________________________________________________________________________________________________________________
Perform input and output operations using the string data type
-------------------------------------------------------------------------------------------------------------------------------------
Read data from a file (include examples)

In this example there is a file named “neededdata.txt”
In that file it will display the following 
Hi! 
This is group1.

#include <iostream>
#include <fstream> 
#include <string>

using namespace std;

int main() {

    ifstream inputFile("neededdata.txt");

    string line;
    cout << "Contents of the file:" << endl;
  
  while (getline(inputFile, line)) {
        cout << line << endl;
    }

    inputFile.close();

    return 0;
}

Once we run the code it will display “neededdata.txt” line by line.

Review Question
-------------------------------------------------------------------------------------------------------------------------------------
Write data to a file (include examples)

In this example there will be a text written to the file “needed.txt”

#include <iostream>
#include <fstream>

using namespace std;

int main() 
{
    
    ofstream outputFile("needed.txt");

    outputFile << "Hi!" << endl;
    outputFile << "This is group 1." << endl;

    outputFile.close();

    cout << "Data has been input into needed.txt" << endl;

    return 0;
}

Once we run the code a file named “needed.txt” would then be created and the following “Hi!
This is group 1” will be displayed inside of that file.

Review Question
-------------------------------------------------------------------------------------------------------------------------------------

Summary

Key terms

Predefined functions: a wealth of functions that are already written. 
Function call: causes the code attached to the predefined function pow to execute and, in this case, computes 2.0^3.0


References 

