# Introduction
 Goals

* **The importance of algorithm analysis:** efficiency
* **Key concepts:** Notations, relationships, and problem-solving techniques related to algorithms.
* **Learning outcomes:**  determine the complexity of algorithms
### 1. Variables
  
  * Consider the equation "x + 2 - y = 1" as an example.
  * 'x' and 'y' in the equation are "names" that "hold values" or "data."
  * these names act as "placeholders" for representing data.
  * in computer programming, "variables" serve the same purpose of holding data.
### 2.  Data Types
  
  * **Variable values:** Variables like 'x' and 'y' can hold various data types, including integers, real numbers, or binary values (0 and 1).
  * **Data types:** A data type defines the kind of values a variable can hold. Examples include integer, floating-point, character, and string.
  * **Memory representation:** Computer memory stores data as zeros and ones. Data types simplify programming by allowing us to work with higher-level abstractions.
  * **Data type size:** Different data types occupy different amounts of memory (e.g., an integer might take 2 bytes, a float 4 bytes).
  * **Data type categories:**
      * System-defined (primitive) data types: Built-in data types provided by the programming language.
      * User-defined data types: Data types created by the programmer.
  
  ####  System-defined data types (Primitive data types) 
  
   * **Definition:** System-defined data types are built-in data types provided by programming languages.
    * **Examples:** Common primitive data types include `int`, `float`, `char`, `double`, and `bool`.
    * **Size variation:** The size (in bits) of these data types can vary depending on the programming language, compiler, and operating system.
    * **Domain impact:** The size of a data type determines the range of values it can represent.
    * **Integer example:**
        * A 2-byte (16-bit) integer can store values from -32,768 to 32,767.
        * A 4-byte (32-bit) integer can store values from -2,147,483,648 to 2,147,483,647.
    * **Generalization:** This size and domain variation applies to other primitive data types as well.

  #### User defined data types
    
  * **Necessity:** created when system-defined (primitive) data types are insufficient.
  * **Definition:**  created by the programmer.
  * **Example:** Classes in object-oriented programming (like Python) 
  * **Flexibility:** They allow programmers to combine multiple system-defined data types into a single, custom data type.
  * **Code Example:**

        class NewType(object):
        def __init__(self, datainput1, datainput2, datainput3):
        self.data1 = datainput1
        self.data2 = datainput2
        self.data3 = datainput3

> Python code snippet demonstrates creating a user-defined data type called "NewType" that combines three data inputs (data1, data2, data3).
  * **Benefit:** They enhance flexibility and ease of memory management.

### 3. Data Structures

* **Purpose:** Data structures provide a mechanism for manipulating data stored in variables to solve problems efficiently.
* **Definition:** A data structure is a specific way of organizing and storing data in a computer.
* **Examples:** Common data structure types include arrays, files, linked lists, stacks, queues, trees, and graphs.
* **Classification:** Data structures are classified into two main categories:
    * **Linear Data Structures:**
        * Elements are accessed sequentially.
        * Elements may or may not be stored sequentially in memory.
        * Examples: Linked lists, stacks, and queues.
    * **Non-linear Data Structures:**
        * Elements are stored and accessed in a non-sequential manner.
        * Examples: Trees and graphs.
### 4. Abstract Data Types (ADTs)

* **Building on Data Types:**  primitive data types have built-in operations, and user-defined types require defining their own.
* **ADT Definition:** An ADT combines a data structure with its associated operations.
* **Components of an ADT:**
    * Declaration of data.
    * Declaration of operations.
* **Purpose:** ADTs simplify problem-solving by providing a clear separation between the data organization and its manipulation.
* **Examples:** Common ADTs include linked lists, stacks, queues, priority queues, binary trees, dictionaries, and graphs.
* **Stack Example:** It uses the stack ADT to illustrate the concept, highlighting its LIFO behavior and common operations (push, pop, etc.).
* **Abstraction:** ADTs focus on what operations are performed, not how they are implemented.
* **Application:** Different ADTs are suitable for different applications, and the book aims to familiarize the reader with various ADTs and their problem-solving capabilities.

### 5. What is an Algorithm?

* **Omelet Example:**

      1) Get the frying pan.
      2) Get the oil.
          a. Do we have oil?
            i. If yes, put it in the pan.
            ii. If no, do we want to buy oil?
                1. If yes, then go out and buy.
                2. If no, we can terminate.
                3) Turn on the stove, etc...
* **Algorithm Definition:** An algorithm is defined as a set of unambiguous, step-by-step instructions to solve a given problem.
* **Algorithm Criteria:**
    * **Correctness:** Does the algorithm provide a solution in a finite number of steps?
    * **Efficiency:** How much memory and time does the algorithm require?
*NOTE: **No Proof Required:**  individual steps of an algorithm do not need to be proven.
### 6.Why the Analysis of Algorithms?
  * **Multiple Algorithms:** Just as there are multiple ways to travel, there are often multiple algorithms to solve the same problem (e.g., sorting).
  * **Algorithm Analysis Purpose:** Algorithm analysis helps determine which algorithm is the most efficient in terms of time and space consumption.

### 7. Goal of the Analysis of Algorithms
 The goal is to compare algorithms (or solutions) mainly in terms of running time but also in terms of other
factors (e.g., memory, developer effort, etc.)

### 8. What is Running Time Analysis?
  * It is the process of determining how processing time increases as the size of the problem (input size) increases. 
  * Input size is the number of elements in the input, and depending on the problem type, the input may be of different types.
  * The following are the common types of inputs.
    *  Size of an array
    *  Polynomial degree
    *  Number of elements in a matrix
    *  Number of bits in the binary representation of the input
    *  Vertices and edges in a graph.
### 9. How to Compare Algorithms
  certain metrics are unsuitable for comparing algorithms so we proposes an ideal solution:

* **Unsuitable Metrics:**
    * **Execution Times:** These are too dependent on the specific computer's hardware.
    * **Number of Statements Executed:** This varies based on the programming language and coding style.
* **Ideal Solution:**
    * Express the algorithm's running time as a function of the input size, denoted as $f(n)$.
    * Compare these functions to analyze the algorithms' efficiency, regardless of machine-specific times or programming styles.
### 10 What is Rate of Growth?
The concept of the rate of growth of a function is used to analyze algorithm efficiency:

* **Rate of Growth:** The rate at which running time increases with input size is "growth rate."
* **Ignoring Low-Order Terms:** For a given function, low-order terms and constant factors are ignored when analyzing growth rate, especially for large input sizes (n).
    * Eg.  $f(n) = n^2 + n \approx n^2$ 
* **Example:** In the function $n^2 + 2n + 100 + 500$, the $n^2$ term has the highest growth rate, so the function is approximated to $n^2$.

### 11. Commonly Used Rates of Growth
  $2^{2^n} > n! > 4^n > 2^n > n^2 > n ~log(n) > log(n!) > n > 2^{log(n)} > log^2(n) > \sqrt(log(n)) > log(log(n)) > 1$.
  | Time Complexity | Name               | Example                                                    |
|-----------------|--------------------|------------------------------------------------------------|
| 1               | Constant           | Adding an element to the front of a linked list            |
| log n           | Logarithmic        | Finding an element in a sorted array                      |
| n               | Linear             | Finding an element in an unsorted array                    |
| n log n         | Linear Logarithmic | Sorting n items by ‘divide-and-conquer’ - Mergesort       |
| n^2             | Quadratic          | Shortest path between two nodes in a graph                 |
| n^3             | Cubic              | Matrix Multiplication                                      |
| 2^n             | Exponential        | The Towers of Hanoi problem                               |

### 12. Types of Analysis
To analyze a given algorithm, we need to understand its performance with different inputs, specifically which inputs result in faster execution and which lead to slower execution. We represent algorithm performance using mathematical expressions, with different expressions for different scenarios.

**Analysis Types:**

* **Worst-case:**
    * Defines the input that results in the longest execution time.
    * Provides an upper bound on the algorithm's runtime.
    * Input is the one for which the algorithm runs the slowest.
* **Best-case:**
    * Defines the input that results in the shortest execution time.
    * Provides a lower bound on the algorithm's runtime.
    * Input is the one for which the algorithm runs the fastest.
* **Average-case:**
    * Predicts the algorithm's running time for typical inputs.
    * Involves running the algorithm with many random inputs and calculating the average runtime.
    * Assumes the inputs are randomly generated.
    * Provides a prediction about the running time of the algorithm.
    * Run the algorithm many times, using many different inputs that come from some distribution that generates these inputs, compute the total running time (by adding the individual times), and divide by the number of trials.
    * Assumes that the input is random.

**Expression Representation:**

For a given algorithm, we can represent the best, worst, and average cases in the form of expressions. For example, let f(n) be the function representing the given algorithm:

* Worst-case: f(n) = n² + 500
* Best-case: f(n) = n + 100 + 500

Similarly, for the average case, the expression defines the inputs with which the algorithm takes the average running time (or memory).

### 13. Asymptotic Notation
 Having the expressions for the best, average and worst cases, for all three cases we need to identify the upper and lower bounds. To represent these upper and lower bounds, we need some kind of syntax, and that is the subject of the following discussion. Let us assume that the given
 algorithm is represented in the form of function $f(n)$.

### 14. Big-O Notation 
**Big O Notation (O-notation): Asymptotic Upper Bound**

This notation provides the asymptotic upper bound of a given function. It's generally represented as f(n) = O(g(n)). This means that for larger values of 'n', the upper bound of f(n) is g(n).

* **Example:**
    * If f(n) = n² + 100n + 10 + 50, then f(n) is O(n²).
    * This indicates that n² represents the maximum rate of growth for f(n) at large values of 'n'.

* **Formal Definition:**
    * O(g(n)) = {f(n): there exist positive constants c and n₀ such that 0 ≤ f(n) ≤ c * g(n) for all n ≥ n₀}.
    * g(n) is an asymptotic tight upper bound for f(n).

* **Objective:**
    * To find the smallest rate of growth g(n) that is greater than or equal to the given algorithm's rate of growth f(n).
* **Ignoring Lower Values:**
    * Lower values of 'n' are typically discarded.
    * The rate of growth at lower 'n' values is considered insignificant.

* **Threshold (n₀):**
    * n₀ is the point from which the rate of growth is considered.
    * Below n₀, the rate of growth might be different.
** No Uniqueness? **
  There is no unique set of values for and in proving the asymptotic bounds. Let us consider, 100 + 5 = O( ). For this function there are multiple and values possible.

### 15. Omega-Ω Notation
**Omega Notation (Ω-notation): Asymptotic Lower Bound**

This notation provides the tighter lower bound of a given algorithm. It's represented as f(n) = Ω(g(n)). This means that for larger values of 'n', the lower bound of f(n) is g(n).

* **Formal Definition:**
    * Ω(g(n)) = {f(n): there exist positive constants c and n₀ such that 0 ≤ c * g(n) ≤ f(n) for all n ≥ n₀}.
    * g(n) is an asymptotic tight lower bound for f(n).

* **Objective:**
    * To find the largest rate of growth g(n) that is less than or equal to the given algorithm's rate of growth f(n).

* **Example:**
    * If $f(n) = 100n^{1.15} + 10n + 50$, then $f(n)$ is $Ω(n^{1.15})$.

    * n₀ is called the threshold for the given function.
### 16. Theta- $\Theta$ Notation
**Theta Notation (Θ-notation): Asymptotic Tight Bound**

This notation determines if the upper and lower bounds of a given function (algorithm) are the same. It indicates that the algorithm's growth rate is tightly bound by a specific function.

* **Definition:**
    * Theta notation decides whether the upper and lower bounds of a given function (algorithm) are the same.
    * If the upper bound (O) and lower bound (Ω) give the same result, then the Θ notation will also have the same rate of growth.
* **Relationship to Bounds:**
    * The average running time of an algorithm is always between the lower bound and the upper bound.
    * If the upper and lower bounds are the same, the average case (Θ) will also have the same growth rate.
* **Example:**
    * If f(n) = 10n + n², then O(f(n)) = n² and Ω(f(n)) = n².
    * Therefore, Θ(f(n)) = n².
* **Varying Bounds:**
    * If O and Ω are different, then Θ might also be different.
    * In such cases, all possible time complexities need to be considered, and their average is calculated.
* **Formal Definition:**
    * Θ(g(n)) = {f(n): there exist positive constants c₁, c₂, and n₀ such that 0 ≤ c₁ * g(n) ≤ f(n) ≤ c₂ * g(n) for all n ≥ n₀}.
    * g(n) is an asymptotic tight bound for f(n).
    * Θ(g(n)) is the set of functions with the same order of growth as g(n).

### 17. Why is it called Asymptotic Analysis?
**Asymptotic Analysis: Approximating Algorithm Performance**

The core concept behind Big O, Omega, and Theta notations is to approximate the performance of an algorithm for large input sizes.

* **Approximation at Higher Values:**
    * For a given function f(n) representing an algorithm's performance, we aim to find another function g(n) that approximates f(n) as 'n' becomes large.
    * This means g(n) represents the algorithm's behavior for large input sizes.
* **Asymptotic Curve:**
    * g(n) acts as an asymptotic curve for f(n).
    * In mathematics, such a curve that approaches another curve as a limit is called an asymptote.
* **Asymptotic Analysis:**
    * Therefore, the process of analyzing algorithms using these notations is called asymptotic analysis.

 ### 18. Guidelines for Asymptotic Analysis
   1. **Loop Time:** Loop time is the time for inner statements multiplied by loop iterations.

           #executes n times
           for i in range(0,n):
               print ('Current Number :', i, sep=" ") #constant time 
   > **Example:** A `for` loop running `n` times with constant-time operations inside has O(n) time complexity.
  
   2.  * **Nested Loops:** Analyze inside-out.
       * **Time:** Product of loop iterations.
       * **Example:** Two 'n' iteration loops result in O(n²).
         # outer loop executed times

    for i in range(0,n):
       # inner loop executes n times
       for j in range(0,n):
           print ('i value {i} and j value {j}') #constant time

### 26. Amortized analysis
Absolutely! You've provided a good overview of amortized analysis. Let's summarize and clarify some key points:

**Amortized Analysis: Key Concepts**

* **Focus on Sequences:** Amortized analysis examines the average cost of operations within a sequence, not the cost of individual operations.
* **Worst-Case, Sequence-Based:** It provides a worst-case guarantee for the *entire sequence* of operations, even if some individual operations are expensive.
* **No Distribution Assumptions:** Unlike average-case analysis, it doesn't assume any specific probability distribution of inputs.
* **Motivation:** To obtain a tighter, more realistic bound on the performance of algorithms where some operations are costly but infrequent.
* **Amortized Cost:** An artificial cost assigned to each operation. The total amortized cost of a sequence bounds the total actual cost.
* **Accounting for State Changes:** Amortized analysis accounts for how expensive operations can alter the data structure, making subsequent operations cheaper.

**Why Amortized Analysis is Useful**

* It provides a more accurate picture of performance when expensive operations are rare but have a significant impact.
* It helps in understanding the efficiency of data structures and algorithms that have varying operation costs.

**Example Explanation (Finding the Smallest Element)**

Your example of finding the smallest element in an array highlights the benefit of amortized analysis.

* **Sorting:** Sorting the array once takes O(n log n) time.
* **Subsequent Minimum Queries:** After sorting, finding the minimum element is O(1).
* **Sequence of operations:** If we have m find minimum operations, then the first operation is O(n log n) and the next m-1 operations are O(1) each.
* **Amortized cost:** If m is large, the total cost is O(n log n + m). The amortized cost per operation is approximately O((n log n + m) / m). If m is greater than n log n, then the amortized cost becomes O(1).
* **Benefit:** By performing the initial expensive sort, we significantly reduce the cost of subsequent minimum queries. This is a classic example of how an expensive operation can "pay" for future cheap operations.

**In essence:**

Amortized analysis helps us understand that even if some operations are expensive, their impact is "averaged out" over the entire sequence, leading to a more accurate assessment of overall performance.
