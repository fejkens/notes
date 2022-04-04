# Static vs instance members

A class definition can have either static or instance members. Any property/method with the 'static' keyword means that the property/method belongs to the class itself and can be used without creating an object of that type.

Class definition --------> Object of type Class

        |                           |
        |                           |
        |                           |
        *                           *

Static members               Non-static members

## Using a static method

```C#
    class Program
    {
        public static void Main(string[] args)
        {
            Animal.MakeASound(); // We don't need to create an instance of the Animal class, we can just call the method
        }
    }
    class Animal
    {
        public static void MakeASound()
        {
            Console.WriteLine("Generic animal sound");
        }
    }
```

## Using a non-static method

```C#
    class Program
    {
        public static void Main(string[] args)
        {
            Cat myCat = new Cat(); // We have to create an instance of the Cat class (Cat object)
            myCat.MakeASound(); // We can call the non-static method on the object
        }
    }
    class Cat
    {
        public void MakeASound()
        {
            Console.WriteLine("meow");
        }
    }
```