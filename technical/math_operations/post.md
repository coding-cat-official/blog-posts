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
    img.diagram {
        max-width: 90%;
        margin: 1rem 2rem;
        max-height: 30rem;
    }
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", by Jaya Nikalantan and Bennett Axtell
</small>

### Math Operators & Operands 

As we’ve seen previously, <span class="bold">operators<span class="bold"> are special tokens that represent computational operations. Python has many operators that it borrowed from maths, which you may already be familiar with. 

The following are all legal Python expressions whose meaning is more or less as you expect: 

```
20 + 32 
hour - 1 
hour * 60 + minute 
minute / 60 
5 ** 2 
(5 + 9) * (15 - 7)
``` 

The tokens `+`, `-`, `*`and `/`, and the use of parenthesis for grouping, mean in Python what they mean in mathematics. The asterisk (`*`) is the token for multiplication, `/` for normal division, and `**` is the token for exponentiation. Addition, subtraction, multiplication, and exponentiation all do what you expect. 

Division (`/`) is always converted to a floating point number after the operation is done. 

```python
minutes = 645 
hours = minutes / 60 
print(hours)
``` 

What do you think this code will print?

<details>
    <summary>Answer</summary>
    `10.75`
</details>
<br />

<span class="bold">Integer division</span> is just like normal division, but the result is always an integer. It uses the token `//`. It always truncates the result down to the next smallest integer. 

```python
print(7 / 4) 
print(7 // 4) 
minutes = 645 
hours = minutes // 60 
print(hours)
print(6//4) 
print(-6//4)
``` 

The <span class="bold">modulus operator</span>, sometimes also called the remainder operator or integer remainder operator, works on integers (and integer expressions) and yields the remainder when the first operand is divided by the second. In Python, the modulus operator is a percent sign (`%`). The syntax is the same as for other operators. Here’s a visual representation: 

<img class="diagram" alt="Explanation of the modulus operator, featuring 3 groups of 4 coins, with 1 leftover coin" src="/blog-images/modulus-operator.png">

We’re dividing 13 into groups of 4. But since 13 is not divisible by 4, we have a remainder of 1. Thus, `13%4=1`. 

### Order of Operations  

When more than one operator appears in an expression, the order of evaluation depends on the rules of precedence. Python follows the same precedence rules for its mathematical operators that mathematics does. 

1. Parentheses have the highest precedence and can be used to force an expression to evaluate in the order you want. Since expressions in parentheses are evaluated first, 2 \* (3-1) is 4, and (1+1)\*\*(5-2) is 8. You can also use parentheses to make an expression easier to read, as in (minute \* 100) / 60, even though it doesn’t change the result. 

2. Exponentiation has the next highest precedence, so 2\*\*1+1 is 3 and not 4, and 3\*1\*\*3 is 3 and not 27. Can you explain why? 

3. Multiplication and both division operators have the same precedence, which is higher than addition and subtraction, which also have the same precedence. So 2\*3-1 yields 5 rather than 4, and 5-2\*2 is 1, not 6. 

4. Operators with the same precedence (except for `**`) are evaluated from left-to-right. In algebra we say they are left-associative. So in the expression 6-3+2, the subtraction happens first, yielding 3. We then add 2 to get the result 5. If the operations had been evaluated from right to left, the result would have been 6-(3+2), which is 1. 

Note: An exception to the left-to-right left-associative rule is the exponentiation operator `**`. A useful hint is to always use parentheses to force exactly the order you want when exponentiation is involved: 

```python
print((2**3)**5)
print(2**(3**5))
```

What do you think this code will print?

<details>
    <summary>Answer</summary>
    `32768`
    
    `14134776518227074636666380005943348126619871175004951664972849610340958208`
</details>
<br />