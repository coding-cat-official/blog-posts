<style>
    #comic-wrapper>img {
        margin: 1rem;
    }
</style>

Throughout your learning journey on CodingCat, you will assuredly encounter bugs of all kinds. This article is meant for you to have a series of steps you can follow when you encounter bugs

### Things to Keep in Mind While Debugging

<div style="background-color: #8ae514; padding: 1rem; border-radius: 1rem; border: 1px solid black; color: black; box-shadow: 5px 5px black; margin-bottom: 1rem;">
    <span style="font-weight: bold;">Bugs are normal!</span> We all encounter them, regardless of our skill level. You will eventually become better at spotting and fixing them, but they will never magically disappear.
</div>

**You have to understand the bug before fixing it.** Random changes will only make you lose sight of what you’re debugging in the first place. Once you understand what’s happening, you can fix the bug quickly and effectively.

**Always try one solution at a time.** You may not know exactly how to fix the bug, so test one change before changing something else. If you don’t think about the changes in advance, you can accidentally break something else. You also won’t know which of your changes fixed the bug in the end.
A novice programmer debugging will make random changes and hope the program fixes itself. Don’t do this!

### A Helpful Checklist


<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Use error messages</label>
</div>

When your code doesn’t run, error messages appear. These are configured in CodingCat to give you hints for the next step.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Check for typos</label>
</div>

Go over your code to make sure you didn’t misspell anything. Remember to check the tabulation.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Find similarities in failed test cases</label>
</div>

Look at the test cases where your code is failing. Do you see any similarities?

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Compare with similar working code</label>
</div>

If you’ve completed similar CodingCat problems before, compare your current code with the functional code you wrote back then.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Trace your code</label>
</div>

Find out what’s going on in your code by simulating its output on paper.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Read the documentation</label>
</div>

If you’re unsure about a concept, read official Python documentation. Resources are linked in < other blog post >

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Look at the original prompt</label>
</div>

Re-read the problem’s scenario and make sure you fully understand it.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Take a break</label>
</div>

If nothing works right now, take a walk and come back in 5 minutes.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">Ask a friend</label>
</div>

Unclog your brain by talking to a friend about your program.

<div>
    <input type="checkbox" style="margin: 0.5rem;">
    <label style="font-size: 1.25rem; font-weight: bold;">… Ask the teacher</label>
</div>

As a last resort, speak to your teacher if you’ve been stuck after trying all of this 

### A Few Comics For You

<div style="display: flex; flex-wrap: wrap; background-color: #8ae514; border-radius: 1rem; border: 1px solid black; box-shadow: 5px 5px black;padding: 1rem;" id="comic-wrapper">
    <img src="https://wizardzines.com/images/uploads/understand-can-fix.png" alt="A short comic about how much easier it is to fix a bug once you understand it" style="max-width: 20rem;">
    <img src="https://wizardzines.com/images/uploads/change-one-thing-at-a-time.png" alt="A short comic about how you should fix a bug by changing only one thing at a time" style="max-width: 20rem;">
</div>