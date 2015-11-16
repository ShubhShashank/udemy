# Udemy Chapter 7: PHP

___

## Lecture 170: Error Messages

* php.ini 

 * will tell you if there are errors in your code.
 
 * `display_error = on
    display_startup_errors = on`
 
___
 
## Lecture 171: Variables

* Variable Syntax
 
 * no #'s at beginning of variable

 * `$varName="what its equal to";`
 
* Escaping Characters

 * Use backslash `\`
 
 * `$var="\"This var is set to a string, inside double quotations\"";`
 
* to display

 * `echo $varName`
 
* Concatenate: use "." instead of "+"

 * `echo $var1.$var2;`
 
* Variable Variables 

 * `$name="devon";
    $var="name";
    echo $$var;`
    
 * echos devon
 
 ___
 
## Lecture 173: Arrays

* to print array

 * `$myArray=array("dogs", "food", "stuff");
      print_r($myArray);`

* echo particular object in array

 * `$myArray=array("dogs", "food", "stuff");
      print_r($myArray);
      echo $myArray[0];`
      
* line breaks needed to separate lines

 * `echo "<br />";`
  
* another array setup, named index
 
 * `$otherArray=array(
       "riley" => "dog",
       "germany => "country"
     );`
  
 * value "dog" is at index "riley"
 
* remove value from array

 * `unset($otherArray["germany"]);`
 
 ___
 
 
## Lecture 174: if statements

* if $x equals $y 

 * `if ($number==$otherNumber) {
        echo "number equals otherNumber";
        }
    else {
            echo "number does not equal otherNumber";
        }`
        
* if $x does not equal $y

 * `if ($thiss!=$that) {
            echo "this is not that";
        }
    else {
            echo "this is that";
        }`
        
* if $x equals $y AND $z

 * `if ($number==$otherNumber AND $number==$that) {
            echo "number equals otherNumber AND that";
        }
    else {
            echo "number does not equal otherNumber AND that";
        }`
        
## Lecture 175: for and Foreach:

* for loops 

 * `for ($i=1; $i<=10; $i++) {
        echo $i."<br />";
      }`
      
* for each

 * ` $array=array("devon", "riley", "auri");
     foreach ($array as $key => $value) {
            echo "Key: $key Value: $value <br />";
        }`
        
___
        
## Lecture 177: While loops

* loops for arrays 

 * `$i=0;
    $array=array("devon ", "riley ", "auri");
        while ($array[$i]) {
        echo $array[$i];
     $i++;
    }`
    
 ___
 
## Lecture 178: Sending emails with php

* inside body of html file

 * `<?php    
            $emailTo="test@greenhost.org.uk";
            $subject="this should work"
            $body="body text";
            $headers="From: devonwarmack@blabla.com";  
            mail($emailto, $subject, $body, $headers);
        ?>`
        
* to check if mail was SENT:

 * `if (mail($emailto, $subject, $body, $headers)) {
        echo "Mail was sent.";
    }
    else {
        echo "mail was not sent.";
    }`
    
    ___
    
## Lecture 180 GET variables:

* $_GET 

 * get array with all variables in URL of website
    
* use with a form 

 * `<?php
        if($_GET["submit"]) {            
            if($_GET["name"]) {    
                echo "your name is ".$_GET['name'];
            }  
            else {
                echo "enter your name";
            }
        }
    ?>`
    
    ___
    
## Lecture 182 POST variables:

* `<?php   
           $names=array("devon", "riley", "auri");   
               if($_POST["submit"]) {
                   if($_POST["name"]) {   
                       foreach ($names as $name) {
                           if ($_POST["name]==$name) {
                               echo "I know you. your name is ".$name;
                               $knowYou=1;
                           }   
                       }
                       if (!$knowYou) echo "i dont know you. ".$_POST['name'];
                   }
                      else {
                       echo "enter your name";
                   }
               }
           ?>`
            
___

 

 
 
 

