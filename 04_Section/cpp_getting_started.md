
## C++ Getting started

Hello World!
- Boilerplate(Template) Code
- Building and running a C++ code

<details>
  <summary> C++ Boilerplate(Template) Code </summary>

```cpp
#include<iostream>
using namespace std;

int main(){
    // Code logic
    return 0;
}
```

> `#` Directives

> `<iostream>` Headerfile

> `namespace`

> `main()` Starting point

> Main Function : Function Name, Function Body

</details>
<!-------------------->

<details>
  <summary> Compilation Phase and Running Phase </summary>

Whenever we write code, there is a starting point. <br/>
The programs start executing from `main()`.

**1. Compilation Phase**
- Always happens from TOP to BOTTOM
- Line 1, Line 2, Line 3,........., Line 8

**2. Running Phase**
- Step 1 : Our code will get compiled.
- Step 2 : **Object Files** and a **linker** will be created
- Step 3 : Linker will combine all the object files and create something called **executable file**

> **Executable file is the file that can run on a particular machine.**

</details>

### C++ Hello World!

```cpp
#include<iostream>
using namespace std;

int main(){

  cout << "Hello World!";

  return 0;
}
```
Here, `cout` is an object. `cout` means Console Output.
The code behind `cout` is in `<iostream>` headerfile.

`"Hello World!"` is a string.

Every statement in C++ ends with `;` semicolon.

> **These are the rules of the programming language.**


### Code Editors and Compiler Setup

Code Editors like Visual Studio Code, Sublime Text, TurboC++ etc

Compilers for C++ are like g++, GNU C++ 


### Input and Output

**Average of the marks**

Given marks of a student in 3 subjects Physics, Chemistry and Maths.
Print the average of the marks.

Sample Input : 90 75 68

Sample Output : 77.66

<details>
  <summary> Code 1 </summary>

```cpp
#include <iostream>

using namespace std;

int main(){

  int phy = 90;
  int chem = 75;
  int maths = 68;

  float avg = (phy + chem + maths) / 3; // 3.0

  cout << Average Marks  << avg;

  return 0;
}
```

</details>

<details>
  <summary>  Code 2 </summary>

```cpp
#include <iostream>

using namespace std;

int main(){

  // USER INPUT
  int phy, chem, maths;
  cin >> phy;
  cin >> chem;
  cin >> maths;

  // PROCESSING
  float avg = (phy + chem + maths) / 3.0; 

  cout << Average Marks  << avg;

  return 0;
}
```

</details>

### Building and running code

Compiler understands all of these keywords, operators as per the rules of the programming language. 

<details>
  <summary> Code </summary>


```hello.cpp
#include<iostream>

using namespace std;

int main(){

  // logic
  cout << "Hello World" << endl;

  return 0;
}

```


`hello.cpp` to C++ Compiler which run this hello.cpp and generate a new exectable file that is `hello.exe`
on window or `hello.out` on macOS

STEP 1 : Building the code which includes compilations
`
g++ hello.cpp
`

STEP 2 : Run the executable file
`
./hello.out
`

</details>

### Square of a Number

Take input a number N and print its square.

Sample Input : 
5

Sample Output :
25

<details>
  <summary> Code </summary>

```cpp
#include <iostream>
using namespace std;

int main(){

  int N;
  cin >> N;
  cout << N*N << endl;

  return 0;
}
```
  
</details>

