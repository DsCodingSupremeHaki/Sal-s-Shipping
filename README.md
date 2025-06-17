# Sal-s-Shipping

---

# 📦 Sal's Shipping

This Python script calculates the cost of shipping packages using different methods offered by Sal's Shipping. It demonstrates how shipping rates can vary based on package weight and the chosen service.

---

## How It Works

The script contains logic to determine shipping costs for:

* **Standard Ground Shipping:** Rates vary by weight, plus a flat rate.
* **Ground Shipping Premium:** A fixed, higher cost for expedited ground service.
* **Drone Shipping:** Rates are calculated solely based on package weight.

The script currently has a hardcoded package weight for both ground and drone shipping, and it will output the calculated cost for each. It also includes some fun ASCII art of a drone!

---

## Getting Started

### Prerequisites

You'll need **Python 3** installed on your computer to run this script.

### Installation

No special installation is required. Just save the code to a `.py` file.

1.  **Save the code:** Copy the entire code block provided and save it as `sals_shipping.py` (or any other name ending with `.py`) on your computer.

---

## Usage

1.  **Open your terminal or command prompt.**
2.  **Navigate to the directory** where you saved `sals_shipping.py`.
    ```bash
    cd path/to/your/project
    ```
3.  **Run the script** using Python:
    ```bash
    python sals_shipping.py
    ```
4.  The script will immediately print the calculated shipping costs for the predefined `weightForGround` and `weightForDrone` variables.

### Modifying Package Weights

To see how the shipping costs change for different package weights, you can directly edit the script:

* Change the value of `weightForGround` on line 1:
    ```python
    weightForGround = 15 # Example: set to 15 lbs
    ```
* Change the value of `weightForDrone` on line 2:
    ```python
    weightForDrone = 8 # Example: set to 8 lbs
    ```
    After making changes, save the file and run the script again.

---

## Code

Here's the complete code for the Sal's Shipping project:

```python
weightForGround = 41
weightForDrone = 41

# Ground shipping
groundShippingPremium = 125.00
flatRate = 20.00
if 2 >= weightForGround:
    print("Ground Shipping: $", flatRate + 1.50 * weightForGround)
elif 2 < weightForGround and 6 >= weightForGround:
    print("Ground Shipping: $", flatRate + 3.00 * weightForGround)
elif 6 < weightForGround and 10 >= weightForGround:
    print("Ground Shipping: $", flatRate + 4.00 * weightForGround)
else:
    print("Ground Shipping: $", flatRate + 4.75 * weightForGround)

print("Ground Shipping Premium: $", groundShippingPremium)

# Drone Shipping
if 2 >= weightForDrone:
    print("Drone Shipping: $", 4.50 * weightForDrone)
elif 2 < weightForDrone and 6 >= weightForDrone:
    print("Drone Shipping: $", 9.00 * weightForDrone)
elif 6 < weightForDrone and 10 >= weightForDrone:
    print("Drone Shipping: $", 12.00 * weightForDrone)
else:
    print("Drone Shipping: $", 14.25 * weightForDrone)

# ASCII Art Of Drone - This section is for visual representation and not part of the shipping calculations.
print('')
print("D D D D D      D D D D D")
print("    D            D    ")
print("    D   D D D D  D    ")
print("    D D D D D D D D   ")
print("        D D D D       ")
print("          D D         ")
```

---

## Learning Context & Credits

This project was developed as part of the **"Computer Science Path"** curriculum on [Codecademy](https://www.codecademy.com/). It served as an excellent exercise to practice **conditional logic** (`if/elif/else` statements) and basic **arithmetic operations** in Python.

---

## Future Enhancements (Ideas for Improvement)

This project lays a solid foundation. Here are some ideas to expand its functionality:

* **User Input:** Allow the user to input the package weight directly when running the script, rather than modifying the code.
* **Function Abstraction:** Create separate functions for each shipping method (e.g., `calculate_ground_shipping(weight)`, `calculate_drone_shipping(weight)`) to make the code more organized and reusable.
* **Find Cheapest Method:** Add logic to compare the costs of all available shipping methods for a given weight and recommend the cheapest option.
* **Error Handling:** Implement checks to ensure valid input (e.g., positive numbers for weight).
* **More Shipping Options:** Introduce additional shipping methods or delivery speeds.

---
