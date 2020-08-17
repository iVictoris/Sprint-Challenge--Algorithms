#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a)
n = 1 => 1 iterations
n = 2 => 2 iterations
n = 3 => 3 iterations
O(n)

b)
n = 1 => 1 -- 1 for loop
n = 2 => 2 -- 2 for loop
n = 3 => 5 -- 3 for loop 2 while loop
n = 4 => 6 -- 4 for loop 2 while loop
n = 5 => 8 -- 5 for loop 3 while loop
O(n log n)

c)
n = 1 => 1
n = 2 => 2
n = 3 => 3
O(n)

## Exercise II

this is similar to a guessing game

ok so we know the n is the building, if we don't know
we simply divide the building till we hone into a guess
so say the building is 100 stories high and f is 37

store max = n (starting floor)
check if egg.drop(max)
    if it doesn't
    return max

// while loop here
now we need to get the middle
middle = max // 2
check if egg.drop(middle) <-- this would probably return a boolean -->
    if egg is broken
        max = middle
        middle = max // 2
        repeat check for egg drop
    if egg is not broken
        next_floor = middle + 1
        check if egg.drop(next_floor)
            see if it breaks
            if it does then return middle
        
        otherwise we need to bring up the search space
        middle = (max + middle) // 2

this would be o(log n)