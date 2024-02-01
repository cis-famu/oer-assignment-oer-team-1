Identify input and output streams

Read data from the standard input device

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

Use manipulators in a program to format output

Perform input and output operations using the string data type

Read data from a file (include examples)

Write data to a file (include examples)

Summary

Key terms

Predefined functions: a wealth of functions that are already written. 
Function call: causes the code attached to the predefined function pow to execute and, in this case, computes 2.0^3.0


References 

