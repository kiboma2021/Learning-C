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
		print("%d",x+y+z); 
	 }


--BASIC FORMAT SPECIFIERS---

%d or %i 	int

%f		float

%c		char

%s		strings

%lf		double


---BASIC DATA TYPES SIZES---

int	4 bytes

float	4 bytes

char	1 byte

double	8 bytes


---CONSTANTS---

used to declare variables that cannot latter be changed.

const char ADMINNAME='Brian'

const int BIRTHDAYYEAR=1980;


	#include<stdio.h>
	int main()
	{
	int x=10;
	x+=5;
	printf("%d",x);  //output:15
	return 0;

	}


---IF STATEMENT---

if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}

	#include<stdio.h>
	int main()
	{ 
	int time=20;
	if (time<17){ 
		printf("Time is less than 17\n");
	} else if (time<25){
		print("Time is less than 25\n");
	}else{
		printf("Time is more than 25\n");
	 }
	return 0;
	}


---SHORT HAND IF-ELSE STATEMENT (Ternary Operator)---

variable = (condition) ? expressionTrue : expressionFalse;

	#include<stdio.h>
	int main(){  
		int time=13;
		(time<20)?printf("Time is less than 20"):printf("Time is more than 20\n");
		
		return 0;
	}


---SWITCH STATEMENT---

Instead of using many if--else statements, we can use switch statement to select one of the codes to be executed.

	switch(expression){

	case x:
		//code block;
		break;

	case y:
		//code block;
		break;

	default:
		//code block;

	}


Example:

	#include<stdio.h>

	int main(){

	  int day=4;
	  switch(day){ 
		case 1:
		   printf("Monday");
		   break;
		case 2:
		   printf("Tuesday");
		   break;
		case 3:
		   printf("Wednesday");
		   break;
		case 4:
		   printf("Thursday");
		   break;
		case 5:
		   printf("Friday");
		   break;
		default:
		   printf("Not between Monday to Friday");
		 }
	}

---WHILE LOOP---

A while loop loops through a block of code as long as the specified condition is true

while (condition){
	//block of code
}


	#include<stdio.h>
	int main(){
	int i=0;
	while(i<5){
		printf("%d\n",i);
		i++;
	}
	return 0;
	}

---DO WHILE LOOP---

This excutes a block of code once even if false before checking if the condition is true

do{
#block of code
}
while(condition);

	#include<stdio.h>
	int main(){
	int i=0;
	do{
		printf("%d",i);
		i++;
	}
	while(i<5);
	return 0;
	}

---FOR LOOP---

Used when you aleady know how many times you want to loop though a block of code.

for(statement1;statement2;statement3){
//block of code  
}

	#include<stdio.h>
	int main(){

		int i;
		for(i=0;i<10;i++){
			printf("%d\n",i);
		}
	return 0;
	}
	

---BREAK AND CONTINUE---

Break statement is used to jump out of a loop e.g when i is equal to 4

	#include<stdio.h>
	int main(){
	int i;
	for(i=0,i<10,i++){ 
	   if(i==4){
		break;
		}
	   printf("%d\n",i);
	 }
	return 0;
	}

Continue statement skips current iteration and continous in the next iteration if the specified condition is  fulfilled

	#include<stdio.h>
	int main(){

	int i;
	for(i=0,i<10,i++){  

	if(i==4){
		continue;
	}
		printf("%d\n",i);
	}
		return 0;
	}


---ARRAYS---

Arrays are used to store multiple values in a single variable

int MyNumbers[]={23,45,11,87};

printf("%d",MyNumbers[2]); // access the elements of the array

MyNumbers[0]=33; //change elements of the arrays


	#include<stdio.h>
	int main(){
		int MyNumbers[]={23,4,43,12,12};
		int i;
		for(i=0,i<10,i++){
			printf("%d\n",MyNumbers[i]);
		}
		return 0;
		}

Another common way to create an array is to specify the size of the array and add the elements latter

	#include<stdio.h>
	int main(){
	int myNumbers[4]; //cant change the size after creation

	myNumbers[0]=12;
	myNumbers[1]=33;
	myNumbers[2]=44;
	myNumbers[3]=56;

	printf("%d\n",myNumbers[0]); //result is 12
	return 0;

	}


---STRINGS---

	char greeting[]="Hello world";
	printf("%s",greeting); //Hello world

	printf("%c",greeting[0]);  //H



	#include <stdio.h>

	int main() {
	  char greetings[] = {'H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd', '!', '\0'};
	  char greetings2[] = "Hello World!";
	  
	  printf("%lu\n", sizeof(greetings)); //13
	  printf("%lu\n", sizeof(greetings2)); //13
	  
	  return 0;
	}


---USER INPUT---

To get user input you use scanf() function


	#include<stdio.h>
	int main(){
	int myNum;
	printf("Type a number and press Enter\n");

	scanf("%d",&myNum);

	printf("Your number is: %d",myNum);
	return 0;

	}

You can also get a string entered by the user

	#include<stdio.h>
	int main(){
	char myString[30];
	printf("Print enter a string and press Enter\n");
	scanf("%s",myString);
	printf("The entered string is:%s",myString);

	return 0;
	}


---MEMORY ADDRESS---

---POINTERS---


---FUNCTIONS---

A function is a block of code which only runs when called

	void myFunction(){
		//code to be executed
	}

myFunction - Name of the function

void - Function does not have return value


	#include<stdio.h>
	void myFunction(){
		printf("Function executed");
	}
	int main(){
		myFunction();
		myFunction();
		
		return 0;
	}




	#include<stdio.h>
	void myFunction(char name[],int age[]){
		printf("Hello %s, so you are now %d years old\n", name,age);
	}
	int main(){
		myFunction("Ben",14);
		myFunction("Jane",56);
		return 0;
	}

		
	#include<stdio.h>
	int summations(int x, inty){
		return x+y;
	}
	int main(){
		 printf("Result is: %d", myFunction(5, 3));
		 return 0;
	}


---RECURSION---

Recursion is the technique of making a function call itself

	#include <stdio.h>

	int sum(int k);

	int main() {
	 int result = sum(10);
	 printf("%d", result);
	 return 0;
	}

	int sum(int k) {
	 if (k > 0) {
         return k + sum(k - 1); //sums all interges between 0 and 10
	 } else {
        return 0;
    }
    }		



---NESTED WHILE LOOPS---
They are while loops inside a while loop

	#include<stdio.h>

	/*
	while (condition)
	{
	while(condition){
	  statement;
	  increment;
	}
	  statement;
	  increment;
	}
	*/

	main()
	{
	  
	  int i=0, j;
	  
	  while(i<5)
	  {
	    j=0;
	    while(j<3)
	    {
	      printf("2 ");
	      j++;
	    }
	    printf("\n");
	    i++;
	  }
	  return 0;
	}


