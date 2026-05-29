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

### Equality Operators

As we’ve seen [previously](/#/blogs/types), <span class="bold">booleans</span> are a kind of data type that can be either True or False, like an on/off switch. There are many ways to manipulate booleans in Python.

Sometimes, we need to transform other variable types into booleans. Let’s say we want to check whether a product’s price is equal to 100$ or not. This is a statement that can be either True or False.

```py
price = 105
print(price == 100)
```

What do you think the code above prints?

<div>
<details>
    <summary>Answer</summary>
    `False`
</details>
<br />
</div>

Here, we’re using an <span class="bold">equality operator</span> to check whether the variable `price` is equal to 100. Notice that, unlike in mathematics, we’re using two equal signs (`==`) instead of one. This is to avoid conflicts with the assignment statement, which already uses one equal sign. [Here's the article if you need a refresher](/#/blogs/statements_expressions)

Python also has the <span class="bold">inequality operator</span> (`!=`). It does the opposite of the equality operator. If the operands on either side of it are equal, it evaluates to False, and if they’re <span class="bold">not equal</span>, it evaluates to True. Suppose we want to make sure that the price of a product is anything other than 100$:

```py
price = 105
print(price != 100)
```

What do you think the above statement prints? 

<div>
<details>
    <summary>Answer</summary>
    `True`
</details>
<br />
</div>

It evaluates to True because both sides are <span class="bold">not equal</span>. This is why we call it an inequality operator.

Let’s look into more complex scenarios. We want to check whether the product’s price is over 100$:

```py
price=105
print(price>100)
```

What do you think the code above prints? 

<div>
<details>
    <summary>Answer</summary>
    `True`
</details>
<br />
</div>

Here, we’re using a <span class="bold">comparison operator</span> to check whether the variable `price` is above 100. The inequality and equality operators also belong to the category of comparison operators. There are a few more comparison operators that can be used, like `<` (lesser than), `>` (greater than), `<=` (lesser than or equal to), and `>=` (greater than or equal to). These can be used to compare numbers:

```py
print(45 >= 50)  -> False
print(-10<=20)  -> True
print(0<38)  -> True
print(9>19)  -> False
```

In Python, comparison operators can also be used to compare strings. We can check whether two strings are equal or not:

```py
message = "hello"
print(message == "Hello")
print(message != "hi there")
```

What do you think the above code prints?

<div>
<details>
    <summary>Answer</summary>
    `False`
    
    `True`
</details>
<br />
</div>

Be careful, because the capitalization of the string matters! "Hello" and "hello" are considered two different strings.

We can also use other comparison operators to compare strings in alphabetical order:

```
print("aaa" < "bbb")
```

The above statement will print `True`, because alphabetically, `"aaa"` is inferior to `"bbb"` in the alphabetical order (it comes first).

### Logical Operators

There is another category of operators in Python. <span class="bold">Logical operators</span> are used when working with multiple boolean values. Suppose we want to ensure that a product’s price is below 100 <span class="bold">and</span> above 0:

```python
price = 95
print(price > 0 and price < 100)
```

What do you think is the output of the above code?

<div>
<details>
    <summary>Answer</summary>
    `True`
</details>
<br />
</div>

The `and` logical operator will only return `True` if the expressions on both sides evaluate to True. We use it when we want to make sure that multiple things are true at once.

| Expression          | Result |
|---------------------|--------|
| **True and True**   | True   |
| **True and False**  | False  |
| **False and True**  | False  |
| **False and False** | False  |

What if we only need one of two things to be True? For example, let’s say the price can be either under 100 <span class="bold">or</span> over 1000:

```
price = 24
print(price < 100 or price > 1000)
```

What do you think that code prints? 

<div>
<details>
    <summary>Answer</summary>
    `True`
</details>
<br />
</div>

The `or` logical operator will return `True` as long as at least one side of the statement evaluates to True. In the example above, the price is under 100. Even though it’s not over 1000, the use of the `or` operator makes sure that only one of the two conditions needs to be satisfied.

| Expression         | Result |
|--------------------|--------|
| **True or True**   | True   |
| **True or False**  | True   |
| **False or True**  | True   |
| **False or False** | False  |

Lastly, what if we want to "flip" whether a statement is True? Let’s take a look at this example, where the goal is to find out whether a product is expensive or <span class="bold">not</span>:

```python
product_cheap = True
print(not product_cheap)
```

What do you think that code prints?

<div>
<details>
    <summary>Answer</summary>
    `False`
</details>
<br />
</div>

The `not` logical operator flips the boolean to the other state. The expression `not True` evaluates to `False`, and the expression `not False` evaluates to `True`.

| Original variable | Result |
|-------------------|--------|
| True              | False  |
| False             | True   |

Let’s try combining the logical operators together. Remember PEMDAS, and that the expressions are evaluated left-to-right.

```python
price = 45
is_good_quality = True
print(price > 39 and is_good_quality)
print(price < 39 or is_good_quality)
print(not is_good_quality)
```

What does this code print, one line at a time?

<div>
<details>
    <summary>Answer</summary>
    `True`

    `True`
    
    `False`
</details>
<br />
</div>

### Parentheses

When mixing and and or, use parentheses to make your intent clear. In the order or operations, and comes before or.

Example:

```py
a = True
b = True
c = False

print(a or b and c)
```

The expression is evaluated thusly:

```py
True or True and False
True or (True and False)  
# 'and' evaluated first, so it's as if there were parentheses there
True or False
True
```

Let's try having the same expression but with parentheses:

```py
a = True
b = True
c = False
print((a or b) and c)
```

This expression is evaluated differently:

```py
(True or True) and False  # parentheses first
True and False
False  # different result!
```

