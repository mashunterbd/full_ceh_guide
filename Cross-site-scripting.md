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

 waybackurls bytecapsuleit.com | grep -a -i \=http | qsreplace 'http://evil.com' | while read host do;do curl -s -L $host -I|grep "evil.com" && echo -e "$host \033[0;31mVulnerable\n" ;done

 # for install 
 ## waybackurls
 ```
go install github.com/tomnomnom/waybackurls@latest

```
## qsreplace
 ```
go install github.com/tomnomnom/qsreplace@latest
```

### Download path is 
```
cd go/bin
```

## for command setup in go 

```
cp waybackurls /usr/local/bin
```

after do thet you can use this tool from anywere on terminal.

# Automate vulenervale site find from all links 

Gf, A tool made by @tomnomnom "is A wrapper around grep, to help you grep for things". The Github Repository for GF can be found here:
https://github.com/tomnomnom/gf

GF Patterns is an open-source project made by @1ndianl33t and this project contains custom patterns that can be used with the original GF tool to grep for patterns for common bugs like XSS, SQLi, and SSRF.
The Github repository for this can be found here: 
https://github.com/1ndianl33t/Gf-Patt...

Note: You need to have GO installed correctly before you can install this tool. You can install Go on your OS here: https://golang.org/doc/install

Installation:
1) First install GF-Patterns by @1ndianl33t in the root directory-
```
git clone https://github.com/1ndianl33t/Gf-Patterns
```
3) Then install Gf by @Tomnomnom- https://github.com/tomnomnom/gf
   ```
   go install https://github.com/tomnomnom/gf@latest
   ```
   <code> mv gf /user/local/bin </code>
   
4) go get -u github.com/tomnomnom/gf
5) This should install GF and GF Patterns correctly.
6) If you faced any errors during Installation then please comment down below.

Usage:

Configure GF to work with GF Patterns:

1)Go to the root directory
2) mkdir .gf
3) Go to /root/Gf-Patterns
4) mv *.json /root/.gf 
5) Now to test if GF is working: 

```
gf -list
```

CONFIGURED GF CORRECTLY!

(-list)To list all of the available patterns
The most important command:
(cat urls.txt | gf "name of pattern")

This command doesn't work all that properly, it searches specific for keywords.
So it can give some invalid results too(as in the results not useful for us)

We will use some regex to use GF at it's best!

We will get the target URLs using Waybackurls, as demonstrated in our previous
video:

echo "vulnweb.com" | waybackurls -no-subs | tee urls.txt

The final command:

cat urls.txt | gf "name of pattern" | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee output.txt

## xss
```
cat urls.txt | gf xss | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee output.txt
```
## lfi
```
cat urls.txt | gf lfi | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee output.txt
```
## SQLI
```
cat urls.txt | gf sqli | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee output.txt
```
## redirecti
```
cat urls.txt | gf redirect | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee output.txt
```
# 1 cli to do all
## just modify remove.text file to your target text file
### 1st Create an new folder as you like : mkdir Remove && cd Remove 
```
cat remove.txt | gf sqli | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee sqli.txt && cat remove.txt | gf redirect | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee redirect.txt && cat remove.txt | gf lfi | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee Lfi.txt && cat remove.txt | gf xss | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee xss.txt && cat remove.txt | gf idor | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee idor.txt && cat remove.txt | gf ssrf | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee ssrf.txt && cat remove.txt | gf rce | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee rce.txt && cat remove.txt | gf interestingparams | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee interestingparams.txt && cat remove.txt | gf img-traversal | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee img-traversal.txt && cat remove.txt | gf interestingEXT | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee interestingEXT.txt && cat remove.txt | gf interestingsubs | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee interestingsubs.txt && cat remove.txt | gf debug_logic | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee debug_logic.txt && cat remove.txt | gf jsvar | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee jsvar.txt && cat remove.txt | gf ssti | sed 's/=.*/=/' | sed 's/URL: //' | sort -u | tee ssti.txt
```

Now we got all urls with parameters that might be vulnerable to XSS, SQLi etc.
So, this way we can try different payloads and start fuzzing.

Video: https://www.youtube.com/watch?v=aYkD9BvAjwg


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/6b976f9a-0df9-4ea9-a7d7-c0270489af51)

![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/f2b4e457-b0e6-401a-b6a8-4a55a0f84704)

![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/84fb6ae0-cfaf-4862-b904-5202536eb775)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/34d4f0c7-59c3-480b-a468-bb65a6442f16)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/cb2a5d3f-25f8-4e19-ad71-a951e49cb3f3)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/d553acd0-34d6-4fa1-85e3-982504d8b226)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/15867c52-0b41-406b-be42-84e35346d1d0)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/09a8b208-de6e-458b-b718-01e03901212a)



![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/ff88364c-eff5-43f4-acb1-53991b9895f6)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/e3fe75dc-1acf-4e03-877e-a8a0379707f8)


![image](https://github.com/masshuvo/full_ceh_guide/assets/108648096/a1c0d4ec-de7d-4ed3-9265-a17369192457)


Video Link https://www.youtube.com/watch?v=G8lSO9BvO5Y&list=LL&index=10&t













