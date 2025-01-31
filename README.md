# CODTECH-TASKS
import turtle

# Function to perform the calculation
def calculate():
    # Clear previous drawings
    turtle.clear()

    # Get user input for two numbers
    num1 = turtle.numinput("Input", "Enter the first number:-", minval=-10000, maxval=10000)
    num2 = turtle.numinput("Input", "Enter the second number:-", minval=-10000, maxval=10000)

    # Display operations for the user to choose
    operations = "Choose an operation:\n1. Addition (+)\n2. Subtraction (-)\n3. Multiplication (*)\n4. Division (/)"
    operation = turtle.textinput("Operation", operations)

    # Perform the selected operation
    if operation == '1' or operation == '+':
        result = num1 + num2
        operation_symbol = '+'

    elif operation == '2' or operation == '-':
        result = num1 - num2
        operation_symbol = '-'

    elif operation == '3' or operation == '*':
        result = num1 * num2
        operation_symbol = '*'

    elif operation == '4' or operation == '/':
        if num2 != 0:
            result = num1 / num2
            operation_symbol = '/'
        else:
            result = "Error! Division by zero."
            operation_symbol = '/'

    else:
        result = "Invalid operation selected."
        operation_symbol = ''

    # Display the result with attractive colors
    turtle.color("white")
    turtle.write(f"Result: {num1} {operation_symbol} {num2} = {result}", align="center", font=("Arial", 16, "bold"))

# Set up the turtle screen with a background color
turtle.setup(600, 500)
turtle.title("Simple Calculator")
turtle.bgcolor("midnight blue")

# Create a turtle object for displaying the result
turtle.hideturtle()
turtle.speed(0)
turtle.penup()
turtle.goto(0, 0)

# Run the calculator function
calculate()

# Keep the window open until the user closes it
turtle.done()
