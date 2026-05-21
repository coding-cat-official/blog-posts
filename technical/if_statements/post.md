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
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", by Jaya Nikalantan and Bennett Axtell
</small>

Now that we understand how to use booleans, we can control our code better. In almost all scenarios, we need the ability to check something to control what our code does. This can be done using <span class="bold">if statements</span>.

Let’s use the real-world example of a website where you can register to vote. We only want people aged 18 years or older to be able to access it. Other people shouldn’t be able to see it.

```py
age = 31
if age >= 18:
	print("You can access the website")
else:
	print("You cannot access the website")
```

What do you think this code prints?

<details>
    <summary>Answer</summary>
    `You can access the website`
</details>
<br />

An `if` statement checks whether the condition is true before moving onto the next block of code it should execute. Its syntax goes as follows:

```py
if BOOLEAN_EXPRESSION:
	CODE_BLOCK_1
	#only executed if the boolean expression evaluates to True
else:
	CODE_BLOCK _2	
	# only executed if the boolean expression evaluates to False
```

The code gets executed as follows:
 
Let’s look again at the first example, with the voting booth.

We know that the age is over 18, so the `if` statement evaluates to True. That means the code goes to line 3, where it prints "You can access the website". The code on line 5 never gets executed – it can only be accessed when the `if` statement evaluates to False.

### Indentation

Indentation in Python is very important. You may have noticed that the lines of code following an `if` statement are all <span class="bold">indented one level further than the previous line</span>. In Python, `if` you want a line of code to belong to a block of code, they must have the same level of indentation.

```py
age = 43
job = "programmer"
if age >= 18:
	print("You are over 18.")
	if job == "programmer":
		print("Your job seems fun!")
	else:
		print("You're not a programmer")
else:
	print("You are not over 18.")
```

Lots of things are happening here! Let’s break this down with a chart.

<img class="diagram" alt="Nested if statements" src="/blog-images/if-statements/nested-ifs.png">
 
Knowing the flow of execution, what do you think gets printed by that piece of code?

<details>
    <summary>Answer</summary>
    `You are over 18`
    
    `Your job seems fun!`
</details>
<br />

In the piece of code above, all lines between 3 and 7 are indented one level further. This means that they all belong to the block of code that <span class="bold">only</span> gets executed when the `if` statement is true. 

When an `if` statement is written inside another `if` statement, it’s called a <span class="bold">nested `if` statement</span>. You can have as many nested `if` statements as you want, but it’s recommended to keep it under 3 or 4 to make your code more readable for other programmers. Each `if` statement can also have as many statements as you want in their block of code.

Python also accepts `if` statements <span class="bold">without an `else` clause<span class="bold">. Here’s an example:

```py
price = 25
if price > 100:
	print("The price is too expensive.")
print("Program over.")
```

What do you think the above code prints?

<details>
    <summary>Answer</summary>
    `Program over`
</details>
<br />

Since the condition is not met for the `if` statement, the block of code inside it doesn’t get executed. We jump straight to line 4, which is the first thing outside of that block of code. Here’s a diagram to demonstrate that:

<img class="diagram" alt="Simple if statement" src="/blog-images/if-statements/simple-if.png">
 
### Chaining if/else Statements

You can chain `if` statements together to make branching paths using `elif`. `elif` statements combine `else` and `if` statements. They <span class="bold">only</span> run when the `if` statement above them evaluates to false, and their own condition evaluates to true.

Here's the syntax for `elif` statements:

```py
if CONDITION_1:
    BLOCK_OF_CODE_1
elif CONDITION_2:
    BLOCK_OF_CODE_2
else:
    BLOCK_OF_CODE_3
REST_OF_CODE
```

And here's a diagram explaining the flow of the chained elif statements:

<img class="diagram" alt="branching elif statements" src="/blog-images/if-statements/branching-elif.png">