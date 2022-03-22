# Cross Site Scripting.

An XSS vulnerability occurs when attacker can inject an executable script into HTML pages viewed by the victim user.

common types of XSS includes:

1. Stored XSS

it happens when user input is stored on a server and retrieved unsafely. 

stored XSS is the most severe XSS type. it has the potential of attacking many more users than reflected, DOM, or self-XSS.

2. Blind XSS

blind XSS is a special kind of stored XSS, whose malicious input is stored by the server but executed in another part of the application or in another application that you cannot see.

3. Reflected XSS

it happens when user input is returned to the user without being stored in a database.

4. DOM-based XSS

DOM-based XSS behave almost the same with Reflected XSS, but one key difference is that it doesn't require server involvement. while the payload of reflected XSS gets sent to the server.

5. Self XSS

self-xss attacks require victims to input a malicious payload themselves. attacker must trick the users into doing much more than simply viewing a page or browsing to a particular URL.


## Prevention

there are mainly two prevention mechanisms: robus input validation and contextual output escaping and encoding.

## Hunting for XSS

while most XSS vulnerabilites occure in web applications, it is important to remember that XSS vulnerabilities can also arise in non-HTTP protocols such as SMTP, SNMP, and DNS.

1. look for input opportunities.

note that don't limit yourself to text input fields. sometimes drop-down menus or numeric fields can allow you to perform XSS.

for reflected and DOM XSS, try user input in URL parameters, fragments or pathnames and compare end rendered result with your input strings.

2. insert payloads.

simple XSS typically works on IoT or embedded application that don't use the latest frameworks.

for most modern web application, simple xss won't work. we need more complex payloads to get around the defense mechanisms.

use \<img\> tag instead of the script tag. add your script in onload or onerror attribute.

another way is through special URL schemes. such as javascript: and data:

```
javascript:alert("XSS")
```

use XSS polyglot to test. [link](https://web.archive.org/web/20190617111911/https://polyglot.innerht.ml/)


another way of testing for XSS more efficiently is to use generic test string to test which characters are escaped or blacklisted and which are not. then construct your css payload accordingly.

tools for XSS: [xsshunter.com](https://xsshunter.com/)

3. escalating

XSS can be used to read sensitive information on the victim's page. this means you can use XSS to escalate your attack from there.


## Bypassing XSS blacklist or filtering

use alternative javascript syntax.

capitalization and ecoding.

filter logic errors.

