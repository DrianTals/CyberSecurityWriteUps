# Love at First Breach 1st Challenge: Valefind

## Step 4: Token and File Breaching

1. Turn off the Intercept Button, Go back to the Cupid Profile and Change the layout to "Modern Dark" and Turn On again the Intercept button and Refresh.

2. guess or make a LFI (Local File Inclusion) such as " **/../../etc/passwd** " and replace/paste in the 1st GET line after the parameter of "layout=...until .html" before HTTP/1.1 and right click and send it to repeater.

3. you cann see the passwords of the user in the website. you can erase one forward slash to see the error and see the correct path file directory.

4. Copy the path directory "/opt/Valentind/templates/components/" and paste it in the first line same thing did earlier and add "app.py"

5. erase "/templates/components/" and turn it into /opt/Valentind/app.py and you can see the Admin API Key, copy it and save it for later

---
[**Back**](Valefind2.md) [**Next**](Valefind4.md)