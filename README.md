# 🧮 Simple Calculator (CLI)

This is a simple Python calculator that supports **addition, subtraction, multiplication, and division**.

## 🚀 Code

```python
def add(x, y):
    return x+y
def sub(x, y):
    return x-y
def mul(x, y):
    return x*y
def divide(x, y):
    try:
        return x/y
    except ZeroDivisionError:
        return "Error: Zero Division Error"

print("==simple calculator==")

while True:
    print("\n choose operation + - * / (or 'q' to quit)")
    op=input("enter operator:")

    if op.lower()=='q':
        print("exiting--Goodbye")
        break
    try:
        x=float(input("enter first number:"))
        y=float(input("enter second number:"))
    except ValueError:
        print("Invalid Number,try again")
        continue

    if op=='+':
        result=add(x,y)
    elif op=='-':
        result=sub(x,y)
    elif op=='*':
        result=mul(x,y)
    elif op=='/':
        result= divide(x,y)
    else:
        result="invalid operator"

    print("Result:",result)
    input("press enter if you want to continue")

#🎯 Sample Output:

==simple calculator==

 choose operation + - * / (or 'q' to quit)
enter operator:+
enter first number:10
enter second number:5
Result: 15.0
