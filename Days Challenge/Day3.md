# Day 3 Web Server Challenge

### 1st Challenge: HTML - Source code (Easy Mode)

1. Visit Challenge URL

2. View source code of the challenge (CTRL+U)

3. On line 29 there is password which is required to complete challenge

4. Submit the password to complete challenge

### 2nd Challenge: HTTP - IP restriction bypass (Easy Mode)

1. First things First you need to download Burp Suite to intercept http requests

2. Open Burp Suite and click the proxy tab where you can intercept

3. Click Open Browser, and turn on the "intercept on/off" button

4. paste the url link and there will be a request tab below and will show the information

5. under the first line below "GET" type "X-Forwarded-For: 192.168.100.9" this will intercept or change the IP address to bypass

6. refresh the page and there will be Validation Password for the challenge " Ip_$po0Fing "

### 3rd Challenge: HTTP - Open redirect (Easy Mode)
1. Open Burp Suite and open browser in Proxy Tab

2. http://challenge01.root-me.org/web-serveur/ch52/ Input this link in the browser and intercept it

3. Then Right Click the Request and click "Do Intercept" and "Response to this Request" to request the html code

4. you can see 3 links, choose one of them to edit, change one of them to google and edit the url and search up "MD5 Hash Generator" for its url hash

5. Click Forward and refresh the page and click the Google Button, and validation Flag will appear.

### 4th Challenge: HTTP - User-agent
1. In Burp Suite, Open the link "http://challenge01.root-me.org/web-serveur/ch2/" in the browser and intercept it

2. right click and send it to repeater

3. Click Send, and you can see in the Request below there is a "User Agent"

4. Delete the text and simply replace it with "admin"

5. and this will appear in response tab

### 5th Challenge: Weak password (Easy Mode)
1. Open browser in Burp Suite and open the link "http://challenge01.root-me.org/web-serveur/ch3/"

2. Turn on "intercept" and Test the username and password inputting "test" and "test"

3. below Request Tab, you can see "Authorization", Right click the tab and send it to repeater

4. Highlight the code after the word "Basic" and right click and Click "Converstion Selection" and "Base64" and Decode it

5. you can see the username and password of the site, click send and refresh the page

6. this would be the response and "admin" is the validation flag to complete the challenge

