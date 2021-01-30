# Loop Iteration

## For Loops

### Traditional Style

- initialization statement
- condition statement
- increment statement

Similar syntax as many other languages: </br>
```php
$nums = [5,4,3,2,1];
for ($i = 0; $i < count($nums); $i++) {
    echo $nums[i] // 5 then 4 then 3 ...
};
```

### Foreach Loop

Iterates over an iterable element (e.g., array or object) with each iterable assigned to a variable </br>
```php
$nums = [5,4,3,2,1];
foreach ($nums as $num) {
    echo $num // 5 then 4 then 3 ...
};

$phone_numbers = [
  "Alex" => "415-235-8573",
  "Jessica" => "415-492-4856",
];
foreach ($phone_numbers as $name => $number) {
  echo "$name's number is $number.\n"; 
  //Alex's number is 415-235-8573
  //Jessica's number is 415-492-4856
};
//or destructure value only
foreach ($phone_numbers as $number) {
  echo "Someone's number is $number.\n";
  //Someone's number is 415-235-8573
  //Jessica's number is 415-492-4856
};
```
### While Loops

Execute code until condition statement evaluates to false: </br>
```php
$counter = 0;
while ($counter < 10) {
    $counter += 1;
}
```

## Control Flow Statements

### Continue

`continue;` will skip the rest of code remaining for that loop block (starting the next iteration)

### Break

`break;` will stop execution for that loop