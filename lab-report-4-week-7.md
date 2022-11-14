# Lab report 1
## **Part 1**

![Image](CSE15L_Images\Lab4Part1(2).PNG)

    :%c/start/base/gc<Enter>. This command will finds and replace all the places where it contains the word "start" with the word "base". /start is looking for the places that has the word "start". /base is replacing the old word with the word "base". /gc gives confirmation prompt everytime it found a place that contains the word "start".

![Image](CSE15L_Images\Lab4Part1(1).PNG)

    Each one of these prompts requires one key stroke <y>. Each time, the computer will replace the word "start" with "base" and move on to the next place that has the word "start" and ask for another user input.

*`<Shift>+<:>, <%>, <s>, </>, <s>, <t>, <a>, <r>, <t>, </>, <b>, <a>, <s>, <e>, </>, <g>, <c>, <Enter>, <y>, <y>, <y>, <n>`. In total, there are 23 keystrokes required to replace all the words "start" with the word "base"*

## **Part 2**

*Editing on Visual Studio Code:*

    It took me about 42 seconds to edit the TestDocSearch file on VSCode, the scp the file onto the remote server, then run to confirms that I have fixed the code using "bash test.sh".

*Editing on Vim:*

    It took me about 17 seconds to cd into the repository, then go into vim on TestDocSearch file, and edit there. Then I exit, and run "bash test.sh".

### *Question 1:*

- Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?

    It really depends, if I am working on a big project that relies heavily on fixing a lot of lines, then I would prefer using an IDE before I would copy it onto the remote server and test it there. I would use vim if I just need to fix a few mistakes because it would be more convenient to test since you don't have to move to the remote server everytime I need to test.

### *Question 2:*

- What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)

    The size of the project is the biggest factor for me in choosing which way to go with. Another factor is the amount of testing will I be doing. If I have to continuously testing a single method, then I would choose to edit on vim, so it is more convenient to exit the file and test.
