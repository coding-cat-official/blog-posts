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

A <span class="bold">statement</span> is an instruction in Python that DOES something. One example covered in a <a href="/#blogs/variables">previous article</a> is assignment statements, where a variable gets assigned a value. Another example is a print statement, which means that the print function gets called.

An <span class="bold">expression</span> is a combination of values, variables, operators, and calls to functions. Expressions need to be evaluated. It's a line of code that can be simplified by Python.

In the examples below, Python first evaluates the expressions, then displays the result in the `print` statement.

```python
print(1+1)
print(0 < 10)
```

The <span class="bold">evaluation of an expression</span> produces a value, which is why expressions can appear on the right-hand-side of assignment statements. A value by itself is a simple expression, and so is a variable. Evaluating a variable gives the value that the variable refers to.

<span class="bold">Operators</span> are special tokens that represent computations like addition, multiplication and division. The values the operator works on are called <span class="bold">operands</span>.

When a variable is encountered in place of an operand, Python replaces the variable with the value it represents, and then performs the calculation.

### Operator precedence

Here's a complete list of the order in which operators are evaluated in Python (kind of like PEMDAS in maths!). You may not know the meaning of all the terms yet; for now, just take care of the operators you do know.

<div class="highlight">
Note: Evaluation begins with the top row and progresses downwards. Operators on the same line are evaluated left-to-right if there aren't any parentheses. Parentheses are the topmost operation, they're always the top priority.
</div>

|                                 Operator                                |                               Description                               |
|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
|  (expressions...),\[expressions...\], {key: value...}, {expressions...}  | Binding or tuple display, list display, dictionary display, set display |
|  x\[index], x\[index:index\], x(arguments...), x.attribute                 | Subscription, slicing, call, attribute reference                        |
| **                                                                      | Exponentiation (groups right to left)                                   |
| -x                                                                      | Negation                                                                |
|  *, /, //, %                                                            | Multiplication, real and integer division, remainder                    |
|  +, -                                                                   | Addition and subtraction                                                |
|  in, not in, is, is not, <, <=, >, >=, !=, ==                           | Comparisons, including membership tests and identity tests              |
| not x                                                                   | Boolean NOT                                                             |
| and                                                                     | Boolean AND                                                             |
| or                                                                      | Boolean OR                                                              |

### Math Operators & Operands

<a href="/#/blogs/math_operators">Click here for more details on math operators and operands.</a>

### Logic & Comparison Operators

<a href="/#/blogs/logic_comparison">Click here for more details on boolean operators and operands.</a>

### String Operations

<a href="/#/blogs/string_operations">Click here for more details on string operators and operands.</a>

### Quiz