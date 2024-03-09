I. Recognizing the Power of Repetition

Outcome 1: Explain the core concept of repetition in programming.
Outcome 2: Identify real-world scenarios where repetition control structures streamline code.
Outcome 3: Compare the efficiency of code written with and without repetition structures.

1. Repetition in programming is the basic ability to perfrom a block a code multiple times based on a condition that hass been set by the programmer. This allows the program to run automatically perform task with the same set of insctrctions without having to rewrite the code however many times is need. Those instructions are replaced with loops. All in all it is a time saver.
2. A Real world scenario where repetition control structure streamline code is to take a survey for your buisness growth. The survey may have 5 questions with 3 answer choices or outcomes. The code conducted would multiply the set number 3; 5 times to display all possible outcomes.
3. The efficicency of the coode with repition decreases the amount if human error which will enhance the code likely hood of success. On the opposite end a code written without repetion could have human errors and the codes readabiltiy will be lower.


II. Demystifying While Loops

Outcome 1: Construct basic while loops with correct initialization, condition checking, and updates.
Outcome 2: Differentiate between for loops, do-while loops, and EOF-controlled loops, using examples.
Outcome 3: Modify loops to iterate a specific number of times or until a user-defined condition is met.

1.
#include <iostream>

int main() {
 
    int count = 1;

    while (count <= 5) {
       cout << count << endl; 
        count++; 
    }

    return 0;
}
2. A for loop excutes a code a certian amount given of times.
   #include <iostream>

int main() {
    for (int i = 0; i < 5; i++) {
        cout << i << " ";
    }
    return 0;
}
  
   
   A do-while loop excutes a code at least once and continues if given statement is true or correlates. 
   #include <iostream>

int main() {
    int i = 0;
    do {
       cout << i << " ";
        i++;
    } while (i < 5);
    return 0;
}


   A EOF-controlled loop excutes a code by reading from file until EOF is reached. 
   #include <iostream>

int main() {
    int num;
    while (cin >> num) {
        cout << "You entered: " << num << endl;
    }
    return 0;
}

3.
#include <iostream>

int main() {
    int level = 5;
    for (int i = 0; i < level; i++) {
        cout << "level" << i + 1 << endl;
    }
    return 0;
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------






III. Conditional Logic: Controlling Flow with If and Else
Outcome 1: Write 'if' statements to implement decision-making within loops.
Outcome 2: Incorporate 'else' and 'else if' statements to create multi-branch conditional logic.
Outcome 3: Apply nested 'if' statements to handle complex decision scenarios within loops.

If statements are a type of conditional statement that allows the programer to ensure a certian set of execuables only happen when a conditon or a number of conditons is met. In other words the function executes _if_ the conditon(s) are true. An else if statement is one that only exists within a larger conditional branch, else if statements execute if their conditional statement is true and the previous statement reads false. Several if else statments can be used one after the other for different conditons creating a large tree of differnet paths. Else statements execute if all the previous if and if else statements read false. Nested if statements create more complex trees by creating conditional statements within conditional statements. Each of the 3 statments and a nested if statement can be found with explainations below.

    #include <iostream>
    #include <string>
    using namespace std;

    int main(){

    string answer1, answer2, answer3, answer4, answer5, userinput;

    int points;

    cout << "Thanks for playing my trivia game. Type S to begin!" << endl;
    cin >> userinput;

    if (userinput == "S"){

     cout << "How many United States Presdents have there been? (enter the answer below)" << endl;
    cout << "a) 45" << endl << "b) 49" << endl << "c) 51 " << endl << "c) 42 " << endl;
    cin >> userinput;
    if (userinput == "a" ){
    
      cout << "Great Job! +1 point" << endl;
      points++;
      
       }
      else{
      cout << "Incorrect! loser get rekt" << endl;
      }
    cout << "What year did World War II end?" << endl;
     cin >> userinput;
    if (userinput == "1945"){
      cout << "Good job!" << endl;
      points++;
    }
    
    else if (userinput < "1900"){
      cout << "Bro youre dumb" << endl;
    }
    else if (userinput > "1900" && userinput <"1945"){
      cout << "Under shot it a bit but close." << endl;
      }
    else if (userinput < "1945"){
      cout << "Too far!" << endl;
    }
    else {
      cout << "This isnt even an integer bro?" << endl; 
    
      }
    


    
  


    }

    cout << points << " points";
    }

IV. Manipulating Loop Behavior: Break and Continue
Outcome 1: Demonstrate the use of 'break' to prematurely exit a loop.
Outcome 2: Apply 'continue' to skip the remaining portion of a loop iteration and advance to the next.
Outcome 3: Design scenarios where the strategic use of 'break' and 'continue' enhances code readability and efficiency.


____________________________________________________________________________________________________________________________________________________________
V. Nesting Control Structures: Loops within Loops

Outcome 1: Create nested loops to solve problems requiring multiple levels of iteration.


#include <iostream>
using namespace std;
int main (){


    for (int i = 1; i <= 5; i++)
    {
        for (int j = 1; j <= i; j++)
            cout << ":)";
        cout << endl;
     }
    return 0;
}


Outcome 2: Control the execution flow of nested loops effectively to achieve the desired outcome.

To control the execution flow of nested loops effectively, you can use the control statements like break and continue to alter the loop behavior based on certain conditions. 


Outcome 3: Debug nested loops with multi-dimensional iteration patterns


A software patch is a piece of code written on top of an existing piece of code intended to fix a bug in the original code.  Adding a patch can eliminate the symptom.

Patch example: 

If (i != 4)


![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/d1c38fda-f46e-4f5e-8661-18a904c79e00)



REVIEW QUESTIONS

1. True or False? Nested loops are loops within a loop.

 True/ False
 
ANSWER: TRUE


2. True or False? The break statement can only be used within the innermost loop in a nested loop structure.
   
True/False

ANSWER: FALSE


4. Fill in the Blank.
   
In nested loops, the inner loop runs _____ times for each iteration of the outer loop.

ANSWER: MULTIPLE

____________________________________________________________________________________________________________________________________________________________
VI. Debugging Strategies: Perfecting Your Loops

Outcome 1: Identify common logical errors arising in repetition control structures.

Incorrect loop boundaries may lead to off-by-one errors. Ensure the loop condition is correct and terminates at the intended point. Failure
to update the loop control variable inside the loop may result in an infinite loop. Initializing the loop control variable with the wrong
value can cause unexpected behavior. Complex conditions in loop statements may lead to unintended behavior. You also need to ensure a
proper mechanism exists to exit the loop when the desired condition is met. Another common error is incorrectly updating the loop control
variable; it may result in unexpected behavior. Verify that loop control variables are used appropriately within the loop. Lastly, be 
cautious with direct equality comparisons for floating-point variables due to precision issues.

Outcome 2: Utilize debugging tools to trace code execution and locate the source of errors within loops.

#include <iostream>

using namespace std;

int main() {

    int n = 5;
    int sum = 0;

    // The Loop calculates the sum of numbers from 1 to n
    for (int i = 1; i <= n; ++i) {
        // Print loop control variable and intermediate result for debugging
        cout << "Iteration " << i << ": ";
        cout << "Current sum = " << sum << ", Adding " << i << endl;

        // Update the sum
        sum += i;
    }

    // Print the final result
    cout << "\nFinal sum: " << sum << endl;

    return 0;
}

In this example, these print statements serve as a form of debugging output, helping you understand the flow of execution and verify 
variable values.

Outcome 3: Develop preventive coding practices to minimize the occurrence of logic errors in loops.

To minimize the occurrence of logic errors in loops in C++, you can adopt preventive coding practices. These practices focus on writing 
clean and understandable code that executes properly.

Test Edge Cases:
Thoroughly test loops with boundary values and edge cases to identify and address potential issues related to loop conditions and variable
values.

Initialize Loop Control Variables:
Always initialize loop control variables before using them in a loop. This helps prevent unexpected behavior due to uninitialized variables.

Avoid Unnecessary Infinite Loops:
When confronted with an infinite loop, the root cause typically lies in the logical expression controlling the loop's execution. It is 
crucial to meticulously inspect the logical expression for potential issues, such as reversed inequalities, mistaken assignment symbols in 
place of equality operators, or improper use of && instead of ||. Always ensure there is a clear exit condition for loops to prevent 
unintentional infinite loops. Use a break statement or an appropriate condition to exit the loop when needed. 

Review questions:
1. What is the most common error associated with loops?

2. What is the significance of debugging in the software development process?

3. What is it called when you test the loops with boundary values?
   
Answers:
1. The most common error associated with loops is off-by-one.
2. It ensures the program's reliability by discovering and fixing issues before releasing it to users.
3. Test Edge Cases.
____________________________________________________________________________________________________________________________________________________________
Key Terms 

Infinite loop: A loop that continues to execute endlessly.

Counter controlled while loop: A while loop that is used when you know how many items of data are to be read.

Sentinel: A special value that will tell the loop to stop.

Flag controlled while loop: Usess a boolean varaible to control the execution of the loop.

End of fike controlled while loop: A while loop that stops when it reaches the end of the input file.

For loop: Used to simplify the writing of counter controlled loops; consiists of an initalization statement, loop condition, and the update statement.

Nesting: A process that involves putting one control structure inside another.

Pretest loops: While and for loops evalutes the loop condition before executing the body of the loop.

Posttest loops: Do while loops areevaluted after executing the body of the loop. 

____________________________________________________________________________________________________________________________________________________________
References

https://www.bing.com/images/search?view=detailV2&ccid=rFFSCduI&id=DB2F9AFB214969E4D1D99D5F0A53521829B54E00&thid=OIP.rFFSCduIZgjqWUDw1Mc5ugHaC-&mediaurl=https%3a%2f%2fpynative.com%2fwp-content%2fuploads%2f2021%2f06%2fpython-nested-for-loop-768x308.png&cdnurl=https%3a%2f%2fth.bing.com%2fth%2fid%2fR.ac515209db886608ea5940f0d4c739ba%3frik%3dAE61KRhSUwpfnQ%26pid%3dImgRaw%26r%3d0&exph=308&expw=768&q=example+of+nestd+loop+C%2b%2b&simid=608008911287628791&FORM=IRPRST&ck=214E7D892FEDA9E883326E78F94C8DFB&selectedIndex=68&itb=0&ajaxhist=0&ajaxserp=0
____________________________________________________________________________________________________________________________________________________________
