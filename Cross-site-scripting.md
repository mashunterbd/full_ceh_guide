# What's XSS

<p> XSS (Cross-Site Scripting) vulnerability is a type of security vulnerability that allows an attacker to inject malicious code into a web page viewed by other users. This can be done by exploiting a vulnerability in a web application that does not properly validate user input, such as a search field or comment section. 

When a user visits the affected web page, the malicious code can execute on their browser and steal sensitive information, such as login credentials or session tokens. The attacker can also use this vulnerability to modify the content of the web page and trick users into performing unintended actions.

XSS attacks can be prevented by properly validating and sanitizing user input, encoding output data, and implementing security measures like Content Security Policy (CSP). Web developers should also stay up-to-date with the latest security best practices and vulnerabilities to protect their applications from attacks. </p>


-------------------------------------------------------


# Types of XSS?
There are three main types of XSS attacks:

- Reflected XSS: This is the most common tupe of XSS attack. It occurs when an attacker
injects malicious code into a URL that is then visited bụ the victim. The malicious code is then
reflected to the victim's browser, where it is executed.

- Stored XsS: This tupe of XSS attack occurs when malicious code is stored in a web
application. This can happen when an attacker is able to upload a file to the application, or
when they are able to modify existing content. When a victim visits the web application, the
malicious code is executed.

- DOM-based XSS:This type of XSS attack does not involve the injection of malicious code into
a URL Or a web application. Instead, the malicious code is injected into the Document Object
Model (DOM) of the web page. The DOM is the internal representation of a web page that is
used bu the browser. When a victim visits the web page, the malicious code is executed in the
browser's DOM.

![Screenshot_2024-01-24-10-53-37-825_com google android youtube](https://github.com/masshuvo/full_ceh_guide/assets/108648096/ead9efa4-4640-457a-8e4d-b610d0b18dd5)


# Some Java Script event and Function for our XSS Exploitatio
```
alert
```
Use Case: To Popup Message
```
prompt0
```
Use Cese: To show prompt
```
print
```
Use Case: To Print current page
```
document.cookie[]
```
Use Case: cookie used bụ current website
```
document.getElementByld(id)
```
Use Case: This method is used to retrieve an element from the DOM based on its unique id attribute. It is
helpful when you need to access a specific element to manipulate its content or behavior.
```
document.query Selector(selector)
```
Use Case: This method allows you to select the first element that matches a specified CSS selector. It
is helpful when you want to select elements using CSs-ike syntax.



# What is Open Redirection Vulnerability?
A web application accepts a user-controlled input that specifies a
link to an external site, and uses that link in a Redirect. This
simplifies phishing attacks.
By modifying the URL value to a malicious site, an attacker may
successfully launch a phishing scam and steal user credentials.
Because of the server name in the modified link is identical to the
original site, phishing attempts have a more trustworthy
appearance.


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/dcb0e9e3-46e0-45f3-a6f6-a24ecaa8d71b)
![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/28268084-fd79-4a78-aeea-ebe9e2d4b5dd)
![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/8172273f-1fa2-4e06-bf3d-b9be8158dffd)
# pre

![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/35d4c96b-3633-4c5d-911a-bdded80232e5)

waybackurls testphp.vulnweb.com| tee savvuln. txt
