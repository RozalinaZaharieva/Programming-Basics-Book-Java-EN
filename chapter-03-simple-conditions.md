# Chapter 3.1 Simple Conditions

This chapter will discuss **conditional statements in the Java language**. Depending on the condition, a program may have different behavior. First will be explained the syntax of conditional operators **`if`** and **`if-else`** with appropriate examples. Then we will see in what range (**scope**) a variable lives. Finally, we will look through **debugging** techniques to track the step-by-step execution of our programs.

## Video

<div class="video-player">
  Watch the video lesson about what we will learn in this chapter: <a target="_blank" href="https://www.youtube.com/watch?v=cXKIVmjEgHw">https://www.youtube.com/watch?v=cXKIVmjEgHw</a>.
</div>

## Comparing numbers

In programming, we can compare values using the following **operators**:

* Operator **`<`** (less than)
* Operator **`>`** (greater than)
* Operator **`<=`** (less than or equals)
* Operator **`>=`** (greater than or equals)
* Operator **`==`** (equas)
* Operator **`!=`** (not equals)

When comparing values, the result is of the Boolean type with a value **`true`** or **`false`**, depending on whether the result of the comparison is true or false.

### Examples for Comparing Numbers

![](assets/chapter-3-1-images/00.Comparing-numbers-01.png)

### Comparison Operators

In Java, we can use the following comparison operators when comparing numbers:

<table>
<tr>
<th>Description of the Operator</th> <th>Notation</th>
</tr>
<tr>
<td>Equals to</td><td align="center"> == </td>
</tr>
<tr>
<td>Not Equals to</td><td align="center"> != </td>
</tr>
<tr>
<td>Greater than</td><td align="center"> &gt; </td>
</tr>
<tr>
<td>Gerater than or equals</td><td align="center"> &gt;= </td>
</tr>
<tr>
<td>Less than</td><td align="center"> &lt; </td>
</tr>
<tr>
<td>Less than or equals</td><td align="center"> &lt;= </td>
</tr>
</table>

The following example demonstrates how to use comparison operators in expressions:

![](assets/chapter-3-1-images/00.Comparing-numbers-02.png)

## Simple If Conditions

In programming, we often **check given conditions** and perform different actions depending on the result. This is done by **`if`** conditional statement, which has the following structure:

```java
if (condition) {
    // body of if construction
	// single command or block of code to be executed if the condition is true  
}
```

### Example: Excellent Grade

**Read the grade** from the console and check if it is excellent (**`≥ 5.50`**).

![](assets/chapter-3-1-images/01.Еxcellent-result-01.png)

Test the code (from the example) locally. Test with different grades, like **4.75**, **5.49**, **5.50**, and **6.00**. If the grade is **less than 5.50**, the program will not output any result, otherwise (if the grade is **greater than or equals 5.50**), the program will output "**Excellent!**" text.

#### Test the code in the Judge System

Test your solution here:
[https://judge.softuni.bg/Contests/Practice/Index/651#0](https://judge.softuni.bg/Contests/Practice/Index/651#0).


## If-Else Conditions

Simple **`if`** conditions could be extended with **`else`** conditional statement, which specifies a block of code to be executed, if the Boolean expression (defined at the beginning **if(condition)**) return **`false`**. The resulting **conditional statement** is called **`if-else`** construction and have the following behavior: if the condition returns **positive** (**`true`**) result – will be executed the code described in the curly brackets after the **`if`** clause, otherwise if the condition returns **negative** (**`false`**) result – will be executed the code described in the curly brackets after the **`else`** clause. The format of the construction is:

```java
if (condition) {
    // body of if construction
    	// single command or block of code to be executed if the condition is true
} else {
    // body of else construction
    	// single command or block of code to be executed if the condition is false
}
```

### Example: Excellent Grade or Not

Like the example above, read the grade from the console and check if it is excellent, but we should **return the output in both cases**.

![](assets/chapter-3-1-images/02.Excellent-or-not-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#1](https://judge.softuni.bg/Contests/Practice/Index/651#1).


## The Curly Brackets {} After If / Else 

When we have **only one command** in the body of the **`if` construction**, we can **skip the curly brackets**. When we want to execute **block of code** (group of commands), curly brackets are required, because if we skip them, **only the first line** after the **`if` clause** will be executed.

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td>It is a good practice to <strong>always put curly brackets</strong>, because it makes our code more readable and cleaner.</td>
</tr></table>

Here is an example that skipping curly brackets leads to confusion:

![](assets/chapter-3-1-images/00.Brackets-tip-01.png)

Executing the above code will output the following result on the console:

![](assets/chapter-3-1-images/00.Brackets-tip-03.png)

Here is the same example, but with using curly brackets: 

![](assets/chapter-3-1-images/00.Brackets-tip-02.png)

Executing the code with curly brackets will output the following result on the console:

![](assets/chapter-3-1-images/00.Brackets-tip-04.png)

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td>Both use cases are <strong>correct</strong> and could be used depending on the concrete case and/or particular requirements, but always must be careful and check with expected results.</td>
</tr></table>

### Example: Even or Odd Number

Write a program that checks whether an integer is **even** or **odd**.

### Hint and Guidelines

We can solve the problem with one **`if-else`** statement and the operator **`%`**, which returns a **remainder by dividing** two numbers.

![](assets/chapter-3-1-images/03.Even-or-odd-02.png)

Executing the above code will output the following result:

![](assets/chapter-3-1-images/03.Even-or-odd-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#2](https://judge.softuni.bg/Contests/Practice/Index/651#2).


### Example: The greater Number

Write a program that reads two integer numbers, from the console, and return the greater of them. Print the output in the following format: “Greater number: x”, where the x is the returned number.

### Hint and Guidelines

Our first task is to **read** both integer numbers from the console. Then we must perform the check using one **`if-else`** statement in combination with the **operator for greater than** (**`>`**). Part of the code is consciously blurred to test what we have learned so far.

![](assets/chapter-3-1-images/04.Greater-number-02.png)

Executing the above code will output the following result for numbers 3 and 5:

![](assets/chapter-3-1-images/04.Greater-number-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#3](https://judge.softuni.bg/Contests/Practice/Index/651#3).


## Variable Scope

Each variable has a scope in which it exists, called **variable scope**. This scope determines the lifetime of the variable, viz. the scope where be able to use. In the Java language, a variable scope begins from the line in which we **defined it** and ends with the first closing curly bracket **`}`** (of the method, of the **`if` statement**, etc.). Thus, it is important to know that **any variable defined inside the body of `if` statement will not be available outside of it**, unless we have defined it above in the code.

In the example below we will get an **error**, because on the last line we are trying to print the variable **`salary`** that is defined inside the **`if` statement**, and we do not have access to it outside the if statement (in this case we will receive notification from the **IDE** about variable scope).

![](assets/chapter-3-1-images/00.Variable-scope-01.png)

## Sequence of If-Else Conditions

Sometimes we need to do a sequence of conditions before we decide what actions our program will execute. In such cases, we can apply the construction  **`if-else if… -else`**. For this purpose, we use the following format:

```java
if (condition) {
    // body of if construction
} else if (условие2) {
    // body of if construction
} else if (условие3) {
    // body of if construction
} … else {
    // body of else construction
}
```

### Example: Digits 0..9 to Text

Print the digit in rage from 1 to 9 in English (digit is read from the console). 

### Hint and Guidelines

First, we read the digit from the console. Then using a **sequence of conditions** and print the relevant English word:

```java
Scanner scanner = new Scanner(System.in);
int num = Integer.parseInt(scanner.nextLine());

if (num == 1) {
	System.out.println("one");
} else if (num == 2) {
	System.out.println("two");
} else if (…) {
	…
} else if (num == 9) {
	System.out.println("nine");
} else {
	System.out.println("number too big");
}
```

The program logic from the above example **sequentially compares** the input digit from the console with the numbers from 1 to 9. **Each following comparison is being performed only in case the preceding comparison is false**. If none of the **`if`** statements return true, then the last **`else` clause** is executed.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#4](https://judge.softuni.bg/Contests/Practice/Index/651#4).


## Exercises: Sequence of If-Else Conditions

To consolidate our knowledge of the conditional constructions **`if`** and **`if-else`**, let's solve several practical problems.


### Exercise: Bonus score

An **integer** is read from the console - the number of points. A **bonus score** adds to it according to the rules described below. Write a program that calculates the **bonus score** for this integer and **the total number of points** with the bonuses.

- If the integer is **up to 100** inclusive, the bonus score is 5.
- If the integer is **greater than 100**, the bonus score is **20%** from the integer.
- If the integer is **greater than 1000**, the bonus score is **10%** from the integer.
- Additional bonus score (added separately from previous)
 - If the integer is **even** -> +1 bonus score
 - If the integer is odd, with **last digit equals 5** -> +2 bonus score 
 
#### Sample Input and Output

| Input | Output |
| --- | ---- |
| 20 | 6<br>26 |
| 175 | 37<br>212 |
| 2703 | 270.3<br>2973.3 |
| 15875 | 1589.5<br>17464.5 |

#### Sample Input and Output

We can calculate the main and additional bonus score with a sequence of **`if-else-if-else`** statements. For **the main bonus score, we have 3 cases** (when the input integer is up to 100, between 100 and 1000, and greater than 1000). For **the additional bonus score – 2 more cases** (when the integer is even and odd, ended with 5).

![](assets/chapter-3-1-images/06.Bonus-score-01.png)

Executing the above code will output the following result:

![](assets/chapter-3-1-images/06.Bonus-score-02.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#5](https://judge.softuni.bg/Contests/Practice/Index/651#5).


### Exercise: Summing Up seconds

Three athletes finish in a particular number of **seconds** (between **1** and **50**). Write a program that reads the times of these from the console and calculates their **total time** in "minutes:seconds" format. Seconds need to be **zeroed at the front** (2 -> "02", 7 -> "07", 35 -> "35").

#### Sample Input and Output

| Input | Output |
| --- | ---- |
| 35<br>45<br>44 | 2:04 |
| 22<br>7<br>34 | 1:03 |
| 50<br>50<br>49 | 2:29 |
| 14<br>12<br>10 | 0:36 |

#### Hint and Guidelines

The task has several solutions, but in the context of this chapter, we can do the following:
First, sum up the three numbers to get the total result in seconds. Since **1 minute = 60 seconds**, we will have to calculate the number of minutes and seconds in the range 0 to 59:

- If the result is between 0 and 59, print 0 minutes + calculated seconds.
- If the result is between 60 and 119, print 1 minute + calculate seconds minus 60.
- If the result is between 120 and 179, print 2 minutes + calculate seconds minus 120.
- If the seconds are less than 10, print the number with zero in front.

![](assets/chapter-3-1-images/07.Sum-seconds-01.png)

Another solution, which does not use **`if-else`** constructs, is more appropriate because you can use it for greater time values:

![](assets/chapter-3-1-images/07.Sum-seconds-02.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#6](https://judge.softuni.bg/Contests/Practice/Index/651#6).


### Exercise: Unit converter

Write a program that **converts the distance** between the following **units**: **`m`, `mm`, `cm`, `mi`, `in`, `km`, `ft`, `yd`**. Use the table below when a conversion from one unit to another:

| Input Unit | Output Unit |
| :-------------: | :--------------: |
| 1 meter (m) | 1000 millimeters (mm) |
| 1 meter (m) | 100 centimeters (cm) |
| 1 meter (m) | 0.000621371192 miles (mi) |
| 1 meter (m) | 39.3700787 inches (in) |
| 1 meter (m) | 0.001 kilometers (km) |
| 1 meter (m) | 3.2808399 feet (ft)  |
| 1 meter (m) | 1.0936133 yards (yd) |

The program will receive three input lines:

- First line: a number for converting.
- Second line: input unit.
- Third line: output unit (for the result).

#### Sample Input and Output

| Input | Output |
| --- | ---- |
| 12 <br>km <br>ft | 39370.0788 |
| 150 <br>mi <br>in | 9503999.99393599 |
| 450 <br>yd <br>km | 0.41147999937455 |

#### Hint and Guidelines

Read the input data. We can use the **`toLowerCase()`** function, which will make all letters lowercase. As we can see from the table in the condition, we can convert **between meters and some other unit**. Then, first calculate the result from converting the input number in meters, doing a set of checks to define the input unit. Then calculate the output unit.

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td>Keep in mind that in Java, you cannot use operator <strong><code>==</code></strong> for string comparison. For this purpose, you may use the built-in functions.</td>
</tr></table>

![](assets/chapter-3-1-images/08.Metric-converter-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#7](https://judge.softuni.bg/Contests/Practice/Index/651#7).


## Debugging

There were probably errors in the code you wrote so far. There is a way to find errors more easily, using a tool. In the following section, we will look at one of them.

### What is "Debugging"?

**Debugging** lets you find and resolve errors, called **bugs**, a lot faster. Debugging is the process that lets you **track step by step the execution of a program** This tracking is possible by pausing the execution of the program and **analyzing** its state by thorough examination, **line by line**, of logic that follows, defined variables and how they are changed, and so on.

![](assets/chapter-3-1-images/00.Debugging-01.png)

### Debugging with IntelliJ Idea

By pressing, a combination of buttons [**Shift + F9**], you run the current program in **debug mode**. To move to **the next line** in the code, use the [**F7**] button.

![](assets/chapter-3-1-images/00.Debugging-02.png)

By pressing, a combination of buttons [**CTRL + F8**] you create special markers called **breakpoints**, which suspend program execution at a specific point.

## Exercises: Simple Conditions

To get a better understanding of what we learned, let's solve a few practical exercises.

### Empty project in IntelliJ Idea

Create a new project with name **Java** in IntelliJ Idea and leave all others options by default. In order to better organize the solutions of the tasks from the exercises - each solution will be in a separate class and all classes will be in the **src** directory of the project.

Run IntelliJ Idea. Create a new **Java project:** [**File**] → [**New**] → [**Project**].

![](assets/chapter-3-1-images/00.IntelliJ-01.png)

Choose **Java** from the left panel and anything else leaves it by default, and press [**Next**]. In the next dialog box, we have an option to create a project from a template. Usually, we will do this, but now we can skip it and press [**Next**]. In the last dialog box, enter the project's name and storage location, and then click [**Finish**].

![](assets/chapter-3-1-images/00.IntelliJ-02.png)
![](assets/chapter-3-1-images/00.IntelliJ-03.png)

We now have an empty Java project:

![](assets/chapter-3-1-images/00.IntelliJ-04.png)

### Exercise: Check for Excellent Grade

The first task of the exercises on the topic is to write a **program that reads input data from the console**. As input data **enter a score** (decimal number) and as output print "**Excellent!**" if the score is **5.50** or above. 

#### Sample input and output

| Input | Output |
| --- | ---- |
| 6 | Excellent! |
| 5 | (no output) |
| 5.5 | Excellent! |
| 5.49 | (no output) |

#### Hint and Guidelines

Create a **new class** in the existing project in **IntelliJ Idea** by right-click over  [**src**] folder. Choose [**New**] → [**Java Class**].

 ![](assets/chapter-3-1-images/09.Excellent-result-01.png)

A dialog box with two fields will open. In the upper one - enter the name of the class, and in the lower one - the type (there are other options besides classes, but so far they are out of our scope), then press [**OK**] button to create our class. We set a name, for example, "Excellent-Result":

 ![](assets/chapter-3-1-images/09.Excellent-result-02.png)
 
We already have a class with one console application in it. It remains to write the code to solve the problem.

To do this, go to the body of the method **`main (string [] args)`** and place the cursor between the opening and closing curly brackets of the method. If the main method is not created automatically in **IntelliJ Idea**, there is a keyboard shortcut to do this - **`psvm`**. Inside the main method, we write the following code:

 ![](assets/chapter-3-1-images/09.Excellent-result-03.png)

**Run** the program from the green arrow in front of the class name to **test it** with different input values:

 ![](assets/chapter-3-1-images/09.Excellent-result-04.png)

 ![](assets/chapter-3-1-images/09.Excellent-result-05.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#0](https://judge.softuni.bg/Contests/Practice/Index/651#0).

 ![](assets/chapter-3-1-images/09.Excellent-result-06.png) 

 ![](assets/chapter-3-1-images/09.Excellent-result-07.png)


### Exercise: Excellent Grade or Not

The next task of the exercises on the topic is to write a **program that reads input data from the console**. As input data **enter a score** (decimal number). As output print "**Excellent!**" if the score is **5.50** or above, otherwise "**Not excellent!**".

#### Sample input and output

| Input | Output |
| --- | ---- |
| 6 | Excellent! |
| 5 | Not excellent. |
| 5.5 | Excellent! |
| 5.49 | Not excellent. |

#### Hint and Guidelines

Create a **new class** in the existing project in **IntelliJ Idea** by right-click over [**src**] folder. Choose [**New**] → [**Java Class**].

We already have a class with one console application in it. It remains to **write the code** to solve the problem. We can help ourselves with the sample code from the picture:

 ![](assets/chapter-3-1-images/02.Excellent-or-not-01.png)

**Run** the program from the green arrow in front of the class name to **test it** with different input values:

 ![](assets/chapter-3-1-images/02.Excellent-or-not-02.png)
 ![](assets/chapter-3-1-images/02.Excellent-or-not-03.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#1](https://judge.softuni.bg/Contests/Practice/Index/651#1).

 ![](assets/chapter-3-1-images/02.Excellent-or-not-04.png)


### Exercise: Even or Odd Number

The next task is to write a **program that reads input data from the console**. As input data enter **an integer**. As output print **even** or **odd**.

#### Sample input and output

| Input | Output |
| --- | ---- |
| 2 | even |
| 3 | odd |
| 25 | odd |
| 1024 | even |

#### Hint and Guidelines

Create a **new class** in the existing project in **IntelliJ Idea** by right-click over [**src**] folder. Choose [**New**] → [**Java Class**].
  
In the main method, **`public static void main()`** write the code to solve the problem. To check if a number is even, we ca use operator **`%`**, which returns **the remainder of integer division by 2** in following way: **`boolean isEven = (number %2 == 0);`**.

**Run** the program from the green arrow in front of the class name to **test it** with different input values:

![](assets/chapter-3-1-images/03.Even-or-odd-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#2](https://judge.softuni.bg/Contests/Practice/Index/651#2).


### Exercise: Find the Greater Number

The next task is to write a **program that reads input data from the console**. As input data, enter **two integers** each on a separate line. As output print the greater integer of them.

#### Sample input and output

| Input | Output |
|-----|------|
|5<br>3| 5 |
|3<br>5| 5 |
|10<br>10| 10 |
|-5<br>5| 5 |

#### Hint and Guidelines

Create a **new class** in the existing project in **IntelliJ Idea** by right-click over [**src**] folder. Choose [**New**] → [**Java Class**]. To solve the problem is necessary one **`if-else`** statement. You can use the code from the image below, but part of it is consciously blurred.

![](assets/chapter-3-1-images/04.Greater-number-02.png)

**Run** the program from the green arrow in front of the class name to **test it** with different input values:

![](assets/chapter-3-1-images/04.Greater-number-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#3](https://judge.softuni.bg/Contests/Practice/Index/651#3).


### Exercise: Write the number (from 0 to 9 ) in English.

The next task is to write a **program that reads input data from the console**. As input data, enter **an integer in range [0 … 9]**. As output, **print the integer in English**. If the integer is outside range, print "**number too big**".

#### Sample input and output

| Input | Output |
| --- | ---- |
| 5 | five |
| 1 | one |
| 9 | nine |
| 10 | number too big |

#### Hint and Guidelines

To solve the problem, we can use sequential **`if-else`** statements to cover **all eleven possible cases**.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#4](https://judge.softuni.bg/Contests/Practice/Index/651#4).


### Exercise: Password guess

The next task is to write a **program that reads input data from the console**. As input data, enter **a password** (a single line with random text) and check if the input data is **the same** as phrase "**s3cr3t!P@ssw0rd**". As output, print "**Welcome**" if the result is true and "**Wrong password!**" if the result is false.

#### Sample input and output

| Input | Output |
| --- | ---- |
| qwerty | Wrong password! |
| s3cr3t!P@ssw0rd | Welcome |
| s3cr3t!p@ss | Wrong password! |

#### Hint and Guidelines

To solve the problem is necessary one **`if-else`** statement.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#8](https://judge.softuni.bg/Contests/Practice/Index/651#8).


### Exercise: Number from 100 to 200

The next task is to write a **program that reads input data from the console**. As input data, enter **an integer** and check if the input data is **below 100**, **between 100 and 200**, and **above 200**. As output, print the corresponding message as shown in the table below.

#### Sample input and output

| Input | Output |
| --- | ---- |
| 95 | Less than 100 |
| 120 | Between 100 and 200 |
| 210 | Greater than 200 |

#### Test the code in the Judge System

Test your solution here:: [https://judge.softuni.bg/Contests/Practice/Index/651#9](https://judge.softuni.bg/Contests/Practice/Index/651#9).


### Exercise: The same words

The next task is to write a **program that reads input data from the console**. As input data, enter **two words** and check if they are the same. Do not distinguish between uppercase and lowercase letters. As output, print "**yes**" or "**no**".

#### Sample input and output

| Input | Output |
| --- | ---- |
| Hello<br>Hello | yes |
| SoftUni<br>softuni | yes |
| Soft<br>Uni | no |
| beer<br>vodka | no |
| HeLlO<br>hELLo | yes |

#### Hint and Guidelines

Before comparing words, turn them to lowercase so that the size of the letters (uppercase/lowercase) does not affect: **`String wordFirst = scanner.next().toLowerCase().`**

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#10](https://judge.softuni.bg/Contests/Practice/Index/651#10).


### Exercise: Speed information

The next task is to write a **program that reads input data from the console**. As input data, enter **speed**(a decimal number). As output, print information about the speed.

* At speed **up to 10** (inclusive), print "**slowly**".
* At speed **above 10 and up to 50**, print "**average**".
* At speed **above 50 and up to 150**, print "**fast**".
* At speed **above 150 and up to 1000**, print "**ultra fast**".
* At greater speed, print "**extremely fast**".


#### Sample input and output

| Input | Output |
| --- | ---- |
| 8 | slow |
| 49.5 | average |
| 126 | fast |
| 160 | ultra fast |
| 3500 | extremely fast |

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#11](https://judge.softuni.bg/Contests/Practice/Index/651#11).


### Exercise: Faces of figures

The next task is to write a **program that reads input data from the console**. As input data, enter **the dimensions of a geometric figure** and **calculates its fac**. The figures are of four types: **square**, **rectangle**, **circle**, and **triangle**.

On the first line of input data, read the type of figure (`square`, `rectangle`, `circle`, `triangle`).
* If the figure is a **square**, on the next line read one number - the length of its side.
* If the figure is a **rectangle**, on the next two lines read two numbers - the lengths of its sides.
* If the figure is a **circle**, on the next line read one number - the radius of the circle.
* If the figure is a **triangle**, on the next two lines read two numbers - the length of its side and the length of the height to it.


Format the output up to **3 digits after the decimal point**.

#### Sample input and output

| Input | Output |
| --- | ---- |
| square<br>5 | 25 |
| rectangle<br>7<br>2.5 | 17.5 |
| circle<br>6 | 113.097 |
| triangle<br>4.5<br>20 | 45 |

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#12](https://judge.softuni.bg/Contests/Practice/Index/651#12).


### Exercise: Calculate what will be the time in 15 minutes 

The next task is to write a **program that reads input data from the console**. As input data, enter **the hour and minutes** (each on a separate line) of a 24-hour day and calculates **what time it will be in 15 minutes**. Print the output in **`hh: mm`** format. The hours are always between 0 and 23, and the minutes are always between 0 and 59. The hours are print in one or two digits. Minutes are always displayed with two digits and a **leading zero** when necessary.

#### Sample input and output

| Input | Output |
| --- | ---- |
| 1<br>46 | 2:01 |
| 0<br>01 | 0:16 |
| 23<br>59 | 0:14 |
| 11<br>08 | 11:23 |
| 12<br>49 | 13:04 |

#### Hint and Guidelines

To solve the problem, add 15 minutes and do a few checks. If the minutes exceed 59, **increase the hours by 1** and **decrease the minutes by 60**. Similarly, consider the case when the hours exceed 23. When printing the minutes, check for **leading zero**.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#13](https://judge.softuni.bg/Contests/Practice/Index/651#13).

### Exercise: Equals three numbers

The next task is to write a **program that reads input data from the console**. As input data, enter **3 integers**. As output, print if they are equals (**yes** / **no**).

#### Sample input and output

| Input | Output |
| --- | ---- |
| 5<br>5<br>5 | yes |
| 5<br>4<br>5 | no |
| 1<br>2<br>3 | no |

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#14](https://judge.softuni.bg/Contests/Practice/Index/651#14).


### Exercise: \* Write a number from 0 to 100 in English

The next task is to write a **program that reads input data from the console**. As input data, enter a number in the range [**0 … 100**] and convert the number into a text. As output print  the text in English.

#### Sample input and output

| Input | Output |
| --- | ---- |
| 25 | twenty five |
| 42 | forty two |
| 6  | six |

#### Hint and Guidelines

To solve the problem, first, check for **one-digit numbers**, and if the number is one-digit, print the appropriate text for it. Then check for **two-digit numbers**. Print them in two parts: left part (**tens** = number / 10) and right part (**units** = number% 10). If the number has three digits, it must be 100 and considered as a special case.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/651#15](https://judge.softuni.bg/Contests/Practice/Index/651#15).
