                                                  # Script-injections
    
# What is a script injection ?  
Code Injection is the general term for attack types which consist of injecting code that is then executed by the application. This type of attack exploits poor handling of untrusted data. These types of attacks are usually made possible because a lack of proper input/output data validation.and The result of successful code injection can be disastrous


# How do these happen?  
 Cross-site scripting(XSS) is a type of computer security vulnerability typically found in web applications.XSS enables      attackers to inject client-side scripts into web pages viewed by other users. 
 the research community proposed and started using two new terms to help organize the types of XSS that can happen:

- Server XSS means that the data comes directly from the server onto the page. For example, the data containing the malicious text is from the HTTP response that made up the weak page.

- Client XSS means that the data comes from JavaScript which has manipulated the page. So it is JavaScript that has added the malicious text to the page, rather than it being in the page at that location when it was first loaded in the browser.



## Example :

[Example site](http://www.techpanda.org/dashboard.php) 

 This is a log in page for admin dashboard, he open the dashboard when you access the right email and password,
lets try adding any email and then add this password = yzyz OR 1 = 1 -- ] Click on Submit button You will be directed to the dashboard

SQL statement will be as follows

SELECT * FROM users WHERE email = 'yzyzy@yzyz.yz' AND password = anything OR 1 = 1 -- ]');

* 1=1 will be True
its like u said tio him thats this command sql 
Select * From users where True AND TRUE

look at this pic 
[Hanan pic](https://scontent.fjrs2-1.fna.fbcdn.net/v/t35.0-12/25316978_2193330904227708_293400160_o.png?oh=618e8042a2ddbe757e8c0a2eab2c0723&oe=5A30E8F3)


***********************************
To prevent the injection we can encode the input password before sending it to the query handling by using 
1- var res = encodeURI(password); in your code  or 
2- • Replace problematic characters with safe ones
• change ’ to \’
• change ; to \;
• change - to -
• change \ to \  
 to prevent that as we will see in this example in atom  .............
 

#Resourse:
[res1](https://en.wikipedia.org/wiki/Code_injection)
[res2](https://www.youtube.com/watch?v=E1zvy7foYR4)
[res3](http://www.itprotoday.com/software-development/script-injection-attacks)
[res4](http://www.techpanda.org/dashboard.php)
[ers5](https://www.veracode.com/security/sql-injection\)
