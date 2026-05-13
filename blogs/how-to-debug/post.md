<style>
    #comic-wrapper>img {
        margin: 1rem;
    }
    input[type='checkbox']{
        margin-right: 1rem;
        height: 1.5rem;
        width: 1.5rem;
        box-shadow: 2px 2px black;
    }
    div.highlight {
        background-color: #8ae514; 
        padding: 1rem; 
        border-radius: 1rem; 
        border: 1px solid black; 
        color: black; 
        box-shadow: 5px 5px black; 
        margin-bottom: 1rem;
        display: block;
        width: fit-content;
    }
    span.bold {
        font-weight: bold;
        color: #8ae514;
    }
    a.learn-more {
        background-color: #8ae514; 
        padding: 0.5rem;
        margin: 1rem 0 1.5rem 0;
        border-radius: 0.5rem; 
        border: 1px solid black; 
        color: black; 
        box-shadow: 3px 3px black; 
        margin-bottom: 1rem;
        display: block;
        width: fit-content;
    }
</style>

Throughout your learning journey on CodingCat, you will assuredly encounter bugs of all kinds. This article is meant for you to have a series of steps you can follow when you encounter bugs

### Things to Keep in Mind While Debugging

<div class="highlight">
    <span style="font-weight: bold;">Bugs are normal!</span> We all encounter them, regardless of our skill level. You will eventually become better at spotting and fixing them, but they will never magically disappear.
</div>

<span class="bold">You have to understand the bug before fixing it.</span> Random changes will only make you lose sight of what you’re debugging in the first place. Once you understand what’s happening, you can fix the bug quickly and effectively.

<p>
    <span class="bold">Always try one solution at a time.</span> You may not know exactly how to fix the bug, so test one thing before changing something else. If you don’t think about the changes in advance, you can accidentally break something else. You also won’t know which of your solutions fixed the bug in the end.
    A novice programmer debugging will make random changes and hope the program fixes itself. Don’t do this!
</p>

### A Helpful Checklist


<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Use error messages</label>
</div>

When your code doesn’t run, error messages appear. These are configured in CodingCat to give you hints for the next step.
<a class="learn-more" href="/#/blogs/use_codingcat_efficiently#error-messages">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Check for typos</label>
</div>

Go over your code to make sure you didn’t misspell anything. Remember to check the tabulation.
<a class="learn-more" href="/#/blogs/use_codingcat_efficiently#typos">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Find similarities in failed test cases</label>
</div>

Look at the test cases where your code is failing. Do you see any similarities?
<a class="learn-more" href="/#/blogs/use_codingcat_efficiently#failed-tests">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Compare with similar working code</label>
</div>

If you’ve completed similar CodingCat problems before, compare your current code with the functional code you wrote back then.
<a class="learn-more" href="/#/blogs/use_codingcat_efficiently#similar-code">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Trace your code</label>
</div>

Find out what’s going on in your code by simulating its output on paper. 
<a class="learn-more" href="/#/blogs/tracing_your_code#trace-your-code">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Read the documentation</label>
</div>

If you’re unsure about a concept, read official Python documentation. 
<a class="learn-more" href="/#/blogs/tracing_your_code#read-the-docs">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Look at the original prompt</label>
</div>

Re-read the problem’s scenario and make sure you fully understand it.
<a class="learn-more" href="/#/blogs/tracing_your_code#original-prompt">Find out more +</a>

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Take a break</label>
</div>

If nothing works right now, take a walk and come back in 5 minutes.

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">Ask a friend</label>
</div>

Unclog your brain by talking to a friend about your program.

<div>
    <input type="checkbox">
    <label style="font-size: 1.25rem; font-weight: bold;">… Ask the teacher</label>
</div>

As a last resort, speak to your teacher if you’ve been stuck after trying all of this 

### A Few Comics For You

<div class="highlight" id="comic-wrapper">
    <img src="https://wizardzines.com/images/uploads/understand-can-fix.png" alt="A short comic about how much easier it is to fix a bug once you understand it" style="max-width: 20rem;">
    <img src="https://wizardzines.com/images/uploads/change-one-thing-at-a-time.png" alt="A short comic about how you should fix a bug by changing only one thing at a time" style="max-width: 20rem;">
</div>