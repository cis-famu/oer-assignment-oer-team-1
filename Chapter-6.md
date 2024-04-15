### Identify the purpose of arrays

Arrays allow a program to specify how many variables must be declared, their data type, and other values with a much simpler statement. An array is a collection of a fixed number of components all of the same data type and in the same memory space. A one-dimensional array is an array in which the components are arranged in a list form. The purpose of arrays is to provide a way to store and access multiple values of the same data type under a single name. 


![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/3202173d-749d-490e-a68e-36517d2265f3)

True or False: Arrays in C++ allow a program to specify how many variables must be declared, their data type, and other values with a much simpler statement.

Answer: True

Arrays are a collection of a fixed number of components all of the same ________ and in the same memory space.

Answer: Data type


What is the purpose of arrays in C++?

A) To provide a way to store and access multiple values of different data types

B) To simplify the declaration of variables in a program

C) To facilitate storage and access of multiple values of the same data type under a single name

D) To dynamically resize collections of elements during program execution


Correct Answer: C) To facilitate storage and access of multiple values of the same data type under a single name








### Declare and initialize arrays

The general form for declaring a one-dimensional array is:


dataType arrayName[intExp];
intExp specifies the number of components in the array and can be any constant expression that evaluates to a positive integer.

The general form (syntax) used for accessing an array component


arrayName[indexExp]
indexExp, called the index, is any expression whose value is a nonnegative integer.

![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/5cc8e8e4-bf05-4bbf-887e-9d59e02360b0)

True or False: In the general form for declaring a one-dimensional array in C++, intExp specifies the number of components in the array, and it can be any expression, regardless of its value.

Answer: False


The general form (syntax) used for accessing an array component in C++ is arrayName[________].

Answer: indexExp


What does indexExp represent in the context of accessing an array component in C++?

A) The number of components in the array

B) The data type of the array elements

C) Any expression whose value is a nonnegative integer

D) The name of the array

Correct Answer: C) Any expression whose value is a nonnegative integer







### Demonstrate manipulating data into arrays

An example of data into arrays will be provided below:

![image](https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156258365/e9dc08c1-2afe-4fa4-9a83-67a18d61b3ca)

True or False: The code provided calculates the average of five test scores entered by the user and displays test scores that are less than the calculated average.

Answer: True


In the provided code, the array named ________ stores the five test scores entered by the user.

Answer: test

What is the purpose of the loop with the condition index < 5 in the given code?

A) To calculate the sum of the test scores

B) To calculate the average of the test scores

C) To iterate through each element of the test scores array

D) To check if any test score is greater than the average

Correct Answer: C) To iterate through each element of the test scores array








### Distinguish the restrictions on array processing

The restrictions on array processing can differ. To start, arrays cannot be directly manipulated or assigned as a whole unit. The only way it could work is if the individual elements are accessed and modified component wise. They would have to be copied individually. When reading data into an array everything must be performed element by element using loops. The restrictions come into play when you try to perform everything together and not individually. 





Which statement  best describes the restrictions on array processing ?

A) Arrays can be directly manipulated and assigned as a whole unit.


B) Individual elements of arrays cannot be accessed or modified separately.


C) Operations on arrays must always be performed collectively, without considering individual elements.


D) Array processing requires accessing and modifying elements individually, as aggregate operations on arrays are not allowed.





Answer: D



### Pass an array as a parameter to a function

Arrays are passed by C++ references, the function receives a reference to the original array. It is different from just copying. The sizing of a one dimensional array that is being declared as a formal parameter is usually omitted. From the example below you see that the size of both arrays are unspecified. At times the number of elements in an array could be less than the size of the array. The function initialize takes an integer array if any size as its first parameter and the size of the actual array is passed as the second parameter when the function is called 


<img width="801" alt="Screen Shot 2024-04-14 at 4 41 20 PM" src="https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156829293/3868767b-cf65-4a5a-b47d-5fa7726bd96d">



The sizing of a one dimensional array declared as a formal parameter is ususally ommited? T/F



Answer
T

### Demonstrate how to search and sort an array


<img width="550" alt="Screen Shot 2024-04-14 at 4 46 07 PM" src="https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156829293/e19408e3-7d2a-48ac-a459-f163316a958c">










<img width="585" alt="Screen Shot 2024-04-14 at 4 47 06 PM" src="https://github.com/cis-famu/oer-assignment-oer-team-1/assets/156829293/e4657afd-c0a6-43ab-bd4d-7cb4baceaae7">


### Use auto declarations
C++11 has this cool feature called auto declaration. It's basically like a shortcut that lets you declare and set up a variable without
needing to say what type it is. Like, you just write auto instead of the type. So, if you wanna make a variable called num and set it to 
30, you can just do:



        auto num = 30;

Since 30 is, like, an int, C++ figures out that num should be an int too.
But it's not just for simple types like integers. You can use auto with more complex types too, like iterators or even complicated objects:

        
        auto it = myVector.begin(); // it's an iterator
        auto result = someFunction(); // result's type depends on what someFunction() returns

This can save you a lot of typing, especially with complicated types where you might not want to write out the whole thing every time; auto can also make your code cleaner and more concise.


### Evaluate range-based for loops

Range-based for loops are like the "easy mode" for going through elements in a collection, like an array or a container. Instead of dealing with index variables and loop conditions, just say, “Hey, C++, go through each thing in this collection and do something with it."

Let’s say you've got an array of integers called numbers. Instead of writing a loop with an index variable like this:

```cpp
for (int i = 0; i < size; ++i) {
    // do something with numbers[i]
}
```

You can use a range-based for loop like this:

```cpp
for (auto num : numbers) {
    // do something with num
}
```

Here, num takes on the value of each element in numbers one at a time, without you having to worry about indices or sizes.

But it's not just for arrays. You can use range-based for loops with any collection that supports iteration, like vectors, lists, sets, maps, and even your own custom types if you provide the proper iterator functions.

For example, if you have a vector of strings called words, you can loop through it like this:

```cpp
for (const auto& word : words) {
    // do something with word
}
```

And if you have a map of integers to strings called phoneBook, you can loop through its key-value pairs like this:

```cpp
for (const auto& pair : phoneBook) {
    // do something with pair.first (the key) and pair.second (the value)
}
```

Range-based for loops make your code cleaner and more readable by hiding the messy details of iteration behind a simple and intuitive syntax. 


### Use C-strings to input data into—and output data from—a C-string

C-strings are strings where each character (type ‘char’) is stored in an array. The size of the array is determined when the array is initialized, it is the size of the string plus 1 extra for the null identifier (‘\0’) at the end to indicate the c-string has ended.	To initialize a cstring use the following as an example: 

    char example[] = "Bikes"; //initializes the c-string

This code creates a c-string named example and enters characters in bikes one into each slot of the array, it simultaneously sets the size of the array and adds a null identifier to the end of the c-string. Below you will find annotated code explaining how to input or output data to/from a cstring:

    #include <iostream>
    #include <string>

    using namespace std;

    int main(){

      char example[] = "Bikes"; //initializes the c-string

    for (int i = 0; example[i] != '\0'; ++i){
      cout << example[i]; // outputs the c-string
     }
    cout << endl;

    for (int i = 0; example[i] != '\0'; ++i){ // turns each vowel in the c-string into a dash
      if (example[i] == 'a' || example[i] == 'e' ||example[i] == 'i' || example[i] == 'o' ||   example[i] == 'u')
        example[i] = '-';
    }
  

     for (int i = 0; example[i] != '\0'; ++i){ //outputs the updated c-string
      cout << example[i]; 
    }
    cout << endl;

    }


### Define parallel, two-dimensional, and multidimensional arrays
Parallel arrays are 2 separate arrays where information correlates to one another. This correlation is defined by the programer and can be used to store separate kinds of information in separate places while also making possible to reference them knowing the information lines up an example of a parallel array can be found below:

    #include <iostream>
    #include <string>

    using namespace std;

    int main(){

    string students[] = {"John", "Sylvie", "Rhonda"}; //initalizes students array

    int grades[] = {30, 97, 77};// initalizes grades array

    int size = sizeof(students)/sizeof(students[0]); // finds the size of the students array

    for (int i = 0; i < size; ++i){ //outputs each student and grade while using the same counter
      cout << students[i] << " has grade: " << grades[i] << endl;

    }

    return 0;
    }

Two-dimensional arrays have information in rows and columns like a coordinate plane with an x and y axis. They are initialized, and information is input/output from them very similarly, the main difference is that when you want to reference them the row and column are necessary.

    #include <iostream>
    #include <string>

    using namespace std;

    int main(){

    int example[3][3] = {
      {2,4,8},
      {16,32,64},
      {128,256,512}
      };
    cout << "example:" << endl;
    for (int i = 0; i < 3 ; ++i) { //rows
      for (int j = 0; j < 3; ++j) { //columns
      cout << example[i][j] << " ";
      }
      cout << endl; 
    }
    return 0;

    }

This code will output:

    example:
    2 4 8
    16 32 64
    128 256 512

3-D and higher arrays can be thought of as adding a layer to the previous. Its as if you have the layer you saw above on top of another layer. As seen below:

    #include <iostream>
    #include <string>

    using namespace std;

    int main(){

    int example[2][3][3] = {
      {{2,4,8}, {16,32,64}, {128,256,512}}, //the double {{}} indicate the layer
      {{1,2,3}, {4,5,6}, {7,8,9}}
      };
    cout << "example:" << endl;    
    for (int i = 0; i < 2 ; ++i) { //layers
    for (int j = 0; j < 3; ++j) { //rows
    for (int n = 0; n < 3; ++n) { //columns
      cout << example[i][j][n] << " ";
      }
      cout << endl << endl; 
    }

    cout << "new layer: " << endl;

    }
    return 0;
    }
This program should output

    example:
    2 4 8 

    16 32 64 

    128 256 512 

    new layer: 
    1 2 3 
    
    4 5 6 

    7 8 9 

