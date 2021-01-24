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