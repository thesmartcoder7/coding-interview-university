<br><br>

# How to solve coding problems
Interviews are a way to find out if you can solve a company's problem and if you will be more valuable to them than the salary they are paying you.

What do you do when you get into an interview? See, even if you know all the data structures and algorithms inside out, you still aren't guaranteed to pass. You might even end up realizing that it is not always the smartest interviewee that gets hired. It comes down to "can you solve our problem"

That being said, you need to understand that it is more about knowing how to breakdown the problem than having crammed through all the data structures and algorthms. The coding interview process is all about the interviewer getting to know your thought process. It is about the interviewer getting to know how you break down the problem and if you know and understand the tradeoffs between different data structures and different algorithms. These interviews aim to analyze the following: 
- Analytic Skills - How can you think through problems and analyze things?
- Coding Skills - Do you code well, by writing clean, simple, organized, readable code?
- Technical knowledge - Do you know the fundamentals of the job you're applying for?
- Communication skills: Does your personality match the companies’ culture?


When you are preparing for an iterview or are in an interview room, you must remember the 3 pillars of good code:
- Readability 
- Time Complexity
- Space Complexity

<br>

## Step By Step through a problem:
- When the interviewer says the question, write down the key points at the top. Make sure you have all the details. Show how organized you are.

- Make sure you double check: What are the inputs? What are the outputs?

- What is the most important value of the problem? Do you have time, and space and memory
etc.. What is the main goal?

- Don't be annoying and ask too many questions. Keep in mind that you do not have enough time. Ask the most important questions to get you fired up then save some more for the end

- Start with the naive/brute force approach. First thing that comes into mind. It shows that5.
you’re able to think well and critically (you don't need to write this code, just speak about it).

- Tell them why this approach is not the best (i.e. O(n^2) or higher, not readable, etc...).

- Walk through your approach, comment things and see where you may be able to break things.
Any repetition, bottlenecks like O(N^2), or unnecessary work? Did you use all the information
the interviewer gave you? Bottleneck is the part of the code with the biggest Big O. Focus on
that. Sometimes this occurs with repeated work as well.

- Before you start coding, walk through your code and write down the steps you are going to8.
follow.

- Modularize your code from the very beginning. Break up your code into beautiful small pieces.
and add just comments if you need to.

- Start actually writing your code now. Keep in mind that the more you prepare and understand.
what you need to code, the better the whiteboard will go. So never start a whiteboard
interview not being sure of how things are going to work out. That is a recipe for disaster.
Keep in mind: A lot of interviews ask questions that you won’t be able to fully answer on time.
So think: What can I show in order to show that I can do this and I am better than other
coders. Break things up in Functions (if you can’t remember a method, just make up a function
and you will at least have it there. Write something, and start with the easy part.

- Think about error checks and how you can break this code. Never make assumptions about the11.
input. Assume people are trying to break your code and that Darth Vader is using your
function. How will you safeguard it? Always check for false inputs that you don’t want. Here is
a trick: Comment in the code, the checks that you want to do... write the function, then tell the
interviewer that you would write tests now to make your function fail (but you won't need to
actually write the tests).

- Don’t use bad/confusing names like i and j. Write code that reads well.

- Test your code: Check for no params, 0, undefined, null, massive arrays, async code, etc... Ask13.
the interviewer if we can make assumption about the code. Can you make the answer return
an error? Poke holes into your solution. Are you repeating yourself?

- Finally talk to the interviewer where you would improve the code. Does it work? Are there14.
different approaches? Is it readable? What would you google to improve? How can
performance be improved? Possibly: Ask the interviewer what was the most interesting
solution you have seen to this problem.

- If your interviewer is happy with the solution, the interview usually ends here. It is also15.
common that the interviewer asks you extension questions, such as how you would handle the
problem if the whole input is too large to fit into memory, or if the input arrives as a stream.
This is a common follow-up question at Google, where they care a lot about scale. The answer
is usually a divide-and-conquer approach — perform distributed processing of the data and only
read certain chunks of the input from disk into memory, write the output back to disk and
combine them later.

<br>

## Here's a checklist to make sure your code is good:
- It works
- Good use of data structures
- Code Re-use/ Do Not Repeat Yourself
- Modular - makes code more readable, maintainable and testable
- Less than O(N^2). We want to avoid nested loops if we can since they are expensive. Two
separate loops are better than 2 nested loops
- Low Space Complexity --> Recursion can cause stack overflow, copying of large arrays may
exceed memory of machine

No one and I mean no one has all these things down. It is all about training the muscle. Think out loud through the problem. It is all in the practice
