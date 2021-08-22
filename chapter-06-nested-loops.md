# Chapter 6.1 Nested Loops

This chapter will discuss **nested loops in the Java language**. We will use **`for`** loops to **draw** different **figures** containing symbols and signs arranged in rows and columns **on the console**. We will use **`for` loop** and **nested loops** (loop statement inside another loop statement), **calculations** and **checks**, to print on the console simple and not so simple figures in given sizes.


## Video

<div class="video-player">
  Watch the video lesson about what we will learn in this chapter: <a target="_blank" href="https://www.youtube.com/watch?v=96SoFtFTPBc">https://www.youtube.com/watch?v=96SoFtFTPBc</a>.
</div>


### Example: A rectangle with a size of 10 x 10 asterisks

Write a program that draw, on the console, a rectangle with a size of **10 x 10** asterisks.

|Input|Output|
|---|---|
|(no input)|<code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code>|

#### Hint and Guidelines
To perform the task, we will use a method. In Chapter 10, we will look in detail at what methods are and how to use them. The method will allow us to execute the same code more than once and in more than one place in a program. At this stage, we will not reveal more than the concept of methods.

![](assets/chapter-6-1-images/01.Rectangle-of-10-x-10-stars-01.png)

How does the example work? The variable of the **cycle (`i = 0`)** is initialized and is incremented on each iteration, as long as it is **less than 10** (the check is performed after each execution of the code, in the body of the loop, and after the iteration). Thus the code in the body of the loop is executed exactly **ten times**. The code, in the body of the loop, will be called for each row of the rectangle. Here as you can see, we call the method **`generateFrom`**. The method will use the class **`StringBuffer`** and another **`for`** loop. Each iteration of a **`for`** loop (the one in the method) will append one asterisk, thus creating a row of ten asterisks. When the execution of the loop (the one in the method) is complete as a result we have a string. Then, the execution of the code returns to the point where we call the method. Then, prints the resulting string on the console.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#0](https://judge.softuni.bg/Contests/Practice/Index/657#0).


### Example: A rectangle with a size of N x N asterisks

Write a program that reads an integer **n** from the console, and as output, draws a **rectangle with a size of n x n asterisks**.

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|2|<code>\*\*</code><br><code>\*\*</code>|3|<code>\*\*\*</code><br><code>\*\*\*</code><br><code>\*\*\*</code>|4|<code>\*\*\*\*</code><br><code>\*\*\*\*</code><br><code>\*\*\*\*</code><br><code>\*\*\*\*</code>|

#### Hint and Guidelines

To perform the task, we will use the **`Scanner`** class, which allows us to read the input size of the figure from the console. 

![](assets/chapter-6-1-images/02.Rectangle-of-N-x-N-stars-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#1](https://judge.softuni.bg/Contests/Practice/Index/657#1).


## Nested Loops

Nested loops are construction in which **in the body of one loop** (called outer), **another loop is performed** (called inner). For each iteration of the outer loop, the inner is perform **the whole**. This happens as follows:

 - When starting the execution of nested loops, first **the outer loop starts** which includes the following steps: the control variable is **initialized**, then checks the condition for the end of the loop, and then the code in the body starts to execute.
 - Then **the inner loop is executed**, which includes the same steps: the control variable is initialized, then checks the condition for the end of the loop, and then the code in the body starts to execute.
 - When the condition for **the end of the inner loop** is met, the program returns one step up, and the started execution of the outer loop continues. This results that the variable of the outer loop is changing (incremented), then checks whether the end condition of the outer loop is satisfied. If not, **a new execution of the nested (inner) loop starts**.
 - This is repeated until the outer loop variable reaches the **end of loop** condition.

Here is an **example** with which to illustrate the nested loops. The goal is to print a rectangle of **`n`** x **`n`** asterisks, where for each row iterates the outer loop from **1** to **`n`**, and for each column iterates a inner loop from **1** to **`n`**:

![](assets/chapter-6-1-images/00.Nested-loops-01.png)

How does the example work? After the initialization of the **outer** loop, its **body** begins to execute, which contains **another (inner) loop**. The inner loop returns **`numberOfstars`** as a row of asterisks. After the **inner** loop **completes** its execution, the program control returns at the first iteration of the outer one, and  **the outer loop continues** to execute. A row (**`System.out.println ()`**) exists to the body of the outer loop, which will take care to move to the next row when the inner loop completes. Without this code, all asterisks will be output on one line. If we use **`println ()`** in the inner loop instead of **`print ()`**, all asterisks are printed on separate lines. You can try and see for yourself. The **increment** of the variable (increase, in our case by 1) of the **outer** loop follows, and the whole **inner** loop starts execution again. The inner loop executes as many times as the body of the outer loop is executed, in the case of **`numberOfstars`** times.

### Пример: квадрат от звездички

Да се начертае на конзолата квадрат от **N x N** звездички:

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|2|<code>\* \*</code><br><code>\* \*</code>|3|<code>\* \* \*</code><br><code>\* \* \*</code><br><code>\* \* \*</code>|4|<code>\* \* \* \*</code><br><code>\* \* \* \*</code><br><code>\* \* \* \*</code><br><code>\* \* \* \*</code>|

#### Hint and Guidelines

Задачата е аналогична на предходната. Тук обаче е необходимо да се обмисли как да бъде изведен интервал след звездичките така, че да няма излишни интервали в началото или края.

![](assets/chapter-6-1-images/03.Square-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#2](https://judge.softuni.bg/Contests/Practice/Index/657#2).


### Пример: триъгълник от долари

Да се напише програма, която въвежда число **n** и печата **триъгълник от долари**.

|Input|Output|Input|Output|Input|Output
|---|---|---|---|---|---|
|3|<code>$</code><br><code>$ $</code><br><code>$ $ $</code>|4|<code>$</code><br><code>$ $</code><br><code>$ $ $</code><br><code>$ $ $ $</code>|5|<code>$</code><br><code>$ $</code><br><code>$ $ $</code><br><code>$ $ $ $</code><br><code>$ $ $ $ $</code>|

#### Hint and Guidelines

Задачата е **сходна** с тези за рисуване на **правоъгълник** и **квадрат**. Отново ще използваме **вложени цикли**, но тук има **уловка**. Разликата е в това, че **броят на колонките**, които трябва да отпечатаме, зависи от **реда**, на който се намираме, а не от входното число **`n`**. От примерните входни и изходни данни забелязваме, че **броят на доларите зависи** от това на кой **ред** се намираме към момента на печатането, т.е. 1 знак долар означава първи ред, 2 знака долар означават втори ред и т.н. Нека разгледаме долния пример по-подробно. Виждаме, че **променливата** на **вложения** цикъл е обвързана с променливата на **външния**. По този начин нашата програма печата желания триъгълник.

![](assets/chapter-6-1-images/04.Triangle-of-dollars-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#3](https://judge.softuni.bg/Contests/Practice/Index/657#3).


### Пример: квадратна рамка

Да се напише програма, която въвежда цяло положително число **n** и чертае на конзолата **квадратна рамка** с размер **n \* n**.

|Input|Output|Input|Output|
|---|---|---|---|
|3|<code>+ - +</code><br><code>&#124; - &#124;</code><br><code>+ - +</code>|4|<code>+ - - +</code><br><code>&#124; - - &#124;</code><br><code>&#124; - - &#124;</code><br><code>+ - - +</code>|

|Input|Output|Input|Output|
|---|---|---|---|
|5|<code>+ - - - +</code><br><code>&#124; - - - &#124;</code><br><code>&#124; - - - &#124;</code><br><code>&#124; - - - &#124;</code><br><code>+ - - - +</code>|6|<code>+ - - - - +</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>+ - - - - +</code>|

#### Hint and Guidelines

Можем да решим задачата по следния начин:
* Четем от конзолата числото **`n`**.
* Отпечатваме **горната част**: първо знак **`+`**, после **n-2** пъти **`-`** и накрая знак **`+`**.
* Отпечатваме **средната част**: печатаме **n-2** реда като първо печатаме знак **`|`**, после **n-2** пъти **`-`** и накрая отново знак **`|`**. Това можем да го постигнем с вложени цикли.
* Отпечатваме **долната част**: първо **`+`**, после **n-2** пъти **`-`** и накрая **`+`**.

Ето и примерна имплементация на описаната идея, с вложени цикли:

![](assets/chapter-6-1-images/05.Square-frame-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#4](https://judge.softuni.bg/Contests/Practice/Index/657#4).


### Пример: ромб от звездички

Да се напише програма, която въвежда цяло положително число **n** и извежда в конзолата **ромб от звездички** с размер **n**.

|Input|Output|Input|Output|
|---|---|---|---|
|1|<code>\*</code>|2|<code>&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;</code><br>|


|Input|Output|Input|Output|
|---|---|---|---|
|3|<code>&nbsp;&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;\*&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;&nbsp;</code>|4|<code>&nbsp;&nbsp;&nbsp;\*&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;\*&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*&nbsp;\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;\*&nbsp;\*&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;&nbsp;\*&nbsp;&nbsp;&nbsp;</code>|

#### Hint and Guidelines

За да решим поставената задача е необходимо мислено да разделим ромба на **две части**: **горна** (включва **и** средния ред) и **долна**. За **извеждането** в конзолата на всяка една част ще използваме **два** цикъла, като читателя сам трябва да открие зависимостта между **`n`** и променливите в циклите.

За първия цикъл може да използваме следните насоки:
* Отпечатвaме **`n-row`** интервала.
* Отпечатваме **`*`**.
* Отпечатваме **`row-1`** пъти **` *`**.

**Втората** (долна) част ще изведем по **аналогичен** начин, което отново оставяме читателя да се опита да направи сам.

![](assets/chapter-6-1-images/06.Rhombus-of-stars-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#5](https://judge.softuni.bg/Contests/Practice/Index/657#5).


### Пример: коледна елха

Да се напише програма, която въвежда число **n** (1 ≤ n ≤ 100) и извежда "коледна елха" с височина **n+1**.

|Input|Output|Input|Output|
|---|---|---|---|
|1|<code>&nbsp;&nbsp;&#124;&nbsp;&nbsp;</code><br><code>\*&nbsp;&#124;&nbsp;\*</code>|2|<code>&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;</code><br><code>\*\*&nbsp;&#124;&nbsp;\*\*</code>|

|Input|Output|Input|Output|
|---|---|---|---|
|3|<code>&nbsp;&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*\*&nbsp;&#124;&nbsp;\*\*&nbsp;</code><br><code>\*\*\*&nbsp;&#124;&nbsp;\*\*\*</code>|4|<code>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*\*&nbsp;&#124;&nbsp;\*\*&nbsp;&nbsp;</code><br><code>&nbsp;\*\*\*&nbsp;&#124;&nbsp;\*\*\*&nbsp;</code><br><code>\*\*\*\*&nbsp;&#124;&nbsp;\*\*\*\*</code>|

#### Hint and Guidelines

От примерите виждаме, че **елхата** може да бъде **разделена** на **три** логически части. **Първата** част са **звездичките (`*`) и празните места преди и след тях**, **средната** част е **` | `**, а **последната** част са отново **звездички** (`*`), като този път **празни** места има само **преди** тях. Отпечатването може да бъде постигнато само с **един цикъл** и отново ще прибегнем до метода, който изпозлвахме в началото. 

![](assets/chapter-6-1-images/07.Christmas-tree-01.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#6](https://judge.softuni.bg/Contests/Practice/Index/657#6).


## Чертане на по-сложни фигури

Да разгледаме как можем да чертаем на конзолата фигури с по-сложна логика на конструиране, за които трябва повече да помислим преди да почнем да пишем.

### Пример: слънчеви очила
Да се напише програма, която въвежда цяло число **n** (3 ≤ n ≤ 100) и печата слънчеви очила с размери **5\*n x n** като в примерите:

|Input|Output|Input|Output|
|---|---|---|---|
|3|<code>\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*</code><br><code>\*////\*&#124;&#124;&#124;\*////\*</code><br><code>\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*</code>|4|<code>\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*</code><br><code>\*//////\*&#124;&#124;&#124;&#124;\*//////\*</code><br><code>\*//////\*&nbsp;&nbsp;&nbsp;&nbsp;\*//////\*</code><br><code>\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*</code><br>|

|Input|Output|
|---|---|
|5|<code>\*\*\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*\*\*</code><br><code>\*////////\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*////////\*</code><br><code>\*////////\*&#124;&#124;&#124;&#124;&#124;\*////////\*</code><br><code>\*////////\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*////////\*</code><br><code>\*\*\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*\*\*</code><br>|

#### Hint and Guidelines

От примерите виждаме, че очилата могат да се разделят на **три части** – горна, средна и долна. По-долу е част от кода, с който задачата може да се реши.

При рисуването на горния и долния ред трябва да се изпечатат **`2 * n`** звездички, **`n`** интервала и **`2 * n`** звездички.

![](assets/chapter-6-1-images/08.Sunglasses-01.png)

При печатането на **средната** част трябва да **проверим** дали редът е **`(n-1) / 2 - 1`**, тъй като от примерите е видно, че на **този ред** трябва да печатаме **вертикални чертички** вместо интервали.

![](assets/chapter-6-1-images/08.Sunglasses-02.png)

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#7](https://judge.softuni.bg/Contests/Practice/Index/657#7).


### Пример: къщичка

Да се напише програма, която въвежда число **n** (2 ≤ **n** ≤ 100) и печата **къщичка** с размери **n x n**, точно като в примерите:

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|2|<code>**</code><br><code>&#124;&#124;</code><br>|3|<code>-\*-</code><br><code>\*\*\*</code><br><code>&#124;\*&#124;</code>|4|<code>-\*\*-</code><br><code>\*\*\*\*</code><br><code>&#124;\*\*&#124;</code><br><code>&#124;\*\*&#124;</code>

|Input|Output|Input|Output|
|---|---|---|---|
|5|<code>--\*--</code><br><code>-\*\*\*-</code><br><code>\*\*\*\*\*</code><br><code>&#124;\*\*\*&#124;</code><br><code>&#124;\*\*\*&#124;</code>|8|<code>---\*\*---</code><br><code>--\*\*\*\*--</code><br><code>-\*\*\*\*\*\*-</code><br><code>\*\*\*\*\*\*\*\*</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br>|


#### Hint and Guidelines

Разбираме от условието на задачата, че къщичката е с размери **`n` x `n`**. Това, което виждаме от примерните вход и изход, е че:

* Къщичката е разделена на 2 части: **покрив и основа**. 

![](assets/chapter-6-1-images/09.House-01.png)

* Когато **`n`** е четно число, върхът на къщичката е "тъп".
* Когато **`n`** е нечетно число, **покривът** е с един ред по-голям от **основата**.

##### Покрив
* Съставен е от **звезди** (`*`) и **тирета** (`-`).
* В най-високата си част има една или две звезди, спрямо това дали **n** e нечетно или четно, както и тирета.
* В най-ниската си част има много звезди и малко или никакви тирета.
* С всеки един ред по-надолу, **звездите** се увеличават с 2, а **тиретата** намаляват с 2.

##### Основа
* Широка е **`n`** на брой реда.
* Съставена е от **звезди** (`*`) и **вертикални черти** (`|`).
* Редовете представляват 2 **вертикални черти** - по една в началото и в края на реда, както и **звезди** между вертикалните черти с дължина на низа **`n - 2`**.  

Прочитаме **`n`** от конзолата и записваме стойността в променлива от тип **`int`**.  

![](assets/chapter-6-1-images/09.House-02.png)

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td><b>Много е важно да проверяваме дали са валидни входните данни!</b> В тези задачи не е проблем директно да обръщаме прочетеното от конзолата в тип <b><code>int</code></b>, защото изрично е казано, че ще получаваме валидни целочислени числа. Ако обаче правим по-сериозни приложения, е добра практика да проверяваме входните данни. Какво ще стане, ако вместо число потребителят въведе буквата "А"?</td>
</tr></table>

За да начертаем **покрива**, записваме колко ще е началният брой **звезди** в променлива **`stars`**:
* Ако **`n`** е **четно** число, ще са 2 броя.
* Ако е **нечетно**, ще е 1 брой.

![](assets/chapter-6-1-images/09.House-03.png)

Изчисляваме дължината на **покрива**. Тя е равна на половината от **`n`**. Резултата записваме в променливата **`roofLength`**.

![](assets/chapter-6-1-images/09.House-04.png)

Важно е да се отбележи че, когато **`n`** е нечетно число, дължината на покрива е по-голяма с един ред от тази на **основата**. В езика **Java**, когато два числа от целочислен тип се делят и има остатък, то резултатът ще е число без остатъка.

Пример:

```java
int result = 3 / 2; // резултат 1
```

Ако искаме да закръглим резултата нагоре, трябва да използваме метода **`Math.ceil(…)`**:

```java
int result = (int) Math.ceil(3 / 2f);
```

В този пример делението не е от 2 целочислени числа. "`f`" след число показва, че даденото число е от тип **`float`** (число с плаваща запетая). Резултатът от **`3 / 2f`** е **`1.5f`**. **`Math.ceil(…)`** закръгля делението нагоре. В нашият случай **`1.5f`** ще стане 2. **`(int)`** се използва, за да може да трансформираме типа обратно в **`int`**.

След като сме изчислили дължината на покрива, завъртаме цикъл от 0 до **`roofLength`**. На всяка итерация ще:
* Изчисляваме броя **тирета**, които трябва да изрисуваме. Броят ще е равен на **`(n - stars) / 2`**. Записваме го в променлива **`padding`**.

![](assets/chapter-6-1-images/09.House-05.png)

* Отпечатваме на конзолата: "**тирета**" (**`padding`** на брой пъти) + "**звезди**" (**`stars`** пъти) + "**тирета**" (**`padding`** пъти). 

![](assets/chapter-6-1-images/09.House-06.png)

* Преди да свърши итерацията на цикъла добавяме 2 към **`stars`** (броя на **звездите**).

![](assets/chapter-6-1-images/09.House-07.png)

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td>Не е добра идея да правим събирания на много на брой символни низове по показания по-горе начин, защото това води до <b>проблеми със скоростта</b> (performance issues). За повече информация посетете:  <a href="https://bg.wikipedia.org/wiki/%D0%9D%D0%B8%D0%B7#String_Builder">https://bg.wikipedia.org/wiki/Низ#String_Builder</a></td>
</tr></table>

След като сме приключили с **покрива**, е време за **основата**. Тя е по-лесна за печатане:
* Започваме с цикъл от **0** до **n** (изключено).
* Отпечатваме на конзолата: **`|`** + **`*`** (**`n - 2`** на брой пъти) + **`|`**.

![](assets/chapter-6-1-images/09.House-08.png)

Ако всичко сме написали както трябва, задачата ни е решена.

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#8](https://judge.softuni.bg/Contests/Practice/Index/657#8).


### Пример: диамант

Да се напише програма, която въвежда цяло число **n** (1 ≤ **n** ≤ 100) и печата диамант с размери **n**, като в следните примери:

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|1|<code>\*</code><br>|2|<code>\*\*</code>|3|<code>-\*-</code><br><code>\*-\*</code><br><code>-\*-</code>|

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|4|<code>-\*\*-</code><br><code>\*--\*</code><br><code>-\*\*-</code>|5|<code>--\*--</code><br><code>-\*-\*-</code><br><code>\*---\*</code><br><code>-\*-\*-</code><br><code>--\*--</code><br>|6|<code>--\*\*--</code><br><code>-\*--\*-</code><br><code>\*----\*</code><br><code>-\*--\*-</code><br><code>--\*\*--</code><br>|

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|7|<code>---\*---</code><br><code>--\*-\*--</code><br><code>-\*---\*-</code><br><code>\*-----\*</code><br><code>-\*---\*-</code><br><code>--\*-\*--</code><br><code>---\*---</code><br>|8|<code>---\*\*---</code><br><code>--\*--\*--</code><br><code>-\*----\*-</code><br><code>\*------\*</code><br><code>-\*----\*-</code><br><code>--\*--\*--</code><br><code>---\*\*---</code><br>|9|<code>----\*----</code><br><code>---\*-\*---</code><br><code>--\*---\*--</code><br><code>-\*-----\*-</code><br><code>\*-------\*</code><br><code>-\*-----\*-</code><br><code>--\*---\*--</code><br><code>---\*-\*---</code><br><code>----\*----</code>|

#### Hint and Guidelines

Това, което знаем от условието на задачата, е че диамантът е с размер **`n` x `n`**.

От примерните вход и изход можем да си направим изводите, че всички редове съдържат точно по **`n`** символа и всички редове, с изключение на горните върхове, имат по **2 звезди** (**`*`**). Можем мислено да разделим диаманта на 2 части:
* **Горна** част. Тя започва от горният връх до средата.
* **Долна** част. Тя започва от реда след средата до най-долния връх (включително).

##### Горна част
* Ако **n** е **нечетно**, то тя започва с **1 звезда** (**`*`**).
* Ако **n** е **четно**, то тя започва с **2 звезди** (**`**`**).
* С всеки ред надолу, звездите се отдалечават една от друга.
* Пространството преди, между, и след **звездите** (**`*`**) е запълнено с **тирета** (**`-`**).

##### Долна част
* С всеки ред надолу, звездите се събират една към друга. Това означава, че пространството (**тиретата**) между тях намалява, а пространството (**тиретата**) отляво и отдясно се увеличава.
* В най-долната си част е с 1 или 2 **звезди**, спрямо това дали **n** е нечетно или четно.

##### Горна и долна част на диаманта
* На всеки ред звездите са заобиколени от външни **тирета**, с изключение на средния ред.
* На всеки ред има пространство между двете **звезди**, с изключение на първия и последния ред (понякога **звездата е 1**).

Прочитаме стойността на **n** от конзолата и я записваме в променлива от тип **`int`**.  

![](assets/chapter-6-1-images/10.Diamond-01.png)

Започваме да чертаем горната част на диаманта. Първото нещо, което трябва да направим, е да изчислим началната стойност на външната бройка **тирета `leftRight`** (тиретата от външната част на **звездите**). Тя е равна на **`(n - 1) / 2`**, закръглено надолу.

![](assets/chapter-6-1-images/10.Diamond-02.png)

След като сме изчислили **`leftRight`**, започваме да чертаем **горната част** на диаманта. Може да започнем, като завъртим **цикъл** от **`0`** до **`n / 2 + 1`** (закръглено надолу).  

При всяка итерация на цикъла трябва да се изпълнят следните стъпки:
* Рисуваме по конзолата левите **тирета** (с дължина **`leftRight`**) и веднага след тях първата **звезда**.

![](assets/chapter-6-1-images/10.Diamond-03.png)

* Ще изчислим разстоянието между двете **звезди**. Може да го направим като извадим от **n** дължината на външните **тирета**, както и числото 2 (бройката на **звездите**, т.е. очертанията на диаманта). Резултата от тази разлика записваме в променлива **`mid`**. 

![](assets/chapter-6-1-images/10.Diamond-04.png)

* Ако **`mid`** е по-малко от 0, то тогава знаем, че на реда трябва да има 1 звезда. Ако е по-голямо или равно на 0, то тогава трябва да начертаем **тирета** с дължина **`mid`** и една **звезда** след тях.
* Рисуваме на конзолата десните външни **тирета** с дължина **`leftRight`**. 

![](assets/chapter-6-1-images/10.Diamond-05.png)

* В края на цикъла намаляваме **`leftRight`** с 1 (**звездите `*`** се отдалечават).

Готови сме с горната част.

Рисуването на долната част е доста подобна на рисуването на горната част. Разликите са, че вместо да намаляваме **`leftRight`** с 1 към края на цикъла, ще увеличаваме **`leftRight`** с 1 в началото на цикъла. Също така, **цикълът ще е от 0 до `(n - 1) / 2`**.   

![](assets/chapter-6-1-images/10.Diamond-06.png)

<table><tr><td><img src="/assets/alert-icon.png" style="max-width:50px" /></td>
<td><b>Повторението на едно и също парче код се смята за лоша практика</b>, тъй като кодът става труден за поддръжка. Да си представим, че имаме код (напр. логиката за чертането на ред от диаманта) на още няколко места в програмата и се налга да направим някаква промяна. За целта би било необходимо да коригираме кода на всяко едно място, където сме сложили този код. А сега нека се замислим върху следния казус: Какво би станало, ако същият този код трябва да се използва не 1, 2 или 3 пъти, а десетки пъти. Един от подходите за справяне с този проблем е използването на <b>методи</b>. Можете да потърсите допълнителна информация за тях в Интернет, или да прегледате <a href="chapter-10-methods.md">глава “10” (Методи)</a>.</td>
</tr></table>

#### Test the code in the Judge System

Test your solution here: [https://judge.softuni.bg/Contests/Practice/Index/657#9](https://judge.softuni.bg/Contests/Practice/Index/657#9).


## Какво научихме от тази глава?

Научихме се да чертаем фигури с вложени **`for`** цикли:

```java
for (int r = 1; r <= 5; r++)
{
   System.out.println("*");
   for (int c = 1; c < 5; c++)
      System.out.println(" *");
   System.out.println();
}
```

Научихме се, също и как **да използваме методи** за да избягваме повторението на едно и също парче код няколко пъти.
