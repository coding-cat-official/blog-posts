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

Strings are different from integer and float values because they are made up of smaller pieces. Strings are made up of smaller strings each containing <span class="bold">one character</span>.

Types that are comprised of smaller pieces are called <span class="bold">collection data types</span>. Depending on what we are doing, we may want to treat a collection data type as a single entity (the whole), or we may want to access its parts. This ambiguity is useful.

Strings can be defined as sequential collections of characters. This means that the individual characters that make up the string are assumed to be in a particular order from left to right.

A string that contains no characters, often referred to as the <span class="bold">empty string</span>, is still considered to be a string. It is simply a sequence of zero characters and is represented by '' or "" (two single or two double quotes with nothing in between).

### Operations on Strings

In general, you cannot perform mathematical operations on strings, even if the strings look like numbers.

However, there are two exceptions.

First, the `+` operator does work with strings, but the `+` operator represents <span class="bold">concatenation</span> or joining, not numerical addition. For example:

```py
fruit = "banana"
bakedGood = " nut bread"
print(fruit + bakedGood)
```

What do you think this code will print?

<details>
    <summary>Answer</summary>
    `banana nut bread`
</details>
<br />

Thus, the `+` operator will join two strings together without adding anything else to them.

The `*` operator also works on integers with strings. It performs repetition. For example, `'Fun'*3` is `'FunFunFun'`. One of the operands has to be a string and the other has to be an integer.

Note also that the order of operations for `*` and `+` is the same as it was for arithmetic. The repetition is done before the concatenation. If you want to cause the concatenation to be done first, you will need to use parenthesis. Also note that the `*` is <span class="bold">commutative</span> (i.e. `a*b == b*a`), but `+` is <span class="bold">not commutative</span> as the order makes a difference in the joining.

If we want to find out the length of a string (including all characters, even whitespaces), we can use the `len()` function. The string goes inside the parentheses.

`print(len("Hello"))`

Just like PEMDAS in mathematics, we start by evaluating the innermost expression in the parentheses. The length of `"Hello"` is 5 characters. Then, the number `5` gets printed.

### String Methods

Some Python objects can do certain things with built-in functions. We’ve already seen a few functions, like `len()` or `print()`, but those built-in functions are different. They’re called methods, and can be accessed using the "dot notation".

For example, we have methods to turn strings into uppercase or lowercase:

```py
name = "JohnathAn"
print(name.upper())
print(name.lower())
print(name)
```

The result of the first print statement will be `"JOHNATHAN"`, while the second one will give us `"johnathan"`.

Note that these methods do not change the original content of the string. They simply create a new string that’s either all uppercase or all lowercase. The last print statement will still give us the unchanged, original string (`"JohnathAn"`).

Here’s a small list with some string methods you may find useful:

| Method     | Parameters | Description                                                       |
|------------|------------|-------------------------------------------------------------------|
| upper      | none       | Returns a string in all uppercase                                 |
| lower      | none       | Returns a string in all lowercase                                 |
| capitalize | none       | Returns a string with first character capitalized, the rest lower |
| strip      | none       | Returns a string with the leading and trailing whitespace removed |
| lstrip     | none       | Returns a string with the leading whitespace removed              |
| rstrip     | none       | Returns a string with the trailing whitespace removed             |
| count      | item       | Returns the number of occurrences of item                         |
| replace    | old, new   | Replaces all occurrences of old substring with new                |

### Formatted Strings

String concatenation is useful, but it can sometimes lead to lengthy syntax. When we want to create strings out of existing variables, we use string formatting. 

When creating formatted strings, we need to put an `f` in front of the string so Python understands we’re dealing with a Formatted string. Then, to include variables in the string, we can put them between curly braces `{}` inside the string. For example:

```python
grade_midterm = 85
grade_final = 81
print(f'Your grades are {grade_midterm} and {grade_final}'`)
```

This is much more readable than if we used regular string concatenation (with the `+` symbol):

```python
grade_midterm = 85
grade_final = 81
print('Your grades are ' + grade_midterm + ' and ' + grade_final)
```
