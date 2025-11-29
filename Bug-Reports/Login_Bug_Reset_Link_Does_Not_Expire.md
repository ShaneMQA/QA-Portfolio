# BUG-L03 – Password Reset Link Does Not Expire After Use

**Severity:** High  
**Environment:** Chrome (Latest), Windows 10  
**Module:** Forgot Password / Reset

## Steps to Reproduce
1. On the login page, click "Forgot Password."
2. Enter a valid account email and submit.
3. Open the password reset email and click the reset link.
4. Set a new password and complete the reset.
5. Go back to the same email and click the same reset link again.

## Expected Result
Second attempt using the reset link should be rejected with a message such as:  
“This reset link has expired or already been used.”

## Actual Result
The same reset link can be used multiple times to reset the password again.

## Impact
Security risk: anyone with access to the old email or link can continue changing the user’s password.

## Recommendation
Expire the reset token immediately after first successful use and enforce token expiry based on time limit (e.g., 30 minutes).
