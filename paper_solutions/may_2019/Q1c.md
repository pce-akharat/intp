> Explain string functions in PHP. [5M]
***
[1M for each function explained along with the example code]
1. **strlen()** function returns the length of a string (number of characters).  
```
<?php
  echo strlen("Hello world!"); //outputs 12
?>
```
2. **str_word_count()** function counts the number of words in a string. 
```
<?php
  echo str_word_count("Hello world!"); //outputs 2
?>
```
3. **strrev()** function reverses a string.
```
<?php
  echo strrev("Hello world!"); //outputs !dlrow olleH
?>
```
4. **strpos()** function searches for a specific text within a string. 
If a match is found, the function returns the character position of the first match. If no match is found, it will return FALSE.
```
<?php
  echo strpos("Hello world!", "world"); //outputs 6
?>
```
5. **str_replace()** function replaces some characters with some other characters in a string. 
Example: The example below replaces the text "world" with "Dolly".
```
<?php
  echo str_replace("world", "Dolly", "Hello world!"); //outputs Hello Dolly!
?>
```
***
Note: There are many string functions, you could write any five of them along with the example. 
Check them [here](http://www.w3schools.com/php/php_ref_string.asp)
