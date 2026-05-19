<style>
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
</style>

<small>
    This article and others in the "technical" section are based on the textbook "How to Think Like a Computer Scientist: The Dawson College Edition", by Jaya Nikalantan and Bennett Axtell
</small>

A <span class="bold">value</span> is one of the fundamental things — like a word or a number — that a program manipulates. For example, 2, 3, and 5 (the result when we added 2 + 3) are values, as is "Hello, World!". We often refer to these values as objects and we will use the words value and object interchangeably in Python. A variable allows us to name the value so that we can refer to it elsewhere.

Variables are classified into different <span class="bold">data types</span>, or classes. The most common data types are:

### Integers

<span class="bold">Integers</span>, or int, are positive and negative whole numbers, like:

- 23
- 0
- -28

### Strings

<span class="bold">Strings</span> are sequences of 0 or more characters. They can be recognized because they’re always surrounded by quotes (`""` or `''`). The characters can be anything – letters, numbers, symbols – as long as they’re enclosed between quotes. They can also be abbreviated to str.

-	"Hi there!"
-	'username123'

<small>Note: Strings can usually only be on one line. However, they can span multiple lines if triple quotes are used:

-	'''Hello
there'''

-	"""How many times
did you read this article?"""</small>

<small>Note 2: What about values like "17" and "0.6"? They look like numbers, but the quotation marks mean they are strings.</small>
