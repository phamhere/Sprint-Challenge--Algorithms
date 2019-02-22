Add your answers to the Algorithms exercises here.

### Exercise I

a) The number operations outside of the while loop is 3, the assignment of `a` to `0` and multiplying twice in n*n*n for the given n giving O(3). The code in the while loop will execute n times since it's looping from 0 to n*n*n and `a` is increasing each loop by n*n giving O(n) (we're essentially dividing n*n*n by n*n). I tested this out by calculating n(1), n(10), and n(100). The number of operations per while loop is 4, comparing a to n, assigning a to a + n _ n, adding a to n _ n, and multiplying n \* n. This overall gives O(4n +3) which rounds down to O(n). There is an edge case where n = 0 where the loop goes on infinitely though.

b) At a glance, since there are four sequentially nested four loops, each with an approximate runtime of O(n), the total runtime complexity would be about O(`n**4`).

c) The number of operations per function run is 3: checking if bunnies == 0, adding 2 to the recursive call, and subtracting one inside the recursive call, so O(3) there. The function will be called n times since it's a recursive function that calls with n-1 until n == 0. So overall the runtime complexity would by O(3n) or O(n).

### Exercise II

Since the building levels acts essentially like a sorted list, we can employ binary search to approximately get a quick runtime of O(log n). We would start at the middle floor, test to see if the egg broke there. If it does, then we would eliminate the upper floors and test the lower floors. If the egg didn't break there, we would do the opposite and eliminate the lower floors and check the upper floors. Since we're halfving each time the number of possible floors that the floor could be on, at worst the runtime would be O(log n).

def find_floor_helper(n, l, h):
base case to stop recursion and return
find middle of l and h
check to see if egg breaks at floor[middle]
if egg breaks, call find_floor_helper(n, l, middle)
if egg doesn't break, find_floor_helper(n, middle, h)

def find_floor(floors):
return find_floor_helper(floors, low, high)
