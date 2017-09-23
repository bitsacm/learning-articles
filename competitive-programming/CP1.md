# Starting out with Competitive Programming

(This article is meant for beginners.
If you have solved 100+ problems and are looking for guidance on
how to solve problems involving algorithms and data structures,
this document is not for you.)

Competitive Programming is an interesting activity which mixes problem solving with programming.
It is not only enjoyable but also very demanded in placements.
Competitive programming will make you very good at writing efficient programs quickly.
If you get really serious with competitive programming, it will make you an expert in data structures and algorithms.

All Computer Science students are recommended to try it out.

So how to get started?

## Learn a programming language

Any programming language will do.
But most problems are set with C/C++ and Java programmers in mind,
so knowing any one of them will be really helpful.

You don't need to know really advanced concepts, like classes or generics/templates.
You should just know if/else, loops, arrays, functions
and have some familiarity with the standard library,
like math functions, string/array operations and input/output.
For C, `<string.h>`, `<stdio.h>`, `<math.h>`, `<stdlib.h>` will generally be sufficient to start.

If you know only C, you can easily start.
But at some point of time (especially when you reach advanced stages),
you'll need features which most languages have but C does not.
Learning C++ is very easy if you know C.
If you already know C, you should start competitive programming in C and learn C++ in parallel.
> You may refer to [C to C++ for Competitive Programming](c2cpp.md) for a brief intro and resources after you solve [a few basic problems](#making-the-first-step) using C.

Even if you are not confident of your skills in a programming language, you can (and should) still start.
Competitive programming is also a good way to practice a new language you have learned.

If you have no prior knowledge you can begin with [CS50 2016](http://cs50.tv/2016/fall/) (week 0 to week 5)
The course teaches C which anyways is useful as it's a part of BITS curriculum.

## Making the first step

You'll find problems on many websites.

Most websites will give you a specification and ask you to write a program implementing that.
You will then have to submit your code.
Your program will be automatically compiled and run and you'll be told whether it ran correctly or not.
Such websites are known as online judges.

You will find many online judges on the internet.
Here is a small list of the most popular ones:

* [CodeChef](http://www.codechef.com/)
* [SPOJ](http://www.spoj.com/)
* [Codeforces](http://codeforces.com/)
* [HackerRank](https://www.hackerrank.com/domains)
* [TopCoder](https://arena.topcoder.com/)
* [HackerEarth](https://www.hackerearth.com/)

Apart from that, there is also a website called [Project Euler](https://projecteuler.net/archives).
Project Euler does not ask you to submit code. It has direct problems.
For example, their [problem 7](https://projecteuler.net/problem=7)
asks you to find the 10001<sup>th</sup> prime and submit the answer.
You'll need to write code to find this out (since you can't solve this by hand).
But once you have written the code, you just need to run it,
find out the answer, and submit the answer (not the code).

Sometimes it takes time to get used to online judges and Project Euler can help you easily start.
But if you choose to solve problems on Project Euler, do it only when starting out.
It has advanced problems as well, but solving problems on online judges will
help you learn faster and is a better use of your time.

You should stick to just one (or maybe two) online judges when you start.

Most online judges have problems categorized by difficulty levels.
For each difficulty level, easier problems generally have more submissions.
So you can sort problems based on number of submissions to find the easiest ones.

For beginners, Codechef is a good site.
If you have never before solved a problems on an online judge, you can begin by solving
the easiest problem on Codechef - [Life, the Universe, and Everything](https://www.codechef.com/problems/TEST).
You will have to read the [Input/Output tutorial](http://blog.codechef.com/2009/02/24/54/) to solve the problem.
If you face problems, you can refer to [Eklavya's solutions](https://www.codechef.com/status/TEST,sharmaeklavya2).
He has submitted code in many languages, so you'll most likely find a solution in the language of your choice.
Also, Codechef has [screencasts](https://www.youtube.com/playlist?list=PLi0ZM-RCX5ntfqwXRirwA_pcufHinjllG) explaining this problem in C, C++ and Java.

After this you can move on to more problems from [Codechef's beginner section](https://www.codechef.com/problems/school?sort_by=SuccessfulSubmission&sorting_order=desc).
These problems require only basic knowledge of programming (arrays, strings, loops) and math/logic.
The problems with code beginning with `FLOW` are particularly easy and helpful in getting aquainted with submissions on online judges.

SPOJ is also a good place to start.
There are problems there even for people who are new to programming.

## Practice

Remember that it is very important to practice.
Try to solve at least one or two questions everyday.

It is helpful if you stay in touch with people who do competitive programming regularly.
This will keep you motivated.

Often while practicing, you will not be able to solve some problems.
Do not give up easily! Keep trying!
But sometimes even after trying for hours, we are not able to solve it.
In those cases, it is advisable to look at the editorials.
Editorials are step-by-step explanations on how to solve a problem.
Often you'll find new innovative ways of solving problems on reading them.
So sometimes you should read editorials even if you have been able to solve a problem.

Sometimes reading editorials is not enough to understand how to solve a problem.
This is usually the case when you know how to solve it
but you are not able to express your ideas as code easily.
When that happens, you should try looking at others' code.
Some online judges make other people's code public (like Codechef) while some don't (like SPOJ).

## Contests

Once you solve 15 to 20 problems, you should occasionally take part in programming contests.
Many websites host contests regularly.

Codechef has 3 monthly contests - Long challenge, Cookoff and LunchTime.
Long Challenge has 10 questions to be solved in 10 days.
You should try to solve as many questions as you can (without taking hints from others).
Cookoff has 5 questions to be solved in 2.5 hours.
Regularly taking part in Cookoff and trying to perform better in it will increase your speed.

You should not be disheartened if you are able to solve only one or two questions.
This is natural when starting out. As you get better, you'll be able to solve more and more.
If you are not able to solve any question, you should contact a senior and he/she will help you.

When you have solved more than 50 to 75 problems,
you should also start solving problems on Codeforces and taking part in Codeforces' contests.
This is one of the sites where the most serious programmers of the world can be found.

With regular practice, you should become pretty good.
One BITSian solved average 4 questions per day for a year
and he got AIR 7 in a Codechef Long challenge!

## Compiler

One frequently asked question is what compiler or IDE to use.

If you have Linux or Mac, it is best to use:

* gcc for C
* gcc/g++ for C++
* javac for Java (both oracle and openjdk are good)

If you are on windows, you might want to use an IDE.
Code::Blocks is good for C and C++.

There are also some online compilers available.
The most well known is [ideone](https://ideone.com/).
Codechef has an online compiler called [code-compile-run](https://www.codechef.com/ide).

## Standard library

You can often benefit a lot from the rich standard libraries offered by most programming languages.
After gaining sufficient experience with a programming language,
it is advisable to sift through its software libraries to see what all does it offer.

For C/C++, these are good reference sites:

* [cppreference.com](http://en.cppreference.com)
* [cplusplus.com's reference](http://www.cplusplus.com/reference/)

cppreference has the advantage of having an
[offline version](http://en.cppreference.com/w/Cppreference:Archives#Html_book).
However, cplusplus.com's reference is better when you are unfamiliar with the things you are reading about
(which will generally happen with relatively advanced concepts like iterators and STL containers).
cplusplus.com has better explanations for these topics.

Some people realize very late that C++ offers a [sort function](http://www.cplusplus.com/reference/algorithm/sort/).
This is one of the most used functions in competitive programming.

Links to documentation of other languages
* [Python library reference](https://docs.python.org/3/library/index.html)
* [Java library reference](https://docs.oracle.com/javase/8/docs/api/overview-summary.html)
