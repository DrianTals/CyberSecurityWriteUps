# Love at First Breach 1st Challenge: Valefind

## Step 3: Exploiting

1. Scroll Down and Find the user named "Cupid"

2. There's a hint on his User Profile Description "I keep the database secure, no peeking". which means he's the admin of the website that we can exploit.

3. Copy the url page and paste it into burp suite browser

4. Turn on the Intercept button and Refresh the page to get Request Data tab and Click Forward Button

5. Go to "HTTP History" and find the path of cupid profile "/profile/cupid to see the Response.

6. Scroll down in Response Tab and you can see comment code about Vulerability of the Page "Layout" which allows and can access file location using the parameters. 

---
[**Back**](Valefind1.md) [**Next**](Valefind3.md)