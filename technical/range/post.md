<style>
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
    table>tbody>tr>td {
        padding: 0 1rem;
    }
    a {
        color: gray;
    }
    a:hover {
        color: darkgrey;
    }
    summary {
        cursor: pointer;
    }
    div.highlight {
        background-color: #8ae514; 
        padding: 1rem; 
        border-radius: 1rem; 
        border: 1px solid black; 
        color: black; 
        box-shadow: 5px 5px black; 
        margin-bottom: 1rem;
    }
    img.diagram {
        max-width: 90%;
        margin: 1rem 2rem;
        max-height: 30rem;
    }
    span.special-bold {
        font-weight: bold;
        color: black;
    }
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", by Jaya Nikalantan and Bennett Axtell
</small>

Consider the following example: I want to display 5 `*` characters in the terminal. Instead of writing 5 print statements, I will write a loop that repeats the print statement 5 times.

```python
for i in [0, 1, 2, 3, 4]:
    print('*', end='')
```

A few things to note:

- The call to the `print` function has a named parameter `end`. This named parameter tells the print function to end the line of printing with an empty string. By default, print end the line with a new line, so the next thing to be printed is on the next line.

- We use a list of five integers to cause the iteration to happen five times. In fact, we could have used any five values, since the values in the list are not important, just that the iteration happens five times. If we change the code so that line 1 says `for i in ['a', 'b', 'c', 'd', 'e']:`, the loop still runs the same way. That is because the variable `i` is not used anywhere in the loop body; it is only used to track the place in the list.

Let’s say the teacher changed the assignment and now we have to display 200 `*` characters. Ugggghhhh!!!! It would be really tedious to write 200 random values in the list. It would be better to have a <span class="bold">single value</span> that counts the number of iterations. The huge benefit of coding this way is abstraction: if you need to change the number of `*` drawn, you don’t have to count anything manually, <span class="bold">you just need to change one value</span>.

It turns out that iterating through a loop for a specific number of times is a common thing to do. Python gives us special built-in <span class="bold">`range` objects</span> that can deliver a sequence of values to the `for` loop. When called with one parameter, the sequence provided by `range` always starts with 0. If you ask for `range(5)`, then you will get 5 values starting with 0. In other words, 0, 1, 2, 3, and finally 4. Notice that 5 is not included since we started with 0. Likewise, `range(10)` provides 10 values, 0 through 9.

```python
for i in range(6):
	print('*', end='')
```
How many values are produced by range(6)? What are they?

<details>
    <summary>Answer</summary>
    6 values

    `0, 1, 2, 3, 4, 5`
</details>
<br />

<div class="highlight">
Note: Like we saw with the indexing, <span class="bold">programming languages count from 0</span>! 0 is the first element, 1 is the second, etc.
</div>

The `range` function is actually a very powerful function when it comes to creating sequences of integers. It can take one, two, or three parameters. We have seen the simplest case of one parameter such as `range(4)` which creates `[0, 1, 2, 3]`. 

But what if we really want to have the sequence `[1, 2, 3, 4]`? We can do this by using a two parameter version of `range` where the first parameter is the starting point and the second parameter is the ending point+1. The evaluation of range(1,5) produces the desired sequence. Why is the second parameter 5 and not 4? In this case we interpret the parameters of the range function to mean `range(start,beyondLast)`, where $beyondLast - start$ tells you how many numbers are in the sequence.

Why does range not just work like `range(startNumber, lastNumber)` with 2 parameters? Think about it like this. Because computer scientists start counting at 0 instead of 1, `range(N)` produces a sequence of things that is N long. But the consequence of this is that the final number of the sequence is N-1. With range(start,beyondLast), it helps to think that the sequence begins with start and continues as long as the number is less than beyondLast.

<div class="highlight">
Note: The range function is lazy: It produces the next element only when needed. With a regular Python 3 interpreter, printing a range does not calculate all the elements. We need to put them in a list first.
</div>

```python
print(range(4))
print(list(range(4)))
print(list(range(1, 5)))
```

The output of the print statements would be:
- `range(0, 4)`
- `[0, 1, 2, 3]`
- `[1, 2, 3, 4]`

Finally, suppose we want to have a sequence of even numbers. How would we do that? Easy, we add another parameter, a step, that tells range what to count by. For even numbers we want to start at 0 and count by 2’s. So if we wanted the first even numbers up to but not including 20 we would use `range(0,20,2)`. The most general form of the range is `range(start, beyondLast, step)`. You can also create a sequence of numbers that starts big and gets smaller by using a negative value for the step parameter.

```python
print(list(range(0, 19, 2)))
print(list(range(0, 20, 2)))
print(list(range(10, 0, -1)))
```

What would be the output of the first print statement?


<details>
    <summary>Answer</summary>
    `[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]`
</details>
<br />
