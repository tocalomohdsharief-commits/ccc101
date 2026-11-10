# Quick Activity 1: School Supplies Calculator

**Name:** Mohammad Sharief N. Tocalo

**Section:** CCC101/BSCA

### Scenario Overview

A folder costs **₱25**, and a highlighter costs **₱30**. A student buys several folders and highlighters and pays a certain amount. The following solution shows the analysis, pseudocode, and dry-run calculations to find the total cost and change.

### 1. Problem Analysis

* **Inputs:**

  * Number of folders (`num_folders`)

  * Number of highlighters (`num_highlighters`)

  * Payment amount (`payment`)

* **Processes:**

  1. Calculate the total cost for folders by multiplying the quantity by 25.

  2. Calculate the total cost for highlighters by multiplying the quantity by 30.

  3. Add the total folder cost and total highlighter cost to get the overall total cost.

  4. Subtract the overall total cost from the payment amount to get the change.

* **Outputs:**

  * Total cost (`total_cost`)

  * Change (`change`)

### 2. Step-by-Step Order of Tasks

1. Ask for the quantity of folders, highlighters, and payment amount.

2. Calculate total folder cost = `num_folders * 25`.

3. Calculate total highlighter cost = `num_highlighters * 30`.

4. Calculate total cost = `total_folder_cost + total_highlighter_cost`.

5. Calculate change = `payment - total_cost`.

6. Display the total cost and change.

### 3. Pseudocode

```
START
    // Declare prices
    SET folder_price = 25
    SET highlighter_price = 30

    // Get input values
    DISPLAY "Enter number of folders:"
    INPUT num_folders

    DISPLAY "Enter number of highlighters:"
    INPUT num_highlighters

    DISPLAY "Enter payment amount:"
    INPUT payment

    // Perform calculations
    SET folder_total = num_folders * folder_price
    SET highlighter_total = num_highlighters * highlighter_price
    SET total_cost = folder_total + highlighter_total
    SET change = payment - total_cost

    // Output results
    DISPLAY "Total Cost: ₱", total_cost
    DISPLAY "Change: ₱", change
END
```

### 4. Dry Run Calculations

#### **Test Case 1**

* **Given Inputs:**

  * Folders = 4

  * Highlighters = 2

  * Payment = ₱200

* **Step-by-step Calculations:**

  * `folder_total` = 4 \* ₱25 = **₱100**

  * `highlighter_total` = 2 \* ₱30 = **₱60**

  * `total_cost` = ₱100 + ₱60 = **₱160**

  * `change` = ₱200 - ₱160 = **₱40**

* **Final Outputs:**

  * **Total Cost:** ₱160

  * **Change:** ₱40

#### **Test Case 2**

* **Given Inputs:**

  * Folders = 2

  * Highlighters = 4

  * Payment = ₱250

* **Step-by-step Calculations:**

  * `folder_total` = 2 \* ₱25 = **₱50**

  * `highlighter_total` = 4 \* ₱30 = **₱120**

  * `total_cost` = ₱50 + ₱120 = **₱170**

  * `change` = ₱250 - ₱170 = **₱80**

* **Final Outputs:**

  * **Total Cost:** ₱170

  * **Change:** ₱80