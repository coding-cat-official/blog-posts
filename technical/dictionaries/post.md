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

We’ve seen lists already, which allow us to store multiple pieces of data under one variable. 

Let’s say we work for a car company, and we want to keep track of information related to a car. With our current knowledge, we have two ways to do that. We can store the information in a list:

```python
car_info = ['Hyundai', 'Sonata', 2011, 2015, 'blue']
```

Or we can store it as a series of variables:

```python
car_brand = "Hyundai"
car_model = "Sonata"
car_year_released = 2011
car_year_bought = 2015
car_color = "blue"
...
```

But both approaches are flawed. In the list, we may forget which value represents what, especially if we have values that are similar (like `car_year_released` and `car_year_bought`). For the approach using variables, if we have multiple cars, we can quickly confuse which variable belongs to which car.

This is where the Python <span class="bold">dictionary</span> comes into play. It allows us to mix both approaches, creating a list which has “labels” assigned to each value in the list. Those labels are called <span class="bold">keys</span>. 

```python
car_info = {
    'brand': 'Hyundai', 
    'model': 'Sonata', 
    'year_released': 2011, 
    'year_bought': 2015, 
    'color': 'blue'
}
```

Each item in the dictionary is called a <span class="bold">key-value pair</span>. The key is the label of the item, like `color`, and the value is the value held inside the item, like `'blue'`.

Notice how the dictionary uses <span class="bold">curly braces</span> `{}` instead of square brackets like arrays do. This is important to remember, otherwise Python won’t understand what you’re trying to do.

A dictionary is ordered, mutable, and doesn’t allow duplicates. You cannot have two keys that are the same, otherwise Python won’t run your code.

To get the amount of items in a dictionary, you can use the `len()` method, similarly to strings:

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
print(len(today))
```

What will the code above print?

<details>
    <summary>Answer</summary>
    `2`
</details>
<br />

### Getting an element from a dictionary

To fetch an item from a dictionary, we can use the <span class="bold">index operator</span>, just like in arrays. However, we need to put the <span class="bold">key</span> in the brackets instead of the index number.

```python
car_info = {
    'brand': 'Hyundai', 
    'model': 'Sonata', 
    'year_released': 2011, 
    'year_bought': 2015, 
    'color': 'blue'
}
print(car_info['year_bought'])
```

What do you think the code snippet above prints?

<details>
    <summary>Answer</summary>
    `2015`
</details>
<br />

A key must be a <span class="bold">string</span>. It can contain any characters, as long as it is enclosed in quotation marks and is not empty.

A value can be anything you want. It can even be a list or another dictionary!

If you enter an invalid key in the index (meaning a key that doesn’t exist in the dictionary), the program will throw an error and crash. To avoid things like that, you can also use the `get()` method to obtain items from a dictionary:

```python
car_info = {
    'brand': 'Hyundai', 
    'model': 'Sonata', 
    'year_released': 2011, 
    'year_bought': 2015, 
    'color': 'blue'
}
print(car_info.get('model'))
```

What will the code above print?

<details>
    <summary>Answer</summary>
    `Sonata`
</details>
<br />

With this method, if you enter an invalid key, the value returned will be `None`.

### Changing and adding items

If you want to <span class="bold">change the value</span> associated to a key, it works the same way as in lists. You simply have to assign a new value to the dictionary’s key using the assignment operator:

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
today['weather'] = 'windy'
```

<div class="highlight">
    Watch out! You can’t do this using the `get()` method, because this method only <span class="special-bold">retrieves</span> the value, and it cannot change it.
</div>

If a key doesn’t exist yet, updating it using the indexing operator will create that key.

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
today['season'] = 'summer'
```
How many keys does the `today` dictionary have after this code is run?

<details>
    <summary>Answer</summary>
    `3`
</details>
<br />

You can also update and create keys using the `update()` method. The first parameter is the name of the key, and the second parameter is the new value.

```python
today = {
	'weather': 'sunny',
	'day': 'Tuesday'
}
today.update('weather', 'windy')
```
How many keys does the `today` dictionary now have?

<details>
    <summary>Answer</summary>
    `2`
</details>
<br />

