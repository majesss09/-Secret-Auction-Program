# 💰 Secret Auction Program

A simple **Python console application** that simulates a *secret auction* where participants place hidden bids.  
When all bids are collected, the program determines and displays the highest bidder.  

This project demonstrates key Python concepts like loops, conditionals, and dictionaries — all wrapped in a fun, interactive experience.

---

## 🖼️ ASCII Art Logo

The program displays this logo when it starts:

                     ___________
                     \         /
                      )_______(
                      |"""""""|_.-._,.---------.,_.-._
                      |       | | |               | | ''-.
                      |       |_| |_             _| |_..-'
                      |_______| '-' `'---------'` '-'
                      )"""""""(
                     /_________\\
                   .-------------.
                  /_______________\\


---

## 🧠 Features
- Accepts multiple bidders’ names and bids  
- Keeps bids **secret** by clearing the console (simulated with blank lines)  
- Automatically finds the **highest bidder**  
- Simple and beginner-friendly Python implementation  

---

## 💻 Code Overview
```python
from art import logo

print(logo)
print("Welcome to the secret auction program.")
bidders = {}
more_bidders = "yes"

while more_bidders == "yes":
    name = input("What is your name?: ")
    bid = float(input("What's your bid?: $"))
    bidders[name] = bid
    more_bidders = input("Are there any other bidders? Type 'yes' or 'no'.\n")
    print("\n" * 20)

winner = ["name", 0]
for key in bidders:
    if bidders[key] >= winner[1]:
        winner[0] = key
        winner[1] = bidders[key]

print(f"The winner is {winner[0]}, with a bid of ${winner[1]}.")
```
🧮 Example Output

Welcome to the secret auction program.

What is your name?: Alice

What's your bid?: $250

Are there any other bidders? Type 'yes' or 'no'.

yes

What is your name?: Bob

What's your bid?: $300

Are there any other bidders? Type 'yes' or 'no'.

no

The winner is Bob, with a bid of $300.

