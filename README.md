# jbook

### Java Programming Tutorial

#### 1. **Java Hello World**

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
Output:
```
Hello, World!
```

#### 2. **Variables and Data Types**

```java
public class VariablesExample {
    public static void main(String[] args) {
        int num = 10;
        double floatingNum = 3.14;
        String text = "Java programming";
        boolean isTrue = true;
        System.out.println("Number: " + num + ", Float: " + floatingNum + ", String: \"" + text + "\", Boolean: " + isTrue);
    }
}
```
Output:
```
Number: 10, Float: 3.14, String: "Java programming", Boolean: true
```

#### 3. **Input and Output**

##### Taking User Input

```java
import java.util.Scanner;

public class UserInputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello, " + name + "!");
        scanner.close();
    }
}
```
Output (assuming user inputs `Alice`):
```
Enter your name: Alice
Hello, Alice!
```

##### Reading and Writing Files

```java
import java.io.*;

public class FileExample {
    public static void main(String[] args) {
        String fileName = "output.txt";
        try (PrintWriter writer = new PrintWriter(new FileWriter(fileName))) {
            writer.println("Hello, Java!");
        } catch (IOException e) {
            System.err.println("Error writing to file " + fileName + ": " + e.getMessage());
        }
    }
}
```
Creates `output.txt` with content `Hello, Java!`.

#### 4. **Control Structures**

##### Conditional Statements

```java
public class ConditionalExample {
    public static void main(String[] args) {
        int num = 10;
        if (num == 10) {
            System.out.println("Number is 10.");
        } else if (num > 10) {
            System.out.println("Number is greater than 10.");
        } else {
            System.out.println("Number is less than 10.");
        }
    }
}
```
Output:
```
Number is 10.
```

##### Loops

###### For Loop

```java
public class ForLoopExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Iteration " + i);
        }
    }
}
```
Output:
```
Iteration 1
Iteration 2
Iteration 3
Iteration 4
Iteration 5
```

###### While Loop

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int count = 0;
        while (count < 5) {
            System.out.println("Count: " + count);
            count++;
        }
    }
}
```
Output:
```
Count: 0
Count: 1
Count: 2
Count: 3
Count: 4
```

#### 5. **Arrays**

```java
public class ArraysExample {
    public static void main(String[] args) {
        String[] fruits = {"Apple", "Banana", "Cherry"};
        System.out.println("First fruit: " + fruits[0]);
        System.out.println("All fruits: " + String.join(", ", fruits));
    }
}
```
Output:
```
First fruit: Apple
All fruits: Apple, Banana, Cherry
```

#### 6. **ArrayList**

```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Cherry");
        System.out.println("List: " + list);
    }
}
```
Output:
```
List: [Apple, Banana, Cherry]
```

#### 7. **Object-Oriented Programming (OOP)**

##### Classes and Objects

```java
public class Person {
    private String name;
    private int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getter methods
    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    public static void main(String[] args) {
        Person person = new Person("Alice", 30);
        System.out.println("Person's name: " + person.getName() + ", Age: " + person.getAge());
    }
}
```
Output:
```
Person's name: Alice, Age: 30
```

##### Inheritance

```java
// Parent class
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

// Child class (inherits from Animal)
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class InheritanceExample {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound();
    }
}
```
Output:
```
Dog barks
```

##### Polymorphism

```java
// Animal class
abstract class Animal {
    abstract void sound();
}

// Dog class extending Animal
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

// Cat class extending Animal
class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

public class PolymorphismExample {
    public static void main(String[] args) {
        Animal dog = new Dog();
        Animal cat = new Cat();

        dog.sound();
        cat.sound();
    }
}
```
Output:
```
Dog barks
Cat meows
```

##### Encapsulation

```java
// Person class
public class Person {
    private String name;
    private int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getter and setter methods
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public static void main(String[] args) {
        Person person = new Person("Bob", 25);
        System.out.println("Name: " + person.getName() + ", Age: " + person.getAge());
    }
}
```
Output:
```
Name: Bob, Age: 25
```

