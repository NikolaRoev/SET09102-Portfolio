# Code review

```C#
class Car
{
  public string model;

  // Class constructor
  public Car()
  {
    model = "Mustang"; // Set the initial value for model
  }

  static void Main(string[] args)
  {
    Car Ford = new Car();
    Console.WriteLine(Ford.model);
  }
}
```

- The property "model" should be uppercase. Could probably user a getter and setter functions, depending on how we might use it.
- Indentation is consistent but could be 4 spaces rather than 2. Do we really need a comment that the constructor is a constructor, etc.

```C#
class Car {
    public string Model { get; set; } = "Mustang";

    static void Main() {
        Car Ford = new();
        Console.WriteLine(Ford.Model);
    }
}
```

Following C# best practices I renamed the public property 'model' to be uppercase. Following the KISS principle I simplified the class by removing the constructor, adding a getter and a setter, and setting 'Model' to the initial default value.
