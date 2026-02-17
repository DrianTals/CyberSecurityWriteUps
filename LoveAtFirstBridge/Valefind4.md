# Love at First Breach 1st Challenge: Valefind

## Step 5: CTF Capturing

1. Scroll down in the response tab, and find the admin api export database, til you see "api/admin/export.db"

2. Copy the LFI or path, and paste it in the First line after GET and replace the path all by the copied path like this " GET /api/admin/export.db HTTP/1.1"

3. you can see the auth_header in the repsonse tab which is "X-Valetine-Token" and paste it under the 3rd Line.

4. Copy and Paste the Token you've just copied earlier and type the token "X-Valetine-Token: XXXXXXXXX" and click Send Button to request.

5. Scroll down and you can find the Flag to validate the Challenge. 

--- 
[**Back**](Valefind3.md)
