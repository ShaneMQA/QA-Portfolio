# Checkout & Payment Flow – Test Cases

## TC01 – Successful Checkout
**Preconditions:** Item in cart  
**Steps:**  
1. Enter valid shipping address  
2. Choose Standard Shipping  
3. Enter valid card details  
4. Click Place Order  
**Expected Result:** Order confirmation page displays.

---

## TC02 – Invalid Credit Card Number
**Steps:**  
1. Enter valid address  
2. Enter card number: 12345678  
3. Click Place Order  
**Expected Result:** Error message “Invalid card number.”

---

## TC03 – Missing ZIP Code
**Steps:**  
1. Leave ZIP code blank  
2. Click Continue  
**Expected Result:** “ZIP code is required.”

---

## TC04 – Incorrect CVV Length
**Steps:**  
1. Enter CVV: 12  
2. Click Place Order  
**Expected Result:** Error: “Invalid CVV.”

---

## TC05 – Total Price Calculation
**Data:** Item: $39.99, Shipping: $5.00, Tax: $3.20  
**Expected Total:** $48.19  
**Actual:** System calculation shown during test  
