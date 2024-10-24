### Introduction to Excel Formulas and Functions

## 1. Objective
By the end of this session, students should understand the basics of Excel formulas, the structure of functions, and how to use essential Excel functions such as `SUM`, `AVERAGE`, `MIN`, `MAX`, `COUNT`, and `IF`.

## 2. Introduction to Excel Formulas
Excel formulas allow you to perform calculations, manipulate data, and analyze information in your worksheets.

A formula is an equation you can enter into a cell that performs a calculation or other action. To start any formula, begin with the equal sign (`=`).

### Order of Operations
Excel follows the same mathematical order of operations (PEMDAS):
- **Parentheses**
- **Exponents**
- **Multiplication and Division** (left to right)
- **Addition and Subtraction** (left to right)

### Relative and Absolute Cell References
When creating formulas, it’s important to understand the difference between relative and absolute references:

- **Relative References**: Change based on the position of the formula. For example, if you copy the formula `=A1+B1` from cell C1 to cell C2, it will change to `=A2+B2`.
- **Absolute References**: Stay the same, no matter where the formula is copied. Absolute references are written with dollar signs (`$`). For example, `$A$1` refers to cell A1, and it won’t change if copied.

## 3. Introduction to Excel Functions
Functions are pre-built formulas that perform specific calculations. Excel has hundreds of functions, but today, we’ll focus on some of the most commonly used ones.

### Function Structure
All functions in Excel follow the same structure:
- **Equal sign (`=`)**: Tells Excel you’re entering a function.
- **Function name**: The name of the function (e.g., `SUM`, `AVERAGE`, etc.).
- **Parentheses**: Contain the function’s arguments. These are the values, cell references, or ranges of cells you want the function to operate on.

**Example**: `=SUM(A1:A5)` adds the values from cells A1 through A5.

### Common Excel Functions

#### SUM Function
The `SUM` function adds together a range of numbers.
- **Example**: `=SUM(A1:A5)` adds all the values in the range A1 to A5.

#### AVERAGE Function
The `AVERAGE` function calculates the average (mean) of a group of numbers.
- **Example**: `=AVERAGE(B1:B5)` calculates the average of the values in B1 to B5.

#### MIN and MAX Functions
The `MIN` and `MAX` functions return the smallest and largest value in a range, respectively.
- **MIN example**: `=MIN(C1:C5)` returns the smallest value in cells C1 to C5.
- **MAX example**: `=MAX(C1:C5)` returns the largest value in cells C1 to C5.

#### COUNT Function
The `COUNT` function counts the number of cells in a range that contain numbers.
- **Example**: `=COUNT(D1:D10)` counts how many cells in the range D1 to D10 contain numbers.

#### IF Function
The `IF` function checks whether a condition is true or false and returns one value if true, and another value if false.
- **Example**: `=IF(E1 > 100, "High", "Low")` checks if the value in E1 is greater than 100. If it is, the function returns "High"; if not, it returns "Low."

## 4. Hands-On Practice with Excel Functions

## 5. Additional Formula Examples
Here are some additional ways to combine functions:

- **Nested Functions**: Functions can be combined to perform more complex calculations.
  - **Example**: `=IF(AVERAGE(A1:A5) > 50, "Pass", "Fail")` returns "Pass" if the average of A1 to A5 is greater than 50, otherwise it returns "Fail."

- **SUM with IF**: You can sum values that meet specific criteria using the `IF` function inside a `SUM` formula.
  - **Example**: `=SUM(IF(A1:A5 > 50, A1:A5, 0))` adds only the values in A1 to A5 that are greater than 50.

## 6. Wrap-Up and Review
### Key Takeaways:
- **Formulas** allow you to perform calculations using values from other cells.
- **Functions** simplify common calculations like adding numbers, averaging, finding minimums and maximums, counting, and more.
- Using functions like `SUM`, `AVERAGE`, `MIN`, `MAX`, `COUNT`, and `IF` can greatly speed up your workflow in Excel.
- **Absolute and relative references** help control how cell references behave when formulas are copied.
