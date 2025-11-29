# BUG-002 – Expired Credit Card Accepted

**Severity:** Critical  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Checkout → Payment

## Steps to Reproduce
1. Enter valid card number  
2. Enter expiration date in the past (e.g., 01/23)  
3. Enter valid CVV  
4. Click Place Order

## Expected Result
System should reject payment and show:  
“Card has expired. Please use a valid card.”

## Actual Result
System displays **Payment Successful** and completes the order.

## Impact
Allows invalid transactions → financial loss, fraud exposure, and incorrect payment processing.

## Recommendation
Add expiration date validation on both frontend and backend. Reject expired cards.
