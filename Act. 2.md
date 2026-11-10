# Quick Activity 2: Canteen Group Order

**Name:** Mohammad Sharief N. Tocalo

**Section:** CCC101/BSCA

### Scenario Overview

A canteen sells **noodle bowls at ₱90 each** and **iced teas at ₱30 each**. Every order gets a **15% discount on the noodle bowl subtotal only**. The canteen also adds a **₱10 eco-box fee per noodle bowl**. This activity shows the problem analysis, ordered tasks, pseudocode, dry runs, and a short explanation for calculating the final bill and change.

### 1. Problem Analysis

* **Inputs:**

  * Number of noodle bowls (`num_bowls`)

  * Number of iced teas (`num_teas`)

  * Payment amount (`payment`)

* **Processes:**

  1. Calculate noodle bowl subtotal: `num_bowls * 90.00`

  2. Calculate iced tea subtotal: `num_teas * 30.00`

  3. Calculate 15% discount on noodle bowl subtotal: `bowl_subtotal * 0.15`

  4. Calculate discounted noodle bowl total: `bowl_subtotal - discount`

  5. Calculate eco-box fee: `num_bowls * 10.00`

  6. Calculate final bill: `discounted_bowl_total + tea_subtotal + eco_box_fee`

  7. Calculate change: `payment - final_bill`

* **Outputs:**

  * Bowl Subtotal (`bowl_subtotal`)

  * Tea Subtotal (`tea_subtotal`)

  * Discount (`discount`)

  * Eco-box Fee (`eco_box_fee`)

  * Final Bill (`final_bill`)

  * Change (`change`)

### 2. Step-by-Step Order of Tasks

1. Get the inputs: `num_bowls`, `num_teas`, and `payment`.

2. Compute `bowl_subtotal` = `num_bowls * 90.00`.

3. Compute `tea_subtotal` = `num_teas * 30.00`.

4. Compute `discount` = `bowl_subtotal * 0.15`.

5. Compute `eco_box_fee` = `num_bowls * 10.00`.

6. Compute `final_bill` = `(bowl_subtotal - discount) + tea_subtotal + eco_box_fee`.

7. Compute `change` = `payment - final_bill`.

8. Format all monetary values to two decimal places and display them.

### 3. Pseudocode

```
START
    // Declare constants
    SET BOWL_PRICE = 90.00
    SET TEA_PRICE = 30.00
    SET DISCOUNT_RATE = 0.15
    SET BOX_FEE = 10.00

    // Input section
    DISPLAY "Enter quantity of Noodle Bowls:"
    INPUT num_bowls

    DISPLAY "Enter quantity of Iced Teas:"
    INPUT num_teas

    DISPLAY "Enter payment amount:"
    INPUT payment

    // Calculations
    SET bowl_subtotal = num_bowls * BOWL_PRICE
    SET tea_subtotal = num_teas * TEA_PRICE
    SET discount = bowl_subtotal * DISCOUNT_RATE
    SET eco_box_fee = num_bowls * BOX_FEE
    
    SET final_bill = (bowl_subtotal - discount) + tea_subtotal + eco_box_fee
    SET change = payment - final_bill

    // Output section
    DISPLAY "Noodle Bowl Subtotal: ₱", FORMAT(bowl_subtotal, 2)
    DISPLAY "Iced Tea Subtotal:    ₱", FORMAT(tea_subtotal, 2)
    DISPLAY "Discount (15% Bowls): ₱", FORMAT(discount, 2)
    DISPLAY "Eco-box Fee:          ₱", FORMAT(eco_box_fee, 2)
    DISPLAY "--------------------------------"
    DISPLAY "Final Bill:           ₱", FORMAT(final_bill, 2)
    DISPLAY "Change:               ₱", FORMAT(change, 2)
END
```

### 4. Dry Run Calculations

#### **Test Case 1**

* **Inputs:** 3 Noodle Bowls, 2 Iced Teas, Payment = ₱500.00

* **Step-by-step Calculations:**

  * `bowl_subtotal` = 3 \* ₱90.00 = **₱270.00**

  * `tea_subtotal` = 2 \* ₱30.00 = **₱60.00**

  * `discount` = ₱270.00 \* 0.15 = **₱40.50**

  * `eco_box_fee` = 3 \* ₱10.00 = **₱30.00**

  * `discounted_bowl_total` = ₱270.00 - ₱40.50 = **₱229.50**

  * `final_bill` = ₱229.50 + ₱60.00 + ₱30.00 = **₱319.50**

  * `change` = ₱500.00 - ₱319.50 = **₱180.50**

* **Displayed Results:**

  * Bowl Subtotal: **₱270.00**

  * Tea Subtotal: **₱60.00**

  * Discount: **₱40.50**

  * Eco-box Fee: **₱30.00**

  * Final Bill: **₱319.50**

  * Change: **₱180.50**

#### **Test Case 2**

* **Inputs:** 4 Noodle Bowls, 4 Iced Teas, Payment = ₱600.00

* **Step-by-step Calculations:**

  * `bowl_subtotal` = 4 \* ₱90.00 = **₱360.00**

  * `tea_subtotal` = 4 \* ₱30.00 = **₱120.00**

  * `discount` = ₱360.00 \* 0.15 = **₱54.00**

  * `eco_box_fee` = 4 \* ₱10.00 = **₱40.00**

  * `discounted_bowl_total` = ₱360.00 - ₱54.00 = **₱306.00**

  * `final_bill` = ₱306.00 + ₱120.00 + ₱40.00 = **₱466.00**

  * `change` = ₱600.00 - ₱466.00 = **₱134.00**

* **Displayed Results:**

  * Bowl Subtotal: **₱360.00**

  * Tea Subtotal: **₱120.00**

  * Discount: **₱54.00**

  * Eco-box Fee: **₱40.00**

  * Final Bill: **₱466.00**

  * Change: **₱134.00**

### 5. Short Explanation

**Question:** Why would applying the discount to the entire bill produce an incorrect result?

**Answer:**

Applying the discount to the entire bill will produce an incorrect result because the rule clearly says the discount is only for the main meals (noodle bowls). If we apply the discount to the whole bill, the iced teas and the extra packaging fees will also get discounted, which gives a bigger discount than what the canteen allows. This makes the final bill smaller than what the customer should actually pay.