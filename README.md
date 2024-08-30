# Cnic_Text_Detection
# SED & AWK Practice Problem

## Problem Statement

You have been given a dataset named `employees.txt` which contains information about the employees of a company. Each row of the dataset contains the following information in the order given below:

- Employee ID
- Employee Name
- Employee Age
- Employee Department
- Employee Salary

Your task is to use `SED` and `AWK` commands in a Bash script to perform the following operations:

1. Replace all occurrences of the word "Software" in the "Employee Department" field with "IT".
2. Remove all rows where the "Employee Age" field is less than 30.
3. Calculate the average salary of employees in each department.
4. Save the updated dataset in a new file named `updated_employees.txt`.

## Dataset

Here is the dataset you will used

text:
101,John Smith,25,Software,50000
102,Jane Doe,30,Marketing,60000
103,Bob Johnson,28,Software,55000
104,Alice Wong,32,HR,65000
105,James Davis,26,Software,52000
106,Sarah Lee,35,Marketing,70000
107,David Brown,29,Software,58000
108,Lisa Jones,27,HR,62000
109,Michael Kim,31,Software,60000
110,Amy Patel,33,Marketing,75000

## Solution

### Bash Script

The script `process_employees.sh` performs the required operations using `SED` and `AWK`.

### Script Details

1. **Replace "Software" with "IT":**
   - Uses `sed` to replace "Software" with "IT" in the Employee Department field.

2. **Remove rows where the Employee Age is less than 30:**
   - Uses `awk` to filter out employees with an age less than 30.

3. **Calculate the average salary of employees in each department:**
   - Uses `awk` to compute the average salary for each department and prints it.

4. **Save the updated dataset:**
   - The final filtered data is saved in `updated_employees.txt`.

### Script Execution

To run the script, follow these steps:

1. **Create the dataset file:**
   - Save the dataset in a file named `employees.txt`.

2. **Create the script file:**
   - Create a file named `process_employees.sh` and add the script provided below.

3. **Make the script executable:**
   - Run the command:
     ```bash
     chmod +x process_employees.sh
     ```

4. **Run the script:**
   - Execute the script with:
     ```bash
     ./process_employees.sh
     ```

### Expected Output

**`updated_employees.txt`:**
```plaintext
102,Jane Doe,30,Marketing,60000
104,Alice Wong,32,HR,65000
106,Sarah Lee,35,Marketing,70000
108,Lisa Jones,27,HR,62000
109,Michael Kim,31,IT,60000

