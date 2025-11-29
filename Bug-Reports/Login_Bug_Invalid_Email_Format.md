# BUG-L02 – Invalid Email Format Not Validated

**Severity:** Medium  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Login

## Steps to Reproduce
1. Navigate to the login page.
2. In the email field, enter "userexample.com" (no `@` symbol).
3. Enter any password.
4. Click "Login."

## Expected Result
System should prevent login and show a validation message such as:  
“Please enter a valid email address.”

## Actual Result
System attempts to log in and displays a generic error: “Incorrect email or password.”

## Impact
Poor user experience and unclear feedback. Users are not informed that the email format is invalid, making troubleshooting difficult.

## Recommendation
Add frontend and backend email format validation and display a clear error message when the format is invalid.
