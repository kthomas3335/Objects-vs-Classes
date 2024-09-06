# Objects-vs-Classes

Explanation of Objects and Classes
Objects and classes are central concepts in object-oriented programming (OOP). A class is a blueprint or template that defines the structure and behavior (methods) of objects. Think of it as a design plan for creating objects. It specifies what attributes (fields) and methods (functions) the objects created from it will have. However, a class does not hold any actual data—it only provides the structure.

An object, on the other hand, is an instance of a class. It’s a concrete entity created based on the class blueprint, with its own unique values for the fields defined by the class. In simpler terms, if a class is like the blueprint of a house, then an object is an actual house built using that blueprint. Each object can have different properties, even though they all follow the same structure provided by the class.

Conceptual Differences
Class: A class defines the properties and methods but does not allocate memory for them.
Object: An object is an instance of a class, and it occupies memory. It contains specific values for the attributes defined by the class.

Here is another way to think about it. Imagine you're building with Legos. Before you build anything, you have a plan or instruction booklet. This plan tells you what pieces you need and how to put them together. In programming, this plan is called a class. A class is like a set of instructions that tells the computer what something should look like and what it can do.

For example, think of a Car class. This class says every car has certain things like a brand (Toyota, Honda), a model (Camry, Civic), and a year (2020, 2018). It also says that every car can do things like "drive" or "stop." But remember, the class is just a plan—no real car yet!

Now, when you actually build a car with your Legos, you're making an object. The object is a real thing you can see and touch, while the class is just the instructions. In programming, when you make an object, you're creating a real car based on the class plan.

You can make lots of objects (cars) from the same class (instructions). Maybe you build a red car first (that’s one object), and then a blue car (that’s another object). Each car is different, but both were built using the same instructions. This is how objects and classes work together in Java.

So, a class is like the idea or plan, and an object is the real thing made from that plan. You can make many objects from one class, and they can all have different details, but they follow the same rules.

Example code:
```java
// Define a class called "Car"
class Car {
    // Fields/attributes of the class
    String brand;
    String model;
    int year;

    // Constructor to initialize the object
    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    // Method to display car details
    void displayDetails() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        // Create an object of the class Car
        Car car1 = new Car("Toyota", "Camry", 2020);
        Car car2 = new Car("Honda", "Civic", 2018);

        // Access the object's methods and fields
        car1.displayDetails();  // Output details of car1
        System.out.println();
        car2.displayDetails();  // Output details of car2
        
        // Objects are different instances with their own unique values
        System.out.println("\nCar 1 year: " + car1.year); // Outputs 2020
        System.out.println("Car 2 year: " + car2.year);   // Outputs 2018
    }
}
```
Explanation of Code
Class: The Car class defines attributes such as brand, model, and year. It also contains a constructor to initialize these values when creating an object and a method to display the car’s details.
Object: In the main method, two objects of the Car class, car1 and car2, are created. Both are separate instances with their own attribute values.
Each object occupies memory and holds its specific data, whereas the class is just a blueprint.
