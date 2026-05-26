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

Beyond `for` loops, there are other kinds of looping we can use in Python. One of these is the <span class="bold">`while` loop</span>. With it, we can execute a set of statements as long as a condition is true.

In this example, we’re using a while loop as an alternative to for loops to print a range of numbers.

```python
i = 0
while i < 3:
	print(i)
	i = i + 1
```

What does the above code print?

<details>
    <summary>Answer</summary>
    `0`

    `1`
    
    `2`
</details>
<br />

The syntax used in while loops is the following:

```python
while CONDITION:
	BLOCK_OF_CODE_1
REST_OF_THE_CODE
```

Here’s a diagram explaining the flow of a while loop:

<img class="diagram" alt="Diagram explaining the flow of a while loop" src="/blog-images/while-loop.png">

<div class="highlight">
Watch out! For loops will end on their own once they reach the end of the list, but while loops DO NOT.
</div> 

If you don’t change anything about the starter condition, your code will get stuck in an <span class="bold">infinite loop</span>, which means the program could technically run forever.

```python
i = 0
while i < 3:
	print(i)
```

The code above will run <span class="bold">forever</span>, because we’re never changing the value of `i`. Since we’re never changing it, the condition will always be true and the loop will never exit.

### Quiz