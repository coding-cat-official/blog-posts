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

A lot of computations involve processing (also called <span class="bold">iterating over</span>) a collection one item at a time. For collection data types this means that we would like to process one character at a time. Often we start at the beginning, select each character in turn, do something to it, and continue until the end. This pattern of processing is called a <span class="bold">traversal</span>.

The `for` statement can iterate over the items of a sequence (a list of strings in the case below).

```python
grocery_list = [ 'Tomato', 'Butter', 'Oregano', 'Fettuccini' ]
for product in grocery_list:
	message = f'You need to buy {product}!'
	print(weather_prediction)
```

The loop variable takes on <span class="bold">each value</span> in the sequence of names. The loop body (i.e., the indented lines of code) is performed once for product.

How many times will the code above print something? What will it print on the 3rd time it prints something (if anything)?

<details>
    <summary>Answer</summary>
    The code will print something 4 times.

    The 3rd thing it will print is `You need to buy Oregano`
</details>
<br />

The syntax used in a for loop is the following:

```python
for ITEM in ITERABLE:
	BLOCK_OF_CODE_1
REST_OF_THE_CODE
```

`ITERABLE` here designates anything that can be iterated over, like a list or a string. To simplify things, here’s a diagram explaining the flow of it all.

<img class="diagram" alt="Diagram demonstrating the flow of a for loop" src="/blog-images/for-loop.png">
 
Since a string is a sequence of characters, the for loop iterates over each character automatically.

```python
for character in "Camila GR":
	print(character)
```

How many times will the program above print something? What will be the 5th thing it prints?

<details>
    <summary>Answer</summary>
    The code will print something 9 times.

    The 5th thing it will print is `l`
</details>
<br />

The loop variable `character` is automatically reassigned each character in the string “Camila GR”. We will refer to this type of sequence iteration as <span class="bold">iteration by item</span>. Note that it is only possible to process the characters one at a time from left to right.

