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
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", by Jaya Nikalantan and Bennett Axtell
</small>

In Python, a <span class="bold">function</span> is a named sequence of statements that belong together and does something. One purpose is to help us organize programs into chunks that match how we think about the solution to the problem. We’ve used a bunch of functions already (e.g., print).

Another important purpose of functions is to group code that <span class="bold">performs a single task</span> together so that we can easily reuse in more than one place.

The syntax to define a new function in Python is:

```python
def function_name():
```

Don’t forget the colon!

Any statements after the definition of a function need to be <span class="bold">indented</span> so that Python can understand that they belong to that function. For example:

```python
def new_function():
	# do something
```

<small>
Note: If you want to write notes for yourself in the code, you can add comments with `#` as above. Lines starting with `#` will be ignored by Python and won’t affect the execution of the code.
</small>

You can think of the keyword `def` as short for "definition". After all, what we’re doing is defining a function.

### Parameters

Functions can also take in <span class="bold">parameters</span>, or inputs. This means that the parameters we define can be used from inside that function. Any parameters in a function have to be enclosed within the parentheses, `()`, following the function definition. If there is more than one parameter, they must be separated by commas, like a list.

```python
def add_numbers(number_1, number_2):
	# do something
```

How many parameters does the function `add_numbers` have? What are their names?

<details>
    <summary>Answer</summary>
    2 parameters: `number_1` and `number_2`
</details>
<br />

<div class="highlight">
Watch out! Defining a function doesn’t mean it gets run by the code. To actually find out how to use a function, read further.
</div>

### Calling functions

What use would be a function if you can’t use it elsewhere in the code? <span class="bold">Functions can be called</span> from other places in the code that have the same indentation level as the function definition.

Let’s first call a built-in Python function called `abs()`. It transforms any number given to it into its absolute (it makes the number positive).

```python
absolute_number = abs(-26)
```

You can <span class="bold">call a function</span> by writing its name, then an open parenthesis, `(`, then the parameters (separated by commas), then the closing parenthesis, `)`. If the function takes in no parameters, you can just leave the space between the parentheses empty.

Suppose we have a custom function that adds two numbers, and we need to call it (or use it) in another part of our code.

```python
def add_numbers(number_1, number_2):
	# some code here
add_numbers(1, 5)
```

It works the same way as built-in functions. You just put the name, the parentheses, and the parameters in the right order.

Unlike variables, functions can be defined <span class="bold">anywhere</span> in the code. You can call them on a line before their definition, as long as eventually there exists a function with that name and those parameters.

<div class="highlight">
Watch out! In CodingCat, your functions get run automatically to test them. You don't actually need to call them (unlike when you're building your own Python program).
</div>

### Returning a value

Anything that a function does only affects what’s happening within the function itself. This means that if we create a variable in our function, when the function is done running, that variable is erased forever. We know how to communicate information from the outside of the function to the inside (using parameters), but how do we transmit some information back to the outside?

For this, we can use <span class="bold">return statements</span>. Whenever a return statement is encountered in a function, the function is stopped immediately. The value after the return statement gets given back to the code that called the function.

This is done by writing <span class="bold">the keyword</span> `return`, followed by a value, a variable, or an expression. The value, the content of the variable, or the return of the expression will be given back to the code that called the function.

Let’s take another look at our custom function:

```python
def add_numbers(number_1, number_2):
	return number_1 + number_2
```
Now, every time we call this function, it will give us back the sum of its parameters. Calling the function works will still be done in the way explained earlier. 

We can also <span class="bold">save the result</span> of a function call into a variable:

```python
def add_numbers(number_1, number_2):
	return number_1 + number_2
total = add_numbers(5, 24)
```
What do you think the variable `total` now contains?

<details>
    <summary>Answer</summary>
    `29`
</details>
<br />
