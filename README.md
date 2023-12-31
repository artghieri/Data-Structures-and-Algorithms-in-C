
---

## Algorithms: Their Key Role in Computing

In this chapter, we aim to demystify algorithms. What exactly are algorithms, and why is it worthwhile to delve into their intricacies? How do algorithms differentiate themselves amidst the various computer technologies? This chapter wil answer these questions.

### Algorithms

Informally, an ***algorithm*** is any well-defined computational procedure that takes some value, or set of values, as ***input*** and produces some value, or set of values, as ***output*** in a finite amount of time. An algorithm is thus a sequence of computational steps that transform the input into the output.

```mermaid
flowchart LR
  A{{INPUT}} -.-> B[(ALGORITHM)]
  B -.-> C{{OUTPUT}}
```

Therefore, an algorithm serve as a tool for solving a ***well-specified computational problem***. The statement of the problem specifies in general terms the desired *input/output* relationship for problem instances. The algorithm describes a specific computational procedure for achieving that *input/output* relationship for all problem instances. 

As an example, suppose that you need to *sort a sequence of numbers into increasing order*. Here is how we formally define the ***sorting problem***: 

**INPUT:**  
**A sequence of *n* numbers  $\langle a_{1}, \\, a_{2}, \\, ... \\,,\\, a_{n}  \rangle$**.

**OUTPUT:**   
**A permutation or reordering $\langle a_{1}^{\prime}\\, ,\\, a_{2}^{\prime}\\,,\\, ... \\,,\\, a_{n}^{\prime} \rangle$ of the input sequence such that $a_{1}^{\prime} \leq \\, a_{2}^{\prime} \leq \\, a_{n}^{\prime}.$**

Thus, given the input sequence $\langle 52, \\, 28, \\, 4, \\, 12, \\, 12, \\, 36 \rangle$, a  ***correct sorting algorithm*** returns as output the sequence $\langle 4, \\, 12, \\, 12, \\, 28, \\, 36, \\, 52 \rangle$. 

#

Such an input sequence is called an ***instance*** of the ***sorting problem***. In general, an ***instance of a problem*** consists of the input (satisfying whatever **constraints** are imposed in the problem statement) needed to compute a solution to the problem.

> ***Note:** A constraint problem occurs when the wrong units (e.g.,Fahrenheit instead of Celsius) are input for a temperature conversion algorithm.*

Because many programs use it as an intermediate step, sorting is a fundamental operation in **Computer Science**. As a result, you have a large number of good sorting algorithms at your disposal. Which algorithm is best for a given application depends on several factors, including *item count*, *initial sorting*, *value constraints*, *computer architecture*, and *storage device type* (e.g., main memory or disks), among others.

An algorithm for a ***computational problem*** is ***correct*** if, for every problem instance provided as input, it ***halts*** - *its computing in finite time* - and outputs the correct solution to the problem instance. An ***incorrect*** algorithm might not halt at all on some input instances, or it might halt with an incorrect answer. 

> ***Note:** Surprisingly, incorrect algorithms can have their utility, especially when their error rate is manageable.*

#

**What Kinds of Problems are Solved by Algorithms?**

Algorithms are the unsung heroes of the digital age, silently working behind the scenes to tackle a multitude of problems across various domains. Practical applications of algorithms are ubiquitous and include the following examples: 

- **Social Media Recommendation Algorithms:** Think about how social media platforms like Facebook or Instagram suggest friends to connect with or posts to engage with. These recommendation algorithms analyze your past interactions and those of others to present content and connections tailored to your interests. For instance, when Facebook suggests reconnecting with an old friend you haven't seen in years, it's driven by algorithms mining data on mutual friends, shared interests, and past interactions.

- **Uber's Ride-Matching Algorithm:** When you book a ride through Uber, an algorithm is at work behind the scenes to optimize your journey. Uber's ride-matching algorithm considers various factors like your pickup location, destination, driver availability, and real-time traffic data to calculate the quickest and most cost-effective route. This ensures you get to your destination efficiently and at a fair price, all thanks to complex algorithms.

- **Netflix Recommendation Engine:** Ever wondered how Netflix knows exactly what TV shows and movies you'll love? Netflix's recommendation engine employs powerful algorithms that analyze your viewing history, genre preferences, and even the viewing habits of users with similar tastes. It then suggests personalized content that keeps you binge-watching. For instance, when Netflix suggests a new series that becomes your favorite, it's the result of these recommendation algorithms.

**Algorithms as A Technology**

In a hypothetical scenario where computers possessed infinite processing speed and memory came at no cost, *would you have any reason to study algorithms?* Surprisingly, the answer is **yes**. Even in such a scenario, you would still like to be certain that your solution method terminates and does so with the correct answer. 

In a world of infinitely fast computers, any method that leads to the correct solution would do. While you would still uphold the principles of good ***software engineering*** — *ensuring that your implementation is well-designed and meticulously documented* — the primary criterion for choosing a method would likely be **simplicity and ease of implementation**.

Despite their impressive speeds, computers are not infinitely fast. Time, as a computing resource, is bounded and therefore, exceedingly precious. Although the saying goes, *Time is money*, while well-known, falls short in emphasizing the true value of time; it is even more precious than money itself. Money can be regained after being spent, but once time is expended, it is irrevocably lost.

Memory, on the other hand, may seem relatively inexpensive, but it is **neither infinite nor free**. It is crucial to exercise prudence in selecting algorithms that utilize time and space resources efficiently. **In other words, even with vast computing power and memory at your disposal, the art of algorithm design remains essential, as it ensures that you maximize the utility of your finite resources.**

#

**Efficiency**

Different algorithms devised to solve the same problem often differ dramatically in their efficiency. These differences can be much more significant than differences due to hardware and software. Two common ****sorting algorithms***, **Insertion Sort** and **Merge Sort**, offer a striking contrast in terms of efficiency.

**Insertion Sort**, with its simple and intuitive nature, offers a basic way to sort a collection of elements. On the other hand, **Merge Sort** employs a more sophisticated *divide and conquer* strategy to efficiently sort large datasets. To understand the profound difference in efficiency between these two algorithms, we turn to mathematical analysis.

Efficiency in sorting algorithms can be quantified through their ***time complexity***, often expressed using **Big O** notation. The time complexity provides a mathematical representation of how an algorithm's runtime scales concerning the size of the input data.

**Insertion Sort Efficiency:**
Insertion sort operates with a time complexity of $O(n^2)$ in the worst case. This quadratic growth signifies that as the input size (n) increases, the time required to sort the data grows quadratically. It can be represented as:

$$T_{i}(n) = k_{i} \times n^2$$

$T_{i}(n) \textit{represents the time taken by insertion sort for an input of size n, and } k_{i} \textit{ is another constant factor}$

**Merge Sort Efficiency:**
Merge sort, in contrast, exhibits a time complexity of $O(n \times \log_2(n))$ for all cases, including the worst case. This indicates a more efficient growth rate as the input size increases. It can be represented as:

$$T_{m}(n) = k_{m} \times n \times \log_2(n)$$

$T_{m}(n) \textit{represents the time taken by merge sort for an input of size n, and } k_{m} \textit{ is another constant factor}$

#

Let's illustrate the difference in efficiency using a practical example. We will compare the sorting efficiency of two computers. 

Let's consider the specifications of each computer: **Computer A** operates at an impressive rate of *10 billion instructions per second*. In stark contrast, **Computer B** executes instructions at a much slower pace, managing only *10 million instructions per second*. Consequently, **Computer A** outpaces **Computer B** *by a factor of 1000* in terms of raw computing power.

To accentuate this difference further, let's assume that **Computer A** benefits from the expertise of a highly skilled programmer who codes an optimized version of the insertion sort algorithm in machine language. This finely-tuned code operates at a complexity of $2 \times n^2$ instructions to sort a dataset of n numbers.

On the other hand, **Computer B** takes a different route. Here, an average programmer has implemented the merge sort algorithm using a high-level language with an inefficient compiler. This results in a code with a time complexity of $50 \times n \times \log_2(n)$ instructions to sort the same dataset.

**How long will it take for each computer to sort this 10 million-number dataset?**

$$\text{Computer A (Insertion Sort):}$$

$$T_{i}(10^7) = \frac{k_{i} \times n^2}{10^{10}} \rightarrow \frac{2 \times (10^7)^2}{10^{10}} \\: \frac{ \text{instructions}}{\text{instructions / sec}} = 20.000 \text{ seconds} \approx 5,5 \text{ hours}$$

<br>

$$\text{Computer B (Merge Sort):}$$

$$T_{m}(10^7) = \frac{k_{m} \times n \times \log_2(n)}{10^7} \rightarrow \frac{50 \times 10^7 \times \log_2(10^7)}{10^{7}} \\: \frac{ \text{instructions}}{\text{instructions / sec}} \approx 1.162,5 \text{ seconds} \approx  19,375 \text{ minutes}$$

Here, it becomes evident that as the input size increases, the *efficiency difference* between Insertion Sort and Merge Sort becomes increasingly pronounced. Merge Sort's linearithmic ( $O(n \times \log_2(n) )$ ) complexity allows it to maintain a consistent advantage over Insertion Sort, especially when dealing with large datasets.

**Algorithms and other Technologies**

In computing, algorithms are as crucial as hardware and advanced technologies. Even in the age of machine learning and data science, algorithms underpin most operations, from hardware design to user interfaces and networking. 

Efficient algorithms are essential, especially as computers tackle larger problems. A solid understanding of algorithms remains a defining trait of skilled programmers, enhancing their capabilities in the ever-evolving world of computing.

#

**Analyzing Algorithms**

Analyzing an algorithm involves predicting the resources it requires, such as *memory*, *communication bandwidth*, *energy consumption*, and most commonly, ***computational time***. By evaluating multiple candidate algorithms for a problem, we can identify the *most efficient one*, often eliminating inferior alternatives. This process requires a model of the technology on which the algorithm runs, including the associated resources and their costs.

The **RAM** **(Random-Access Machine)** model is the primary framework for *algorithm analysis*. In this model, instructions execute sequentially with constant time for each operation, closely resembling real computers. It covers *common instructions*, *data types*, and *control flow*. While it simplifies some real-world complexities, like *memory hierarchy*, it offers reliable performance predictions. Analyzing algorithms in the **RAM** model can be challenging, requiring mathematical tools, but it aids in selecting efficient algorithms for various tasks.

**Worst-Case, Average-Case, Best-Case, and Amortized Time Complexity**

**Worst-Case Running Time:** This denotes the behavior of an algorithm with respect to the **worst possible case** of the input instance. The *worst-case running time* of an algorithm is an ***upper bound*** on the running time for any input. Therefore, having the knowledge of worst-case running time gives us an assurance that the algorithm will never go beyond this time limit.

**Average-Case Running Time:** The *average-case running time* of an algorithm is an estimate of the running time for an ***average*** input. It specifies the expected behavior of the algorithm when the input is randomly drawn from a given distribution. Average-case running time assumes that all inputs of a given size are equally likely.

**Best-Case Running Time:** The term ***best-case performance*** is used to analyze an algorithm under optimal conditions. For example, the best case for a simple linear search on an array occurs when the desired element is the first in the list. However, while developing and choosing an algorithm to solve a problem, we hardly base our decision on the best-case performance. It is always recommended to improve the ***average performance*** and the ***worst-case performance*** of an algorithm.

**Amortized Running Time:** Amortized running time refers to the time required to perform a sequence of (related) operations averaged over all the operations performed. Amortized analysis guarantees the average performance of each operation in the worst case.

### Asymptotic Notation

When we analyze algorithms for large inputs, we focus on their ***asymptotic efficiency*** – *how their running time scales as input size approaches infinity*. In practice, algorithms with superior asymptotic efficiency are usually the best choice, except for exceptionally small inputs. This approach helps us understand the long-term performance characteristics of algorithms.

**$O$-Notation**

$O$-Notation characterizes an *upper bound* on the ***asymptotic*** behavior of a function. In other words, it says that a function grows no faster than a certain rate, based on the highest-order term.

Consider, for example, the function $f(x) = 3n^3 - 2n^2 + 5n + 1$ . Its highest-order term is $3n^3$, and so we say that this function’s rate of growth is $n^3$. Because this function grows no faster than $n^3$ , we can write that it is $O(n^3)$. More generally, it is $O(n^c)$ for any constant $c \gg 3$. Here is the formal definition of $O$-Notation. 

For a given function $g(n)$, we denote by $O(g(n))$ (*pronounced big-oh of g of n*) the *set of functions*):

$$O(g(n)) = \\{ f(n) : \text{ there exist positive constants c and } n_{0} \text{ such that }  0 \leq f(n) \leq cg(n), \forall \text{  n } \geq n_{o} \\}$$

#

A function $f(n)$ belongs to the set $O(g(n))$ if there exists a ***positive constant*** $c$ such that $f(n) \leq cg(n)$ for sufficiently large $n$.

The definition of $O(g(n))$ requires that every function $f(n)$ in the set $O(g(n))$ be ***asymptotically nonnegative***: $f(n)$ must be nonnegative whenever $n$ is sufficiently large. (An ***asymptotically positive*** function is one that is positive for all
sufûciently large $n$.). 

Consequently, the function $g(n)$ itself must be ***asymptotically nonnegative***, or else the set $O(g(n))$ is **empty**. We therefore assume that every function used within $O$-Notationis ***asymptotically nonnegative***. 

You might be surprised that we defined $O$-notation in terms of sets. Indeed, you might expect that we would write $f(n) \in O(g(n))$ to indicate that $f(n)$ belongs to the set $O(g(n))$. Instead, we usually write $f(n) = O(g(n))$ and say
$f(n)$ is big-oh of $g(n)$ to express the same notion. 

Let’s explore an example of how to use the formal definition of $O$-Notation to justify our practice of discarding lower-order terms and ignoring the constant coefficient of the highest-order term: 

We'll show that $f(x) = 4n^2 + 100n + 500 = O(n^2)$. 

We need to find positive constants $c$ and $n_0$ such that $f(x) = 4n^2 + 100n\leq O(n^2)$ for all $n \geq n_0$. 

By definition, we have:

$$0 \leq 4n^2 + 100n\leq cn^2$$

Dividing both sides of the inequality by $n^2$ yields: 

$$0 \leq 4 + \frac{100}{n} \leq c$$ 

Now to determine the value of $c$, we see that $4 + \frac{100}{n}$ is maximum when $n = 1$. Therefore, $c = 104$.

To determine the value of $n_0$:

$$0 \leq 4 + \frac{100}{n_0} \leq 104$$ 

$$-4{n_0} \leq 100 \leq 100{n_0}$$ 

This implies, $n_0 = 1$. Hence, $0 \leq 4n^2 + 100n \leq n^2 \\: \forall \text{  n } \geq n_{0} = 1 \\}$


#

**$\Omega$-Notation**

$\Omega$-Notation characterizes a *lower bound* on the ***asymptotic*** behavior of a function. In other words, it says that a function grows at *least as fast* as a certain rate, based on the ***highest-order term***. 

Because the ***highest-order term*** in the function $f(x) = 7n^3 + 100n^2 - 20n + 6$ grows at least as fast as $n^3$, this function is $\Omega(n^3)$. This function is also $\Omega(n^2)$ and $\Omega(n)$. More generally, it is $\Omega(n^c)$ for any constant $c \leq 3$. 

Just as $O$-notation provides an ***asymptotic upper bound*** on a function, $\Omega$-Notation provides an ***asymptotic lower bound***. For a given function $g(n)$, we denote by $\Omega(g(n))$ (*pronounced big-omega of g of n*) the set of functions 

$$\Omega(g(n)) = \\{ f(n) : \text{ there exist positive constants c and } n_{0} \text{ such that }  0 \leq cg(n) \leq f(n), \forall \text{  n } \geq n_{o} \\}$$

#

Now let’s show that $f(x) = 4n^2 + 100n + 500$ is $\Omega(n^2)$. We need to find positive constants $c$ and $n_0$ such that $f(x) = 4n^2 + 100n + 500 \leq cn^2$ for all $n \geq n_0$. As before, we divide both sides by $n^2$: 

$$4 + \frac{100}{n} + \frac{500}{n^2} \leq c$$

This inequality holds when $n_0$ is any positive integer, and we can choose $c = 4$.

What if we had a small coefficient for the $n^2$ term? The function would still be $\Omega(n^2)$. For example, let’s show that $f(x) = n^2/100 + 100n + 500$ is $\Omega(n^2)$. Dividing by $n^2$ gives: 

$$\frac{1}{100} + \frac{100}{n} + \frac{500}{n^2} \leq c$$ 

We can choose any value for $n_0$ that is at least 10,005 and find a positive value for $c$. For example, when $n_0 = 10,005$, we can choose $c = 2.49 \times 10^{-9}$. If we select a larger value for $n_0$, we can also increase $c$. For example, if $n_0 = 100,000$, then we can choose $c = 0.0089$. The higher the value of $n_0$, the closer to the coefficient $\frac{1}{100}$ we can choose $c$.

#

**$\Theta$-Notation**

$\Theta$-Notation characterizes a *tight bound* on the ***asymptotic behavior*** of a function. It says that a function grows *precisely at a certain rate*, based once again on the ***highest-order*** term. Put another way, $\Theta$-Notation characterizes the rate of growth of the function to within a **constant factor from above** and to within a **constant factor from below**. 

These two constant factors *don't need to be equal*. If you can show that a function is both $O(f(n))$ and $\Omega(f(n))$ for some function $f(n)$, then you have shown that the function is $\Theta(f(n))$. For example, $f(x) = 7n^3 + 100n^2 - 20n + 6$ it's a $\Theta(n^3)$

For a given function $g(n)$, we denote by $\Theta(g(n))$ (*theta of g of n*) the set of functions

$$\Theta(g(n)) = \\{ f(n) : \text{ there exist positive constants } c_1 \text{ and }c_2 \text{ and } n_{0} \text{ such that }  0 \leq c_{1}g(n) \leq f(n) \leq c_{2}g(n), \forall \text{ n } \geq n_{o} \\}$$

#

For all values of n at and to the right of $n_0$, the value of $f(n)$ lies at or above $c_{1}g(n)$ and at or below $c_{2}g(n)$. In other words, for all $n \geq n_0$, the function $f(n)$ is equal to $g(n)$ to within constant factors. The definitions of $O$-, $\Omega$-, and  $\Theta$-Notations lead to the following theorem.

For any two functions $f(n)$ and $g(n)$, we have $f(n) = \Theta(g(n))$ if and only if

$$f(n) = O(g(n)) \text{ and } f(n) = \Omega(g(n))$$

<br>

## Understanding the Fundamentals of Data Structures

In this chapter, we explore data structures, the essential components of computer science. What are data structures, and why are they crucial for efficient algorithms? How do they impact the world of technology and problem-solving? Let's demystify data structures and discover their profound significance.

### Data Structures

For many problems, the ability to formulate an ***efficient algorithm*** depends on being able to organize the data in an appropriate manner. The term *data structure* is used to denote a particular way of organizing data for particular types of operation.

Data structures are like organizational tools in programming, defining how data is stored and handled. They come in various forms, each tailored for specific tasks. Examples include *arrays*, *trees*, and *graphs*. These structures are vital for crafting efficient solutions in coding.
 

**Why are They Important in Programming?**

A program should undoubtedly give correct results, but along with that it should also run **efficiently**. A program is said to be efficient when it executes in *minimum time* and with *minimum memory space*. In order to write efficient programs we need to apply certain ***data management*** concepts.

The concept of data management is a complex task that includes activities like *data collection*, *organization of data into appropriate structures*, and *developing and maintaining routines for quality assurance*. A data structure is basically a group of data elements that are put together under one name, and which defines a particular way of ***storing*** and ***organizing data*** in a computer so that it can be used efficiently

Specific data structures are essential ingredients of many efficient algorithms as they enable the programmers to manage huge amounts of data easily and efficiently. Some formal design methods and programming languages emphasize data structures and the algorithms as the key organizing factor in software design. This is because **representing information is fundamental to computer science**. The primary goal of a program or software is not to perform calculations or operations but to *store* and *retrieve information* as fast as possible.

**Choosing the Right Data Structure**

In the world of problem-solving, choosing the right data structure is a fundamental step toward achieving *efficient solutions*. To gauge efficiency, we examine if a solution not only meets the problem's needs but also operates effectively within set **resource constraints**, including ***storage space*** and ***processing time***. And the best solution is the one that requires fewer resources than known alternatives. The ultimate goal is to minimize resource usage, particularly in terms of time, while still adhering to other resource limits.

In today's programming landscape, writing code extends beyond problem-solving; it's about crafting ***efficient solutions***. To accomplish this, programmers embark on a process of problem analysis, where they establish **clear performance objectives**. Subsequently, they meticulously select the data structure that best suits the task at hand.

However, in some cases, program designers lacking a solid grasp of data structure concepts may bypass this crucial analysis phase. Instead, they opt for a data structure they're familiar with. Unfortunately, this choice may not align with the specific problem, potentially leading to subpar performance, such as sluggish operation speeds.

Conversely, if a program meets its performance goals with a data structure that is simple to use, then it makes no sense to apply another complex data structure just to exhibit the programmer’s skill. When selecting a data structure to solve a problem, the following steps must be performed.

1. **Analysis of the problem to determine the basic operations that must be supported.**
2. **Quantify the resource constraints for each operation.**
3. **Select the Data Structure that best meets these requirements.**

> ***Note:** In the approach above, the first concern is the data and the operations that are to be performed on them. The second concern is the representation of the data, and the final concern is the implementation of that representation.*

C language supports various data structure types, each with its unique characteristics. Some structures allow adding data items only at the beginning, while others permit insertion at any position. Some enable sequential data access, while others facilitate random access. So, selection of an appropriate data structure for the problem is a crucial decision and may have a major impact on the performance of the program.

#

**Operations On Data Structures**

This section discusses the different operations that can be performed on the various data structures previously mentioned.

**Traversing:** It means to access each data item exactly once so that it can be processed. For example, to print the names of all the students in a class.

**Searching:** It's used to locate data items that may or may not be present in the given collection, satisfying a given constraint. For example, to find the names of all the students who secured 100 marks in mathematics.

**Inserting:** It is used to add new data items to the given list of data items. For example, to add the details of a new student who has recently joined the course.

**Deleting:** It means to remove (*delete*) a particular data item from the given collection of data items. For example, to delete the name of a student who has left the course.

**Sorting:** Data items can be arranged in some order like *ascending order* or *descending order* depending on the type of application. For example, calculating the top three winners by arranging the participants’ scores in descending order and then extracting the top three.**

**Merging:** Lists of two sorted data items can be combined to form a single list of sorted data items.

Frequently, multiple operations need to be applied simultaneously in a given situation. For instance, consider the scenario where we need to delete the details of a student with the name "X". In this case, we must first conduct a search within the list of students to determine whether the record of "X" exists and, if so, identify its location. Subsequently, we can proceed to delete the details from that specific location.

#

**Classification of Data Structures**

Classification of Data Structures categorizes them based on their organization and functionality, helping programmers choose the right tool for specific tasks. These categories include *Linear*, *Non-Linear* data structures, each suited to distinct data manipulation requirements. 

**Data structures are generally categorized into two classes: *Primitive* and *Non-Primitive* Data Structures.**

**Primitive and Non-Primitive Data Structures**  
Primitive Data Structures are the fundamental data types which are supported by a programming language. Some basic data types are *integer*, *real*, *character*, and *boolean*. The terms ***data type***, ***basic data type***, and ***primitive data type*** are often used interchangeably. 

Non-Primitive data structures, on the other hand, are constructed using primitive data types. They encompass complex structures such as *linked lists*, *stacks*, *trees*, and *graphs*. Non-Primitive data structures can be categorized into two primary types: **Linear Structures**, which follow a linear progression, and **Non-Linear Structures**, characterized by their more intricate relationships between elements.

**Linear and Non-Linear Structures**  
If data elements within a structure are organized in a sequential manner, it falls into the category of Linear data structures. Well-known examples encompass arrays, *linked lists*, *stacks*, and *queues*. Linear structures can be stored in memory using two approaches: ***contiguous memory locations*** to maintain a direct linear relationship between elements or ***linked structures*** where connections establish the linear order.

Conversely, when data elements are not arranged in a sequential order, the structure is classified as Non-Linear. Non-Linear data structures lack adjacency relationships among their elements, making them suitable for more complex scenarios. Examples of Non-Linear structures include *trees* and *graphs*, which allow for versatile data organization and retrieval.

```mermaid
---
title: Classification of Data Structure
---
flowchart TB
  A("Data Structure") -.-> L(["Primitive Data Structure"])
  L -.-> N{{"Integer"}}
  L -.-> O{{"Real"}}
  L -.-> P{{"Character"}}

  A -.-> M(["Non-Primitive Data Structure"])

  M -.-> C["Non-Linear Structures"]
  C -.-> D{{"Graphs"}}
  C -.-> E{{"Trees"}}

  M -.-> B["Linear Structures"]
  B -.-> J{{"Stack"}}
  B -.-> K{{"Linked List"}}
  B -.-> H{{"Array"}}
  B -.-> I{{"Queue"}}

```


## Data Types in C

A data type determines the set of values that a data item can take and the operations that can be performed on it.

**Integers, Floating-point, and Characters.**

The C language classifies variables based on the type of data they can hold, ensuring efficient memory usage and precise operations. Thus, C provides fundamental types such as integers, characters, and floating-point numbers, offering versatility in data representation.

For instance, the **char** data type is of **one byte** and is used to store *single characters*. Note that C does not provide any data type for ***storing text***, this is because text is made up of individual characters.


| Data Type       | Description                | Size (in bytes) | Range                                                   |
|-----------------|----------------------------|:-------------------------:|---------------------------------------------------------|
| **int**           | Integer                         | 4                   | $\pm \\: -2.147 \times 10^9  \text{ to } \pm \\: 2.147 \times 10^9$                        |
| **char**          | Character                       | 1                   | $-128 \text{ to } 127$  (or $0 \text{ to } 255$ for unsigned char)      |
| **float**         | Single-Precision Floating Point | 4                   |  $\pm  \\: 1.2 \times 10^{-38} \text{ to } \pm \\: 3.4 \times 10^{38}$            |
| **double**        | Double-Precision Floating Point | 8                   |  $\pm  \\: 2.2 \times 10^{-308} \text{ to } \pm \\: 1.8 \times 10^{308}$           |

> **Note:* In addition, C also supports four modifiers — two sign specifiers (***signed*** and ***unsigned***) and two size specifiers (***short*** and ***long***).*

These ranges provide a general idea of the value limits for each of the principal data types in C. However, it's important to note that the actual range may vary depending on the specific system and compiler.

**Data Type Compatibility**

Data type compatibility is a vital concept, especially in languages like C, where precise control over data representation and memory management is crucial. It essentially deals with how different data types interact with each other in a program. It governs how variables of various types can be used together, ensuring that operations are carried out correctly and safely.

**Example of Data Type Compatibility:**

Let's consider a simple example to illustrate data type compatibility in C:

```c
#include <stdio.h>

int main(void)
{
int integerVariable = 42;
double doubleVariable = 3.14159265359;

double result = integerVariable + doubleVariable;

printf("Result:" %lf\n, result);

return 0;
}
```

In this C program, we have an **int** variable and a **double** variable. We want to add these two variables together and store the result in the result variable, which is also of type double.

Here's what's happening in terms of data type compatibility:

- The int variable is implicitly converted to a double when it's added to ***doubleVariable***. This is an example of implicit type conversion to ensure that both operands have a compatible type for the addition operation.
- The result of the addition, which is a double, is then stored in the result variable.
- Finally, we print the result using the %lf format specifier because it's of type double.

This example demonstrates how data type compatibility allows for operations involving different data types. C's rules for type conversion ensure that the code compiles and produces the expected result without requiring explicit type casting. 

> [!NOTE]
> For more reference about Data Types and The C Language, check my [Student Guide - The C Language](https://github.com/artghieri/Student-Guide-The-C-Language/blob/main/guide.md)

## Arrays

In this chapter, we will discuss arrays. An *array* is a user-defined data type that stores related information together. All the information stored in an *array* belongs to the **same data type**. So, in this chapter, we will learn how arrays are defined, declared, initialized, and accessed. We will also discuss the different operations that can be performed on array elements and the different types of arrays such as two-dimensional arrays, multi-dimensional arrays, and sparse matrices.

**An Array as a Concept**

Consider a situation in which we have 20 students in a class and we have been asked to write a program that reads and prints the marks of all the 20 students. 

Now to read the values of these 20 variables, we must have 20 read statements. Similarly, to print the value of these variables, we need 20 write statements. If it is just a matter of 20 variables, then it might be acceptable for the user to follow this approach. But would it be possible to follow this approach if we have to read and print the marks of students,

- **In the entire course (say 100 students)**
- **In the entire college (say 500 students)**
- **In the entire university (say 10,000 students)**

The answer is no, definitely **not**! To process a large amount of data, we need a data structure known as an ***array***.

An array is a collection of similar data elements. These data elements have the same data type. The elements of the array are stored in consecutive memory locations and are referenced by an index (also known as the *subscript*). The subscript is an ordinal number which is used to identify an element of the array.

```c
#include <stdio.h>  

int main(void)  
{
// Declare an integer array named "students" with 5 elements and initialize it with these values.
int students[5] = {10, 8, 7, 5, 10};  

// Print the value of the element at index 2 (third element) of the "students" array.
printf("%d", students[2]);  
return 0;  
}
```

#


**Declaration and Initialization of Arrays.**

In programming, every variable must be declared before it is used, and the same concept applies to array variables. Before using an array, it must be declared. Declaring an array involves specifying the following information:

- **Data Type**: This indicates the kind of values the array can store, such as *int*, *char*, *float*, or *double*.
- **Name**: An identifier used to uniquely identify the array.
- **Size**: The maximum number of elements that can be stored in the array.

**Arrays are declared using the following syntax:**

```sql
datatype name[size];
```

The data type can be either*int*, *char*, *float*, *double* or any other valid data type. The number within brackets indicates the *size* of the array.  
For example, if we declare:

```sql
int marks[5];
```

Then the statement declares marks to be an array **containing 10 elements**. In C, the array index starts from zero. The first element will be stored in **marks[0]**, second element in **marks[1]**, and so on. Therefore, the ***last element***, that is the 5th element, will be stored in **marks[9]**. 

> ***Note:** Note that 0, 1, 2, 3 written within square brackets are the subscripts.*

**In the memory, each element of the array will be stored as shown:**

<table>
  <tr>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">1st</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">2nd</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">3rd</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">4th</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">5th</td>
  </tr>
</table>

#

**Accessing Elements of an Array.**

To access all the elements, we must use a loop. In other words, we can access all the elements of an array by incrementing the value of the subscript into the array within a loop.

```c
// Declare an integer array named "marks" with a size of 5 elements
int marks[5];

// Initialize each element of the "marks" array to 0 using a loop
for (int i = 0; i < 5; ++i)
{
    marks[i] = 0;
}
```

> ***Note:** The subscript must be an integral value or an expression that evaluates to an integral value.*

The first element of the array **marks[5]** can be accessed by writing **marks[0**]. To process all the elements of the array, we use a loop that accesses each individual element of the array and sets its value to 0. 

In the for loop, first, the value of **marks[0]** is set to 0, then the value of the ***index*** i is incremented, and the next value, **marks[1**], is set to 0. This procedure continues until all 5 elements of the array are set to 0.

**Array marks after executing the code given:**

<table>
  <tr>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">0</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">0</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">0</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">0</td>
    <td style="text-align:center; background-color:#3498db; color:white; width: 120px; height: 80px; font-size: 10px;">0</td>
  </tr>
</table>


> ***Note:** There is no single statement that can read, access, or print all the elements of an array. To do this, we have to use a loop to execute the same statement with different index values.*


**Storing Values in Arrays**

When declaring an array, we allocate space for its elements without storing values. Three methods exist for storing values in an array: initializing elements during declaration, inputting values for individual elements from the keyboard, or assigning values to individual elements.

```mermaid
graph LR
    A(Storing values in an array)
    B(Initialize elements during declaration)
    C(Input values for individual elements from the keyboard)
    D(Assign values to individual elements)

    A --> B
    A --> C
    A --> D

```

**Initializing Arrays During Declaration**

Arrays can be initialized at the time of declaration, just like any other variable. When initializing an array, you must provide a value for every element within the array. This is done by specifying the values within curly braces, separated by commas, in the following format:

```sql
type array_name[size] = {list of values};
```

It's important to ensure that the number of values matches the number of elements in the array; specifying more values than there are elements will result in a compiler error.

```sql
int marks[5] = {90, 82, 78, 95, 88};
```

In this example, an array named marks is declared with enough space to store five elements. The first element, **marks[0]**, is assigned the value 90, the second element, **marks[1]**, is assigned 82, and so on. 

**Inputting Values from the Keyboard**

Arrays can be initialized by inputting values from the keyboard using loops, such as **while/do–while** or **for** loops. 

```c
int i, marks[10];
i = 0;

while (i < 10)
{
  printf("Enter a value for element %d: ", i);
  
  scanf("%d", &marks[i]); // Input value for the current element
  i++;  // Increment index i
}
```

For instance, a loop iterates through the array elements, starting from index 0 and inputting values for each element. This process continues for arrays with indices ranging from 0 to 9. 

```mermaid
graph TD
    A["Start"]
    B["Initialize index i to 0"]
    C["Input value for element at index i"]
    D["Is i < 10?"]
    F["Increment i"]
    G["Repeat loop"]
    I["End"]

    A --> B
    B --> C
    C --> D
    D -->|Yes| F
    D -->|No| I
    F --> G
    G --> C
```

**Assigning Values to Individual Elements**

The third method involves assigning values to individual elements of the array using the assignment operator. You can assign any value that matches the data type of the array to an individual array element.

```sql
marks[0] = 10
```

To copy the contents of one array into another, you must copy the value of each individual element from the first array to the corresponding element in the second array.

```c
#include <stdio.h>

int main()
{
int firstArray[5] = {1, 2, 3, 4, 5};
int secondArray[5];

// Copy the values from firstArray to secondArray
for (int i = 0; i < 5; i++)
  secondArray[i] = firstArray[i];
return 0;
}
```

In this example, the loop accesses each element of the first array and simultaneously assigns its value to the corresponding element of the second array. The index value i is incremented to access the next element in succession

```mermaid
graph LR
    A["Start"]
    B["Initialize index i to 0"]
    C["Copy value from firstArray[i] to secondArray[i]"]
    D["Is i < 5?"]
    F["Increment i"]
    G["Repeat loop"]
    I["End"]

    A --> B
    B --> C
    C --> D
    D -->|Yes| F
    D -->|No| I
    F --> G
    G --> C
```

> ***Note:** It's important to note that we cannot assign one array directly to another array, even if the two arrays have the same type and size.* 

#

**Common Operations on Arrays.**

There are a number of operations that can be preformed on arrays. These operations include:

- **Traversal:** Iterating through all elements of the array to perform an operation on each.
- **Search:** Looking for a particular value within the array.
- **Insertion:** Adding a new element into the array.
- **Deletion:** Removing an element from the array.
- **Sorting:** Arranging the elements of the array in a specific order.
- **Merging:** Combining two or more arrays into a single array.
- **Copying:** Creating a copy of an array with the same or different size.  

> [!NOTE]
> For more reference, check ["Operations on array in C"](https://www.studymite.com/blog/operation-on-arrays-in-c-1).

**Two-Dimensional Arrays**

Up until now, our discussions have focused on **one-dimensional arrays**. These arrays are organized *linearly* in a *single direction*. However, in certain situations, we encounter the need to store data in a more structured manner, resembling grids or tables.

This is where the concept of one-dimensional arrays extends into **two-dimensional data structures**. A two-dimensional array is defined using two *subscripts*: the first subscript indicates the **row**, and the second denotes the **column**. In the world of programming, a two-dimensional array is essentially treated as an array of one-dimensional arrays.


| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |
|:-----------:|:-----------:|:-------------:|:-------------:|
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |

**Declaring Two-dimensional Arrays**

Any array must be declared before being used. The declaration statement tells the compiler the name of the array, the data type of each element in the array, and the size of each dimension. 

**A two-dimensional array is declared as:**

```sql
datatype array_name[row_size][column_size];
```

For example, if we want to store the marks obtained by three students in five different subjects, we can declare a two-dimensional array as:

```c
int marks[3][4];
```

In the above statement, a two-dimensional array called marks has been declared that has 3 rows and 4 columns. The first element of the array is denoted by **marks[0][0]**, the second element as **marks[0][1]**, and so on. Here, **marks[0][0]** stores the marks obtained by the first student in the first subject, **marks[1][0]** stores the marks obtained by the second student in the first subject.

This two-dimensional array can store a grid of data, making it suitable for situations where you need to organize information in rows and columns.

| | Collumn 0 | Collumn 1 | Collumn 2 |
| :--: | :--: | :--: | :--: | 
| Row 0 | [0][0] | [0][1] | [0][2] |
| Row 1 | [1][0] | [1][1] | [1][2] |
| Row 2 | [2][0] | [2][1] | [2][2] |

Although we have shown a ***two-dimensional array***, in the memory, these elements actually will be stored **sequentially**. There are two ways of storing a two-dimensional array in the memory. The first way is the **row major order** and the second is the **column major order**. Let us see how the elements of a 2D array are stored in a row major order. 

Here, the elements of the first row are stored before the elements of the second and third rows. That is, the elements of the array are stored row by row where n elements of the first row will occupy the first n locations.

<table>
  <tr>
      <td>(0,0)</td>
      <td>(0,1)</td>
      <td>(0,2)</td>
      <td>(0,3)</td>
      <td>(1,0)</td>
      <td>(1,1)</td>
      <td>(1,2)</td>
      <td>(1,3)</td>
      <td>(2,0)</td>
      <td>(2,1)</td>
      <td>(2,2)</td>
      <td>(2,3)</td>
  </tr>
</table>

> ***Note:** Elements of a 3 x 4 2D array in row major order*

However, when we store the elements in a column major order, the elements of the first column are stored before the elements of the second and third column. That is, the elements of the array are stored column by column where m elements of the first column will occupy the first m locations. 
   
<table>
  <tr>
      <td>(0,0)</td>
      <td>(1,0)</td>
      <td>(2,0)</td>
      <td>(3,0)</td>
      <td>(0,1)</td>
      <td>(1,1)</td>
      <td>(2,1)</td>
      <td>(3,1)</td>
      <td>(0,2)</td>
      <td>(1,2)</td>
      <td>(2,2)</td>
      <td>(3,2)</td>
  </tr>
</table>

> ***Note:** Elements of a 4 x 3 2D array in column major order*

**Initializing Two-dimensional Arrays**

Like in the case of other variables, declaring a two-dimensional array only reserves space for the array in the memory. No values are stored in it. A two-dimensional array is initialized in the same way as a one-dimensional array is initialized. For example:

```c
int marks[2][3] = { {90,87,78}, {68, 62, 71} };
```

In the above example, each row is defined as a one-dimensional array of three elements that are enclosed in braces. Note that the commas are used to separate the elements in the row as well as to separate the elements of two rows.

**Operations On Two-Dimensional Arrays**

Two-dimensional arrays can be used to implement the mathematical concept of matrices. In mathematics, a matrix is a grid of numbers organized into rows and columns. Using two-dimensional arrays, we can perform the following operations on an $m \times n$ matrix:

**Transpose:** The transpose of an $m \times n$ $matrix A$ is a new $matrix B$ with dimensions $n \times m$, where each element $B_{(i \times j)}$ of $B$ is equal to the element $A_{(j \times i)}$ of $A$.

$$B_{(i \times j)} = A_{(j \times i)}$$

**Sum:** Two matrices that are compatible with each other can be added together, storing the result in the third matrix. Two matrices are said to be compatible when they have the same number of rows and columns. The elements of two matrices can be added by writing:
$$C_{(j \times i)} = A_{(j \times i)} + B_{(i \times j)}$$

**Difference:** Two matrices that are compatible with each other can be subtracted, storing the result in the third matrix. Two matrices are said to be compatible when they have the same number of rows and columns. The elements of two matrices can be subtracted by writing:
$$C_{(j \times i)} = A_{(j \times i)}- B_{(i \times j)}$$

**Product:** Two matrices can be multiplied with each other if the number of columns in the first matrix is equal to the number of rows in the second matrix. Therefore, $matrix A_{m \times n}$ can be multiplied with a $matrix B_{p \times q}$ if $n = p$. The dimension of the product matrix is a $matrix C_{m \times q}$ The elements of two matrices can be multiplied by writing:
$$C_{(j \times i)}= Σ(A_{(j \times i)} * B_{(i \times j)}) \\: for \\: k = 1 \\: to \\: n$$


## Multi-Dimensional Arrays

A multi-dimensional array in simple terms is an array of arrays. As we have one index in a onedimensional array, two indices in a two-dimensional array, in the same way, we have $n$ indices in an n-dimensional array or multi-dimensional array. 

Conversely, an n–dimensional array is specified using $n$ indices. An n-dimensional $m_1 \times m_2 \times m_3 \times \cdots \times m_n$ array is a collection of $m_1 \times m_2 \times m_3 \times \cdots \times m_n$ elements. In a multi-dimensional array, a particular element is specified by using n subscripts as $A[I_1][I_2][I_3]...[I_n]$, where:

$$I_1 <= M_1 \\: , \\: I_2 <= M_2 \\: , \\: I_3 <= M_3 \\: , \\:  ... \\: I_n <= M_n$$

A multi-dimensional array can contain as many indices as needed and as the requirement of memory increases with the number of indices used. However, in practice, we hardly use more than three indices in any program. 

> ***Note:** A multi-dimensional array is declared and initialized the same way we declare and initialize one- and two-dimensional arrays.*

For instance, consider a three-dimensional array defined as int $A[2][2][2]$. Calculate the number of elements in the array. Also, show the memory representation of the array in the row major order and the column major order.

A three-dimensional array consists of pages. Each page, in turn, contains m rows and n columns

**Row Major Order**
<table>
  <tr>
    <td>(0,0,0)</td>
    <td>(0,0,1)</td>
    <td>(0,1,0)</td>
    <td>(0,1,1)</td>
    <td>(1,0,0)</td>
    <td>(1,0,1)</td>
    <td>(1,1,0)</td>
    <td>(1,1,1)</td>
  </tr>
</table>

**Column Major Order**

<table>
  <tr>
    <td>(0,0,0)</td>
    <td>(0,1,0)</td>
    <td>(0,0,1)</td>
    <td>(0,1,1)</td>
    <td>(1,0,0)</td>
    <td>(1,1,0)</td>
    <td>(1,0,1)</td>
    <td>(1,1,1)</td>
  </tr>
</table>

The three-dimensional array will contain $2 \times 2 \times 2 = 8$ elements.

## Sparse Matrices

Sparse matrix is a matrix that has large number of elements with a zero value. In order to efficiently utilize the memory, specialized algorithms and data structures that take advantage of the sparse structure should be used. If we apply the operations using standard matrix structures and algorithms to sparse matrices, then the execution will slow down and the matrix will consume large amount of memory. Sparse data can be easily compressed, which in turn can significantly reduce memory usage.

**There are two principal types of sparse matrices:**

In a lower-triangular matrix, $A_{(i \times j)} = 0$ where $i < j$. $A_n n \times n$ lower-triangular matrix A has **one non-zero** element in the first row, two non-zero elements in the second row and likewise n non-zero elements in the nth row. 

<table>
  <tr>
      <td>5</td> <!-- Non-zero element -->
      <td>0</td> <!-- Zero element -->
      <td>0</td> <!-- Zero element -->
  </tr>
  <tr>
      <td>3</td> <!-- Non-zero element -->
      <td>7</td> <!-- Non-zero element -->
      <td>0</td> <!-- Zero element -->
  </tr>
  <tr>
      <td>1</td> <!-- Non-zero element -->
      <td>4</td> <!-- Non-zero element -->
      <td>9</td> <!-- Non-zero element -->
  </tr>
</table>

In an upper-triangular matrix, $A_{(i \times j)} = 0$ where $i > j$. $A_n n \times n$ upper-triangular matrix A has **n non-zero** elements in the first row, n–1 non-zero elements in the second row and likewise one non-zero element in the nth row.

<table>
  <tr>
      <td>5</td> <!-- Non-zero element -->
      <td>3</td> <!-- Non-zero element -->
      <td>1</td> <!-- Non-zero element -->
  </tr>
  <tr>
      <td>0</td> <!-- Zero element -->
      <td>7</td> <!-- Non-zero element -->
      <td>4</td> <!-- Non-zero element -->
  </tr>
  <tr>
      <td>0</td> <!-- Zero element -->
      <td>0</td> <!-- Zero element -->
      <td>9</td> <!-- Non-zero element -->
  </tr>
</table>


## Structures

A structure is quite similar to a record, as it helps organize and store related information about an entity. Think of a structure as a custom data type that allows you to group various pieces of information, even if they have different data types, into one package. Unlike an array, which can only handle data of the same type, a structure gives you the flexibility to combine variables of different data types. 

In simpler terms, it's like having a container for multiple variables, each with its own data type and a unique name for easy access within the structure.

**Declaration of Structures.**

A structure is declared using the keyword ***struct*** followed by the structure name. All the variables of the structure are declared within the structure. A structure type is generally declared by using
the following syntax:

```c
struct struct-name
{
  dataype variable-name
  (...)
}
```

For instance, in scenarios involving **2D graphics** or **geometry**, you often need to manage points with both horizontal **(x)** and vertical **(y)** coordinates. To streamline this process, you can create a C structure called Point. This structure combines the x and y coordinates into a single data type, simplifying the handling of 2D spatial data in your program.

```c
struct Point
{
    double x;
    double y;
};
```

Now the structure has become a ***user-defined data type***. Each variable name declared within a structure is called a **member** of the structure. The structure declaration, however, does not allocate any memory or consume storage space. It just gives a template that conveys to the C compiler how the structure would be laid out in the memory and also gives the details of member names. 

Like any other data type, memory is allocated for the structure when we declare a variable of the structure.

```mermaid
classDiagram
class Point{
    - double: x
    - double: y
}
```

> ***Note:** Template of the Point Struct*

For example, we can define a variable of Point by writing:

```c
struct Point p

// Here, struct Point is a data type and p is a variable.
```

> ***Note:** Structure type and variable declaration of a structure can be either local or global depending on their placement in the code*

Last but not the least, structure member names and names of the structure follow the same rules as laid down for the names of ordinary variables. However, care should be taken to ensure that the name of structure and the name of a structure member should not be the same. 

**Typedef Declarations**

The **typedef** (derived from type definition) keyword enables the programmer to create a new data type name by using an existing data type. By using typedef, no new data is created, rather an alternate name is given to a known data type. The general syntax of using the typedef keyword is given as: 

```c
typedef existing_data_type new_data_type;
```

Note that typedef statement does not occupy any memory; it simply defines a new type. When we precede a struct name with the typedef keyword, then the struct becomes a new type. It is used to make the construct shorter with more meaningful names for types already defined by C or for types that you have declared. For example, consider the following declaration:

```c
typedef struct Point
{
  double x;
  double y;
}
```

Now that you have preceded the structure’s name with the typedef keyword, student becomes a new data type. Therefore, now you can straightaway declare the variables of this new data type
as you declare the variables of type int, float, char, double, etc. To declare a variable of structure Point, you may write:

```c
Point p;
```

#

**Initializing and Accessing Structures Members.**

A structure can be initialized in the same way as other data types are initialized. Initializing a structure means assigning some constants to the members of the structure. The initializers are enclosed in braces and are separated by commas. However, care must be taken to ensure that the initializers match their corresponding types in the structure definition.

The general syntax to initialize a structure variable is as follows:

```c
struct Point
{
  double x;
  double y;
}p = {1.0, 2.5}, q = {3.7};
```

```c
struct Point
{
  double x;
  double y;
};

struct Point p = {1.0, 2.5};
struct Point q = {3.7};
```

This is a illustration of how the values will be assigned to individual fields of the structure:

```mermaid
classDiagram
  class p["Point p"]
  p: 1.0
  p: 2.5

  class q["Point q"]
  q: 3.7
  q: 0.0

```

When all the members of a structure are not initialized, it is called partial initialization. In case of partial initialization, first few members of the structure are initialized and those that are
uninitialized are assigned default values.

#

Each member of a structure can be used just like a normal variable, but its name will be a bit longer. A structure member variable is generally accessed using a '.' (dot) operator. The syntax
of accessing a structure or a member of a structure can be given as:

```julia
struct_var.member_name
```

The dot operator is used to select a particular member of the structure. For example, to assign values to the individual data members of the structure variable **p**:

```julia
p.x = 4.5;
p.y = 1.9;
```

To input values for data members of the structure variable **p**:

```c
scanf("%lf", &(p.x));
```

Similarly, to print the values of structure variable **p**:

```c
printf("%lf\n", p.x);
```

Memory is allocated only when we declare the variables of the structure. In other words, the memory is allocated only when we instantiate the structure. In the absence of any variable, structure
definition is just a template that will be used to reserve memory when a variable of type struct is declared.

Once the variables of a structure are defined, we can perform a few operations on them. For example, we can use the assignment operator (=) to assign the values of one variable to another.

**Self-Referenced Structures**

Self-referential structures are those structures that contain a reference to the data of its same type. That is, a self-referential structure, in addition to other data, contains a pointer to a data that is
of the same type as that of the structure. For example, consider the structure node given below.

```c
struct node
{
  int val;
  struct node *next;
};
```

Here, the structure node will contain two types of data: an integer val and a pointer next. You must be wondering why we need such a structure. Actually, self-referential structure is the foundation
of other data structures. We will be using them throughout this guide and their purpose will be clearer to you when we discuss linked lists, trees, and graphs.


## Pointers

Every variable in C has a name and a value associated with it. When a variable is declared, a specific block of memory within the computer is allocated to hold the value of that variable. The size of the allocated block depends on the data type.

Consider the following statement.

```c
int x;
```

When this statement executes, the compiler sets aside **2 bytes of memory** to hold the value 10. It also sets up a symbol tabl in which it adds the symbol **x** and the **relative address in the memory** where those 2 bytes were set aside. Thus, every variable in C has a value and also a **memory location (commonly known as address) associated with it**.

Actually, **pointers are nothing but memory addresses**. A pointer is a variable that contains the memory location of another variable. Therefore, a pointer is a variable that represents the **location of a data item**, such as a variable or an array element. Pointers are frequently used in C*, as they have a number of *useful applications. These applications include:

- Pointers are used to pass information back and forth between functions.
- Pointers enable programmers to return multiple data items from a function via function arguments.
- Pointers provide an alternate way to access the individual elements of an array.
- Pointers are used to pass arrays and strings as function arguments (discussed in subsequent chapters).
- Pointers are used to create complex data structures, such as trees, linked lists, linked stacks, linked queues, and graphs.
- Pointers are used for the dynamic memory allocation of a variable (refer to Appendix A for memory allocation in C programs).

**Declaring Pointer Variables**

The general syntax of declaring pointer variables can be given as below.

```c
dataype *ptr_name;
```

Here, ***data_type*** is the data type of the value that the pointer will point to. For example,

```c
int *ptr;
```

In each of the above statements, a pointer variable is declared to point to a variable of the specified data type. It's worth noting that all pointers, even if they point to different data types, will occupy the same amount of space in memory. However, the exact amount of space they occupy depends on the platform where the code is executed

```c
int x, *ptr;

x = 10;
ptr = &x;
```

In the above statement, **ptr** is the name of the pointer variable. The **\*** informs the compiler that **ptr** is a pointer variable and the int specifies that it will store the address of an integer variable.

An integer pointer variable, therefore, *points to* an integer variable. In the last statement, **ptr** is assigned the address of **x**. The **&** operator retrieves the ddress of **x**, and copies that to the contents of the pointer **ptr**.

We can 'dereference' a pointer, meaning we can access the value of the variable it points to by using the unary * operator, as in *ptr. For example, *ptr = 10 assigns the value 10 to the variable pointed to by ptr, which in this case is equivalent to setting the value of x to 10.

```c
#include <stdio.h>

int main()
{
  int num, *pnum;
  pnum = &num;

  printf("\n Enter the number : ");
  scanf("%d", &num);
  printf("\n The number that was entered is : %d", *pnum);
  return 0;
}
```

**Output**

```julia
Enter the number : 10
The number that was entered is : 10
```

#

**Null Pointers**

In some cases, we may prefer to have a null pointer which is a special pointer value and does not point to any value. This means that a null pointer does not point to any valid memory address.

To declare a **null pointer**, you may use the predefined constant **NULL** which is defined in several standard header files including **<stdio.h>**, **<stdlib.h>**, and **<string.h>**. After including any of these files in your program, you can write

```c
int *ptr = NULL;
```

You can always check whether a given pointer variable stores the address of some variable or contains **NULL** by writing,

```c
if (ptr == NULL)
{
  statement block;
}
```

**Pointer to Pointers**

The pointers in turn point to data or even to other pointers. To declare pointers to pointers, just add an asterisk * for each level of reference

**For example, consider the following code:**

```c
int x;
int *px, **ppx;

int x = 10;
px = &x;
ppx = &px;
```

```mermaid
classDiagram 
	direction LR
	class x["X"]
		x: 10
		x: MemoryAdress(1002)
	
	class px["PX"]
		px: 1002
		px: MemoryAdress(2004)
	
	class ppx["PPX"]
		ppx: 2004
		ppx: MemoryAdress(4008)
	
	x <-- px
	px <-- ppx 
```

## Recursion

**Recursive Binary Search**
  - Implementation of binary search using recursion.
  - Comparison with iterative binary search.
  - Efficiency of recursive binary search.

```c
#include <stdio.h>
#include <stdlib.h>

int binarySearch(int begin, int end, int *array);

int main()
{
	
	return 0;
}

int binarySearch(int begin, int end, int *array)
{
}
```

#

**Fibonacci Sequence**
  - Calculating Fibonacci numbers using recursion.
  - The Fibonacci recurrence relation.
  - Efficiency considerations in recursive implementation.

#

 **Recursive Factorial**
  - Calculating the factorial of a number using recursion.
  - Illustration of the call stack concept.
  - Comparison with iterative approach.

## Linked Lists 



---

## Conclusion

#### Reference

- TENENBAUM, Aaron M. ; LANGSAM, Yedidyah ; AUGENSTEIN, Moshe J. **Data Structures Using C**. Facsimile Edition. Pearson, 1989.
- CORMEN, Thomas H. ; LEISERSON, Charles E. ; RIVEST, Ronald L. ; STEIN, Clifford. **Introduction to Algorithms**. 4th Edition. MIT Press, 2022.




<!-- 
# Study Guide: Data Structures in C


## 7. Linked Lists
- Introduction to linked lists.
- Implementation of a simple linked list.
- Insertion and removal of elements in linked lists.

## 8. Stacks and Queues
- Concept of stacks and queues.
- Implementation of stacks and queues in C.

## 9. Trees
- Introduction to trees.
- Binary search trees.
- Tree traversal.

## 10. Sorting and Searching Algorithms
- Sorting algorithms (e.g., Bubble Sort, Quick Sort).
- Searching algorithms (e.g., Binary Search).

## 11. Advanced Data Structures (Optional)
- Graphs and their representations.
- Hash tables (hash tables).
- Balanced data structures (e.g., AVL trees).

## 12. Best Practices and Efficiency
- Code optimization.
- Proper choice of data structures.

## 13. Examples and Practical Exercises
- Small examples of data structure applications.
- Practical exercises to reinforce learning.
!-->
