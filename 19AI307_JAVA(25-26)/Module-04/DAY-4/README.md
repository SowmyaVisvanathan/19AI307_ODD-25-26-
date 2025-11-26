# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
1. To create animals from two regions (Africa and Asia) using the Abstract Factory Design Pattern.Each region produces two types of animals:
- Herbivore
- Carnivore

## ALGORITHM :
1. Start the program.
2. Define abstract product interfaces:
   - Herbivore
   - Carnivore
3. Define concrete products for each region:
   - Africa: Zebra (Herbivore), Lion (Carnivore)
   - Asia: Deer (Herbivore), Tiger (Carnivore)
4. Define an abstract factory AnimalFactory with methods:
   - createHerbivore()
   - createCarnivore()
5. Create concrete factories:
   - AfricaFactory
   - AsiaFactory
6. In main():
   - Read region name.
   - Choose the factory based on region.
   - Create herbivore + carnivore using that factory.
   - Print interaction like:
7. End program.
   
## PROGRAM:
 ```
Program to implement a Abstract Factory Pattern using Java
Developed by: Sowmya V
RegisterNumber: 212222110045 
```
## SOURCE CODE:
```
import java.util.Scanner;
interface Herbivore {}

interface Carnivore 
{
    void eat(Herbivore h);
}
interface AnimalFactory 
{
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore 
{
    public void eat(Herbivore h) 
    {
        System.out.println("Lion eats Wildebeest");
    }
}

class Deer implements Herbivore {}
class Tiger implements Carnivore 
{
    public void eat(Herbivore h) 
    {
        System.out.println("Tiger eats Buffalo");
    }
}

class AfricaFactory implements AnimalFactory 
{
    public Herbivore createHerbivore() 
    { 
        return new Wildebeest(); 
    }
    public Carnivore createCarnivore() 
    { 
        return new Lion(); 
    }
}
class AsiaFactory implements AnimalFactory 
{
    public Herbivore createHerbivore() 
    { 
        return new Deer(); 
    }
    public Carnivore createCarnivore() 
    { 
        return new Tiger(); 
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();

        AnimalFactory factory;
        
        if (region.equals("africa")) 
            factory = new AfricaFactory();
        else if (region.equals("asia")) 
            factory = new AsiaFactory();
        else 
        {
            System.out.println("Invalid region");
            return;
        }
        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}

```
## OUTPUT:
<img width="583" height="231" alt="image" src="https://github.com/user-attachments/assets/f1c814e0-58a1-4dcd-ad0c-a67fd845c421" />


## RESULT:
The program successfully demonstrates how to use the Abstract Factory Pattern to create families of related animals (herbivore + carnivore) from different regions (Africa/Asia).
