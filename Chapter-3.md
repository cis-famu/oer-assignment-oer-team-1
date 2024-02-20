Identify and use control structures

Identify logical and relational operators, how they work, and order of precedence
_________________________________________________________________________________________________________
Distinguish the relationship of relational operators and simple data types

This topic relates to what we have already learned about data types and variables. In this chapter we are further defining these variables and giving them statements that either are true or false to the subject being expressed in the program. Keep on reading to learn about how you can implement this into your next program.

RELATIONAL OPERATORS AND SIMPLE TYPES 

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
