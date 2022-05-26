# Operator-Overloading

## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ##Algorithm:
 
 1) Create a class for operator overloading
 2) get inputs for length,breadthandheight of the box fromthe user and then calculate the volume in overloading function
 3) after that return a new object for the calculated volume
 4) then create a new object to store the return object
 5) After that print the calculated volume
 
 
 ##Program:
 using System;
class example
{
    public int length, breadth,height, volume;
    public static example operator +(example e1, example e2)
    {
        example e3 = new example();
        Console.WriteLine("Box1");
        Console.WriteLine(e1.length * e1.breadth * e1.height);
        Console.WriteLine("Box2");
        Console.WriteLine(e2.length * e2.breadth * e2.height);
        e3.length = e1.length + e2.length;
        e3.breadth = e1.breadth + e2.breadth;
        e3.height = e1.height + e2.height;
        e3.volume = e3.length * e3.breadth * e3.height;
        return e3;
    }
    public static void Main()
    {
        example e1 = new example();
        e1.length = Convert.ToInt32(Console.ReadLine());
        e1.breadth = Convert.ToInt32(Console.ReadLine());
        e1.height = Convert.ToInt32(Console.ReadLine());
        example e2 = new example();
        e2.length = Convert.ToInt32(Console.ReadLine());
        e2.breadth = Convert.ToInt32(Console.ReadLine());
        e2.height = Convert.ToInt32(Console.ReadLine());
        example e4 = new example();
        e4 = e1 + e2;
        Console.WriteLine("Box3");
        Console.WriteLine(e4.volume);
    }
}

 
 ##Output:
![image](https://user-images.githubusercontent.com/75235128/170470308-8fe5f176-8c25-49d0-be1d-c0909b4a9e18.png)

 ##Result:
Thus a C# program to find the volume of a box using operator overloading is written and executed sucessfully.
