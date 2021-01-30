# String

## Syntax
Single quotes are string literals: `\'` esacpes single quote and `\\` escapes backslash <br>
```php
$str = 'Literally, I\'m way too literal'
```
Double quotes are template literal strings (c.f., Formatting section)

## Formating

Double quotes are template literal strings that output `$` variables in the resulting string </br>
```php
$movie = 'The Room';
echo "The best movie is $movie";
```
Concatenate strings by using the `.` (dot) operator </br>
```php
$example = 'Sorry to ' . 'string you ' . 'along!';
```

## Count

To count chars in a string use this: 
```php
$string = "The length of this string is 43 characters.";
echo strlen($string);
```

## Get Sub String

To get a specific part of a string use this: 
```php
$filename = "image.png";
$extension = substr($filename, strlen($filename) - 3); //png
```
**string** `string` is the input to get subsection from
**offset** `+/- int` defines start of string subsection (postive beginning of string and negative ending of string)
**length** `+/- int` (optional = `null`)  defines end of string subsection (postive beginning of string and negative ending of string) 

## Split via Delimiter 

To split a string via a delimiting string use this: 
```php
$fruits = "apple,banana,orange";
$fruit_list = explode(",", $fruits); //["apples", "banana", "orange"]
```

## Join via Delimiter

To join a string via a delimiting string use this:
```php
$fruit_list = ["apple","banana","orange"]; //"apple,banana,orange"
$fruits = implode(",", $fruit_list);
```