# Day 5 Web Server Challenge

### 1st Challenge - XSS - Stored 1 (Medium)

1. This is an XSS challenge with a simple web form. To test if it is vulnerable, enter “Test” in the title and use an HTML image tag like `<img src="https://www.google.com.au/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">Google` in the message box, then click **Send**. If the Google logo appears, the page is vulnerable to Stored XSS.

2. After observing the page, it becomes clear that messages are being cleared, which suggests an admin is reviewing them while logged in.

3. Since an image tag alone cannot access session data, the next step is to consider JavaScript injection using a `<script>` tag, which could execute when the admin views the page.

4. A request‑collection service such as `http://requestb.in/` can be used to monitor incoming requests and demonstrate how injected scripts might send accessible browser data to an external URL.

5. When the admin loads the infected page, the script executes automatically. This challenge highlights how missing protections like output encoding, HttpOnly cookies, and CSP can lead to Stored XSS vulnerabilities.

