# Calculator
#Code for my calculator app
#This Repo is for my calculator project in fulfilment of Week 8 of The Skills Network Level 3 Software development Skills Bootcamp.

class SimpleCalculator:
    def __init__(self):
        self.history = []

    def add(self, a, b):
        result = a + b
        self.history.append(f"{a} + {b} = {result}")
        return result

    def subtract(self, a, b):
        result = a - b
        self.history.append(f"{a} - {b} = {result}")
        return result

    def multiply(self, a, b):
        result = a * b
        self.history.append(f"{a} * {b} = {result}")
        return result

    def divide(self, a, b):
        if b == 0:
            return "Error: Division by zero is not allowed."
        result = a / b
        self.history.append(f"{a} / {b} = {result}")
        return result

    def show_history(self):
        if not self.history:
            return "No history yet."
        return "\n".join(self.history)

# Example usage:
calculator = SimpleCalculator()
print(calculator.add(10, 5))
print(calculator.subtract(10, 5))
print(calculator.multiply(10, 5))
print(calculator.divide(10, 5))
print(calculator.divide(10, 0))  # Division by zero example
print("History:")
print(calculator.show_history())

