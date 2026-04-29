# Bug Reports

## BUG-01 Incorrect HTTP status code for validation error

**Steps to Reproduce:**
1. Send POST request to /contact-form with invalid email (e.g. test@test)
2. Observe server response

**Expected Result:**
- status code 400 Bad Request
- validation error message returned

**Actual Result:**
- status code 200 OK
- response contains "validation_failed"
- validation error message returned

**Description:**
The server returns HTTP 200 OK even when validation fails. This may complicate error handling on the client side.