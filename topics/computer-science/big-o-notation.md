# Big-O Notation

The Big-O Notation is a way to describe algorithm performance in relation to the size of the input. Algorithms will perform differently depending on the environment (programming language, PC performance, etc) Therefore, the most reasonable way to measure performance is by describing how the performance is affected as the size of the input increases. For example, $O(n)$ - where $n$ is the size of the input - is referred to as linear time. As $n$ increases, the time it takes for the algorithm to run increases proportionally. 

Other examples are: $O(1)$ - constant time, $O(n^2)$ - quadratic time, $O(log n)$ - logarithmic time

The performance is calculated by summing the operations inside of an algorithm:

- A simple assignment operation is equal to $1$
- A loop that iterates over the inputted list is $n$ times operations inside - each operation must be performed $n$ times for each element in the list
- A nested loop is $n^2$

An equation can be derived from summing these steps, such as $T(n) = 3n^2 + 2n + 4$. As n increases, $4$ becomes insignificant in this equation, therefore we do not include it. The same goes for $2n$ and the $3$ multiplier for $n^2$. We are only concerned about $n^2$ here as this is the most significant factor of this equation. Therefore, the Big-O notation for this example is $O(n^2)$.