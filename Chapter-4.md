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
IV. Manipulating Loop Behavior: Break and Continue

Outcome 1: Demonstrate the use of 'break' to prematurely exit a loop.
Outcome 2: Apply 'continue' to skip the remaining portion of a loop iteration and advance to the next.
Outcome 3: Design scenarios where the strategic use of 'break' and 'continue' enhances code readability and efficiency.
V. Nesting Control Structures: Loops within Loops

Outcome 1: Create nested loops to solve problems requiring multiple levels of iteration.
Outcome 2: Control the execution flow of nested loops effectively to achieve the desired outcome.
Outcome 3: Debug nested loops with multi-dimensional iteration patterns.
VI. Debugging Strategies: Perfecting Your Loops

Outcome 1: Identify common logical errors arising in repetition control structures.
Outcome 2: Utilize debugging tools to trace code execution and locate the source of errors within loops.
Outcome 3: Develop preventive coding practices to minimize the occurrence of logic errors in loops.
