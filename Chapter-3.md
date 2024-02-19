Identify and use control structures

Identify logical and relational operators, how they work, and order of precedence

Distinguish the relationship of relational operators and simple data types

Identify how to form and evaluate logical (Boolean) expressions

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
