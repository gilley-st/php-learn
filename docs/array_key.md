# Array (key-indexed)

## Syntax

Arrays can be key/zero index (or hybrid) </br>
```php
$phone_numbers = [
  "Alex" => "415-235-8573",
  "Jessica" => "415-492-4856",
];
echo $phone_numbers["Alex"]; //"415-235-8573"
```

## Insert

To add a key/value pair do this: </br>
```php
$my_array["my_key"] = "my_value";
```

## array_key_exists

To verify a key exists on an array do this: </br>
```php 
$phone_numbers = [
  "Alex" => "415-235-8573",
  "Jessica" => "415-492-4856",
];
array_key_exists("Jones", $phone_numbers); // false
//returns true if key is set to null constant
$phone_numbers["Jones"] = null;
array_key_exists("Jones", $phone_numbers); // true
```
Note that it does not test nested arrays only: top level of inputted array. </br>

## arrays_keys

To get all keys of an arary do this: </br>
```php
array_keys($my_array);
```

## array_values

To get all values of an array do this: </br>
```php
array_values($phone_numbers);
```