<style>
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
    table>tbody>tr>td {
        padding: 0 1rem;
    }
    small>a {
        color: gray;
    }
    small>a:hover {
        color: darkgrey;
    }
    summary {
        cursor: pointer;
    }
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", authored by Jaya Nikalantan and Bennett Axtell
</small>

The fundamental building block of programming is <span class="bold">values</span>, like 0.192 or “Hello”. <span class="bold">Variables</span> allow us to assign names to certain values and to keep track of them. We can use variables to refer to the same value over and over again.

<small>
    <a href="/#/blogs/types">
        Click here for a refresher on variable types
    </a>
</small>
<br/>
<br/>

<span class="bold">Assignment statements</span> create new variables and also initialize them with the values they refer to.

Example:

```python
message = "How are you?"
age=32
percent=0.2165
success=True
```

The above are all example of variable assignments. The first line assigns the string value “How are you?” to a new variable named message. The second associates the integer 32 to the variable age. The third line gives the floating-point number 0.2165 to percent, and the fourth assigns the boolean True to the variable success.

The <span class="bold">assignment operator</span>, `=`, should not be confused with equality that you see in Math, where you can move terms from the right-hand-side to the left, and vice-versa. (We will see later that testing for equality in programming is `==`). The assignment statement links a variable name, always on the left-hand-side of the operator, with a <span class="bold">value</span>, on the right-hand side. This is why you will get an error if you enter:

17 = age

We use variables in a program to “remember” things and/or give a name to a value, like the current score at the football game. But variables are <span class="bold">variable</span>. This means they can change over time, just like the score at a football game. You can assign a value to a variable, and later assign a different value, or the result of a calculation, to the same variable.

### Variable names

Variable names should be meaningful and describe the contents. Remember that they’re a way for YOU to know what’s inside them!

They can contain letters, digits, and underscores, but they have to begin with a letter or an underscore. They cannot contain spaces. You can use uppercase letters as well, but remember that casing matters. `Age` and `age` are considered two different variables.

Try to figure out if the following variables have valid names:

- <details>
    <summary>95percent</summary>
    Invalid, because it doesn’t start with a letter or an underscore
  </details>
- <details>
    <summary>student_grade</summary>
    Valid!
  </details>
- <details>
    <summary>good!_grade!</summary>
    Invalid. this variable contains characters that are not a letter, number, or underscore.
  </details>
- <details>
    <summary>student grade</summary>
    Invalid, it contains a space.
  </details>
- <details>
    <summary>grade</summary>
    Valid!
  </details>
- <details>
    <summary>int</summary>
    Invalid. this variable is a keyword reserved for Python
  </details>

Wait… what? <span class="bold">Reserved keywords</span>?

Gotcha: Python has reserved some keywords for itself, like `str` or `class`, which it highlights in blue. It won’t allow you to use those keywords. Here’s a non-exhaustive list of keywords you’re not allowed to use (don’t memorize it!):


|    |      |      |     |     |
|--------|----------|---------|----------|--------|
| False     | await     | else      | import   | pass       |
| None      | break     | except    | in       | raise      |
| True      | class     | finally   | is       | return     |
| and       | continue  | for       | lambda   | try        |
| as        | def       | from      | nonlocal | while      |
| assert    | del       | global    | not      | with       |
| async     | elif      | if        | or       | yield      |
| sum       | trunc     | str       | int      | bool       |

When you name a variable, make sure it’s meaningful to you without being too long. Which of those pairs do you think is the better name choice?:

-	`number`  OR  `final_grade`
-	`teacher_name`  OR  `name`
-	`average_weight`  OR  `avg_w`
-	`score_of_the_best_football_player_in_the_league`  OR  `best_player_score`

<details>
    <summary>Answers</summary>
    <ul>
        <li><span class="bold">final_grade</span> is better because it's a more descriptive variable name than just number.</li>
        <li><span class="bold">teacher_name</span> is also more descriptive than just "name", so it's better.</li>
        <li><span class="bold">average_weight</span> is better, because even though it's longer, it's more meaningful. Be careful not to abbreviate your variable names too much!</li>
        <li><span class="bold">best_player_score</span> is better, because the other option is just way too long</li>
    </ul>
</details>
<br />

Note: The actual name of the variable you end up choosing has <span class="bold">no impact</span> on how the computer runs your code. Just because you called a variable `total` doesn’t mean the program will automatically calculate the total. Variable names exist only for you and other programmers to understand the code more easily.

Likewise, do not name your variables with their type, such as name_str or cost_float. Humans should be able the figure out what the variable contains based on its name, and Python is definitely not deciding on the type based on the name! 
