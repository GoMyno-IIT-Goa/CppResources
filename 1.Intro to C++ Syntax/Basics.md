
# Hello World Program

A brief description of what this project does and who it's for
```cpp
#include<iostream>
using namespace std;

int main()
{
    cout<<"Hello world"<<endl;
    return 0;
}
```
Here;

- ```#include<iostream>``` is a preprocessor directive that includes the content of the standard C++ header file
iostream.
- iostream is a standard library header file that contains definitions of the standard input and output
streams. These definitions are included in the std namespace.
- The standard input/output (I/O) streams provide ways for programs to get input from and output to an
external system -- usually the terminal.
- ```int main() { ... } ```defines a new function named main. By convention, the main function is called upon
execution of the program.
- Here, the int is what is called the function's return type. The value returned by the main function is an exit
code.
- By convention, a program exit code of 0 or EXIT_SUCCESS is interpreted as success by a system that executes
the program. 
- Any other return code is associated with an error.
If no return statement is present, the main function (and thus, the program itself) returns 0 by default. In this
example, we don't need to explicitly write ```return 0;```


# Variables and Datatypes
A variable is a container (storage area) used to hold data.
example:
```int a = 5;```

Here a is the variable name that holds the integer value 2. 
The value of a can be changed, hence the name variable

### Rules of declaring a variable:
- Variables can have alphabets, numbers,  underscores.
- Variable can not be begin with a number.
- Can not be a keyword in C++.
- Can not begin with an uppercase character.

## Fundamental Datatypes in C++
Data types are declarations for variables.
- int
1. this datatype stores integer values.
2. occupies 4 bytes in the memory.

- float and double
1. Used to store decimals and exponentials numbers.
2. size of float is 4 bytes where size of double is 8 bytes.
3. Float can store upto 7 decimal digits whereas double can store upto 15 decimal digits.

- char
1. This data type is used to store character.
2. It occupies 1 byte in memory.
3. ASCII code is used to store characters in memory.
4. Characters in C++ are enclosed inside single quotes ' '.

example: ```char a = 'a'; ```

- bool 
1. This data type has 2 values true and false. True is represented by 1 and false is represented by 0.
2. It occupies 1 byte in memory.

# Comments
- A comment is a way to put arbitrary text inside source code without having the C++ compiler interpret it with any
functional meaning. Comments are used to give insight into the design or method of a program.
- single line comment is written by two forward-slash "//"
```cpp
//This is a single line comment
```
- In the multiline comments the sequence /* is used to declare the start of the comment block and the sequence */ is used to declare the end of comment.
```cpp
/*This is 
a multi line 
comment */
```

# I/O in C++
## Standard output
- With the help of cout operator and insertion operator (<<) we can print the message in screen.
- The << operator can be used multiple times in a single statement. Take a look 
at an example:

```cpp
#include <iostream>
using namespace std;

int main()
{   
    int a = 3;
    cout<<"value of a is "<< a;
    return 0;
}
```
output: ```Value of a is 3```

we can use ```endl``` manipulator or newline charencter(```"\n"```) for a line break

```cpp
#include <iostream>
using namespace std;

int main()
{
    int a = 3;
    int b= 5;
    cout<<"value of a is \n"<< a<<endl;
    cout<<"value of b is \n"<<b;
    return 0;
}
```

## Standard input
With the cin and >> operators we can take the input from the keyboard.

```cpp
#include <iostream>
using namespace std;

int main()
{
    int a;
    cin>>a;
    cout<<"The value of a is "<<a;
    return 0;
}
```
- The cin operator will always return the variable type that you use with cin. So if you request an integer you will get an integer and so on. 
- This can cause an error when the user of the program does not return the type that you are expecting. (Example: you ask for an integer and you get a string of characters.)

cin operator is also chainable like cout
```cpp
// Addition of two numbers

#include <iostream>
using namespace std;

int main()
{
   int a, b;
   cin>>a>>b;
   cout<< "Addition of a and b is "<< a + b;
   return 0;
}
```

# conditional statements 
## if- else statements
The if block is used to specify the code to be executed if the condition specified in if is true, if the condition in the if block returns false then else block is executed.
```cpp
// Lets check if a person is eligible for voting or not.

#include <iostream>
using namespace std;

int main()
{
    int age;
    cin>>age;

    if(age >= 18){
        cout<<"You are eligible for voting";
    }
    else{
        cout<<"You are ineligible for voting"
    }
    return 0;
}
```
## else if statements 
``` cpp
//  Program to check if a triangle is scalene, isosceles or equilateral.

#include <iostream>
using namespace std;

int main()
{
    int a,b,c;    //specifying the sides
    cout<<"Enter the measurements of sides"<<endl;
    cin>>a>>b>>c;

    if(a==b && b==c){
        cout<<"Given triangle is an equilateral triangle";
    }
    else if(a==b || b==c || a==c){
        cout<<"Given triangle is an isoscales triangle"
    }
    else{
        cout<<"Given triangle is a scalene triangle"
    }
    return 0;
}
```
## Nested if conditions
``` cpp
//Program to find the maximum among three numbers

#include <iostream>
using namespace std;

int main() {
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if (n1 >= n2) {
        if (n1 >= n3)
            cout << "Largest number: " << n1;
        else
            cout << "Largest number: " << n3;
    }
    else {
        if (n2 >= n3)
            cout << "Largest number: " << n2;
        else
            cout << "Largest number: " << n3;
    }

    return 0;
}
```
