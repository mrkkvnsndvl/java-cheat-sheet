**Java Cheat Sheet** - This is a concise Java cheat sheet based on core concepts and syntax. It is designed to help you quickly reference Java fundamentals.

## **1. Basic Syntax**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

- `public class Main`: Defines a class named `Main`.
- `public static void main(String[] args)`: Entry point of the program.
- `System.out.println()`: Prints output to the console.

---

## **2. Data Types**

| Data Type | Size       | Description                     |
|-----------|------------|---------------------------------|
| `byte`    | 1 byte     | Stores whole numbers (-128 to 127) |
| `short`   | 2 bytes    | Stores whole numbers (-32,768 to 32,767) |
| `int`     | 4 bytes    | Stores whole numbers (-2^31 to 2^31-1) |
| `long`    | 8 bytes    | Stores whole numbers (-2^63 to 2^63-1) |
| `float`   | 4 bytes    | Stores fractional numbers (6-7 decimal digits) |
| `double`  | 8 bytes    | Stores fractional numbers (15 decimal digits) |
| `boolean` | 1 bit      | Stores `true` or `false`        |
| `char`    | 2 bytes    | Stores a single character/letter |

---

## **3. Variables**

```java
int num = 10;               // Integer
double pi = 3.14;           // Double
char letter = 'A';          // Character
boolean isJavaFun = true;   // Boolean
String name = "Java";       // String
```

---

## **4. Operators**

| Type          | Operators                          |
|---------------|------------------------------------|
| Arithmetic    | `+`, `-`, `*`, `/`, `%`, `++`, `--`|
| Assignment    | `=`, `+=`, `-=`, `*=`, `/=`        |
| Comparison    | `==`, `!=`, `>`, `<`, `>=`, `<=`   |
| Logical       | `&&`, `||`, `!`                    |

---

## **5. Control Flow**

### If-Else
```java
if (condition) {
    // code
} else if (condition) {
    // code
} else {
    // code
}
```

### Switch
```java
switch (variable) {
    case value1:
        // code
        break;
    case value2:
        // code
        break;
    default:
        // code
}
```

### Loops
```java
for (int i = 0; i < 5; i++) {
    // code
}

while (condition) {
    // code
}

do {
    // code
} while (condition);
```

---

## **6. Arrays**

```java
int[] numbers = {1, 2, 3, 4, 5};  // Array declaration
System.out.println(numbers[0]);   // Access first element
numbers[1] = 10;                  // Modify second element
int length = numbers.length;      // Get array length
```

---

## **7. Methods**

```java
public static int add(int a, int b) {
    return a + b;
}

// Method call
int result = add(5, 10);
```

---

## **8. Object-Oriented Programming (OOP)**

### Class and Object
```java
class Car {
    String brand;  // Field

    // Constructor
    public Car(String brand) {
        this.brand = brand;
    }

    // Method
    public void drive() {
        System.out.println("Driving " + brand);
    }
}

// Create an object
Car myCar = new Car("Toyota");
myCar.drive();
```

### Inheritance
```java
class Vehicle {
    void run() {
        System.out.println("Vehicle is running");
    }
}

class Bike extends Vehicle {
    void run() {
        System.out.println("Bike is running");
    }
}
```

### Encapsulation
```java
class Person {
    private String name;  // Private field

    // Getter
    public String getName() {
        return name;
    }

    // Setter
    public void setName(String name) {
        this.name = name;
    }
}
```

### Polymorphism
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}
```

---

## **9. Exception Handling**

```java
try {
    int[] arr = new int[5];
    System.out.println(arr[10]);  // Throws ArrayIndexOutOfBoundsException
} catch (Exception e) {
    System.out.println("An error occurred: " + e.getMessage());
} finally {
    System.out.println("This will always execute");
}
```

---

## **10. File Handling**

```java
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");
            FileWriter writer = new FileWriter(file);
            writer.write("Hello, Java!");
            writer.close();
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```

---

## **11. Common String Methods**

```java
String str = "Hello, Java!";
int length = str.length();                // Length of string
String upper = str.toUpperCase();         // Convert to uppercase
String lower = str.toLowerCase();         // Convert to lowercase
boolean contains = str.contains("Java");  // Check if string contains substring
String substring = str.substring(0, 5);   // Extract substring
```

---

## **12. Collections Framework**

### ArrayList
```java
import java.util.ArrayList;

ArrayList<String> fruits = new ArrayList<>();
fruits.add("Apple");
fruits.add("Banana");
System.out.println(fruits.get(0));  // Access element
fruits.remove(1);                   // Remove element
```

### HashMap
```java
import java.util.HashMap;

HashMap<String, Integer> map = new HashMap<>();
map.put("Apple", 10);
map.put("Banana", 20);
System.out.println(map.get("Apple"));  // Access value
map.remove("Banana");                  // Remove key-value pair
```

---

## **13. Lambda Expressions**

```java
interface MathOperation {
    int operate(int a, int b);
}

public class Main {
    public static void main(String[] args) {
        MathOperation add = (a, b) -> a + b;
        System.out.println(add.operate(5, 10));  // Output: 15
    }
}
```

---

## **14. Threading**

```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.start();  // Start the thread
    }
}
```
