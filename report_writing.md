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

Vulnerability Report 

Vulnerability: Cross site scripting (XSS)

Severity: High

Description:

Cross site scripting is a type of computer security vulnerability, the attacker aims to execute malicious scripts in a web browser of the victim by including malicious code in a legitimate web page of web application.

Instance:

URL: www.xyz.com/deb/search?query=

Payload:

<script> alert(1); </script>

Proof of Concept: Screen shots of the browser page

Steps to Reproduce:

1. Go to www.xyz.com/deb/search?query=

2. Insert the payload in search box

3. Check the response

Impact:

* Open Redirection

* Session Hijack

* Phishing

* Defacement

* Cookie Stealing

Mitigation:

* Input Validation

* Encoding

Reference: OWASP/CVE/NVD
