Add your answers to the Algorithms exercises here.

### Exercise I

a) The number operations outside of the while loop is 3, the assignment of `a` to `0` and multiplying twice in n*n*n for the given n giving O(3). The code in the while loop will execute n times since it's looping from 0 to n*n*n and `a` is increasing each loop by n*n giving O(n) (we're essentially dividing n*n*n by n*n). I tested this out by calculating n(1), n(10), and n(100). The number of operations per while loop is 4, comparing a to n, assigning a to a + n _ n, adding a to n _ n, and multiplying n \* n. This overall gives O(4n +3) which rounds down to O(n). There is an edge case where n = 0 where the loop goes on infinitely though.

b)

c)

### Exercise II
