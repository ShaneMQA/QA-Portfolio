# BUG-003 – Order Submission Allowed with Empty Payment Fields

**Severity:** High  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Checkout → Payment

## Steps to Reproduce
1. Leave card number, expiration date, and CVV empty  
2. Click Place Order

## Expected Result
Form should not submit and should show:  
- “Card number required”  
- “Expiration date required”  
- “CVV required”

## Actual Result
System attempts to process the order with no validation errors.

## Impact
Allows incomplete or invalid orders; breaks payment flow logic; disrupts user experience.

## Recommendation
Implement required field validation and disable Place Order until all fields are completed.
