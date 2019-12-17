![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Recursion


## Overview
We've seen that a function can call other functions to perform an action. When a function becomes too large to read or test easily, we split them into smaller functions that perform parts of the larger whole. 

**Recursion is a function that calls itself.** A recursive function achieves a small part of the larger task, then passes the partially completed result to another call of itself.  Recursion is a useful alternative to iteration methods like loops. They are especially helpful for looking at all combinations or permutations of a given input.

There are two parts to this lesson:
1. [myGA module: Recursion](https://my.generalassemb.ly/activities/773)
2. [In-Class Exercise: Writing Recursive Functions](exercises/recursion.js)

> **Note**: The myGA module contains a link to an exercise in CodePen. **The code in CodePen is the exact same as the code for the in-class exercises.** Try out the exercise in CodePen and see how far you can get with it. Leave off where you get stuck and we'll review the solution in class.

## Learning Objectives
By the end of this lesson, you will be able to:
- Define recursion.
- Write the base case and recursive cases of a recursive function.
- Identify functions that use recursion and explain why it’s used.

## Duration
1 hour total:
- 0.5 hour myGA
- 0.5 hour in class

## Prerequisites
- Big O Notation

## Three steps of recursion
We can break a recursive function into three steps: 

1. Base case
2. Action
3. Recursive case leading towards the base case

First, establish a base case. Ask when do we know the process can stop? At this point we can return a specific value, instead of calling the function again recursively.

Next, perform the action of the function. If recursive functions simply called themselves forever without doing anything else, they wouldn't be very useful. Regular recursive functions do some kind of computation that helps lead to the final result.

Finally, we call the function recursively inside itself. Make sure we progress towards the base case. If we do not make progress toward the base case we will cause a stack overflow when the stack of unresolved function calls gets too large to handle.

### Memoization
Memoization is often useful in recursion. This is when the results of a function call are remembered so they can be used again in later function calls. This is like caching your results to use again.

### Tail Recursion
Tail recursion is where calculations are performed first and then the recursive call is executed. Some programming languages, usually functional ones, optimize tail calls so they take up less room on the call stack.

## Applications of Recursion
- Permutations
- Traversing Multiple Paths
- Divide and Conquer

Now that you understand the how of recursion, let's talk about when and why to use it. Keep in mind that any recursive function can also be written using iteration, and iteration will usually be more efficient than recursion. Recursion is useful because it allows for more straightforward, elegant code to solve complex problems.

Consider using recursion any time you're exploring multiple possibilities or paths, such as calculating all possible combinations of elements, or checking all paths between two destinations. Recursion provides the simplest solution by continuing through each possibility using a new recursive call.

Recursion also lets us divide a larger problem into smaller subproblems. Merge sort, for example, can use recursion to break down sorting an array into sorting two, smaller arrays. Eventually it will reach the base case of a single element array, and then zip these single-element arrays back together into a single sorted array. While this could be done using iteration, it would become difficult to read, modify, and debug compared to the recursive version.

## Additional Resources
- How recursion comes up in [job interviews](https://hackernoon.com/coding-interview-recursion-f0d60c9dbb60).
- More thoughts on recursion in [job interviews](https://www.byte-by-byte.com/recursion/).
- Sketching out a [recursive function](https://www.youtube.com/watch?v=bGC2fNALbNU).
- Recursion for Coding Interviews: [The Ultimate Guide](https://www.byte-by-byte.com/recursion/).
- Just for fun: The [recursion subreddit](https://www.reddit.com/r/recursion).


### Sources/Contributors
- [Carlos Godoy](https://git.generalassemb.ly/seir-826/recursion)
- [Ryan Fleharty](https://git.generalassemb.ly/ryanfleharty/recursion-exercises/blob/master/lesson.md)
- [Ali Spittel](https://github.com/aspittel/coding-cheat-sheets/blob/master/fundamentals/recursion.md)
