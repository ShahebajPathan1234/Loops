Python Programming Guide: Various Functions and Examples
1. Pyramid Pattern
Code:
# Pyramid Pattern
rows = int(input("Enter the number of rows: "))
for i in range(1, rows + 1):
    print(" " * (rows - i) + "*" * (2 * i - 1))
Explanation:
Purpose: This code generates a pyramid pattern using asterisks (*) based on the number of rows provided by the user.
input() function: It takes user input for the number of rows.
range(1, rows + 1) loop: This loop iterates through each row of the pyramid. For each iteration, it calculates the number of spaces (" " * (rows - i)) and stars ("*" * (2 * i - 1)) needed for that row.
Example:
If you input 5 as the number of rows, the output will be:

    *
   ***
  *****
 *******
*********
Functions Used:
input(): Used to get user input as a string. This is then converted to an integer using int().
String Multiplication (*): Used to generate repeated spaces and stars.
2. Prime Number Checker
Code:
# Prime Number Checker
number = int(input("Enter a number: "))
is_prime = True

if number > 1:
    for i in range(2, int(number ** 0.5) + 1):  # Check divisibility up to sqrt(number)
        if number % i == 0:
            is_prime = False
            break
else:
    is_prime = False

if is_prime:
    print(f"{number} is a prime number.")
else:
    print(f"{number} is not a prime number.")
Explanation:
Purpose: The code checks if a number is prime.
Prime Check: A prime number is greater than 1 and divisible only by 1 and itself. This check is performed by trying to divide the number by all integers from 2 to sqrt(number).
% (Modulo Operator): Used to check if a number is divisible by another. If the remainder is 0, then the number is not prime.
Example:
If you input 29, the output will be:

29 is a prime number.
3. Factorial Calculator
Code:
# Factorial Calculator
number = int(input("Enter a number: "))
factorial = 1
for i in range(1, number + 1):
    factorial *= i
print(f"The factorial of {number} is {factorial}.")
Explanation:
Purpose: This code calculates the factorial of a given number.
Factorial: The factorial of n is the product of all positive integers from 1 to n.
for loop: Iterates over each integer from 1 to n and multiplies them to get the factorial.
Example:
If you input 5, the output will be:

The factorial of 5 is 120.
4. Fibonacci Sequence Generator
Code:
# Fibonacci Sequence Generator
terms = int(input("Enter the number of terms: "))
a, b = 0, 1
print("Fibonacci Sequence:")
for _ in range(terms):
    print(a, end=" ")
    a, b = b, a + b
Explanation:
Purpose: Generates the Fibonacci sequence up to a specified number of terms.
Fibonacci Sequence: The sequence starts with 0 and 1, and each subsequent number is the sum of the previous two.
a, b = b, a + b: Swaps and updates the variables to generate the next term in the sequence.
Example:
If you input 6, the output will be:

Fibonacci Sequence:
0 1 1 2 3 5
5. Interactive Menu
Code:
# Interactive Menu
while True:
    print("\nMenu:")
    print("1. Say Hello")
    print("2. Add Two Numbers")
    print("3. Exit")
    choice = int(input("Enter your choice: "))

    if choice == 1:
        print("Hello!")
    elif choice == 2:
        a = int(input("Enter first number: "))
        b = int(input("Enter second number: "))
        print(f"The sum is {a + b}.")
    elif choice == 3:
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please try again.")
Explanation:
Purpose: An interactive menu that allows the user to choose between different options.
while True: Keeps the program running in a loop until the user selects the exit option.
if, elif, else: Used to handle user choices and execute corresponding actions.
Example:
If you select option 2, the program will ask for two numbers and then output the sum.

Enter first number: 3
Enter second number: 4
The sum is 7.
6. Sum, Max, and Frequency in a List
Code:
# Sum, Max, and Frequency in a List
numbers = [1, 4, 4, 7, 8, 4, 9, 2]
print("List:", numbers)
print("Sum of elements:", sum(numbers))
print("Maximum element:", max(numbers))
freq = numbers.count(4)
print("Frequency of 4:", freq)
Explanation:
Purpose: This code demonstrates how to calculate the sum, maximum value, and frequency of an element in a list.
sum(): Calculates the sum of all elements in the list.
max(): Returns the maximum value from the list.
count(): Counts the occurrences of a specific element in the list.
Example:
The output for the list [1, 4, 4, 7, 8, 4, 9, 2] will be:

List: [1, 4, 4, 7, 8, 4, 9, 2]
Sum of elements: 39
Maximum element: 9
Frequency of 4: 3
Summary of Functions:
input(): Reads input from the user.
int(): Converts input or variables to an integer.
for loop: Used for iteration over a range or list.
sum(), max(), count(): Built-in Python functions for calculating the sum, maximum, and frequency of items in a list.
% (Modulo): Used to check for divisibility.
String multiplication: Used to create repeated characters (e.g., spaces or asterisks).
