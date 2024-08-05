# Experiment 5 and 6
**Experiment 5** <br>
<br>
**Aim:** <br>
To study and implement C++ decision making statements. <br>
<br>
**Theory:** <br>
Conditional statements allow you to make decisions within your programs. Specifically they can be used to execute specific blocks of code for particular situations only. <br>
There are four primary conditional statements in C language: _if statement_, _if-else statement_,_ if-else if-else statement_, and _switch statement_. <br> 
_if:_ The simplest form among conditionals where a certain condition is evaluated and if it evaluates true then certain flow control unit executes its commands. <br>
_if-else:_ This is an extension of the first form since we have the alternative block whose commands get executed provided that the original statement was false when selected. <br>
_if-elseif-else:_ This enables the evaluation of several conditions sequentially until it finds one which is true whereby if this happens its contained or associated block will be executed while ignoring all other blocks. <br>
_switch case:_ This facilitates picking one among many subprograms depending on a variable’s value. So rather than using multiple nested if-else statements we can use switch instead.<br>
<br>
**Code:** <br>

```
#include <iostream>
using namespace std;
int main()
{
    int a,b,c;
    cout<<"if-else ladder"<<endl;
    cout<<"Enter the first number: ";
    cin>>a;
    cout<<"Enter the second number: ";
    cin>>b;
    cout<<"Enter the third number: ";
    cin>>c;
// if-elif-else ladder
    if ((a>b) && (a>c))
    {
        cout<<"First number is the largest."<<endl;
    }

    else if ((b>a) && (b>c))
    {
        cout<<"Second number is the largest."<<endl;
    }

    else
    {
        cout<<"Third number is the largest."<<endl;
    }
    cout<<endl;
    cout<<endl;

//nested if
    cout<<"nested if"<<endl;
     if ((a>b) && (a>c))
    {
        if (b>c)
        cout<<"Sum of first and second number: "<<a+b<<endl;
        else
        cout<<"Sum of first and third number: "<<a+c<<endl;
    }
    else if ((b>a) && (b>c))
    {
        if (a>c)
        cout<<"Subtraction of second and first number: "<<b-a<<endl;
        else
        cout<<"Subtraction of second and third number: "<<b-c<<endl;
    }
    else
    {
        if (a<b)
        cout<<"Product of third and first number: "<<c*a<<endl;
        else
        cout<<"Product of third and second number: "<<c*b<<endl;
    }

    cout<<endl;
    cout<<endl;
    //switch case
    cout<<"switch case"<<endl;
    int ch;
    float ans;
    cout<<"Enter the first number: ";
    cin>>a;
    cout<<"Enter the second number: ";
    cin>>b;
    cout<<"Press 1 for addition."<<endl;
    cout<<"Press 2 for subtraction. "<<endl;
    cout<<"Press 3 for multiplication. "<<endl;
    cout<<"Press 4 for division"<<endl;
    cout<<"Enter your choice: ";
    cin>>ch;

    switch (ch)
    {
    case 1:
    {
        ans = a + b;
        cout<<"Sum: "<<ans;
        break;
    }

    case 2:
    {
        ans = a - b;
        cout<<"Subtraction: "<<ans;
        break;
    }
    
    case 3:
    {
        ans = a * b;
        cout<<"Product: "<<ans;
        break;
    }

        case 4:
    {
        ans = a / b;
        cout<<"Division "<<ans;
        break;
    }

    default:
    {
        cout<<"INVALID INPUT";
    }
        break;
    }
}
```

<br>

**Output:** <br>

![exp5](https://github.com/tanishaamenon/CDS---Control-Statements/blob/main/exp5.JPG)
<br>

**Conclusion:** <br>
&#8594; We learnt about conditional statements and their use case. <br>
&#8594; We learnt how to utilize these statements efficiently. <br>
<br>

******************


**Experiment 6** <br>
<br>
**Aim:** <br>
To study and implement C++ decision making statements Loops. <br>
<br>
**Theory:** <br>
In C++, loops are programming constructs that allow a certain section of code to be repeated as many times as needed. 
The main loops in C++ are *for* loop, *while* loop and *do-while* loop. <br>
_for:_ Suitable for situations where the number of iterations has been determined beforehand. It consists of a starting value, condition checker and an increment or a decrement value in one single line making it neat and easy to read. <br>
_while:_ Mostly used on cases whose number of repetitions is unknown and whose state depends on a condition which is first checked then continues to the execution of the loop body itself. The loop will continue as long as the condition holds true. <br>
_do-while:_ It is like the while loop but it assures  that the code will  run at least once because its condition is examined after its block runs. This comes in handy especially if your code needs to be executed no less than once. <br>
<br>

**Code:** <br>

```
#include <iostream>
using namespace std; 

int main()
{
    //do-while
    cout<<"Using do while loop: "<<endl;
    int a = 10;
    do
    {
        cout<<a<<endl;
        a--;
    } while (a != 0);

    cout<<endl;
    cout<<endl;

   //for loop
    cout<<"Using for loop: "<<endl;
    int i = 0;
    for(i = 0; i <=10;i++)
    {
        cout<<i<<endl;
    }
    cout<<endl;
    cout<<endl;

    //while loop
    cout<<"Using while: "<<endl;
    int b = 10;
    while(b>0)
    {
        cout<<b<<endl;
        b--;
    }
    cout<<endl;
    cout<<endl;

    //for loop
    cout<<"Using for: "<<endl;
    for(i = 0; i <=100; i = i + 5 )
    {
         cout<<i<<endl;
    }
    cout<<endl;
    cout<<endl;

    //nested for - pattern
    cout<<"Using nested for loops for pattern: "<<endl;
    int ii,j,k = 0,n2 = 5;
    for(ii = 1; ii <= n2; ii++)
    {
        for(j = 1; j <= (n2-ii);j++)
        {
            cout<<" ";
            while(k != (2*ii-1))
            {
                cout<<"* ";
                k++;
            }
            k=0;
            cout<<endl;    
        }   
        cout<<endl;
    }
    cout<<endl;
    cout<<endl;

    //nested do while
    cout<<"Using nested do-while to find the product of numbers:"<<endl;
    int q = 0,r = 0;
    do
    {
        q++;
        do
        {
            r++;
            cout<<"Product of two numbers:  "<<q*r<<endl;
        }while(r<10);
        

    } while(q<10);
    cout<<endl;
    cout<<endl; 

    //nested while
    cout<<"Sum of 2 numbers using nested while: "<<endl;
    int q2 = 10, r2 = 10;
    while(q2>0)
    {
        q2--;
        while(r2>0)
        {
            r2--;
            cout<<"Sum: "<<q2+r2<<endl;
        }

    }
    cout<<endl;
    cout<<endl; 
    
    //nested for - matrix
    cout<<"Using nested for loops for matrix: "<<endl;
    int m,n,p;
    int mat[2][2][2] = {
                            {
                                {1, 2},
                                {3, 4}
                            }, 
                            {
                                {5, 6}, 
                                {7, 8}
                            }
                        };

    for (int m = 0; m < 2; ++m) 
    {
        for (int n = 0; n < 2; ++n) 
        {
            for (int p = 0; p < 2; ++p) 
            {
                cout<<mat[m][n][p];
            }
            cout<<endl;
        }
    }
    cout<<endl;
    cout<<endl; 
    
    //nested for + while - matrix
    cout<<"Using nested for loops and while for matrix and checking some condition: "<<endl;
        int m1,n1,p1;
        int mat1[2][2][2] = {
                                {
                                    {1, 2},
                                    {3, 4}
                                }, 
                                {
                                    {5, 6}, 
                                    {7, 8}
                                }
                            };

        for (int m1 = 0; m1 < 2; ++m1) 
        {
            for (int n1 = 0; n1 < 2; ++n1) 
            {
                for (int p1 = 0; p1 < 2; ++p1) 
                {
                    while(mat1[m1][n1][p1] < 8)
                    {
                        cout<<mat1[m1][n1][p1];
                        break;

                    }
                    
                }
                cout<<endl;
            }
        }
    cout<<endl;
    cout<<endl;
    return 0;
}

```

<br>

**Output:** <br>

![exp61](https://github.com/tanishaamenon/CDS---Control-Statements/blob/main/exp61.JPG)
![exp62](https://github.com/tanishaamenon/CDS---Control-Statements/blob/main/exp62.JPG)
![exp63](https://github.com/tanishaamenon/CDS---Control-Statements/blob/main/exp63.JPG)
![exp64](https://github.com/tanishaamenon/CDS---Control-Statements/blob/main/exp64.JPG)
<br>

**Conclusion:** <br>
&#8594; We learnt about loops and their use case. <br>
&#8594; We learnt about nested loops and using one loop in the other. <br>

<br>
