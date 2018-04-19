# CyberSec_Week8
# Victor Hong

## Green Page
### XSS Exploit
The XSS exploit that I used in the project is a simple Javascript injection on the feedback input in the Contact page. The script simply displays an alert when submitting the feedback. We first go to the _Contact_ page and fill in the email and name fields with any values. In the Feedback field we will put
```
<script>alert('Victor Hong was here');</script>
```
and submit the feedback. The alert should show up then. 

#### GIF Tutorial
<img src='https://github.com/vhong000/CyberSec_Week8/blob/master/xss-exploit.gif'/>

### Username Enumeration
In the login for the Green page, when the entered username is incorrect, the response is in regular text. However, when the username is a correct match, the response gets __bolded__. We can see that this in the css of file of the page. 

#### GIF Tutorial
<img src='https://github.com/vhong000/CyberSec_Week8/blob/master/UE_exploit.gif'/>

## Red Page
### CSRF Exploit
The CSRF exploit that I used in the project is an attack that takes the url of the link and manually changes the content within that file. This attack is executed through the opening of an html file that will run a script that changes the users in a system. We first open the html file containing the script on our browser. Then we can reload the users page to find the content modified by our script.

#### GIF Tutorial
<img src='https://github.com/vhong000/CyberSec_Week8/blob/master/csrf-exploit.gif'/>

### IDOR Exploit
The IDOR exploit that I used in the project uses the knowledge of a signed in user to find hidden sales people in Globitek. We first log in as another color and find that there are salespeople that should be hidden. We then take the id number of these people and manually access them through the URL in the blue page without having to log in.

#### GIF Tutorial
<img src='https://github.com/vhong000/CyberSec_Week8/blob/master/IDOR_exploit.gif'/>

## Blue Page
### SQL Injection Exploit
The SQLi exploit that I used in the project is an injection that will make the database wait for 5 seconds. We first go to the _find a Salesperson_ page and select any person's link. In the URL we will add to it:
```
' AND SLEEP(5)=0--'
```
This will cause the server to wait for 5 seconds before reloading. 

#### GIF Tutorial
<img src='https://github.com/vhong000/CyberSec_Week8/blob/master/sqli_exploit.gif'/>

