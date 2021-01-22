# OOP_Unit_2

# Inheritance in C++

The capability of a class to derive properties and characteristics from another class is called Inheritance. Inheritance is one of the most important feature of Object Oriented Programming.
Sub Class: The class that inherits properties from another class is called Sub class or Derived Class.
Super Class:The class whose properties are inherited by sub class is called Base Class or Super class.


## Why and when to use inheritance?

Consider a group of vehicles. You need to create classes for Bus, Car and Truck. The methods fuelAmount(), capacity(), applyBrakes() will be same for all of the three classes. If we create these classes avoiding inheritance then we have to write all of these functions in each of the three classes as shown in below figure:

![](https://media.geeksforgeeks.org/wp-content/uploads/inheritance.png)

You can clearly see that above process results in duplication of same code 3 times. This increases the chances of error and data redundancy. To avoid this type of situation, inheritance is used. If we create a class Vehicle and write these three functions in it and inherit the rest of the classes from the vehicle class, then we can simply avoid the duplication of data and increase re-usability. Look at the below diagram in which the three classes are inherited from vehicle class:

![](https://media.geeksforgeeks.org/wp-content/uploads/inheritance2.png)

Using inheritance, we have to write the functions only one time instead of three times as we have inherited rest of the three classes from base class(Vehicle).

[For more info. use link](https://www.geeksforgeeks.org/inheritance-in-c/).

# Program 1

![](https://media.giphy.com/media/9weuRH37aE3X0U83q6/giphy.gif)

```C++
/*Program based on inheritance*/

#include <iostream>
using namespace std;

class Base 
{
  int x;

  public:
      void set_x(int n)
      {
        x = n;
      }

      void show_x()
      {
        cout<<"X = "<<x<<endl;
      }
};

class derived: public Base
{
  int y;

  public:
      void set_y(int n)
      {
        y = n; 
      }

      void show_y()
      {
        cout<<"Y = "<<y<<endl;  
      }
};

int main()
{
  int x, y;
  derived obj;
  cout<<"Enter value of x:\n";
  cin>>x;
  cout<<"Enter value of y:\n";
  cin>>y;
  obj.set_x(x);
  obj.set_y(y);
  obj.show_x();
  obj.show_y();

  return 0;
}
```
[Code Link](https://repl.it/@Siddharthsing13/Program-21#main.cpp)

# Program 2

![](https://media.giphy.com/media/TqiwHbFBaZ4ti/giphy.gif)


