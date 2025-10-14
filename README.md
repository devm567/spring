# Prerequisites for Learning Spring Framework

## Core Java
- OOPs Concepts
  - Encapsulation
  - Inheritance
  - Polymorphism
  - Abstraction
- Exception Handling
- Multithreading
- Collections
  - List
  - Set
  - Map
  - Properties

## Advanced Java
- JDBC
- Web Applications
  - Servlet
  - JSP

## Frameworks
- Hibernate
- Spring
- Spring Boot

## Tools
- Build Tools
  - Maven
  - Gradle

## Spring Basics
- Spring Core
  - Inversion of Control (IoC)
  - Dependency Injection (DI)

# Basics of SB

![](images/1.png)

```java
class Student{
    //instance variable
    //methods : constructor, setter and getters, normal methods
}


Student s = new Student();
```

*) Dependency: A variable (instance variable) exist inside a class (Spring Bean)

=> Types of Dependencies: (3)
1. **Primitive Type Dependency (PTD) [8+1]** :
byte, short, int, long, float, double, boolean, char and `String`. If a variable is created using one of above datatype then it is called as PTD.

1. **Collection Type Dependency (CTD) [4] (java.util)** :
If a variable is created using one of below types
List, Set, Map (I) and Properties (C) then it is called as CTD.

1. **Reference Type Dependency (RTD)** :
A class or interface is used as a DataType and variable is created then it is called as RTD.


>Example:
![](images/2.png)
---

<img src="images/3.png" height="350">

> The process of injecting Dependable object to Target object is referred as `DI`.
 
![](images/4.png)

# Rules for Writing a Bean (Class) in Spring

1. public class (must be)
2. class should be in a package. </br>
   [must be in base package or sub-package].
3. variables recommended to be private.</br>
   Methods need to be public only.
4. Provide default constructor with mutators</br>
   (setter/getter methods)</br>
   [or]</br>
   Parameterized constructor</br>
   (Even both are also valid)</br>
5. Our class can have Object class methods overridden. toString(), equals() and hashCode().
   
6. class can inherit (extends / implements ) other valid Spring Beans only.</br>
   But not Servlets/EJB ... (other external APIS) 
* Spring Beans can implement java.io.Serializable (I)
1. Annotations: (can be)</br>
*) Core Annotations (java.lang package)</br>
*) ---- Spring F/W Annotation</br>
*)---- Custom Annotation