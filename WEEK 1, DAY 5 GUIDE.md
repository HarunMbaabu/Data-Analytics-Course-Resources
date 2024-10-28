### Day 4: Microsoft Excel Training - Class Notes

#### Objective
To learn intermediate Excel functions for data analysis, including COUNTIF, SUMIF, and AVERAGEIF. We’ll also cover basic date and text functions.

---

#### Overview of Conditional Functions (COUNTIF, SUMIF, AVERAGEIF)
Conditional functions allow you to apply criteria or conditions in calculations.

##### COUNTIF Function
COUNTIF counts the number of cells in a range that meet a specific condition.

```excel
=COUNTIF(range, criteria)
```
- range: The cells to check.
- criteria: The condition to count.

**Example:**  
To count the number of cells containing "Apple" in cells A1:A10:

```excel
=COUNTIF(A1:A10, "Apple")
```

##### SUMIF Function
SUMIF adds values in a range that meet a specific condition.

```excel
=SUMIF(range, criteria, [sum_range])
```
- range: The cells to check for the condition.
- criteria: The condition to sum.
- sum_range: The cells to sum if the condition is met.

**Example:**  
To sum sales of "Apple" in column B based on products in column A:

```excel
=SUMIF(A1:A10, "Apple", B1:B10)
```

##### AVERAGEIF Function
AVERAGEIF calculates the average of values in a range that meet a specific condition.

```excel
=AVERAGEIF(range, criteria)
```
- range: The cells to check for the condition.
- criteria: The condition to average.

**Example:**  
To find the average sales of "Apple" based on products in column A and sales in column B:

```excel
=AVERAGEIF(A1:A10, "Apple")
```

---

#### 3. Date Functions (TODAY and NOW)
Excel’s date functions are useful for tracking dates and times.

##### TODAY Function
The TODAY function returns the current date.

```excel
=TODAY()
```
**Example:**  
Entering =TODAY() will display today’s date. This updates automatically each day.

##### NOW Function
The NOW function returns the current date and time.

**Example:**  
Entering =NOW() will display the current date and time, which updates in real time.

---

#### 4. Text Functions
Text functions help you manipulate and format text data in Excel.

##### CONCAT Function
The CONCATENATE function combines text from multiple cells into one cell.

**Syntax:**
```excel
=CONCATENATE(text1, text2, ...)
```

**Example:**  
To combine first names in cell A1 with last names in cell B1:

```excel
=CONCAT(A1, " ", B1)
```

##### UPPER, LOWER, and PROPER Functions
These functions help change the case of text.
- UPPER: Converts text to uppercase.
  
  ```excel
  =UPPER(text)
  ```

- LOWER: Converts text to lowercase.

  ```excel
  =LOWER(text)
  ```

- PROPER: Capitalizes the first letter of each word.

  ```excel
  =PROPER(text)
  ```

**Examples:**
- =UPPER("apple") returns "APPLE".
- =LOWER("APPLE") returns "apple".
- =PROPER("john smith") returns "John Smith".
