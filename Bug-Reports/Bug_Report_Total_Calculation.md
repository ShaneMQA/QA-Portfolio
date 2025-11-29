# BUG-001 – Incorrect Total Price Calculation

**Severity:** High  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Checkout → Order Summary

## Steps to Reproduce
1. Add an item priced at $39.99  
2. Proceed to checkout  
3. Select shipping: $5.00  
4. Tax is displayed as $3.20  
5. Observe the Order Total

## Expected Result
Order total should be **$48.19**.

## Actual Result
Order total is displayed as **$49.99**.

## Impact
Incorrect financial calculation affects users, revenue, billing accuracy, and trust.

## Recommendation
Review calculation logic for price + shipping + tax. Validate rounding methods.
