> Explain the role of a cookie and differentiate it from sessions.
Write a PHP script to check whether the cookie is set or not. [6M]
***
#### The role of a cookie [1M]
An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. 
The browser may store it and send it back with the next request to the same server. 
Typically, it's used to tell if two requests came from the same browser — keeping a user logged-in, for example.
The main purpose of a cookie is to identify users and possibly prepare customized Web pages or to save site login information for you.

#### Difference between cookie and sessions [2M]
|Cookie|Session|
|---|---|
|Cookies can store only “string” datatype.| Session can store any type of data because the value is of data type of “object” |
|They are stored at client side.|These are stored at server side.|
|Cookie is non-secure since stored in text-format at client side.|Sessions are secured because it is stored in binary format/encrypted form and gets decrypted at server.|
|Size of cookie is limited to 40 and number of cookies to be used is restricted to 20.|There is no limitation on the size or number of sessions to be used in an application.|
|Cookies can be disabled.|We cannot disable the sessions. Sessions can be used without cookies also.|
|Cookies can be persistent or non-persistent.|Sessions are called as Non-Persistent cookies because its life time can be set manually|

#### PHP Script to check whether the cookie is set or not [3M]
```
 <?php
  $cookie_name = "user";
  $cookie_value = "John Doe";
  setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/"); // 86400 = 1 day
?>

<html>
<body>

<?php
  if(!isset($_COOKIE[$cookie_name])) {
      echo "Cookie named '" . $cookie_name . "' is not set!";
  } else {
      echo "Cookie '" . $cookie_name . "' is set!<br>";
      echo "Value is: " . $_COOKIE[$cookie_name];
  }
?>

</body>
</html> 
```
