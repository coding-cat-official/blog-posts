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

There are many more things to learn about lists and strings. This article is a starting point for that.

### List methods

Remember the <span class="bold">dot operator</span> from the article about strings? Lists also have lots of built-in functions.

The first of these is the `append` function. It adds the provided argument to the end of the list it is used on. It can be used like this:

```python
new_list = []
new_list.append(32)
new_list.append(19)
new_list.append(6)
```

This new list is now `[32, 19, 6]`. Here’s a useful list of other Python list methods:

| Method  | Parameters     | Result         | Description                                      |
|---------|----------------|----------------|--------------------------------------------------|
| append  | item           | mutator        | Adds a new item to the end of a list             |
| insert  | position, item | mutator        | Inserts a new item at the position given         |
| pop     | none           | hybrid         | Removes and returns the last item                |
| pop     | position       | hybrid         | Removes and returns the item at position         |
| sort    | none           | mutator        | Modifies a list to be sorted                     |
| reverse | none           | mutator        | Modifies a list to be in reverse order           |
| index   | item           | return idx     | Returns the position of first occurrence of item |
| count   | item           | return count   | Returns the number of occurrences of item        |
| remove  | item           | mutator        | Removes the first occurrence of item             |

Watch out! All methods that return `None` change the array they’re used on. The original array will be replaced by the new array.

### List Slices

The <span class="bold">slice operation</span> allows us to take an existing array and create a new one that only includes part of the original array. 

Remember that the first index is the starting point for the slice, and the second number is one index past the end of the slice (up to but not including that element). Recall also that if you omit the first index (before the colon), the slice starts at the beginning of the sequence. If you omit the second index, the slice goes to the end of the sequence.

```python
a_list = ['a', 'b', 'c', 'd', 'e', 'f']
print(a_list[1:3])
print(a_list[:4])
print(a_list[3:])
print(a_list[:])
```

Result:
```py
['b', 'c']
['a', 'b', 'c', 'd']
['d', 'e', 'f']
['a', 'b', 'c', 'd', 'e', 'f']
```

The same thing can be done for strings.

### Strings are Immutable

One important thing that makes strings different from some other Python collection types is that you are <span class="bold">not allowed to modify the individual characters</span> in the collection. It is tempting to use the `[]` operator on the left side of an assignment, with the intention of changing a character in a string. For example, in the following code, we would like to change the first letter of `greeting`.

```python
greeting = "Hello, world!"
greeting[0] = 'J'
print(greeting)
```

Instead of producing the output `Jello, world!`, this code produces the runtime error `TypeError: 'str' object does not support item assignment`. 

<div class="highlight">
Strings are immutable, which means you cannot change an existing string. The best you can do is create a new string that is a variation on the original.
</div>

The solution here is to concatenate a new first letter onto a slice of `greeting`. This operation has no effect on the original string.

### Lists are Mutable

Unlike strings, lists are <span class="bold">mutable</span>. This means we can change an item in a list by accessing it directly as part of the assignment statement. Using the indexing operator (square brackets) on the left side of an assignment, we can update one of the list items.

```python
weather = ['rainy', 'sunny', 'cloudy', 'stormy']
weather[0] = "misty"
weather[-1] = "hot"
print(weather)
```

What do you think gets printed by the code above?

<details>
    <summary>Answer</summary>
    `misty`

    `sunny`

    `cloudy`
    
    `hot`
</details>
<br />

An assignment to an element of a list is called <span class="bold">item assignment</span>. Item assignment does not work for strings. Recall that strings are immutable.

By combining assignment with the slice operator we can update several elements at once.

```python
alist = ['a', 'b', 'c', 'd', 'e', 'f']
alist[1:3] = ['x', 'y']
print(alist)
```

We can also remove elements from a list by assigning the empty list to them.

```python
alist = ['a', 'b', 'c', 'd', 'e', 'f']
alist[1:3] = []
print(alist)
```

We can even insert elements into a list by squeezing them into an empty slice at the desired location.

```python
alist = ['a', 'd', 'f']
alist[1:1] = ['b', 'c']
print(alist)
```

### A Few String Methods

Two of the most useful methods on strings involve lists of strings. The `split` method breaks a string into a list of words. By default, any number of whitespace characters is considered a word boundary.

```python
message = “Greetings to employees of Meerkat”
words = message.split()
```

What do you think `words` contains?

<details>
    <summary>Answer</summary>
    `['Greetings', 'to', 'employees', 'of', 'Meerkat']`
</details>
<br />

An optional argument called a <span class="bold">delimiter</span> can be used to specify which characters to use as word boundaries. The following example uses the string `ee` as the delimiter:

```python
message = “Greetings to employees of Meerkat”
words = message.split("ee")
```

What do you think `words` contains?

<details>
    <summary>Answer</summary>
    `['Gr', 'tings to employ', 's of M', 'rkat']`
</details>
<br />

<div class="highlight">
Notice that the delimiter doesn’t appear in the result.
</div>

The inverse of the `split` method is `join`. You choose a desired <span class="bold">separator</span> string, (often called the <span class="bold">glue</span>) and join the list with the glue between each of the elements.

```python
words = ["one", "two", "three"]
glue = ';'
result = glue.join(words)
```

What does `result` contain?

<details>
    <summary>Answer</summary>
    `one;two;three`
</details>
<br />

The list that you glue together (`words` in this example) is not modified. Also, you can use empty glue or multi-character strings as glue.

### In and Not In Operators

The `in` operator tests if one string is a substring of another, or if an element is a member of a list.

```python
print('r' in 'ray of light')
print('x' in 'ray of light')
print('ay' in 'ray of light')
print('ya' in 'ray of light')
```

What do you think the code above prints?

<details>
    <summary>Answer</summary>
    `True`

    `False`

    `True`

    `False`
</details>
<br />

```python
weather = ['rainy', 'sunny', 'cloudy', 'stormy']
print('rainy' in weather)
print('misty' in weather)
```

What do you think the code above prints?

<details>
    <summary>Answer</summary>
    `True`

    `False`
</details>
<br />

The `not in` operator returns the logical opposite result of `in`.

```python
print('x' not in 'ray of light')
```

What do you think the code above prints?

<details>
    <summary>Answer</summary>
    `True`
</details>
<br />

### QUiz