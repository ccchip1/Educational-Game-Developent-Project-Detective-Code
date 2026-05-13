# Detective Code

## Elevator Pitch

A level-based game where players solve puzzles involving searching through python programs & learn how to properly call functions. 

## Influences (Brief)

- Human Resource Machine:
  - Medium: Game
  - Explanation: Human Resource Machine teaches programming logic through small puzzle challenges where players must carefully think through how instructions execute step by step. This game is influenced by its puzzle-based approach, where players must understand how to construct correct sequences of function calls to achieve a desired output, rather than just reading code passively.

- Programming Debuggers:
  - Medium: Software Tool
  - Explanation: Debugging tools in programming environments allow programmers to step through code and observe the call stack as functions are entered and exited. This game is influenced by that workflow, the telephone mechanic replicates the experience of calling a function and observing its behavior.
    
## Core Gameplay Mechanics (Brief)

- Write function calls in a Python terminal to gather information and solve a mystery.
- Use the help() function to learn what functions are available and how to call them correctly.
- Use the telephone to make a "function phone call", placing the text cursor over a function name and clicking the telephone executes that specific function and displays its response as a dialogue message.
- Use the print() statement to submit findings in a report, which is checked against the correct answer.
- Observe the blackboard trace table to understand the order in which functions were called, what arguments were passed, what values were returned, and how deep into nested calls the program went.


# Learning Aspects

## Learning Domains

- Computer Science: specifically programming fundamentals and program execution.
- Computational Thinking: decomposition, sequencing, and logical reasoning when following code execution.

## Target Audiences

Students who are learning to write and use function calls in an introductory programming course.

## Target Contexts

This learning activity or game can be used in introductory programming courses such as high school AP Computer Science classes, introductory college computer science courses, or coding bootcamps. It is also suitable for guided practice in computer labs, homework exercises, and interactive learning games that reinforce program tracing. Informally, it could be used by self-learners studying Python fundamentals, or students practicing how to read function documentation and translate it into correct function call syntax.

## Learning Objectives

- By the end of instruction, students will be able to write syntactically correct function calls in Python given a function description, with 80% accuracy.
- By the end of instruction, students will be able to use the help() function to identify available functions and their parameters, then apply that information to construct appropriate function calls.
- By the end of instruction, students will be able to interpret the output of a function call and use it appropriately inside a print() statement to produce the correct output.

## Prerequisite Knowledge

- Prior to the game, players need to be able to explain what a function is and describe the difference between defining and calling a function.
- Prior to the game, players need to be able to explain what a variable is and how to reference a variable by name in an expression.
- Prior to the game, players need to be able to recognize what a function call looks like syntactically, including function name, parentheses, and arguments.

## Assessment Measures

A short pre-test and matching post-test should be designed to assess student learning of writing and interpreting function calls in Python.

- Given a function description, write a correct function call using the appropriate arguments.
- Given a variable already defined in a program, use it as an argument in a function call and predict the output.
- Given a nested function call, identify what value is returned by the inner function and explain how it is used as the argument for the outer function.

### Examples of Assement Questions:
The following assement question are ordered in difficulty from easiest to hardest to give a range of difficulty. This type of question could technically be written in any type of programming language as long as it has function calls, but these questions will be written in python as this is closer to introductory course level questions

### Question 1: Invocation Order Only 

Given the following python program, trace the order in which the functions are invoked.

```
def greet(name):
    return "Hello " + name

def farewell(name):
    return "Goodbye " + name

def run():
    first = greet("Alice")
    second = farewell("Alice")
    return first + " and " + second

run()
```

|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |                                        |                                        |     |
|2      |                                        |                                        |     |
|3      |                                        |                                        |     |

Answer:
|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |Call run()                              |no parameters                           |1    |
|2      |Call greet("Alice")                     |name = "Alice"                          |2    |
|3      |Call farewell("Alice")                  |name = "Alice"                          |2    |

### Question 2: Entry & Exit Trace

Given the following python program, trace the complete call stack, recording both when the functions are invoked and when they return.

```
def add(a, b):
    return a + b

def multiply(x, y):
    result = add(x, y)
    return result * 2

call = multiply(3, 4)
```

|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |                                        |                                        |     |
|2      |                                        |                                        |     |
|3      |                                        |                                        |     |
|4      |                                        |                                        |     |

Answer:
|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |Call multiply(3, 4)                     |x = 3, y = 4                            |1    |
|2      |Call add(3, 4)                          |a = 3, b = 4                            |2    |
|3      |Return from add                         |returns 7                               |1    |
|4      |Return from multiply                    |result = 7, returns 14                  |0    |

### Question 3: Recursion Trace

Given the following python program, trace the complete call stack, recording both when the functions are invoked and when they return.

```
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)

result = factorial(4)
```

|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |                                        |                                        |     |
|2      |                                        |                                        |     |
|3      |                                        |                                        |     |
|4      |                                        |                                        |     |
|5      |                                        |                                        |     |
|6      |                                        |                                        |     |
|7      |                                        |                                        |     |
|8      |                                        |                                        |     |

Answer:
|Trace #|Event                                   |Details                                 |Depth|
|-------|----------------------------------------|----------------------------------------|-----|
|1      |Call factorial(4)                       |n = 4                                   |1    |
|2      |Call factorial(3)                       |n = 3                                   |2    |
|3      |Call factorial(2)                       |n = 2                                   |3    |
|4      |Call factorial(1)                       |n = 1                                   |4    |
|5      |Return from factorial(1)                |returns 1                               |3    |
|6      |Return from factorial(2)                |returns 2                               |2    |
|7      |Return from factorial(3)                |returns 6                               |1    |
|8      |Return from factorial(4)                |returns 24                              |0    |

# What sets this project apart?

- Focus on a Difficult Programming Concept  
  Many beginner programming games focus on simple sequencing or syntax, but few directly teach how function calls, returns, and the call stack work together during program execution. This game targets a concept that many students struggle with in introductory programming courses, helping them build a clear mental model of how programs actually run.

- Interactive Program Tracing Instead of Passive Learning  
  Rather than reading explanations or watching tutorials, players actively step through program execution. By selecting which function is called next, identifying return values, and maintaining a call stack, players learn through hands-on interaction that mimics real debugging and program analysis.

- Visualizing an Invisible Process  
  The call stack and function execution are normally invisible processes happening inside the computer. This game makes them visual and interactive, allowing players to see functions enter and exit the stack. This visualization helps learners better understand nested functions and program flow.

# Player Interaction Patterns and Modes

## Player Interaction Pattern

This is a game for one person, they click with the mouse/type with the keyboard.

## Player Modes

- Single-player: You repeatedly advance through rounds and levels until you reach the end.

# Gameplay Objectives

The player's goal in each level is to solve a mystery by writing the correct function calls in the Python terminal and submitting the right information in a printed report. To do this, the player must figure out which functions are available, learn how to call them correctly using help() and the telephone, and use print() to output the answer. The level is complete when the printed report contains the correct information and the player clicks the continue arrow.
Alignment: This aligns with the learning objective of understanding function calls, as they are trained to get familiar with how functions calls work in order to be able to solve these puzzles.

# Procedures/Actions

- Type function calls, variable assignments, and print() statements into the terminal by clicking the keyboard or smartboard
- Move the text cursor using the arrow keys or keyboard shortcuts to navigate the terminal
- Click the telephone to make a function phone call on whichever function the cursor is currently over, which displays a dialogue response in a word bubble and updates the blackboard trace table
- Click the printer to run the full terminal program and generate a report, which is checked against the correct answer and displays a hint message
- Drag the word bubble or report panel horizontally out of the way if they are blocking something
- Click the red X on the word bubble, report, or hint box to close them
- Use help() with no arguments to read the full case instructions, or help('function_name') to read documentation for a specific function

# Rules

- The top half of the smartboard is read-only and cannot be edited by the player
- The telephone only works when the text cursor is positioned over the name of a function call in the terminal — placing it elsewhere shows an error message
- Once the player submits a correct report, the terminal becomes read-only and can no longer be edited, though the cursor can still be moved for telephone calls
- The player cannot move to the next level until they have submitted a correct report and clicked the continue arrow
- Variables defined in the transcript are available to use as arguments in function calls written in the terminal

# Objects/Entities

Smartboard — the central screen split into a read-only transcript panel on top and an editable Python terminal on the bottom
Blackboard — displays the function trace table showing the call and return history of the most recent telephone call
Telephone — executes the function call the cursor is over and displays its dialogue response in a word bubble
Printer — runs the full terminal program and produces a report from all print() output, which is compared against the correct answer
Keyboard — clicking it activates the terminal for typing
Word bubble — a draggable panel that appears above the telephone showing the dialogue response from the most recent function phone call
Report panel — a draggable panel showing the printed output from the most recent printer run
Hint box — a panel spanning the bottom of the screen that gives targeted feedback after each printer submission
Continue arrow — appears in the top left corner when the player submits a correct report, allowing them to advance to the next level

## Core Gameplay Mechanics (Detailed)

- Core Gameplay Mechanic #1: Python Terminal  
  Players use a Python terminal to write function calls that gather information needed to solve the mystery. The terminal accepts function calls, variable assignments, and print() statements. By reading the transcript on the smartboard and using help(), players learn which functions are available, what arguments they take, and what they return. Creating a correct function call with the right arguments is the central skill the game develops.

- Core Gameplay Mechanic #2: Function Phone Call
  Players use the telephone to make a "function phone call." With the text cursor positioned over a function name in the terminal, clicking the telephone executes that specific function call and displays a dialogue response in a word bubble, being the function's output as if it were spoken by a contact being called for information. This mechanic helps players understand that functions take inputs and produce outputs, and gives them a way to test their function calls interactively before committing to a final answer.

- Core Gameplay Mechanic #3: Detectives Report, & Hint Box
  When the player clicks the printer, the entire terminal program runs and all print() output is compiled into a report. The report is checked against the correct answer and a hint box appears at the bottom of the screen giving feedback, where it congratulates the player if the report is correct, or gives a targeted hint about what went wrong if it is not. This mechanic teaches players that print() is how a program communicates its final output, and that the correctness of that output depends on whether the right function calls were made with the right arguments.
    
## Feedback

Players receive immediate feedback through the telephone's word bubble each time they make a function phone call. The response dialogue tells the player what the function did, and if an error occurred the bubble explains what went wrong. The blackboard trace table updates after each telephone call, showing the full call and return history for that function including argument values, & return values, giving players a visual record of what the program actually did.

When the player submits a report via the printer, the hint box at the bottom of the screen provides targeted feedback based on the specific mistake made. Different hints appear depending on whether the report is empty, a variable is undefined, the wrong function arguments were used, or the output is simply incorrect. If the report is correct, the player is congratulated and a continue button appears.

Longer-term feedback comes through level progression. Each level presents a new mystery that requires applying the same core skills: reading function documentation, constructing correct calls, and printing the right output, with each level putting that idea in a new context. Successfully completing a level confirms that the player can correctly write and use function calls to produce a desired result.

# Story and Gameplay

## Presentation of Rules

Players learn the mechanics through the first level, which acts as an interactive tutorial. The transcript on the smartboard gives a brief overview of the task and instructions for using the help() function. The help() call is pre-loaded in the terminal when the level starts, so the player's first action is naturally to use the telephone to call it and read the response. From there, the player discovers what functions are available, how to call help('function_name') for more detail, and how to use print() to submit their answer. The hint box guides players who make mistakes without directly giving away the solution.

## Presentation of Content

Programming concepts are taught through increasingly complex mysteries rather than direct instruction. Early levels like the System Login puzzle require only a single function call with one argument, keeping the focus on the basic mechanics of function syntax and the telephone system. Later levels introduce multi-step puzzles where players must chain function calls, using the return value of one function as the argument to another to reach the correct answer. The blackboard trace table is always visible and updates with each telephone call, reinforcing how function calls, arguments, and return values relate to each other throughout the problem-solving process.

## Story (Brief)

The player takes the role of a beginner Detective solving short mysteries and other problems. However, after the recent robotic takeover, everything in his office that he uses to solve these mysteries is now controlled by a single python terminal, including his telephone he uses to call agents for information, his printer that he uses to print out his reports, & even the transcripts he is given that hold information about the mysteries he needs to solve is now embedded into the top part of the new terminal. Make your way through this strange new program to find the truth!

## Storyboarding

This first image is a basic layout of your character's working space. There is a projector on the left that the player will be working with, & a blackboard on the right. On the table is a keyboard, an old telephone & a printer. The player can click on either the keyboard or the bottom half of the smartboard to access the python terminal, allowing them to write function calls & print statements to try to solve the puzzle (note that the top half of the smartboard is a read only, meaning it is unaccessible to the player, but it gives a brief overview of the task, as well as the list of predefined variables).

[![](Detective_Code_StoryBoard_Version2.1.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.1.png)


When the player clicks the phone at the center of the table, it will show a dialogue message based off of the function they choose. This is what we will call a "Function Phone Call". In order for someone to do a function phone call correctly, the text cursor in the terminal needs to be positioned specifically on top of the name of the function they want to call.

The next image shows the function help() being called on the telephone. The help() function is meant to act as the starting place for every puzzle as it gives a proper transcript of the puzzle they need to solve, including some of the functions they can use, & the expected print output for the report.

[![](Detective_Code_StoryBoard_Version2.2.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.2.png)


Shown in the previous image, help() tells the player about a function called building_status() which will be used for solving the puzzle, & they are also told to call help("building_status") if they need help on how to properly use that function. The next image shows what function phone calling help("building_status") would look like.

[![](Detective_Code_StoryBoard_Version2.3.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.3.png)


The next image shows the player calling the building_status() function properly thanks to the help of the help() function. This building_status() function does the typical dialogue in the function phone call, but it also shows the value that is being returned. Also on the smartboard, the player chooses to set that function call to a variable to then put in the print() statement.

[![](Detective_Code_StoryBoard_Version2.4.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.4.png)


It is important to mention that the word bubble from the function phone call is horizontally draggable, & that is because the following image shows that the blackboard that was behind it now has information about the most recent function as well. The blackboard will create a trace of this function in the form of a table that shows the order of when functions are called or returned, as well as extra information about what arguments are being used, or what values are being returned.

[![](Detective_Code_StoryBoard_Version2.5.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.5.png)


Next slide shows the rest of the player's print() statements for solving the rest of the puzzle. Notice they choose to have the specific function calls directly inside of the print statement instead of creating a new variable each time.

[![](Detective_Code_StoryBoard_Version2.6.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.6.png)


When the player clicks the printer on the right side of the table, it will first run the entire python program, then it will bring up a report that shows the expected output of the print() statements. A message box will then appear spanning the bottom of the screen that will comment on how they did. It will give a positive comment if the report looks correct, & if it doesn't it will give the player a hint on how to fix it.

In this final image, it is shown that the player submitted a good report, so they are prompted to click the green arrow that appeared when they are ready to move onto the next level.

[![](Detective_Code_StoryBoard_Version2.7.png)](https://github.com/ccchip1/Educational-Game-Developent-Project-Detective-Code/blob/main/Detective_Code_StoryBoard_Version2.7.png)

# Assets Needed

## Aethestics

In the style of a cartoony detective noire film.

## Graphical

- Characters List
  - Detective Code (main character)
  - Various Co-workers, & Agents
  - Various Witnesses
- Textures:
  - Printer
  - Old Timey Telephone
- Environment Art/Textures:
  - Models for Detective Code's Office 
  - Midnight crime scene

## Audio

- Music List (Ambient sound)
  - Ace Attorney-like music for the title screen
  - Chill jazz music for the main gameplay loop

- Sound List (SFX)
  - Old phone sounds when using the phone: ringing sound, hangup sound
  - Printer sounds when the player clicks the printer to submit their report.

# Metadata

* Template created by Austin Cory Bart <acbart@udel.edu>, Mark Sheriff, Alec Markarian, and Benjamin Stanley.
* Version 0.0.3
