# Arrays of Strings 

This project demonstrates how to work with **arrays of strings** in UiPath. It is part of my RPA learning path and showcases basic string operations inside a workflow.

---

## What This Project Does

- Creates an array of strings (e.g., names or items).
- Displays each string element individually using a loop.
- Combines all array elements into a single string using `String.Join`.
- Displays the combined result.

---
## Main Activities Used

1. Assign Activity  
Used to initialize the array of strings:
stringArray = {"john", "sara"}

Then, I edited the first element of the array:
stringArray(0) = "kyle"

2. For Each Activity  
Used to loop through each string in the array and print it using the Write Line activity.

3. String.Join Function  
Used to join all array elements into a single string:
String.Join(", ", stringArray)

Output:
kyle, sara

4. Write Line Activity  
Used to display:
- Each string during the loop.
- The final combined string after using String.Join.


## Main Sequence 
![Sequence](https://github.com/rewaaalaa7/RPA-Learning/blob/main/arrays/Arrays.jpg)

## Output

![Output](https://github.com/rewaaalaa7/RPA-Learning/blob/main/arrays/output.jpg)

## How to Run

1. Open Main.xaml in UiPath Studio.
2. Run the workflow.
3. Check the Output panel for printed results.
