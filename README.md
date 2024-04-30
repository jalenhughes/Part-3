# Project Creation Guideline: Fundamentals of Programming

## Introduction
This assignment is designed to provide you with a practical and hands-on experience in building a real-world application using C++. Throughout the course, we will iteratively enhance this project by incorporating new programming concepts. The primary goal is to reinforce your understanding of fundamental C++ concepts and gradually apply them to create a more complex and functional program.

## Objectives
1. Given a programming problem, students will be able to demonstrate the ability to break down complex programming problems into smaller, manageable components with complete accuracy.
2. Given a programming problem, students will be able to design and implement efficient algorithms to solve the problem with complete accuracy.
3. Studnets will be able to adhere to coding conventions, document their code effectively, provide clear explanations and comments where necessary, and use appropriate naming conventions consistently in thier code with 90% accuracy.

## Required Programming Concepts
Before diving into the project, ensure that you are familiar with the following programming concepts:

1. **Data Types:**
   - Understand the basic data types in C++ such as int, double, and string.
   - Explore the usage of data types in variable declarations and assignments.
   - Must use at least 3 different types.

2. **File Input/Output:**
   - Learn to read from and write to files using ifstream and ofstream classes.
   - Understand file handling concepts to persistently store and retrieve data.
   - Should incorporate either reading from or writing to a file.

3. **If/Else Statements:**
   - Grasp the fundamentals of conditional statements using if/else.
   - Implement decision-making logic based on certain conditions.
   - Should include error-checking as well as other uses of the if and/or if-else statements. 
   - The use of a switch is optional.

Now that you have a foundational understanding of these concepts, let's apply them to a practical project!



## Example Project Description:

**Title: Personal Finance Tracker**

**Description:**
In this project, I will create a simple personal finance tracker using C++. The program should allow users to input their daily expenses, categorize them, and generate a summary report. This will involve the use of different data types for storing information, file input/output for saving and loading data, and if/else statements to implement decision-making logic.


**Requirements:**

1. **User Input:**
   - Implement a user-friendly input system to capture daily expenses. Prompt the user for details such as expense amount, category, and date.
   - Use appropriate data types (e.g., int, double, string) to store different aspects of the expense information.

2. **Data Storage:**
   - Create a file to store the expense data persistently. Each entry should be stored with details like amount, category, and date.
   - Utilize file input/output operations (ifstream and ofstream) to read from and write to the file.

3. **Expense Categorization:**
   - Implement if/else statements to categorize expenses based on user-defined criteria. For example, categorize expenses as "Food," "Transportation," "Entertainment," etc.

4. **Summary Report:**
   - Develop a function to generate a summary report that displays the total expenses for each category. Ensure proper formatting for readability.

5. **User Interaction:**
   - Implement a user menu that allows users to input new expenses, view the summary report, and exit the program.

6. **Error Handling:**
   - Include if/else statements to handle potential errors, such as invalid user input or file reading errors.

## Submission Guidelines:

1. **Project Description:**
    - Submit a project description follows the example above. Your project can be on any topic that you choose. 
    - Submit on GitHub in a file called `DESCRIPTION.md`
2. **Progress Report:**
    - Submit a list of features completed as well as any questions you have on your project development. This is completed on Canvas.
3. **Final Submission:**
    - Submit your final version of the code and documents. Your submission should include:
      1. Table of Contents
      1. Statement of Independent Effort
      1. Analysis of Specifications/IPO Chart
      1. Pseudocode
      1. Flowchart
      1. Test Cases
      1. Code
      1. User Manual

### Template Files
- [User Manual](GUIDE.md)
- [Submission Template](PROJECT_SUB_TEMPLATE.md)

#### Notes:

Analysis of specifications is where you identify the inputs, outputs, and processes performed by the code. An example process in a blackjack game would be "generate a random card for the user". This section must contain an IPO chart for each function. Remember that your test cases should include edge cases (values near the upper and lower bounds of the allowed values), and acceptable and unacceptable values. Produce at least 5 unique cases.

***Hint:*** Spend time thinking about all the ways a user may enter invalid information.
