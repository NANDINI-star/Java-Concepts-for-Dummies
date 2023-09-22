# 1. Final vs Finally vs Finalize for Dummies
Java Standard Edition 8

````
💡 Java SE 8 reached its end of public updates and support from Oracle in January 2019.
````

## How come I chose this as the first topic?

I was recently going through Garbage Collectors, which led me to `finalize`, which led me to here.

## Final Keyword in Java
Ref. https://docs.oracle.com/javase/tutorial/java/IandI/final.html

Taking it up straight from the official docs, let's try to understand this.

It says you can use the final keyword with `classes and methods`. Well, you can use it with `variables and parameters` as well.

`classes, methods, variables and parameters` are used to design an entity in Java.

````
💡 Entity is something out there in the real world that can be recognized.
````

````
// declaring a final variable
class FinalVariable {

        final int var = 50;
        
        var = 60 //This line would give an error

}
````

For a final reference variable you cannot change what object it refers to. You can, however, modify the object itself.

````
class Reference{
    public int value = 5;
}

class frVariable {
    public static void FinalReference( String args[] ) {

      final Reference example = new Reference(); //declaration
      example.value = 6; // Modifying the object creates no disturbance

      Reference another = new Reference();
      example = another; // Attempting to change the object it refers to, creates an error
     
         }
}
````
