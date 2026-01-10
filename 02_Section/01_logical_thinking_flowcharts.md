
## Logical Thinking & Flowcharts

**FlowCharts**
- Diagrammatic representation
- Breaking down of any problem into smaller steps

**Components of Flowchart** or **Building Blocks of Flowchart**
- Start or Starter [Square Box]
- Read N : Input   [Parallelogram Box]
- Process : Let sum=0 [Rectangle Box]
- Decision [Diamond Shape Box]
- Print N : Output
- End or Terminator [Square Box]
> **Arrows** are use to connect components in flowchart.

Flowchart - Simple Interest Calculator <br/>
```cpp
/*
Read Principle, Rate and Time, Print simple interest. 
Sample Input : P = 100rs, R = 5% & T = 2years 
Sample Output : SI = 10 since, SI=(PxRxT)/100
*/
     Start
      |
   Read P,R,T
      |
SI = (P*R*T)/100
      |
  Print SI
      |
     End
```
Flowchart - Largest Number
```cpp
  /*
Given 3 numbers, find the largest number.
Sample Input : A = 10, B = 30 and C = 20
Sample Output: 30
  */

START
|
Read A,B,C
|
Is A>=B and A>=C ---Yes----Print A ---->END
|
No
|
Is B>=A and B>=C ---Yes----Print B ---->END
|
No
|
Print C
|
END
```
Flowchart - Sum of first N numbers.
```cpp
/*
Find the sum of numbers from 1 to N
Sample Input : N = 4
Sample Output: 10 (1+2+3+4)
*/

START
|
Read N
|
sum = 0  // Initialization
i = 1
|
If(i<=N)----No----- Print Sum ----->END
|
yes
|
sum = sum + i  // Work done
i = i + 1     // update statement
|
Again go to If(i<=N)  //Loop
```
Flowchart - Sum of Multiple Inputs
```cpp
/*
Take input N followed by N more numbers,
Find the sum of those numbers.
Sample Input : N = 4
               10 20 30 40
Sample Output: 100
*/
START
|
Read N
|
sum = 0
i = 1
|
if(i<=N)-----No------> Print sum ------> END
|
yes
|
Read value
|
sum = sum + value
i = i + 1
|
Again go to if(i<=N)
```
Flowchart - Prime Number
```cpp
/*
Given a number, check if it is prime or not.
Sample Input : 11
Sample output: Yes
Prime Number : A number which is only divisible by 1 and itself.
*/
START
|
Read N
|
i = 2
|
if(i<=N-1)-----no----> Print Prime -----> END
|
yes
|
if(N%i==0)----yes----> Print Not Prime -----> EXIT
|
no
|
i = i + 1
Again back to if(i<=n-1)
```

Flowchart - GCD/HCF
```cpp
/*
Find the GCD(Greatest Common Divisor) of two numbers.
Sample Input      Sample Output
A = 3             
B = 12              GCD = 4

A = 8             
B = 24              GCD = 8

A = 9             
B = 11              GCD = 1

GCD(A,B) <= min(A,B)
So, GCD could lies only in the range 1 to min(A,B)
*/

START
|
Read A,B
|
i = 1
|
if( i <= min(A,B) ) ----no-----> Print GCD ----> Exit
|
yes
|
if(A is divisible by i and B is also divisible by i)-----yes-----> GCD = i , i = i+1 ------> Go back to if(i < min(A,B))
|
no
|
i = i + 1
|
Go back to if(i < min(A,B))
```
Flowchart - Bank Employee
```cpp
/*
A bank is open till 6 PM and the banker needs to process requests from customers.
Request can be one of these five types:-
- Cash Deposit
- Cash Withdrawl
- Cheque Deposit
- Making a demand draft
- Miscellaneous Requests
Draw a workflow of the bank employee 
*/

Bank Opened
|
Is (Queue empty and Time > 6 PM) ----yes-----> Bank Closed
|
no
|
Is Queue Empty -----yes-----Go back to loop Is (Queue empty and Time > 6 PM)
|
no
|
Remove customer from the Queue
|
Read request
|
If(request is for Demand Draft)-----yes------> Counter A Job done ------> Go back to loop Is (Queue empty and Time > 6 PM)
|
no
|
If(request is for Cheque Deposit)-----yes------> Counter B Job done ------> Go back to loop Is (Queue empty and Time > 6 PM)
|
no
|
If(request is for Cash Withdrawl)-----yes------> Counter C Job done ------> Go back to loop Is (Queue empty and Time > 6 PM)
|
no
|
If(request is for Cash Deposit )-----yes------> Counter D Job done ------> Go back to loop Is (Queue empty and Time > 6 PM)
|
no
|
Counter E for Miscellaneous Request, job done -----> Go back to loop Is (Queue empty and Time > 6 PM)

/*
We can have separate flowchart for each counter A,B,C,D,E.
So, These counters are connectors which combines 2 different flowcharts
*/

Counter A
|
Read Demand Draft
|
Process Demand Draft
|
Hand it over to customer
|
Exit
```
Flowchart - Bank Security Guard
```cpp
/*
The bank Security Guard is going to wait for the customers outside the bank gate.
If they're coming before 6 PM, He will add the customer to the queue.
Otherwise keep on waiting and if time reaches 6 PM, He is going to close the Bank.
*/
Bank Open
|
Is(Time > 6 PM) ----yes-----> Bank Closed
|
no
|
Is(customer in waiting?)----yes-----> Add the customer to queue
|
no
|
Go back to loop Is(Time > 6 PM)
```
---

Draw a flowchart to find the sum of first N even numbers starting from 2
```cpp
/*
Sample Input :
N = 4
Sample Output:
20 (2+4+6+8)
*/
Start
|
Read N
|
i = 1
num = 2
sum = 0
|
if(i<=N) ----no----> print sum -----> End
|
yes
|
if(num%2==0)-----no----> num = num + 1 -----> Go back to if(i<=N)
|
yes
|
sum = sum + num
i = i + 1
num = num + 1
|
Go back to if(i<=N)
```

Draw a flowchart to input marks in 5 subjects and find their average.
```cpp
/*
Sample Input :
N = 5
100 80 90 70 90
Sample Output :
86 (100+80+90+70+90)/5
*/
Start
|
Read N
|
i = 1
sum = 0
|
if(i<=N)----no----> Print Average=sum/N -----> End
|
yes
|
Read value
|
sum = sum + value
i = i +1
|
Go back to the if(i<=N)
```
Draw a flowchart to find the LCM of two numbers
```cpp
/*
Either Use formula : LCM * HCF = A * B
Or
LCM = Lowest Common Multiplcation
LCM of A,B always lies between max(A,B) to A*B.
*/
Start
|
Read A,B
|
i = max(A,B) 
|
if(i <= A*B) -----no-----> print LCM = i ------> End
|
yes
|
if(i%A==0 and i%B==0)-----yes-----> print LCM = i -----> End
|
no
|
i = i + max
|
Go back to if(i <= A*B)
```

Draw a flowchart to print table of a given number upto 10.
```cpp
/*
Sample Input :
N = 5
Sample Output :
5 10 15 20 25 30 35 40 45 50
*/
Start
|
Read N
|
i = 1
|
if(i <=10) ---no----> End
|
yes
|
print 5*i
i = i + 1
|
Go back to if(i <=10)
```
Write a flowchart to print numbers from 1 to 100. For multiple of 3,print "Fizz" instead of number and for multiple of 5, print "Buzz" and for multiple of both 3 & 5, print "Fizz Buzz".
```cpp
/*
Sample ouput :
 1, 2, Fizz(3), 4, Buzz(5), Fizz(6), 7, 8, 9(Fizz), 10(), 11, 12,
 13, 14, Fizz Buzz(15), 16, 17,.................................
 .........................................,98,Fizz(99),Buzz(100). 
*/
Start
|
i = 1
|
if(i<=100)----no----> End
|
yes
|
if(i%3==0 and i%5==0)---yes----> Print "Fizz Buzz" -----> i = i + 1 -----> Go back to if(i<=100)
|
no
|
if(i%3==0)---yes----> Print "Fizz", i = i + 1 -----> Go back to if(i<=100)
|
no
|
if(i%5==0)---yes----> Print "Buzz", i = i + 1 -----> Go back to if(i<=100)
|
no
|
Print i
i = i + 1
|
Go back to if(i<=100)
```

[< Introduction ]() | Flowchart | [ Pseudocode >]()
