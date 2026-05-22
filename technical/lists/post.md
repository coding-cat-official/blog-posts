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

So far we have seen built-in types like: `int`, `float`, `bool`, and `str`. The first 3 of these (`int`, `float`, `bool`) are considered to be simple, or primitive data types. Their values are not composed of any smaller parts. Strings can be decomposed into smaller parts (characters), so they’re not primitive. They’re a <span class="bold">collection data type<span class="bold">.

<span class="bold">Lists</span> are another kind of collection data type that are made up of smaller pieces. They’re exactly what their name implies: a list of 0 or more items. For example:

```python
programming_languages = ['Python', 'Java', 'C#', 'Rust']
```

This code assigns a list with <span class="bold">4 elements</span> to the variable `programming_languages`. The square brackets mean that we’re creating a list, and each new element needs to be separated by commas.

All <span class="bold">strings</span> are made up of 0 or more smaller strings each containing one character. So the string `'Python'` is made up of the 6 character strings `'P' 'y' 't' 'h' 'o' 'n'`.

Types that are comprised of smaller pieces are called <span class="bold">collection data types</span>. Depending on what we are doing, we may want to treat a collection data type as a single entity (the whole), or we may want to access its parts.

Both lists and strings can be defined as sequential collections. This means that the individual elements/characters that make up the list/string are assumed to be in a particular order; the order that they appear in the list, from left to right in the string

### Indexing

To select an item in an array or string at a specific position, we use a thing called <span class="bold">indexing</span>. In Python, to index we need to write the variable name, followed by a square bracket `[`, then the number of the element we want to obtain, then the closing square bracket `]`. 

The elements of a list or string are indexed left-to-right, beginning with a 0. So, if we want to get the 1st character of a string, we have to look at the contents of index 0. For example, in the string shown below, the 14 characters are indexed left to right from position 0 to position 13:

<img class="diagram" alt="The string 'Dawson College' with its indexes listed out" src="/blog-images/lists.png">

It is also the case that the positions are named from right to left using negative numbers where -1 is the rightmost index and so on.

Let’s say we want to get the character `'n'` from the string `"Dawson College"`. If we start counting from 0, left to right, it ends up having an index of 5. We can also count from -1, right to left, thus getting another index for it, `-9`.

If we want to print the results, we would do it like that:

```python
school = "Dawson College"
print(school[5])
print(school[-9])
```

What do you think the code above prints?


<details>
    <summary>Answer</summary>
    `n`

    `n`
</details>
<br />

The same principle of indexing can be applied to lists. We’ve seen that lists can be used to store, well, lists of information. Let’s try indexing through the following list:

```python
students = [ 'Karl', 'Camila', 'Bianca', 'Normand', 'Nigel']
print(students[2])
print(students[-1])
```

What does that code print?

<details>
    <summary>Answer</summary>
    `Camila`

    `Nigel`
</details>
<br />

### List operations

Just like strings, lists cannot be subjected to mathematical operations. They cannot be subtracted `-`, divided `/`, nor multiplied `*` or added `*` to numbers.

However, just like strings, lists can be <span class="bold">concatenated</span>. This means we can add two lists to one another using the `+` operator:

```python
list_1 = [1, 2, 3]
list_2 = [4, 5, 6]
print(list_1 + list_2)
```

What do you think is the output of the above?

<details>
    <summary>Answer</summary>
    `[1, 2, 3, 4, 5, 6 ]`
</details>
<br />

Lists can also be <span class="bold">multiplied</span> with the `*` operator. Multiplication of a list will simply duplicate its items.

```python
list_1 = [1, 2, 3]
list_2 = [4, 5, 6]
print(list_1 * 2)
print(2 * list_2)
```

What do you think is the output of the above?

<details>
    <summary>Answer</summary>
    `[1, 2, 3, 1, 2, 3]`

    `[4, 5, 6, 4, 5, 6]`
</details>
<br />

### Conclusion

Both lists and strings are <span class="bold">collection data types</span>, meaning they are made up of many smaller pieces of data. These smaller pieces can be accessed based on their position in the data, or their <span class="bold">index</span>, using square brackets.

Lists have lots of built-in methods, just like strings do. 
