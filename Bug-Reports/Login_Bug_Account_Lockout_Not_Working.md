# BUG-L01 – Account Not Locked After Multiple Failed Login Attempts

**Severity:** High  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Login

## Steps to Reproduce
1. Navigate to the login page.
2. Enter a valid email address for an existing account.
3. Enter an incorrect password.
4. Click "Login."
5. Repeat steps 2–4 a total of 5 times.

## Expected Result
After 5 consecutive failed login attempts, the account should be locked and a message displayed:  
“Your account has been locked due to multiple failed login attempts.”

## Actual Result
Login continues to allow attempts with the same account. No lockout occurs and no lockout message is displayed.

## Impact
Security risk: brute-force password guessing is possible. Login policy requirements are not enforced.

## Recommendation
Implement and enforce account lockout logic after the configured number of failed attempts, and display a clear lockout message.
