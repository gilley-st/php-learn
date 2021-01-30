# Object

## PHP

PHP is an OOP language.  It has classes that define the instantiation of an object. </br>

## Terminology

- Class __ defines object behavior (does not contain actual data)
- Object __ instance of class (contians data)
- Member __ variable beloning to object
- Method __ function beling to object (able to access members)
- Constructor __ special method at instantiation of class (creating object)

## Class

Here is an example of a class: </br>
```php
class Student {
    // constructor
    public function __construct($first_name, $last_name) {
        $this->first_name = $first_name;
        $this->last_name = $last_name;
    }

    public function say_name() {
        echo "My name is " . $this->first_name . " " . $this->last_name . ".\n";
    }
}

$alex = new Student("Alex", "Jones");
$alex->say_name();
```

## Inheritance

To extend functionality of the example Class Student, we can add another sub class to it: 

```php
class MathStudent extends Student {
    public function sum_numbers($first_number, $second_number) {
        return $first_number + $second_number;
    }
}

$eric = new MathStudent("Eric", "Jones"); //uses same constructor as Class Student
$eric->say_name(); //has Student methods
$eric->sum_numbers(3, 5); //has new method
```

## Encapuslation (Private versus Public)

In the previous examples, all methods have been `public`. </br>
If we make a function `private`, then that function can only be called **within** the object </br>
Below is an unrealstic but educational example: </br>

```php
class MathStudent extends Student {
    private function sum_numbers($first_number, $second_number) {
        return $first_number + $second_number;
    } // can only be called by other class methods
    public function sum($a, $b) {
        return $this->sum_numbers($a, $b); 
    }
}
$mathGenius = new MathStudent("Kurt", "Godel"); //uses same constructor as Class Student
$mathGenius->say_name(); //has Student methods
$mathGenius->sum(5,7); // has a new method that will work from outside of Class
$mathGenius->sum_numbers(5, 7); //will not work
```