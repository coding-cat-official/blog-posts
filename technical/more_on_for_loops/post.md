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

Recall that the `range` function creates a sequence of integers. When you pass it a single whole number parameter, it creates a sequence of integers starting from 0 up to but not including the parameter. This sequence is similar to a list, but not exactly the same.

It is possible to use the `range` function to generate the <span class="bold">indices</span> of the elements of a list or string. The `for` loop can then be used to iterate over these positions. These positions can be used together with the indexing operator to access the individual characters in the string. 

<div class="highlight">
Note that iterating with the for-loop-by-item pattern discussed in the previous section is usually preferable! 
</div>

Consider the following example.

```python
word = "light"
for i in range(5):
    currentChar = word[i]
    print(currentChar)
```

The index positions in “light” are 0,1,2,3 and 4. This is exactly the same sequence of integers returned by `range(5)`. The first time through the for loop, `i` will be 0 and the “l” will be printed. Then, `i` will be reassigned to 1 and “g” will be displayed. This will repeat for all the range values up to but not including 5. Since “t” has index 4, this will be exactly right to show all of the characters.

In order to make the iteration more general, we can use the `len` function to provide the <span class="bold">bound</span> for `range`. This function returns the length, or number of elements, of a string or list. This is a very common pattern for traversing any sequence by position. Make sure you understand why the range function behaves correctly when using `len` of the string as its parameter value.

```python
word = "light"
length = len(word)
for i in range(length):
    currentChar = word[i]
    print(currentChar)
```

What will this code print?

<details>
    <summary>Answer</summary>
    `l`

    `i`

    `g`
    
    `h`
    
    `t`
</details>
<br />

You may also note that iteration by position allows the programmer to control the direction of the traversal by changing the sequence of index values. Recall that we can create ranges that count down as well as up so the following code will print the characters from right to left.

```python
word = "light"
length = len(word)
for i in range(length - 1, -1, -1):
    currentChar = word[i]
    print(currentChar)
```

### Iterating over a dictionary

Just as you can iterate over list items, you can also iterate over a dictionary using a `for` loop. However, the values that you’re iterating over are the <span class="bold">keys of the dictionary</span>, not the values associated to each key

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
for key in today:
	print(key)
```

This code will print: `weather`, `day`. If you want to access the values associated with each key, all you have to do is use the indexing operator (or the `get()` method).

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
for key in today:
	print(today[key])
```

What will this code print?

<details>
    <summary>Answer</summary>
    `sunny`

    `Tuesday`
</details>
<br />
