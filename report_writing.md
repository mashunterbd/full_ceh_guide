1. vulnerability

2. severity

3. Desc

4. Instance

5.POC (proof of concept)

6. Steps to rep

7. Impact

8. Mitigation

9. Reference


-------------------------------------------------------
                                   # Vulnerability Report

## Vulnerability: Cross-Site Scripting (XSS)

**Severity:** High

### Description

Cross-site scripting is a critical computer security vulnerability where an attacker attempts to execute malicious scripts in a web browser of the victim by injecting malicious code into a legitimate web page or web application.

### Instance

- **URL:** [www.xyz.com/deb/search?query=](www.xyz.com/deb/search?query=)
  
- **Payload:**
  ```html
  <script> alert(1); </script>

# Proof of Concept
Screenshots of the browser page demonstrating the successful execution of the payload.

# Steps to Reproduce

1. Go to www.xyz.com/deb/search?query=

2. Insert the payload in search box

3. Check the response


# Impact
The XSS vulnerability poses a high risk, leading to potential:

* Open Redirection

* Session Hijack

* Phishing

* Defacement

* Cookie Stealing

# Mitigation

* Input Validation

* Encoding

• Input Validation: Validate and sanitize user inputs to ensure they adhere to expected formats. </br>
• Encoding: Encode output data to prevent malicious script execution.

# Reference
OWASP/CVE/NVD link 🔗

Examples screenshot: 

![Screenshot_2024-01-24-10-02-16-362_com google android youtube](https://github.com/masshuvo/full_ceh_guide/assets/108648096/3368e757-9cbd-4607-af6e-af627ee2885b)
![Screenshot_2024-01-24-10-02-37-586_com google android youtube](https://github.com/masshuvo/full_ceh_guide/assets/108648096/dc85fcec-c8e5-439e-8456-11eb5e3f64a2)
