```

________/\\\\\\\\\__/\\\_______/\\\__/\\\_______/\\\____/\\\\\\\\\_________/\\\\\\\____        
 _____/\\\////////__\///\\\___/\\\/__\///\\\___/\\\/___/\\\///////\\\_____/\\\/////\\\__       
  ___/\\\/_____________\///\\\\\\/______\///\\\\\\/____\///______\//\\\___/\\\____\//\\\_      
   __/\\\_________________\//\\\\__________\//\\\\________________/\\\/___\/\\\_____\/\\\_     
    _\/\\\__________________\/\\\\___________\/\\\\_____________/\\\//_____\/\\\_____\/\\\_    
     _\//\\\_________________/\\\\\\__________/\\\\\\_________/\\\//________\/\\\_____\/\\\_   
      __\///\\\_____________/\\\////\\\______/\\\////\\\_____/\\\/___________\//\\\____/\\\__  
       ____\////\\\\\\\\\__/\\\/___\///\\\__/\\\/___\///\\\__/\\\\\\\\\\\\\\\__\///\\\\\\\/___ 
        _______\/////////__\///_______\///__\///_______\///__\///////////////_____\///////_____
```

# Introduction 

This article will go into the basics of the C++ programming language with the standard being C++20. This will mean we will discuss classes, structures, types, variables, functions, modules, header files, macros, typedefs, namespaces, installs, architectures etc.

# Introduction to C++

C++ is a superset of C in other words its like an add on to the C programming language. C++ is a language that is object orriented and typically deemed as more advanced than C with the way it handles types, templates, structures etc. The C++ programming language is often used for desktop development, backend development and in most cases game development. C++ is a really well written and structured language especially given that it is a super set to C and given all of its changes over the years.

# Why C++

C++ has many issues the main one being that the language is not really memory safe. Most of the time that does depend on the programmer and how they are using certain functions but other times it depends on the backend. This means that C++ is a bit of a wonky language for security, if you do not know what you are doing be prepared to come across a bunch of segmentation faults. Outside of that though c++ like C# has some amazing libraries, kits and backends for development and even has its own custom api for operating systems such as windows which can make development easier. I will not bore you with why exactly you need to choose C++ other than stating that it is a well written language, teaches some really cool type system concepts and is great with mathematics.

# The basics of C++

C++ has some very interesting basics. Below is an example of a hello world program the simplist demo ofc.

 > Hello world

```c++
#include <iostream>

int main() {
 std::cout << "hello world" << std::endl;
 return 0;
}
```

this is a pretty simple program so lets start from the top and work our way down to main.

when importing libraries, code, .hpp or .h source code files there are two different ways to include them. First off every library must be imported using `#include` and after that two symbols based on your situation. If you want to include a local .h file you will be using `#include "something.h" ` because when using the "" you are telling C++ that the source code is in the local directory. If you want to include standard libraries, development kits etc you will need to use `#include <software.h>` or whatever the header file is because that tells C++ to look in either its standard library or its root directory. Most software development libraries will be stored around or near the root C++ directory which means that you will use `<>` to import them. These are the two ways to work with importing other code. Now lets move down to our function 

in C++ every function must start with the data type then the function name. In our case like most languages and programming in general every program uses main() to declare the starting brick of the code. other languages may also have `init()` functions like go which are ran before the `main()` functions. typically init functions or functions alike are used to determine cases such as prerequisite's to starting the program. Now when we look under the main function we call the standard library and namespace called `std` and tell it to call a function to output a stream of data and end it. when we use std::cout we want to ensure the lines are going to end with endl in most cases. Some other cases you may not use std::endl but for text organization it is suggestion. In our main function we return 0 as well. The argument or type specified before the function name is the data type of the variable the function will return. if we had another function such as `bool charactercheck() {}` we would have to return a boolean variable to that statement.

> Namespaces

now as we just got done talking about namespaces are spaces in a program or sets in a program that refer to objects. In C++ everything is an object and we can use namespaces to clear some objects up or reference them. The basic use of a namespace is set like this 

```c++
namespace spacename {
   function();
   int variable;
};
```

namespaces are mainly used for organization and to seperate certain code bricks or bricks of data away from other parts of the code. Now using namespaces is pretty simple just call the namespace name followed by the variable like so.

```c++
namespace spacename {
    int variable = 1;
};

int main() {
 spacename spacer;
 std::cout << spacer.variable << std::endl;
 return 0;
}
```

spacename spacer; is our variable name of the namespace. Sometimes you may not want to assign a variable to that namespace so you can use the keyword known as the `using namespace` keywords. This keyword allows you to use and access variables, functions or any object inside a namespace without calling a variable. 
so to refractor our hello world program instead of calling std::cout we can use cout if we simple tell c++ that we are `using` namespace std such as below.

```c++
#include <iostream>

using namespace std;

int main() {
  cout << "data" << endl;
  return 0;
}
```

now this may get confusing in a second but calling to use `using namespace` is known as bad practice and here is why. In the event that you have a bigger code base say with 30+ source code files and you start using namespaces, classes, structure names etc and tie them all together using the keyword `using namespace` can start collisions with other namespaces. In the event that you have a statement saying `using namespace ofstream;` or something along those lines and have a structure, class or even another namespace with that same name you are destined to create an issue with your program. Something also to note is that if that namespace ends up updating with a newer variable, function or object that has the same name of a object it will also collide with your program. I will always tell people for the sake of general programming to stay away from using the keyword `using namespace` on standard libraries, or code that will be updated outside of your control. In smaller sets this really does not matter but it is still good practice to stay away from it.

> Classes 

Classes are a really good way to organize and use your code. 
