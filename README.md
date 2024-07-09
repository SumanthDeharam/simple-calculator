# simple-calculator
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y


def calculator():
    print("Simple Calculator")
    print("Operations: +, -, *, /")

    while True:
        
        num1 = float(input("Enter the first number: "))
        operation = input("Enter the operation (+, -, *, /): ")
        num2 = float(input("Enter the second number: "))

        
        if operation == '+':
            result = add(num1, num2)
        elif operation == '-':
            result = subtract(num1, num2)
        elif operation == '*':
            result = multiply(num1, num2)
        elif operation == '/':
            result = divide(num1, num2)
        else:
            print("Invalid operation!")
            continue

        
        print(f"The result is: {result}")

      
        another = input("Do you want to perform another calculation? (yes/no): ").strip().lower()
        if another != 'yes':
            break

if __name__ == "__main__":
    calculator()
    
