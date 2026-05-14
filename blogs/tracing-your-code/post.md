<style>
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
    span.special-bold {
        font-weight: bold;
        color: black;
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
    li::marker {
        font-weight: bold;
        font-size: 1.5rem;
    }
    h4>a {
        color: gray;
    }
    h4>a:hover {
        color: darkgrey;
    }
</style>

When coding, we often assume that a computer will do things automatically. After all, we've lived our entire lives wth electronic devices that could do stuff on their own forus.

That's not the case when you're the programmer. Computers are not like humans, because they need to be told <span class="bold">every single step</span> of the process you want them to do.

You, as a human, may understand the code you wrote. But you need to carefully look over it to make sure the computer can understand it. Are all the steps listed? What happens at each step of the process?

<div id="trace-your-code"></div>

### Trace Your Code

When your code is running in a way it’s not supposed to, we call that a logic bug. The best remedy against it is to trace your code. 

Tracing code means going through your code on paper, line by line, to see what the computer does.

Follow these simple steps to trace your code effectively:

<div class="highlight">

1.	Starting with the first line, <span class="special-bold">examine the code closely</span>. Don’t let your mental image of the code get in the way.

    * If your code fails a specific test case, trace your code with the variables of the test case it fails.

2.	Get into the mindset of a computer and <span class="special-bold">execute that line</span>. Now, write in plain English what the line does.

    * Does it create a variable? Does it check if something is true or not? Maybe it’s actually changing the content of a variable?

3.	Based on the previous step, write down the <span class="special-bold">contents of the variables</span> you have in your code after “executing” that line.

4.	<span class="special-bold">Double-check your understanding</span> of that line. Do what it tells you to do, not what you would want it to do.

5.	Check <span class="special-bold">what’s the next line</span> you should move onto. It’s often just the one right after, but sometimes, it can be another one.

    * Is there an if statement that’s leading code execution somewhere else? Is there a for loop that you have to go back to the start of?

</div>

Once you go to the next line, <span class="bold">repeat these steps</span> until you reach the end of your code. If you run into a behavior that should be impossible while examining a line, like division by 0, you’ve found your bug!


<div id="read-the-docs"></div>

### Read the Documentation

Sometimes, when you’re tracing your code, you may realize that you’re not exactly sure how something works in Python. In that case, you should check out Python’s official sources to get your memory refreshed. Don’t forget that bugs are a learning opportunity!

Here are a few resources:

#### Official Python documentation: https://docs.python.org/3/tutorial/index.html

* This website can be a bit dense, and isn’t made with beginners in mind. You can search it for help with specific topics, though.

#### Official Python Beginner’s guide: https://wiki.python.org/moin/BeginnersGuide(2f)NonProgrammers.html 

* This is Python’s resource page for beginners. It gathers a whole bunch of informational resources about Python. 

#### A Byte of Python: https://python.swaroopch.com/basics.html 

* This is a comprehensive tutorial about Python, which explains every part of it, beginning with the basics you’re learning in this course. You can look around the website for a tutorial on the feature you’re unsure about, whether it be if statements, types, or simply variable declaration.
* The most relevant sections are “Operators and Expressions” and “Control Flow”. 

<div class="highlight">
    <span class="special-bold">Looking at documentation is perfectly normal!</span> In fact, all industry experts continue looking at documentation throughout their careers. It’s impossible to know 100% of the features of a language you’re using, especially when the language is getting constant updates.
</div>


<div id="original-prompt"></div>

### Look at the Original Prompt

While tracing your code, make sure you remember the possibility of having forgotten to account for some parts of the problem.

If you’re unsure, try writing out a detailed bullet-point list of the things your program should do. Then, look over each point and check if your code takes care of that while you trace it.

<span class="bold">Ask yourself questions</span>. Did you handle all the conditions that the prompt asked you to? Are there any edge cases that you might need to cover?
