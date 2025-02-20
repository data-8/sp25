---
layout: page
nav_order: 8
title: 💻 Debugging
description: >-
    Debugging
---

<style>
    code {
        font-size: 80%;
    }
</style>

# **Debugging**
{:.no_toc}

## Cells and the Autograder

<details>
  <summary><strong>Why does running a particular cell cause my kernel to die?</strong></summary>
  <p style="margin-left:16px;">If one particular cell seems to cause your kernel to die, your code is probably incorrect in a way that is causing the computer to use more memory than it has available. For instance: your code is trying to create a gigantic array. To prevent from crashing the entire server, the kernel will “die”. This is an indication that there is a mistake in your code that you need to fix.
</p>
</details>

<details>
  <summary><strong>My python code cell has turned into a text/markdown cell. How do I change it back?</strong></summary>
  <p style="margin-left:16px;">Click on the cell and select <code>Markdown > Code</code> in the top toolbar. Alternatively, click on the cell and press <code>y</code>.
</p>
</details>

<details>
  <summary><strong>My markdown text cell has turned into a code cell. How do I change it back?</strong></summary>
  <p style="margin-left:16px;">Click on the cell and select <code>Code > Markdown</code> in the top toolbar. Alternatively, click on the cell and press <code>m</code>.
</p>
</details>

<details>
  <summary><strong>How do I quickly run all the cells in a notebook?</strong></summary>
  <p style="margin-left:16px;">Go to the Cell menu in the top toolbar, then “Run All.” You can also select a certain cell and run all cells before this point, or run all cells after this point. You should run all the cells in your notebook before submitting to confirm that you pass all the tests.
</p>
</details>

<details>
  <summary><strong>Why does <code>grader.check_all()</code> fail, if all previous tests passed?</strong></summary>
  <p style="margin-left:16px;">This can happen if you “overwrite” a variable that is used in a question. For instance, if Question 1 asks you to store your answer in a variable named stat, and later on in the notebook you change the value of stat, you’ll see the test after Question 1 pass, but the test at the end of the notebook fail. Make sure to avoid using the same variable name for more than one purpose.
</p>
</details>

<details>
  <summary><strong>Why does a notebook test fail now, when it passed before and I didn’t change my code?</strong></summary>
  <p style="margin-left:16px;">You probably ran your notebook out of order. Re-run all previous cells in order, which is how your code will be graded.
</p>
</details>

<details>
  <summary><strong>Why did a Gradescope test fail, when all the notebook’s tests passed?</strong></summary>
  <p style="margin-left:16px;">This can happen if you’re running your notebook’s cells out-of-order. The autograder runs your notebook top-to-bottom. If you’re defining a variable at the bottom of your notebook and using it at the top, the Gradescope autograder will fail because it doesn’t recognize the variable when it encounters it.
</p>
  <p style="margin-left:16px;">Additionally, this can fail if you have not saved before you run the autograder. Ensure you select File -> Save Notebook to avoid this.
</p>
    <p style="margin-left:16px;">This is why we recommend running Kernel -> Restart and Run All: it “forgets” all of the variables and runs the notebook from top-to-bottom, just like the Gradescope autograder will. This will highlight any issues. Find the first cell that raises an error. Make sure that all of the variables used in that cell have been defined above that cell, and not below.
</p>
</details>

<details>
  <summary><strong>Why do I get an error saying grader is not defined?</strong></summary>
  <p style="margin-left:16px;">If it has been a while since you’ve worked on an assignment, the kernel will shut itself down to preserve memory. When this happens, all of your variables are forgotten, including the grader. That’s OK: you’ll just need to re-run all of the cells. The easiest way to do this is by using Kernel -> Restart and Run All.
</p>
  <p style="margin-left:16px;">This may also occur if you never ran the top cell of the notebook where the grader is defined.
</p>
</details>

<details>
  <summary><strong>I’m positive I have the right answer, but the test fails. Is there a mistake in the test?</strong></summary>
  <p style="margin-left:16px;">While you might see the correct answer displayed as the result of the cell, chances are it isn’t being stored in the answer variable. Make sure you are assigning the result to the answer variable. Make sure there are no typos in the variable name.
</p>
</details>

<details>
  <summary><strong>I accidentally deleted something in a cell that was provided to me – how do I get it back?</strong></summary>
  <p style="margin-left:16px;">There are two solutions:</p>
  <p style="margin-left:16px;">1. In <a href="https://github.com/data-8/materials-sp25">this</a>
 public GitHub repository, you’ll find the “original” versions of all assignments we released this semester. You can look here and manually add back any necessary code or text that you accidentally deleted.</p>
  <p style="margin-left:16px;">2. Suppose you’re working on Lab 5. One solution is go directly to DataHub and rename your <code>lab05</code> folder to something else, like <code>lab05-old</code>. Then, click the Lab 5 link on the course website again, and it’ll bring you to a brand-new version of Lab 5. Then, you can copy your work from your old Lab 5 to this new one, which should have everything in it.</p>
</details>

## Specific Errors
A general rule of thumb when debugging is to look at the very last line of an error message. That’s usually the most informative part of the message, and will often tell you directly what’s wrong.


<details>
  <summary><strong>... object is not callable</strong></summary>
  <p style="margin-left:16px;">This often happens when you use a default keyword (like <code>str</code> or <code>list</code>) as a variable name, for instance <code>list = [1, 2, 3]</code>. These errors can be tricky because they don’t error on their own, but cause problems when we try to use the name list (for example) later on in the notebook.
</p>
<p style="margin-left:16px;">To fix the issue, identify any such lines of code, change your variable names to be something else, and restart your notebook.
</p>
<p style="margin-left:16px;">Python keywords like str and list appear in green text, so be on the lookout if any of your variable names appear in green!
</p>
</details>

<details>
  <summary><strong>SyntaxError at the very beginning of a line of code</strong></summary>
  <p style="margin-left:16px;">Python expected you to continue your last line of code. Typically this means you have mismatched parentheses on the line above the line that is erroring.
</p>
</details>

## DataHub

<details>
  <summary><strong>Why can’t I log in to DataHub?</strong></summary>
  <p style="margin-left:16px;">Log out of all Google accounts or open an incognito window. When prompted, enter your full Berkeley email, username@berkeley.edu, as your credentials.
</p>
</details>

<details>
  <summary><strong>My notebook won’t load. Is DataHub down?</strong></summary>
  <p style="margin-left:16px;">Sometimes DataHub does have availability issues. Usually it is back up and running again within an hour. 
</p>
  <p style="margin-left:16px;">In other instances, there are some things you can do to get the notebook running again: Make sure your internet connection is working. If you can, restart your server by clicking the button at the top right labeled “Control Panel”, then select “Stop My Server”, followed by “Start My Server”. 
</p>
  <p style="margin-left:16px;">If that doesn’t work, try restarting your computer and using a different browser. Whenever you resume working on a notebook, run all cells you’ve previously completed. If your problem persists after trying all these steps, please notify us on Ed.
</p>
</details>

<details>
  <summary><strong>What if I don’t have access to DataHub and I still want to access Data 8 materials?</strong></summary>
  <p style="margin-left:16px;">We welcome the general public to use our materials. If you’re not enrolled in the class, you can access all lectures and assignments in our public GitHub repository. In order to run Jupyter notebooks locally on your own computer, we recommend using Anaconda.
</p>
</details>

---

Courtesies to DSC 10: Principles of Data Science and their [debugging guide](https://dsc10.com/debugging/), as it was of great inspiration!
