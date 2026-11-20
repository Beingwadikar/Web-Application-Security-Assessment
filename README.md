# Web Application Security Assessment Lab

## Project Overview
This beginner-level security assessment was performed on **OWASP Juice Shop**, an intentionally vulnerable web application, using Kali Linux and Docker.

The objective was to understand basic web application behaviour, inspect API requests and responses, and observe how authentication controls respond to authorized and unauthorized access attempts.

## Tools and Environment
- Kali Linux
- Oracle VirtualBox
- Docker
- OWASP Juice Shop
- Mozilla Firefox Developer Tools

## Lab Setup
1. Set up Kali Linux in Oracle VirtualBox.
2. Installed and started Docker.
3. Downloaded the OWASP Juice Shop Docker image.
4. Ran Juice Shop locally at `http://127.0.0.1:3000`.

## Activities Performed
- Started Docker and verified it using the Hello World container.
- Launched OWASP Juice Shop locally.
- Inspected browser network requests.
- Examined the product search API response.
- Observed HTTP response headers.
- Tested login with invalid credentials.
- Created a lab-only test account and performed a successful login.
- Observed authentication behaviour after logout.
- Tested basket access without authentication.
- Explored the application's Error Handling challenge.

## Key Observations
- Invalid login credentials returned HTTP 401.
- Unauthenticated basket access returned HTTP 401.
- After logout, the `whoami` endpoint returned an empty user object.
- Product search returned JSON data.
- An authenticated basket request returned HTTP 304, indicating a cached response.
- The Error Handling challenge was successfully completed in the Juice Shop training environment.

These observations are documented as lab results. They are not presented as confirmed exploitable vulnerabilities.

## Project Scope and Limitations
This was a controlled, beginner-level local lab. Testing was limited to the activities listed above. No claim of a comprehensive penetration test or confirmed security vulnerability is made.


## Project Submission

**Project Title:** Web Application Security Assessment

**Tools Used:** Kali Linux, Docker, OWASP Juice Shop and Firefox Developer Tools.

**Project Report:** The complete 4-page project report is included with the capstone submission on Honeywell Future Skills Edge.

**GitHub Repository:**  
https://github.com/Beingwadikar/Web-Application-Security-Assessment

This project was completed as a beginner-level, hands-on web application security assessment in a local testing environment.


## Evidence
Screenshots of the setup, application, API responses, authentication tests, and challenge activity are stored in the `Screenshots/` directory.

## Disclaimer
This project was conducted in a local, intentionally vulnerable training environment for educational purposes only.
