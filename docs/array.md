# Array

## Syntax
Declared with `[]` and delimited by a `,`. </br> 
```php
$list = [1,2,3,4]
echo $list[1] // 2
```

## Access
To access element, index starts at 0 (zero) </br>
Even if an index (say 5th index) is not defined, using `$myArray[5] = $myValue` will set that value  

## Functions

### General

#### >Print
Use `print_r(**array**)` to display contents of array in a humand readable format

#### >Count/Length
Use `count(**array**)` to get length of array

#### >Concatenate Array
Use `array_merge(**array**, ...**array**)` to concatenate arrays
```php
$some_nums = [1,2,3];
$other_nums = [4,5,6];
$all_nums = array_merge($some_nums, $other_nums);
print_r($all_numbers); // [1,2,3,4,5,6]
```

#### >Sort Array
Use `sort(**array**)` to sort ascending order: `rsort` for descending order </br>
Note that sorting is done on the array itself (does not return new array)

### Access

#### >Get First Index
Using `reset(**array**)` returns first element **and** resets internal iteration pointer (back to first element) </br>

#### >Get Last Index
Using `end(**array**)` returns last element

#### >Get Current Index
Using `current(**array**)` returns the value located at the index of the internal iteration pointer 

#### >Get Elements
Use `array_slice(**array**, **-/+ int for offset**, **int for amount**)` to get elements by offset and amount (defaults to reset of array) </br>
```php
$numbers = [1,2,3,4,5,6]
array_slice($numbers, 3) //[4,5,6] defaults to reset of array
//$numbers unaffected 
array_slice($numbers, 3, 2) //[4,5]
//$numbers unaffected
```
To return selected elements **and** remove elements from inputted array use function `array_splice` 

### Insertion/Deletion

#### >Delete Specific Index
Using `unset(**array**[**n**])` deletes value at index-n </br>
Note that array will not be automiatcally re-indexed to make indexes contiguous </br>
To re-index array use the `array_values`:
```php
$myArray = array_values($myArray) //now the array will have continguous indexes
```

#### >Add/Remove End of Array
Use `array_push` to add to end and `array_pop` to remove from the end of the array
```php
$numbers = [1,2,3]
array_push($numbers, 4)
print_r($numbers) //[1,2,3,4]
array_pop($number) // returns last element: 4
print_r($numbers) //[1,2,3]
```

#### >Add/Remove Beginning of Array
Use `array_unshift` to add to beginning and `array_shift` to remove the beginning of the array
```php
$numbers = [1,2,3]
array_unshift($numbers, 4)
print_r($numbers) //[4,1,2,3]
array_shift($number) // returns frst element: 4
print_r($numbers) //[1,2,3]
```



