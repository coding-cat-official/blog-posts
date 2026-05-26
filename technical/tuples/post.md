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

Tuples, like lists and dictionaries, are used to store multiple values in one variable. However, unlike lists and dictionaries, they are <span class="bold">immutable</span>.

Tuples are defined using parentheses `()`. They can hold values of any type, including other tuples, lists, and dictionaries. 

```python
example_tuple = (120, 'hello', True)
```

You can access an item inside a tuple using the <span class="bold">index operator</span>, just like lists. But unlike lists, you cannot change or add items to a tuple.

```python
example_tuple = (120, 'hello', True)
print(example_tuple[0])
```

What will this code print?

<details>
    <summary>Answer</summary>
    `120`
</details>
<br />

Since tuples use numbered indexes, like lists, and not key-value pairs, like dictionaries, they <span class="bold">allow duplicates</span>. You can have multiples of the same value within a tuple.

```python
example_tuple = (120, 'hello', True, 120)
```

The length of a tuple can be calculated using the `len()` function, just like strings, lists, and dictionaries. It will return the total number of elements, and duplicates are counted as separate elements.

```python
example_tuple = (120, 'hello', True, 120)
print(len(example_tuple))
```

What will this code print?

<details>
    <summary>Answer</summary>
    `4`
</details>
<br />

### Quiz