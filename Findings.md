# Security Assessment Findings

## 1. Invalid Login Attempt
- **Test:** Login using incorrect credentials.
- **Endpoint:** `POST /rest/user/login`
- **Observed Result:** HTTP 401 Unauthorized.
- **Observation:** The application rejected invalid credentials.
- **Assessment:** Expected authentication behaviour.

## 2. Successful Authentication
- **Test:** Login using the lab test account.
- **Observed Result:** HTTP 200 OK.
- **Observation:** The application successfully authenticated the test account.
- **Assessment:** Expected behaviour.

## 3. Logout Verification
- **Test:** Access the `whoami` endpoint after logout.
- **Observed Result:** Empty user object.
- **Observation:** The session was no longer identified as an authenticated user.
- **Assessment:** Expected logout behaviour.

## 4. Unauthenticated Basket Access
- **Test:** Access `/rest/basket/6` without an authorization header.
- **Observed Result:** HTTP 401 Unauthorized.
- **Response:** No Authorization header was found.
- **Assessment:** Unauthenticated access was denied as expected.

## 5. Product Search API
- **Test:** Search for a product using the product search endpoint.
- **Endpoint:** `/rest/products/search?q=banana`
- **Observed Result:** JSON response containing product information.
- **Assessment:** API response behaviour successfully observed.

## 6. HTTP Response Headers
- **Test:** Inspect response headers using browser Developer Tools.
- **Observation:** Headers included `Content-Type`, `X-Content-Type-Options`, `X-Frame-Options`, and `Access-Control-Allow-Origin: *`.
- **Assessment:** Headers were observed. The wildcard CORS value was not independently verified as an exploitable vulnerability.

## 7. Authenticated Basket Request
- **Test:** Inspect the basket request after login.
- **Observed Result:** HTTP 304 Not Modified.
- **Observation:** The browser received a cached response.
- **Assessment:** No vulnerability established from this response.

## 8. Error Handling Challenge
- **Test:** Complete the Juice Shop Error Handling challenge.
- **Observed Result:** Challenge success message displayed.
- **Assessment:** Training challenge completed. This is not, by itself, a confirmed security finding.

## Overall Conclusion
The lab provided practical exposure to API inspection, HTTP responses, authentication, authorization checks, and basic web application testing.

No independently verified exploitable vulnerability was confirmed during the activities documented above.