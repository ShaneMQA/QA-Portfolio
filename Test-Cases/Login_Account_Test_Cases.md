# Login & Account Management – Test Cases

## TC01 – Successful Login with Valid Credentials
**Preconditions:** User account exists with email and password.  
**Steps:**
1. Navigate to the login page.
2. Enter a valid email (e.g., user@example.com).
3. Enter the correct password.
4. Click the "Login" button.
**Expected Result:** User is redirected to the Dashboard page.

---

## TC02 – Login with Incorrect Password
**Preconditions:** Valid account exists.  
**Steps:**
1. Go to the login page.
2. Enter a valid email.
3. Enter an incorrect password.
4. Click "Login."
**Expected Result:** Login is rejected and an error message appears such as “Incorrect email or password.” User remains on the login page.

---

## TC03 – Email Field Left Blank
**Steps:**
1. Leave the email field empty.
2. Enter any password.
3. Click "Login."
**Expected Result:** Login is blocked and a validation message appears: “Email is required.”

---

## TC04 – Invalid Email Format
**Steps:**
1. Enter an invalid email format (e.g., userexample.com).
2. Enter any password.
3. Click "Login."
**Expected Result:** Validation message appears: “Please enter a valid email address.”

---

## TC05 – Password Field Left Blank
**Steps:**
1. Enter a valid email.
2. Leave the password field empty.
3. Click "Login."
**Expected Result:** Login is blocked and a validation message appears: “Password is required.”

---

## TC06 – Account Lockout After 5 Failed Attempts
**Preconditions:** Account exists and is currently active.  
**Steps:**
1. Enter a valid email and wrong password.
2. Click "Login."
3. Repeat steps 1–2 a total of 5 times.
**Expected Result:** After the 5th failed attempt, account is locked and message appears: “Your account has been locked due to multiple failed login attempts.”

---

## TC07 – “Remember Me” Keeps User Logged In
**Preconditions:** User not logged in.  
**Steps:**
1. On login page, check “Remember Me.”
2. Enter valid email and password.
3. Click "Login."
4. Close the browser.
5. Reopen the browser and go back to the site.
**Expected Result:** User remains logged in (no need to log in again).

---

## TC08 – Forgot Password Sends Reset Email
**Preconditions:** Account exists and email is active.  
**Steps:**
1. On login page, click "Forgot Password."
2. Enter a valid account email.
3. Click "Submit."
**Expected Result:** Confirmation message appears and a reset link is sent to the entered email address.

---

## TC09 – Reset Link Can Only Be Used Once
**Preconditions:** User has received a valid reset link.  
**Steps:**
1. Click the reset link from the email.
2. Enter a new password and confirm.
3. Submit and complete reset.
4. Click the same reset link again.
**Expected Result:** Second use of the link is rejected with a message like “This reset link has expired or already been used.”
