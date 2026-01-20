# Project 2
## Tip Calculator

A simple command-line tip calculator I built while learning Python. It calculates tips, totals, and splits bills between people.

## What It Does

- Takes a bill amount
- Calculates tip based on percentage (10%, 12%, or 15%)
- Splits the total evenly between multiple people
- Shows how much each person pays

## Requirements

- Python 3.x

That's it. No fancy libraries needed.

## How to Run
```bash
python3 tip_calculator.py
```

Or on Windows:
```bash
python tip_calculator.py
```

## Example
```text
Welcome to the tip calculator!
What was the total bill? $150
What percentage tip would you like to give? 10 12 15 15
How many people to split the bill? 3
Each person should pay: $57.50
```

## How It Works

The code is pretty straightforward:
```python
print("Welcome to the tip calculator!")
bill = float(input("What was the total bill? $"))
tip = int(input("What percentage tip would you like to give? 10 12 15 "))
people = int(input("How many people to split the bill? "))

total = round(((bill / people) * float(tip / 100 + 1)), 2)

print(f"Each person should pay: ${total:.2f}")
```

1. Gets bill amount from user
2. Gets tip percentage (expects 10, 12, or 15)
3. Gets number of people splitting
4. Calculates per-person cost including tip
5. Rounds to 2 decimal places

## Notes

- Enter bill as a number (like `150` or `150.00`)
- Tip should be a whole number (10, 12, or 15)
- Number of people must be at least 1

## What I Learned

- Using `input()` to get user input
- Converting strings to floats and ints
- Doing calculations with percentages
- Rounding numbers with `round()`
- Formatting output with f-strings

## Potential Improvements

If I expand this project, I might:
- Add input validation (what if someone enters negative numbers?)
- Allow custom tip percentages
- Show the tip amount separately from the total
- Add tax calculation
- Handle edge cases (like 0 people or empty inputs)

---

*Day 2 learning project - built to practice Python basics*
