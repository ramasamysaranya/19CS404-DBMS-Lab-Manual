# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

# code
```

SET SERVEROUTPUT ON;

DECLARE
    a NUMBER := 50;
    b NUMBER := 80;
BEGIN
    IF a > b THEN
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || a);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || b);
    END IF;
END;

```
**Expected Output:**  
Greater number is: 80

 ### output:
 <img width="816" height="221" alt="image" src="https://github.com/user-attachments/assets/ee897496-05a9-4a66-bb60-8afdd53f3c9b" />


## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.
### code:
```

SET SERVEROUTPUT ON;

DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    s NUMBER := 0;
BEGIN
    WHILE i <= n LOOP
        s := s + i;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE(
        'Sum of first ' || n || ' natural numbers is: ' || s
    );
END;
```

**Expected Output:**  
Sum of first 10 natural numbers is: 55
### output:
<img width="707" height="280" alt="image" src="https://github.com/user-attachments/assets/0987cb3c-09a8-4850-85a0-0f40ace4c0f0" />


## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

### code:
```

SET SERVEROUTPUT ON;

DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    s NUMBER := 0;
BEGIN
    WHILE i <= n LOOP
        s := s + i;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE(
        'Sum of first ' || n || ' natural numbers is: ' || s
    );
END;

```


**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

### output:
<img width="746" height="247" alt="image" src="https://github.com/user-attachments/assets/6ba04c0a-8a31-4885-a0de-e9588a09f44e" />


## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.
### code:
```

SET SERVEROUTPUT ON;

DECLARE
    n NUMBER := 1535;
    temp NUMBER := n;
    rev NUMBER := 0;
    digit NUMBER;
BEGIN
    WHILE temp > 0 LOOP
        digit := MOD(temp, 10);
        rev := rev * 10 + digit;
        temp := TRUNC(temp / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('n = ' || n);
    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
END;
```


**Expected Output:**  
n = 1535  
Reversed number is 5351

### output:
<img width="707" height="243" alt="image" src="https://github.com/user-attachments/assets/2e457b4a-671c-4498-ab04-9ca62e98013e" />


## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

### code:
```

SET SERVEROUTPUT ON;

DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    IF a >= b AND a >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || a);
    ELSIF b >= a AND b >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || c);
    END IF;
END;
```

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

### output:
<img width="572" height="265" alt="image" src="https://github.com/user-attachments/assets/fb99de45-b814-4c96-a9ad-c693aeadbdaf" />

## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
