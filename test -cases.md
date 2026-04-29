# Test Cases

## TC-01 GET /posts (positive)

**Precondition:** API is available

**Steps:**
1. Send GET request to /posts

**Expected Result:**
- status code 200 OK
- response body is not empty (length > 0)
- response contains HTML (tag <html> is present)
- response time < 1000 ms

**Actual Result:**
- status code 200 OK
- response body is not empty
- response contains HTML
- response time < 1000 ms


## TC-02 GET /postssss (negative)

**Precondition:** API is available

**Steps:**
1. Send GET request to /postssss

**Expected Result:**
- status code 404 Not Found
- response body is not empty (length > 0)
- error page is displayed (HTML)
- response time < 1000 ms

**Actual Result:**
- status code 404 Not Found
- error page is displayed
- response time < 1000 ms


## TC-03 POST /posts (positive)

**Precondition:** API is available

**Steps:**
1. Send POST request to /posts

**Expected Result:**
- status code 200 OK
- response body is not empty
- response time < 1000 ms

**Actual Result:**
- status code 200 OK
- response body is not empty
- response time < 1000 ms


## TC-04 GET /wp-json (positive)

**Precondition:** API is available

**Steps:**
1. Send GET request to /wp-json

**Expected Result:**
- status code 200 OK
- response body is not empty
- response in JSON format
- response time < 1000 ms

**Actual Result:**
- status code 200 OK
- response body is not empty
- response in JSON format
- response time < 1000 ms


## TC-05 POST /contact-form (negative)

**Precondition:** API is available

**Steps:**
1. Send POST request to /contact-form with invalid data (e.g. incorrect email)

**Expected Result:**
- status code 200 OK
- response contains "validation_failed" status
- error message is displayed
- form is not submitted

**Actual Result:**
- status code 200 OK
- response contains "validation_failed"
- error message is displayed
- form is not submitted