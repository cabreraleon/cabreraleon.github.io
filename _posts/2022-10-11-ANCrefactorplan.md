---
layout: post
title: My Refactoring Plan of Action
---


I created a plan of action to refactor the Adaptive Connector method in the PPL. This plan will help me stay on track with what I must do in order to help my team refactor this code. My plan can help you refactor your code too! I recommend that you follow it if you need help on where to start.

<br>

**Logistics:** My graduate mentors Dr. Homa K. soon-to-be-Dr. Dinae U. will help me refactor my code. At the beginning of each week, the Parasol Laboratory has a PPL open-source meeting for all teams. In this meeting, each team takes turns to present their research updates and their future to-do plans. I presented my updates on nearly all the open-source meeting in Fall 2022. 

<br>

## The Eight Steps of My Refactoring Plan

<br>

1. ### Find research paper that introduced the AdaptiveConnector.h. 
    Source the paper title and authors to the verbose doxygen comment at the top of the method file. This way, the audience of the code can reference the code and read more about the ANC.<br>

2. ### Read the research paper.
    Give the research a paper a minimum of a second pass read. In a second pass read, only look at visual data such as graphs, diagrams, images, and captions in addition to the abstract, titles and subtitles of each section, and conclusion. The second pass foreshadows experimental results and can indicate if the data is realistic and reliable, which is a strong indication of a good research paper. You don't have to read the entire research paper since it's totally okay if you don't understand all of it. If you are a  new student at Parasol, like me, you aren't expected to know what the experienced roboticist in Ekenna et al (2013) know. Just focus on the key items you need that will help you refactor the code! <br>

3. ### Map the ANC pseudocode to the AdaptiveConnector.h raw code.
    This will help me understand the relationship between the ANC method and its representation in C++ code in our PPL world. It is important to know *what* the main chunks of code in our PPL method files are doing, the order of *when* they execute, and *how* functions, variables, and external files interact with each other in regards to the ANC. <br>
    
4. ### Translate the ANC pseudocode into simple English.
    This will help me understand how the ANC method works. <br>

5. ### Run the code in the master branch of the PPL to see what has already been released for public use in present time.
    This will provide a good indication of where the other laboratory students left off in the last refactoring process of the ANC code. The last commit pushed to the PPL master branch was roughly two years ago. <br>

6. ### Check out my own GitLab branch, AdaptiveConnector, and start my refactoring work there.
    Checking out to my own gitlab branch will allow me to refactor my code seperately without affecting the PPL codebase in the master branch or anyone elses' code elsewhere. <br>

7. ### Run the Adaprive Connector code. If the code contains a bug, locate, dissect, and debug it. Repeat until the program returns the expected output file, which must be a connected graph G with additional edges.
    Ensure to write well-written, detailed yet simple to follow comments of what key code chunks do. Remember to add @TODO comments to not forget what you must work on next. My goal at this step is to ensure the ANC program outputs a connected graph. However, it is important to note that **code can run smoothly with no bugs and still output expected outputs that are incorrect and unreliable**. This is why testing, the next step, is so important. <br>

8. ### Develop tests for the Adaptive Connector code to ensure that the output is expected, correct, *and* reliable. The tests must be unique, in varying environments with varying k-values, and signifanct.
    If the tests pass, the refactoring of the ANC method has been successful. If the tests fail, this means the ANC method has silent bugs or fundamental flaws that have made the code to act unexpectedly, incorrectly, and unreliably and you must return to Step 7 until your ANC method succeeds all its test cases. <br>

<br> 
 