<style>
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
</style>

CodingCat is a website built specifically for you, the student, to practice coding. As such, you can use its different features to debug more efficiently.


<div id="error-messages"></div>

### Use Error Messages

If your program isn’t running at all, CodingCat will provide you with the error that’s happening. <span class="bold">Reading that error is crucial</span>, because it can give you hints on which part of your code creates the error, like a variable. This allows you to narrow down your debugging.

The name of the error can also give you hints. It can be things like ZeroDivisionError, TypeError, or IndexError. Usually, there’s a tip that comes up when you run into one of these errors. Read the tip and error message carefully to figure out the best path you should take for debugging.


<div id="typos"></div>

### Scrutinize the Code for Typos

In the CodingCat editor, some Python-specific keywords are supposed to always be highlighted in blue, like these: `return`, `for`, `in`, `and`, `or`, `not`, `def`, `len`. If these keywords aren’t highlighted in blue in your code, there’s definitely a typo.


<div style="background-color: #8ae514; padding: 1rem; border-radius: 1rem; border: 1px solid black; color: black; box-shadow: 5px 5px black; margin-bottom: 1rem;">
    A good rule of thumb is to check if a word is defined in your own code (for example when you create a variable). If it’s not, it should be highlighted in blue.
</div>

Look at your variable names. Make sure that if you’re defining a variable called “result”, you’re using the name “result” when referring to it later, not “resutl”, “Result” or “total”. Computers are pretty stupid, so even a tiny typo or capitalization error can make them completely lose their marbles.

<span class="bold">Python is very particular about tabs.</span> Every time a line ends with a colon (or deux-point), the line after it needs to have one more tab. Any lines that belong to this block of code must also have that extra indentation.


<div id="failed-tests"></div>

### Similarities of the Failed Test Cases

If your code runs and succeeds in a few test cases, but not all of them, <span class="bold">look at the tests that it fails</span>. Are there any commonalities between them? What can they mean?

Once you find the similarities those tests share, you’re one step closer to spotting your bug. You can look for parts of your code that should be doing that job. This method works best when combined with tracing your code.



<div id="similar-code"></div>

### Compare With Similar Working Code

If you’ve already done exercises on CodingCat in the same category, compare your current code with old solutions that work. It’s especially helpful if both problems have similar premises.

Look for similarities and differences. Did you use a for loop here but not in the old solution? Did you move an if statement to another part of the code? <span class="bold">Why did you make those changes?</span>

No two exercises on CodingCat are perfect duplicates. However, looking at times where you succeeded can help remind you of what non-buggy code looks like. It’s part of the learning process to have bugs in your code.

