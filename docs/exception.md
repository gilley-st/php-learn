# Exception

## Try/Catch

Exceptional code ususallys has exceptions </br>
Skeleton of a basic exception is this: </br>

```php
try {
    //hopefully this works
} catch (Exception $e) {
    //well that did not work ... do this
}
```
Multiple `catch` blocks can be used for handling different types of exceptions

## Finally

At the end of a `try/catch` block, a `finally` block can be added to **always** execute regardless of outcome of `try/catch` block.  </br>
```php
try {
    //normal stuff
} catch (Exception $e) {
    //exception stuff
} finally {
    //will always run code in here
}
```
## Custom Exception/Error 

To have a custom exception/error use the following: </br>
```php
throw new Exception("Oooooops!  Write better code!");
```
