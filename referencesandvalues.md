# Comparisons of references and values

## Java
* `==` is a value comparison between primitive types.
* When two reference types are compared, the references are actually compared to see if they reference the same location
* `.equals` is a way to compare values of references
* Java always allows a developer to make a comparison between either the reference of the object, or the value.
## PHP
* [PHP's example of comparing Objects](http://php.net/manual/en/language.oop5.object-comparison.php)
```php

<?php
function bool2str($bool)
{
    if ($bool === false) {
        return 'FALSE';
    } else {
        return 'TRUE';
    }
}

function compareObjects(&$o1, &$o2)
{
    echo 'o1 == o2 : ' . bool2str($o1 == $o2) . "\n";
    echo 'o1 != o2 : ' . bool2str($o1 != $o2) . "\n";
    echo 'o1 === o2 : ' . bool2str($o1 === $o2) . "\n";
    echo 'o1 !== o2 : ' . bool2str($o1 !== $o2) . "\n";
}

class Flag
{
    public $flag;

    function Flag($flag = true) {
        $this->flag = $flag;
    }
}

class OtherFlag
{
    public $flag;

    function OtherFlag($flag = true) {
        $this->flag = $flag;
    }
}

$o = new Flag();
$p = new Flag();
$q = $o;
$r = new OtherFlag();

echo "Two instances of the same class\n";
compareObjects($o, $p);

echo "\nTwo references to the same instance\n";
compareObjects($o, $q);

echo "\nInstances of two different classes\n";
compareObjects($o, $r);
?>
```
Will output:
```
Two instances of the same class
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : FALSE
o1 !== o2 : TRUE

Two references to the same instance
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : TRUE
o1 !== o2 : FALSE

Instances of two different classes
o1 == o2 : FALSE
o1 != o2 : TRUE
o1 === o2 : FALSE
o1 !== o2 : TRUE
```
* PHP allows essentially the same comparisons of references vs. values as Java. It includes both ways to compare both references and values.

## C#
* `Equals` and `==` will compare by reference by default.
* Primitive types being compared with `==` will override the reference comparison to a value comparison.
* C# by default always compares references unless overriden by comparing primitive types.


