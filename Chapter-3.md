Identify and use control structures

Identify logical and relational operators, how they work, and order of precedence
_________________________________________________________________________________________________________
Distinguish the relationship of relational operators and simple data types

This topic relates to what we have already learned about data types and variables. In this chapter we are further defining these variables and giving them statements that either are true or false to the subject being expressed in the program. Keep on reading to learn about how you can implement this into your next program.

RELATIONAL OPERATORS AND DATA TYPES 

You can use relational operators with all three simple data types. For char values whether the expression evaluates to true or false depends on a machine's collating sequence. Comparing values of different data types may produce unpredictable results. There are only two logical values, true and false, they are useful because they permit programs to incorporate decision making that alters the processing flow. A relational operator is a programming language that defines some kind of relation between two entities. Operator symbols/ names can vary with meaning, look at example 2 for a better definition of the six we will use. 

Example 1: “A”= 65 and “a” = 97 
This shows that lower case variables are greater than uppercase variables. 

Example 2: 

![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/f9e61d89-ed76-4f71-ba09-8e49587ef258)

Review Questions


1. What is the purpose of relational operators in programming? 

A) To declare variables 

B) To perform mathematical equations 

C) To create output statements 

D) To define a relatisonhip between two entities

Answer: D

2. Which of the following is a relational operator?
   
A)  &

B) !=

C) /

D %

Answer: B


3. Is the following statement (true/false)
   
3 != 52

Answer: True


_________________________________________________________________________________________________________
Identify how to form and evaluate logical (Boolean) expressions

This topic relates to what we have recently learned in the previous chapters by relating to string and cout statemnts. Stating a boolean expression, is formed with the help of those previous skills and now we will be putting it all together to make our very own logical boolean expressions.


When forming a logical boolean expression it is important to remember that this expression has a value of either true or false. An expression will not work if the case is both true or both false. An incorrect version of an boolean expression would be Example 1, listed below. This expression is incorrect because the parentheses around the logical expression are missing, which is a syntax error. A correct version of a boolean expression would be Example 2, listed below. This version is right because the boolean expression is wrapped around in parenthesis following the if statement. The use of semicolons is important, if you insert a semicolon right after the parenthesis then the statement will not be operated. 


Example 1: Incorrect  version 

If score >= 60
	grade = ‘P’:


Example 2: 

If (score >= 60)
	Grade = ‘P’; 

Example 3: 

![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/72c50849-2c9c-4a69-8ee3-3478106b365a)


Review Questions 

1. If (score >=90)
	Cout << “Congrats! You have received an A!” 

	If the score inserted was the number 89, would the individual receive this output statement? (true/false)

True or False 

Answer: False

2. Fill in the blank.
For a boolean expression to be correct the expression needs to be wrapped around in _______ following the if statement. 

Answer: Parenthesis

3. True or False, a boolean expression can have a value of true for expressions?
 
Answer: False 





_________________________________________________________________________________________________________
Use one-way and/or two-way selection syntax
Selection statements give your code options when it runs, it’s like branches in a road. There are two kinds of selection statements: else/if and switch. Else if statements allow the user to create two potential paths, a primary and a secondary if the conditions of the primary statement fail. Switch statements have an indefinite number of paths the paths have an order of precedence, if the condition for the path is not met then the compiler continues until the condition is met. Each kind of statement can be found below.

**Else/If:**

	#include <fstream>
	 #include <iostream>
	 #include <string>
	 using namespace std;
	 int main()
	 {
	 int grade;
	 cout << "Enter grade here:  ";
	 cin >> grade;
	  if (grade > 60)
	   cout << "You passed!" << endl;
 	  else
   	 cout << "You failed :(" << endl;
   	 return 0;
    
}

**Switch:**

Demonstrate a switch statement in a program
_________________________________________________________________________________________________________
References

Busbee, K. L. (2018, December 15). Relational operators. 
	Programming Fundamentals.
 	https://harpercollege.pressbooks.pub/programmingfundamental
  	s/chapter/relational-operators/ 
_________________________________________________________________________________________________________

Key Words

Logical boolean expressions: an expression that has a value of either true or false. 

Decision maker: the expression in an if statement which determines whether to execute the statement that follows it.

Action statement: the statement following the expression in an if statement. 
_________________________________________________________________________________________________________
