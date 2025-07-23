# Simple Interest Calculator

## Overview
The Simple Interest Calculator is a workflow-based automation project that calculates the simple interest earned on an initial deposit over a specified period at a fixed annual interest rate of 1.75%. The project uses two workflows: a **Main workflow** for user interaction and a **Calculation workflow** for computing the interest. This project demonstrates modular workflow design, user input handling, and result display in an automation tool like UiPath.

## Purpose
The purpose of this project is to:
- Collect user inputs for the initial deposit amount and time period (1, 3, or 5 years).
- Calculate the simple interest using the formula: `Simple Interest = (DepositAmount × Rate × Period) / 100`.
- Display the accumulated interest and final balance (initial deposit + interest) in a user-friendly message box.
- Showcase modular design by separating calculation logic from user interaction.

## Project Structure
The project consists of two workflows:

1. **Calculation Workflow (`Simple_Interest_Logic.xaml`)**
   - **Purpose**: Computes the simple interest based on user inputs.
   - **Input Arguments**:
     - `In_Deposit` (Double): The initial deposit amount (e.g., $1000).
     - `In_Period` (Integer): The time period in years (1, 3, or 5).
   - **Output Argument**:
     - `Out_SI` (Double): The calculated interest.
   - **Logic**:
     - Uses the formula: `Out_SI = (In_Deposit × 1.75 × in_Period) / 100`.
     - The interest rate is fixed at 1.75% for all periods.
   - **Role**: Performs the core calculation and returns the result to the Main workflow.

2. **Main Workflow (`Main.xaml`)**
   - **Purpose**: Handles user interaction, invokes the Calculation workflow, and displays results.
   - **Variables**:
     - `Deposit` (Double): Stores the user-entered deposit amount.
     - `Period` (Integer): Stores the user-selected time period (1, 3, or 5).
     - `SI` (Double): Stores the interest returned from the Calculation workflow.
     - `Result` (Double): Stores the final balance (`Depsoit + SI`).
   - **Logic**:
     - Prompts the user for the deposit amount using an input dialog.
     - Prompts the user to select a period (1, 3, or 5 years) using a multiple-choice input dialog.
     - Invokes the Calculation workflow, passing `Deposit` and `Period`, and stores the result in `SI`.
     - Calculates `Reuslt = Depsoit + SI`.
     - Displays a message box with the accumulated interest and final balance, formatted to two decimal places (e.g., "Simple Interest: $52.50, Final Balance: $1052.50").

## How It Works
1. The user runs the Main workflow.
2. The Main workflow:
   - Prompts for the initial deposit amount (e.g., $1000).
   - Prompts for the time period, offering options: 1 year, 3 years, or 5 years.
   - Stores inputs in `Deposit` and `Period`.
3. The Main workflow invokes the Calculation workflow, passing `Deposit` and `Period`.
4. The Calculation workflow:
   - Computes the simple interest using the formula with a fixed rate of 1.75%.
   - Returns the result to the Main workflow.
5. The Main workflow:
   - Calculates the final balance.
   - Displays the results in a message box.

## Example
- **Input**: Deposit = $1000, Period = 3 years
- **Calculation**:
  - Simple Interest = `(1000 × 1.75 × 3) / 100 = $52.50`
  - Final Balance = `1000 + 52.50 = $1052.50`
- **Output**: "Accumulated Interest: $52.50, Final Balance: $1052.50"

## Setup and Usage
1. **Prerequisites**:
   - An automation tool like UiPath Studio.
   - Basic knowledge of workflow creation and argument passing.

2. **Steps to Run**:
   - Clone or download the repository.
   - Open the project in your automation tool.
   - Ensure both `Main.xaml` and `CalculateSimpleInterest.xaml` are in the project folder.
   - Run the `Main.xaml` workflow.
   - Follow the prompts to enter the deposit amount and select a period.
   - View the results in the message box.

3. **Testing**:
   - Test the Calculation workflow independently with sample inputs (e.g., Deposit = $1000, Period = 3 → Interest = $52.50).
   - Test the Main workflow with various inputs to ensure correct prompts, calculations, and output formatting.
   - Verify edge cases (e.g., small deposits like $10 or the maximum period of 5 years).


## Main Sequence 
![Sequence](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/Main.jpg)

## WorkFLow
![WorkFlow](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/Simple_Interest_Logic.jpg)

## Output

![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/output1.jpg)
![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/output2.jpg)
![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/output3.jpg)
![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/Simple_Interest_Calculator/output4.jpg)


## Notes
- The interest rate is hardcoded at 1.75% as per the project requirements.
- The period is restricted to 1, 3, or 5 years via multiple-choice input to simplify validation.
- Consider adding error handling for invalid inputs (e.g., negative or non-numeric deposit amounts) to enhance robustness.
- The project uses a modular design, making the Calculation workflow reusable for other applications.
