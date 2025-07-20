# Summing Two Arguments

This UiPath project demonstrates how to:

- Create a workflow (`CalculateSum.xaml`) that accepts **two integer arguments**.
- Perform their summation within that workflow.
- Use `Invoke Workflow File` in `Main.xaml` to pass values and get the result.

---
## CalculateSum.xaml

This workflow performs the following:

- Accepts:
  - `In_FirstValue` (`In`, `Double`)
  - `In_SecondValue` (`In`, `Double`)
- Returns:
  - `OutSum` (`Out`, `Double`) → result of summation
  - `IO_ExecutionInfo` (`In/Out`, `String`) → logs the operation performed

## Main.xaml

This is the main controller file that:

1. **Initializes values:**
   - `In_FirstValue = 50.2`
   - `In_SecondValue = 30.5`

2. **Invokes** `CalculateSum.xaml`:
   - Maps the variables to the respective arguments:
     - `In_FirstValue` → `In_FirstValue`
     - `In_SecondValue` → `In_SecondValue`
     - Receives output via `OutSum`
     - Optionally updates `IO_ExecutionInfo` for logging

3. **Displays or logs** the result (`OutSum`).

## Main Sequence 
![Sequence](https://github.com/rewaaalaa7/RPA-Learning/blob/main/arguments/Main%20Sequence.jpg)

## Workflow 
![Workflow](https://github.com/rewaaalaa7/RPA-Learning/blob/main/arguments/Calculate_Sum_Workflow.jpg)

## Output

![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/arguments/output.jpg)

## How to Run

1. Open the project in UiPath Studio.
2. Open `Main.xaml`.
3. Run the workflow.
4. Check the output from `OutSum` (e.g., in a Message Box or Log panel).

## Notes

- Make sure both `Main.xaml` and `CalculateSum.xaml` are in the same project folder.
- You can modify `In_FirstValue` and `In_SecondValue` in `Main.xaml` to test different inputs.
