# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation. Your task is to simulate this system using the Singleton pattern.

## AIM:
1. To simulate an airport scenario where only one Radar Control Tower exists, regardless of how many flights arrive.
2. Every incoming flight must communicate with the same single instance of the tower.
3. Use the Singleton Design Pattern to ensure:
   - Only one RadarControlTower object is ever created.
   - All flights share this same instance to register themselves.
   - The tower keeps a global count of registered flights.

## ALGORITHM :
1. START
2. Create RadarControlTower Singleton with:
   - private static instance
   - private constructor
   - getInstance() returning the same instance
   - registerFlight() to increment flight count
3. Read number of flights n
4. Repeat n times:
   - Read flight name
   - Get tower instance
   - Register the flight
   - Display flight count
5. END
## PROGRAM:
 ```
Program to implement a SOLID Principles in Java Program
Developed by: Sowmya V
RegisterNumber: 212222110045  
```
## SOURCE CODE:
```
import java.util.*;
class RadarControlTower 
{
    private static RadarControlTower instance;
    private int count = 0;
    private RadarControlTower()
    {
    
    }
    public static RadarControlTower getInstance()
    {
        if(instance==null)
            instance = new RadarControlTower();
        return instance;
    }
    public int registerFlight(String name)
    {
        count++;
        return count;
    }
}
public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); 
        for (int i = 0; i < n; i++) 
        {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}

```
## OUTPUT:
<img width="1152" height="175" alt="image" src="https://github.com/user-attachments/assets/42edb6f8-39d4-4ae4-a387-e570798f139b" />

## RESULT:
The program successfully demonstrates how to implement and use the Singleton design pattern by ensuring that all flights communicate with the same single instance of the Radar Control Tower, maintaining a consistent global flight count.
