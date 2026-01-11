## Logical Thinking : Pseudocode

> **Pseudocode** is Human readable description of an ***algorithm***.
> - **Algorithm** is sequence of steps to solve a particular problem.

**Pseudocode** -> plain English text, not a real code that a machine can execute.

**Why Pseudocode ?**
- Language Independent
- Structure your code before writing it.
- Fastest way to verify your code or get a review of your code.

**Pseudocode - Notation**
- You can come up with your own notation of writing pseudocode.
- But there are few basic ways of writing anything.

Let's define our own 6 types of instructions set in order to write any pseudocode.
1. **Input** ```read N```
2. **Assignment** ```sum = 0 , i = 1```
3. **Output** ```print sum, print "Hello World" ```
4. **If Else** ```If i<N then do task1 end Else then task2 end```
```cpp
//IF ELSE Block
if(i<N){
     then do task1
}
else{
 then do task2
}
```
5. **While Loop** ```While i<N do this task until end```
```cpp
//When we do n times if else, so we have a concept of loop
   while(condition is true){
      do the task
      update the condition
   }
```
6. **Exit** ```END/EXIT```

### Pseudocode

Pseudocode - Simple Interest
```cpp
/*
Read P,R,T and calculate SI
Sample Input :
100 2 4
Sample Output :
8
*/
Read P,R,T
SI = (P*R*T)/100
Print SI
Exit
```
Pseudocode - Sum of the number from 1 to N
```cpp
/*
Sample Input :
4
Sample Output :
10
*/
Read N
num = 1, sum = 0
while (num < N){
   sum = sum + num
   num = num + 1
}
Print sum
Exit
```
Pseudocode - Sum of N numbers
```cpp
/*
Sample Input :
N = 4
10 20 30 40
Sample Output :
100
*/
Read N
i = 1, sum = 0
while (i <= N){
     Read value
     sum = sum + value
     i = i + 1
}
Print sum
Exit
```
Pseudocode - Prime or Not Prime
```cpp
/*
Pseudocode to check if a number is prime or not
Sample Input :
11
Sample Outut :
Prime

Prime Number : a number which is only divisible by 1 and itself. It starts with 2.
*/
Read N
i = 2
while (i < N){
    If N%i == 0 then "not prime" Exit
    Else then i = i + 1
}
Print "prime"
Exit
```
Pseudocode - GCD (Greatest Common Divisor)
```cpp
/*
Find GCD of two numbers A and B
Sample Input :
A = 8
B = 20
Sample Output :
GCD = 4

GCD of 2 numbers A,B will always ranges between 1 and MIN(A,B)
*/
Read A,B
i = 1, min = MIN(A,B)
GCD = 1
while (i <= min){
   if A%i==0 AND B%i==0 then GCD = i
   else i = i + 1
}
Print GCD
Exit
```

Pseudocode - Start Pattern
```cpp
/*
Sample Input :
N = 3
Sample Output :
*
**
***
Observation :
1. There are N rows
2. In ith row there are i num of starts
3. In the blank spaces there is a '\n' newline character
*/
Read N
i = 1
While (i <= N){
    star = 1
    while (start <= i){
       Print '*'
       star = star + 1
    }
   Print new line
   i = i + 1
}
Exit
```

Pseudocode - Star Pyramid Pattern
```cpp
/*
Sample Input :
N = 3
Sample Output :
  *
 ***
*****
Observation :
1. There are N rows
2. There are some spaces followed by some stars in ith row
3. New line is there after each row

Star        Row(i)
1 = 2(1)-1 ->  1
3 = 2(2)-1 ->  2
5 = 2(3)-1 ->  3
So, Basically there are 2i-1 stars in each row.

If you don't want to observe, use predefine formula of sequence in AP.
1,3,5,..........
a = starting term
d = differnce = 2
ith term = ?
Ti = a + (i-1)d
   = 1 + (4-1)2
   = 7
*/
Read N
i = 1
while(i <= N){
     //Print space
     space = 1
     while(space <= N-i){
          Print " "
          space = space + 1
     }
     //Print star
     star = 1
     while(star <= 2*i-1){
          Print "*"
          star = star+1
    }
    //Print new line
    Print "\n"
    i = i + 1
}
Exit
```

**Convert all the flowcharts that we created into the Pseudocode**

1. Pseudocode to find the sum of the first N even numbers starting from 2
```cpp
/*
Sample Input :
N = 4
Sample Output :
20 
Sum of 4 even numbers starting from 2 = 2+4+6+8
*/
Read N
i = 1, sum = 0
num = 2
while(i < N){
     if(num%2 = 0){
           sum = sum + num
           i = i + 1
      }
      num = num + 1
}
Print sum
Exit
```

2. Pseudocode to input marks in 5 subjects and find average
```cpp
/*
Sample Input :
N = 5
100 80 90 75 85
Sample Output :
86
Average = (100+80+90+75+85)/5
*/
Read N
i = 1, sum = 0
while(i <=N ){
       Read Value
       sum = sum + value
       i = i + 1
}
avg = sum/N
Print avg
Exit
```
3. Pseudocode to find the LCM of 2 numbers A,B. You may use formala LCM*HCF=A*B
```cpp
/*
Sample Input :
A = 6
B = 8
Sample Output :
LCM = 24
LCM of 2 number A,B is always lie between MAX(A,B) to A*B
*/
Read A,B
i = MAX(A,B)
range = A*B
LCM = 0
while(i <= range){
        if(i%A==0 AND i%B==0){
              LCM = i
              Print LCM
              Exit
        }
        i = i + 1 // to make it faster i = i + max(A,B)
}
LCM = A*B 
Print LCM
Exit
```
```cpp
Read A,B
i = 1
GCD = 1
range = MIN(A,B)
while(i <= range){
      if(A%i==0 AND B%i==0){
            GCD = i
      }
      i = i + 1
}
LCM = (A*B)/GCD
Print LCM
Exit
```

4. Pseudocode to print table of a given number upto 10
```code
/*
Sample Input :
N = 5
Sample Output :
5 10 15 20 25 30 35 40 45 50
*/
Read N
i = 1
while(i <= 10){
     Print N*i
     i = i + 1
}
Exit
```

5. Pseudocode that print numbers from 1 to 100 and for multiple of 3 print "Fizz", for multiple of 5 print "Buzz" and
   for multiple of both 3 and 5 print "Fizz Buzz".
```cpp
/*
Sample Output :
1,2,Fizz,4,Buzz,Fizz,7,8,Fizz,Buzz,11,Fizz,13,14,Fizz Buzz,16,17,....Buzz.
*/
num = 1
While(num <= 100 ){
      if num%3==0 and num%5==0 {
            print "Fizz Buzz"
      }
      if num%3 == 0 {
           print "Fizz"
      }
      if num%5 == 0 {
           print "Buzz"
      }
      else {
           print num
      }
      num = num + 1
}
Exit
```

6. Pseudocode to find factorial of a number.
```cpp
/*
Sample Input :
N = 5
Sample Output :
Fact = 120
Factorial = Product of the numbers from 1 to upto that number
          = 1 * 2 * 3 * 4 * 5
          = 120
*/
Read N
i = 1, factorial = 1
while(i <= N){
    factorial = factorial * i
    i = i + 1
}
Print factorial
Exit
```

[< Flowchart ](https://github.com/pawansinghfromindia/CPP/blob/main/02_Section/01_logical_thinking_flowcharts.md) | Pseudocode | [ C++ Basics >]()
