
### Notes On Secure Coding


<br><br><br>
#### Use More Input Sanitization
 

```
<?php

  if(isset($_REQUEST['cmd'])) {
    $cmd = ($_REQUEST['cmd']);
    system($cmd);
  } else {
    echo "This is robbing a website-act!";
  }
  
?>

```

  * **Defend against command injection by escaping inputs from the HTTP request**
  
  * **Using bind parameters in SQL is safe - Bind parameters are placeholder that the database driver will safely replace with some supplied inputs—like the email or password values or any which you intend to attach to the sql statement**
  
  * **Bind parameters are prefixing your parameters with “escape characters”**
 
 <br>

```

Statement statement = connection.createStatement();
String sql = "SELECT * FROM users WHERE employeeId=" + id_string +
             " AND email ='" + email_string + "'";
statement.executeQuery(sql);

```

  * **Know how your ORM works**

<br>

 
 
 
#### Remote Code Execution Attack

* **Once an attacker found enough detail on your web application they may use remote code execution attack**  

* **In 2013 it was publicized that Ruby on Rails are promptly executing and parsing HTTP request based on their Content-Type header - They were not filtering out more security measures upon parsing code** 

* **Configure web server to deserialize data without executing code** 

<br><br>

#### Protect against File Upload Attacks

  * **Any file with .php is treated by the to server as executable - so when a website is maintaining an unsecure file upload functionality hackers may use this for `File Upload Attack`**


  * **Mitigations **

     * Use secure file hosting such as third party cloudflare
     * Secure file uploads as non-executable - any objects to be written on your disk must lack executable permissions
    
