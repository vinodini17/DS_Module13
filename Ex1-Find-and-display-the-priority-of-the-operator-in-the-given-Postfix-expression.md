# EX 1(A) Display operator precedence in the infix expression.
## DATE: 21/08/2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1.Start the program. 

2.Include the required libraries.

3.Define a function to display the priority of the operator in a postfix expression. 

4.Use if-else statements to specify the priority and return it. 

5.End the program.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Vinodini R
RegisterNumber: 212223040244
*/

#include <stdio.h>
#include<string.h>

    int priority(char x)
{
    
    if(x == '&' || x == '|')
        return 1;
    if(x == '+' || x == '-')
        return 2;
    if(x == '*' || x == '/' || x == '%')
        return 3;
    if(x == '^')
        return 4;
        
    return 0;
}

int main()
{
   int i,j;
   char ch[100]="(A*B)^C+(D%H)/F&G";
   
   for(i=0;i<strlen(ch);i++)
   {
   if(ch[i]=='+'||
   ch[i]=='-'||
   ch[i]=='*'||
   ch[i]=='/'||
   ch[i]=='%'||
   ch[i]=='^'||
   ch[i]=='&'||
   ch[i]=='|')
       {
       j=priority(ch[i]);
       switch(j)
       {
           case 1:
             printf("%c  ----> ",ch[i]);
           printf("Lowest Priority\n");
             break;
            case 2:
             printf("%c  ----> ",ch[i]);
           printf("Second Lowest Priority\n");
             break;
            case 3:
             printf("%c  ----> ",ch[i]);
           printf("Second Highest Priority\n"); 
             break;
            case 4:
             printf("%c  ----> ",ch[i]);
           printf("Highest Priority\n");
             break;
       }
       }
   }
   
    return 0;
}

   

```

## Output:

![437299890-192a7ad7-4af4-4eef-b076-1daef622f064](https://github.com/user-attachments/assets/9cf2c7d4-aeea-497d-9813-f99be4fda328)


## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
