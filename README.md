# Learning-C
What Is C?

It is a high-level programming language that Was developed by Dennis Ritchie in 1972.
Was named C because there was a programming language known as B-language
The difference between C and C++ is that C++ supports classes and objects while C does not

There are two types of programming languages:
1) compiled
2) Interpreted

--INSTALLING CODEBLOCK IDE--
	sudo apt update
	sudo apt --fix-broken install
	sudo apt-get install codeblocks 


To install GCC the C compiler in ubuntu:
	sudo apt install build-essential
	gcc --version
	gcc -o hello hello.c // to run the compile
	./hello


--WRITING C PROGRAM---

	#include <stdio.h>// this header must be included in the C program
	int main()
	{
		printf("This is my first C program \n");
		return 0;
	}


--C VARIABLES---

1) int
2) float
3) char

type variablename =value;
int students=53;

or:
int students;
students=53;
students=72; // This overwrites the previous value

printf(students); //This is not possible in c
printf("%d",students); //This is the correct synthax

	#include<stdio.h> 
	int main()
	{ 
		int x=5;
		int y=20;
		int sum=x+y;
		printf("%d",sum);
	}
	

	#include<stdio.h>
	int main()
	{
		int x=5,y=22,z=30;
		print("%d",x+y+z) 
	 }
