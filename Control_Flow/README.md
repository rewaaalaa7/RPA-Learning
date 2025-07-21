# Leap Year Checker

## Overview
The Leap Year Checker is a UiPath automation project that checks whether a user-entered year is a leap year. It implements the leap year logic in two workflows:
- A **Sequence workflow** using an If activity for linear conditional logic.
- A **Flowchart workflow** using a Flow Decision activity for visual branching.

The project uses a single variable, `Year` (Int32), collected via an input dialog, and displays the result (leap year or not) in a message box.

## Purpose
The purpose of this project is to:
- Accept a user-entered year (`Year`) via an Input Dialog activity.
- Evaluate the leap year condition: `(Year Mod 4 = 0 AndAlso Year Mod 100 <> 0) OrElse (Year Mod 400 = 0)`.
- Demonstrate the use of conditional logic in UiPath with both Sequence and Flowchart workflows.
- Display the result in a user-friendly message box indicating whether the input year is a leap year.

## Logic Used to Determine Leap Year
A year is a **leap year** if:
- It is divisible by 4, **and**
  - Not divisible by 100 **unless** it is also divisible by 400.

This can be expressed as:
```vb
(Year Mod 4 = 0 And Year Mod 100 <> 0) Or (Year Mod 400 = 0)
```

## Project Structure
The project consists of two workflows:

# 1. Sequence Workflow (MainSequence.xaml)
- Input: Prompts the user to enter a year using an Input Dialog activity.
- Variable: Stores the input in Year (Int32).
- Logic: Uses an If activity to evaluate the leap year condition:
- Condition: (Year Mod 4 = 0 AndAlso Year Mod 100 <> 0) OrElse (Year Mod 400 = 0)
- Then: Displays a Message Box: "Year [Year] is a leap year."
- Else: Displays a Message Box: "Year [Year] is not a leap year."


# 2.Flowchart Workflow (Leap_Year.xaml)
- Input: Prompts the user to enter a year using an Input Dialog activity.
- Variable: Stores the input in Year (Int32).
- Logic: Uses a Flow Decision activity to evaluate the leap year condition:
- Condition: (Year Mod 4 = 0 AndAlso Year Mod 100 <> 0) OrElse (Year Mod 400 = 0)
- True Branch: Connects to a Message Box: "Year [Year] is a leap year."
- False Branch: Connects to a Message Box: "Year [Year] is not a leap year."

## Main Sequence 
![Main](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Control_Flow/Leap%20Year%20using%20if%20and%20else.jpg)

## Workflow 
![Workflow](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Control_Flow/Leap_Year.jpg)

## Output 
![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Control_Flow/output1.jpg)
![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Control_Flow/output2.jpg)


