> Create a HTML form to accept name (TextField), address (TextArea), Gender (Radio) and Country (DropDown) fields from user, 
store it into MySQL database using PHP program. [10 M]
***
#### SQL - to create a table in MySQL database [1M]
```
CREATE TABLE user_data (
  uname VARCHAR(50) PRIMARY KEY,
  address VARCHAR(500),
  gender CHAR(1) NOT NULL,
  country CHAR(2) DEFAULT 'IN'
);
```

#### form.html - to accept data from the user [4M]
```
<!DOCTYPE html>
<html>
<head>
<title>Form</title>
</head>
<body>

<h1>Form</h1>
<form action="save.php" method="POST">
    Name: <input name="uname"><br><br>
    Address: <textarea name="address" cols="30" rows="10"></textarea><br><br>
    Gender: Female <input type="radio" name="gender" value="F">
            Male <input type="radio" name="gender" value="M"> <br><br>
    Country: 
    <select name="country">
        <option value="AU">Australia</option>
        <option value="IN" selected>India</option>
        <option value="US">USA</option>        
    </select><br><br>
    <input type="submit" value="Save">
</form>

</body>
</html> 
```

#### save.php - to save data to MySQL database using PHP program [5M]
```
<!DOCTYPE html>
<html>
<body>

<?php

$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "dbname";

$uname = $_POST["uname"];
$address = $_POST["address"];
$gender = $_POST["gender"];
$country = $_POST["country"];

$conn = new mysqli($servername, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$sql = "INSERT INTO user_data (uname, address, gender, country)
VALUES ('$uname', '$address', '$gender', '$country')";

if ($conn->query($sql) === TRUE) {
    echo "New record created successfully";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}

$conn->close();
?> 

</body>
</html>
```
