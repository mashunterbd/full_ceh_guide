# Insecure Direct Object References [IDOR]

- Web application developer uses an identifier for direct access to an internal
implementation object but provides no additional access control and/or
authorization checks.

- For example, if the URL of a transaction could be changed through client-side
user input to show unauthorized data of another transaction.

- For example, a user in a database will usually be referred to via the user ID,
generated automatically.

- Let's say that the web application displays transaction details using the
following URL:
https://www.example.com/transaction.php?id=74656

- A website might save chat message transcripts to disk using an incrementing
filename, and allow users to retrieve these by visiting a URL like the following:
https://insecure-website.com/static/12144.txt

- IDOR vulnerabilities may happen in the case of password change forms. A
badly designed password change form URL might be:
https://www.example.com/change_password.php?userid=1701

#Impact: </br>

- Information Disclosure
- Modification or destruction of data
- Bypassing access controls
- Privilege Escalation
- Account takeover
