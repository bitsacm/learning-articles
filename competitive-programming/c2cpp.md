# C to C++ for competitive

Author: [Divesh Uttamchandani](https://github.com/diveshuttam)

This article was written keeping competetive in mind and not for using C++ in development or any other context.
The aim here is to get started with important features of C++ as quickly as possible, so skips many details.
Most of the C++ features talked here work on C++98 and after but some work only after C++11 so for simplicity we will assume to be using C++11. Also we will be using GCC/G++ compiler.
You can also use an IDE like Code::Blocks it already supports GCC and G++ compilers (MINGW); remember to enable C++11 or C++14 option in Code::Blocks' settings.

Once you are familiar with C its easy to migrate to and learn C++.
First of all since C++ is superset of C so you can use most of the concepts of C in C++.
So I will first mention about porting code and then a couple of things new in C++ useful for Competitive.

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

If you don't know any of the above things, its better to have a recap first and than come back to this article.
We WON'T be requiring concepts like `enum`, `union`, `static`, file I/O etc.
As long as you are familiar with the ones above you are good to go.

## Porting C Code

All of the things listed in prerequisites remain same in C++. You can use C's `scanf` and `printf` in C++ also; they are defined in header file <cstdio>.
Similarly string functions are defined in header file <cstring>, math functions in <cmath>.
We will be using the line `#include<bits/stdc++.h>` in our code to resolve all issues at once.
`<bits/stdc++.h>` is basically a header file containing all the standard C++ header files (header files for C/C++ , most STL files etc.).
Though again its not a good developement practice to include unnecesary headers but it is pretty common in competitive,
as judges use runtime for time limit and this only increases my compile time and not my runtime.
For more details you can refer to [geekforgeeks](http://www.geeksforgeeks.org/bitsstdc-h-c/)

Also we will add another line to our code- `using namespace std;` .
Reason here is related to namespaces but ignore this for now.
If curious refer to the links at the end. NOT a reccommended read for beginners.

Another point to keep in mind is that in C++ the return type of main() has to be int.

Keeping above 2 points in mind here is a sample program:

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
To compile this program on linux use `gcc --std=c++11 filename.cpp -o example` to run use `./example`. For codeblocks use `build and run` in build menu.

## New in C++ (useful for competitive)

### Easier I/O (cin and cout)

Note: You can refer to [this tutorial](http://www.cplusplus.com/doc/tutorial/basic_io/) for a better overwiew of I/O in C++,
Just to minimize the number of jumps I have included their basic usage and some useful details for them.

In C++ the input and output are syntactically a bit easier than in C. For example refer to the following code.

```cpp
#include<iostream>
using namespase std;

int main()
{
    int t;
    cin>>t;
    cout<<t;
    cout<<"Hello world";
}
```
This implements the same functionality as the sample C code before this, this is easier in the sense that you don't need to specify placeholders such as "%d" and "%f" etc. how to print is judged on the basis of type of the variable to be printed. Also iostream is the header file for cin and cout. cin and cout are not functions they may be thout as pointers pointing to keyboard and screen (standard input and standard output) respectively in a vague sense ; actual work for input and output is done by **operators** >> and << .
If I write `cin>>a;` remember that the input is generally broken at whitespaces(including tabs, newline, space) i.e consider the following program for example

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

the line `cin>>a>>b>>c;` is es exactly same as `cin>>a;` `cin>>b;` `cin>>c;` this is known as cascading of `>>` operator similarly we have the next line where `<<` operator is cascaded.
Now if I give the following input:

```
1 2
Hello World
```
in real senerio I will press 1 'space' 2 'enter' Hello 'space' World 'enter'
the output of the above program is
```
a=1
b=2
c=Hello
```
Note:
1. Though the input is broken at white spaces but `cin>>something;` is not executed while you are typing the input it is only executed after you press enter.
That makes me type in `Hello world` without reaching `return 0;` .
2. Multiple whitespace between the input are ignored while using cin.
3. In case of type char the input is broken at each character itself. Though for type char* / char[] input is agan broken at spaces.
Coding a few sample programs will help in understanding the working of cin in more detail.
4. Though cin and cout are useful but as such they are slow and can lead to TLE on certain problems.
The way to resolve this is to either use `scanf` and `printf` or add the line `ios::sync_with_stdio(false)` in begining of main() and then use `cin` and `cout` only.
For more details refer to [this quora question](https://www.quora.com/Is-cin-cout-slower-than-scanf-printf)


### STL
C++ has many new features including classes and templates.
Although these are great and interesting concepts but we can work without knowing many of their details for most of our part in competitive.
The main advantage of c++ for competitive is its extensive range of inbuilt "functions" to use algorithms and Data Structures through Standard Template Library (STL).
Although STL is built upon templates, but one need not be knowing much of templates/classes to use it.
Just a basic overview of what is a class and what is a template will suffice.
You may refer to the links given at the end to read about these concepts.
They are enough for our purposes (Concepts related to oop like (inheritance, polymorpism etc) are never used).
Also I recommend going through these links about classes and templates after you have read the tutorials linked in the paragraph below as you will have a bit of context of their actual usage.

A good resource for getting started with STL are topcoder tutorials
([PART I](https://www.topcoder.com/community/data-science/data-science-tutorials/power-up-c-with-the-standard-template-library-part-1/) |
[PART II](https://www.topcoder.com/community/data-science/data-science-tutorials/power-up-c-with-the-standard-template-library-part-2/) ).
They teach how to use STL in context of competitive.
Since STL was added later to C++, Its syntax may seem a bit unusual at first.
But it gets easier after you use it in a few programs.
There is no need to remember the exact prototype of functions in STL as you can always refer to the [STL Docs](https://www.sgi.com/tech/stl/) (link to official docs of HP's implementation of STL which is amongst the most popular ones) or [cppreference](http://en.cppreference.com/w/).
Even in final rounds of prestigious contests, access to some documentation is always provided.
So after completing the two tutorials, you are pretty much dependent on documentation and Google.
Once you have some idea of STL you can go through classes and templates if you feel the need.
Though not recommended initially as the ratio of their use in competitive v/s the amount of time they can potentially consume is not that good.
Most of the features of classes and templates are not required for using STL.

#### Few google searches which may be helpful in learning some new features:

* auto specifier C++11
* range based loop C++11
* strings in C++
* unordered map in C++

#### Namespaces

http://www.geeksforgeeks.org/namespace-in-c/
https://stackoverflow.com/questions/10460250/cstdio-stdio-h-namespace

#### Classes and Templates

http://www.geeksforgeeks.org/c-classes-and-objects/
http://www.geeksforgeeks.org/templates-cpp/
