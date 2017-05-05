# Properties

## Java
Class properties in Java are accessible through getter and setter methods defined in a class. Java supports public, private, protected, and default access modifiers for properties.

Java does not support backing variables or computed variables; however, Java can replicate computed variables through the use of custom getters/setters.

### Example
An example showing a Java class with private fields and public getters/setters.

```java
public class Pet {
    private String name;
    private String breed;
    private String gender;

    public String getName() {
        return name;
    }

    public String getBreed() {
        return breed;
    }

    public String getGender() {
        return gender;
    }

    public void setName(String name) {
        this.name = name;
    }

    public void setBreed(String breed) {
        this.breed = breed;
    }

    public void setGender(String gender) {
        this.gender = gender;
    }
}
```

## PHP
Class properties in PHP are also accessible through getter and setter methods defined in a class. PHP supports public, private, and protected access modifiers for properties.

Like Java, PHP does not support backing fields or computed variables; however, PHP supports "magic methods" that can be used to set inaccessible fields in addition to standard getter/setters.

### Example
An example showing a PHP class with private fields and public getters/setters.

```php
<?php
An example showing a PHP class with private fields and public getters/setters.

class Pet {
    private $name;
    private $breed;
    private $gender;

    function getName() {
        return $this->name;
    }

    function getBreed() {
        return $this->breed;
    }

    function getGender() {
        return $this->gender;
    }

    function setName($name) {
        $this->name = $name;
    }

    function setBreed($breed) {
        $this->breed = $breed;
    }

    function setGender($gender) {
        $this->gender = $gender;
    }
}

?>
```

## C#
Class properties in C# are accessible through getter and setter methods defined in a class. Java supports public, private, protected, and internal access C# for properties.

Unlike Java and PHP, C# supports backing fields, which privately store data behind public methods, properties, and indexers.

### Example
An example showing a C# class with private backing fields public getter/setter properties.

```cs
public class Pet {
    private string name;
    private string breed;
    private string gender;

    public string Name { get; set; }
    public string Breed { get; set; }
    public string Gender { get; set; }
}
```
