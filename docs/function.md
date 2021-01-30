# Function

## Syntax

Functions enclose their scope, so code outside of its scop cannot access the function's value </br>

```php
function add ($a, $b = 0) { //default $b value to 0 if not supplied
    return $a + $b;
}
add(4) // 4
add(4, 1) // 5
```