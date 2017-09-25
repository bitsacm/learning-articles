# C to C++ for competitive

Author: [Divesh Uttamchandani](https://github.com/diveshuttam)
Contact: diveshuttamchandani@gmail.com

This article was written keeping competitive in mind and not for using C++ in development or any other context.
The aim here is to get started with important features of C++ as quickly as possible, so skips many details.
Most of the C++ features mentioned here work on C++98 and after but some work only after C++11 so for simplicity we will assume to be using C++11.
Also, we will be using GCC/G++ compiler.
You can also use an IDE like [Code::Blocks](http://www.codeblocks.org/downloads/26) it supports GCC and G++ compiler (Windows users need to download the binary with MinGW).
Remember to enable C++11 or C++14 option in Code::Blocks' settings.

In this article I have primarily covered 2 things:
1) Porting C's code to C++
2) A couple of things new/different in C++ w.r.t C and are useful for competitive.

## Prerequisite

We require that you are aware of at least the following concepts in C:

* Basic Syntax of C
    * Basic Input and Output
    * Operators
* Loops
* Arrays/Strings
* Functions
* Structures
* Pointers

If you don't know any of the above things, it's better to have a recap first and then come back to this article.
We WON'T be requiring concepts like `enum`, `union`, `static`, file I/O etc.
As long as you are familiar with the ones above you are good to go.

## Porting C Code

Once you are familiar with C its easy to migrate to and learn C++.
First of all, since C++ is the superset of C, you can use most of the concepts of C in C++.
All of the things listed in prerequisites remain same in C++.

You can use C's `scanf` and `printf` in C++ also; they are defined in header file `<cstdio>`.
Similarly, string functions are defined in header file `<cstring>`, math functions in `<cmath>`.
We will be using the line `#include<bits/stdc++.h>` in our code to resolve all issues at once.
`<bits/stdc++.h>` is basically a header file containing all the standard C++ header files (header files for C/C++ , most STL files etc.).
Though it's not a good development practice to include unnecessary headers. It is pretty common in competitive,
as judges use runtime for the time limit and this only increases my compile time and not my runtime.
For more details, you can refer to [GeeksforGeeks](http://www.geeksforgeeks.org/bitsstdc-h-c/)

Also, we will add another line to our code- `using namespace std;`.
The reason here is related to namespaces but ignore this for now.
However if curious, refer to the links at the [end](#Namespaces) (NOT a recommended read for beginners).

Another point to keep in mind is that in C++ the return type of main() has to be int.

Keeping above points in mind, here is a sample program:

```cpp
#include<bits/stdc++.h> //includes all header files
using namespace std;

int main()
{
    int t;
    scanf("%d",&t);
    printf("%d",t);
    printf("Hello World")
    return 0;
}
```
To compile this program on linux, use `gcc --std=c++11 filename.cpp -o example` to run use `./example`.
For Code::Blocks use `build and run` in the build menu.

## New in C++ (useful for competitive)

### Easier I/O (cin and cout)

Note: You can refer to [this tutorial](http://www.cplusplus.com/doc/tutorial/basic_io/) for a better overview of I/O in C++,
Just to minimize the number of jumps I have included their basic usage and some useful details here.

In C++ the input and output are syntactically a bit easier than in C ; for example, refer to the following code:

```cpp
#include<iostream>
using namespace std;

int main()
{
    int t;
    cin>>t;
    cout<<t;
    cout<<"Hello world";
}
```
This implements the same functionality as the sample C code before this.
It is easier in the sense that you don't need to specify placeholders such as "%d" and "%f" etc.
How to print a variable is judged on the basis of its type.
`<iostream>` here is the header file for `cin` and `cout`.

If I write `cin>>a;` remember that the input is generally broken at whitespaces(including tabs, newline, space)
i.e consider the following program for example:

```cpp
#include<bits/stdc++.h>
using namespace std;

int main()
{
    int a,b;
    char Str[10];

    cin>>a>>b>>Str;
    cout<<"a="<<a<<"\nb="<<b<<"\nc="<<c;
}
```

The line `cin>>a>>b>>c;` is es exactly same as `cin>>a;` `cin>>b;` `cin>>c;`.
Similarly for `cout`.
Now if I give the following input:

```
1 2
Hello World
```
In the real scenario, I will press 1 'space' 2 'enter' Hello 'space' World 'enter'
The output of the above program is
```
a=1
b=2
c=Hello
```
Note:
1. Though the input is broken at whitespaces, `cin>>something;` is not executed while you are typing the input. It is only executed after pressing enter.
That makes us type in `Hello world` without reaching `return 0;`.
2. Multiple whitespaces between the input are ignored while using cin.
3. In case of type `char`, the input is broken at each character itself. Though for type char* / char[] input is again broken at spaces.
Coding a few sample programs will help in understanding the working of `cin` in more detail.
4. Although `cin` and `cout` are easier than `scanf` and `printf`, as such they are relatively slow. This may lead to TLE on certain problems.
There are 2 ways to resolve this
    1. Use `scanf` and `printf` instead.
    2. Add the line `ios::sync_with_stdio(false)` in begining of `main()` and then use `cin` and `cout` ONLY. For more details refer to [this quora question](https://www.quora.com/Is-cin-cout-slower-than-scanf-printf)


### Standard Template Library
C++ has many new features including classes and templates.
Although these are great and interesting concepts, for most of our part we can work without knowing their details.
The main advantage of C++ for competitive is its extensive range of inbuilt "functions" offered through Standard Template Library (STL).
These include implementations of various Algorithms (sorting, binary search etc.) and Data Structures(stacks, queues, hash map etc.).

Although STL is built upon templates, one doesn't need to know much of templates/classes to use it.
Just a basic overview of __What is a class__ and __What is a template__ will suffice.
You may refer to the links given at the end for an introduction to these concepts. They are enough for our purposes.
Concepts related to OOP like inheritance, polymorphism etc. are never used.
I recommend going through these links about classes and templates after you have read the tutorials linked in the paragraph below.
This is to ensure that you have a bit of a context of their actual usage.

A good resource for getting started with STL is Topcoder tutorials
([PART I](https://www.topcoder.com/community/data-science/data-science-tutorials/power-up-c-with-the-standard-template-library-part-1/) |
[PART II](https://www.topcoder.com/community/data-science/data-science-tutorials/power-up-c-with-the-standard-template-library-part-2/) ).
They teach how to use STL in context of competitive.
Since STL was added later to C++, Its syntax may seem a bit unusual at first.
It gets easier after you use it in a few programs.
There is no need to remember the exact prototype of functions in STL as you can always refer to the following links:
* [STL Docs](https://www.sgi.com/tech/stl/)
* [cppreference](http://en.cppreference.com/w/)
* [cplusplus.com](http://www.cplusplus.com/reference/stl/)

Even in final rounds of prestigious contests, access to some documentation is always provided.
Once you have some idea of STL, you can read the [links about classes and templates](classes-and-templates).
Then have a look at the Topcoder tutorials again. This generally helps in getting started easily.
After this, you are pretty much dependent on documentation and google searches

#### Few google searches which may be helpful in learning more new features:

* auto specifier C++11
* range-based loop C++11
* strings in C++
* unordered map in C++

#### Namespaces

http://www.geeksforgeeks.org/namespace-in-c/

#### Classes and Templates

http://www.geeksforgeeks.org/c-classes-and-objects/
http://www.geeksforgeeks.org/templates-cpp/