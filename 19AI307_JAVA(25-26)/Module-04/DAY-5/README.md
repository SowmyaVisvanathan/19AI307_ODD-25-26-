# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:
To build a simple Air Traffic Control System using the Mediator Pattern, where multiple airplanes request landing through one central mediator (ATC). The mediator decides whether landing is granted or denied based on runway availability.

## ALGORITHM :
1. Start
2. Create AirTrafficControl mediator with:
   - runwayFree = true
   - requestLanding() to grant/deny landing
   - releaseRunway() to free the runway
3. Create Airplane class:
   - Stores airplane name and reference to mediator
   - requestLanding() calls mediator to check permission
4. In main():
   - Read number of airplanes
   - Read whether runway should be released after each landing
   - Create ATC mediator
   - Create airplane objects and store them
   - Each airplane requests landing from ATC
5. End
## PROGRAM:
 ```
Program to implement a Behaviour Pattern using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.util.*;
class AirTrafficControl 
{
    private boolean runwayFree=true;
    public boolean requestLanding(Airplane plane)
    {
        if(runwayFree)
        {
            runwayFree = false;
            System.out.println(plane.getName()+" granted landing."); 
            return true;
        }
        else
        {
            System.out.println(plane.getName()+" denied landing. Runway busy.");
            return false;
        }
    }
    public void releaseRunway()
    {
        runwayFree=true;
    }
}

class Airplane 
{
    private String name;
    private AirTrafficControl atc;
    public Airplane(String name, AirTrafficControl atc)
    {
        this.name=name;
        this.atc=atc;
    }
    public String getName()
    {
        return name;
    }
    public void requestLanding(boolean releaseAfterLanding)
    {
        boolean granted = atc.requestLanding(this);
        if(granted)
        {
            System.out.println(name+ " landed successfully.");
            if(releaseAfterLanding)
                atc.releaseRunway();
        }
    }
}
public class AirTrafficSystem 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        AirTrafficControl atc = new AirTrafficControl();
        boolean release = sc.nextLine().equalsIgnoreCase("true");
        List<Airplane> planes = new ArrayList<>();
        for(int i=0;i<n;i++)
        {
            String name = sc.nextLine();
            planes.add(new Airplane(name,atc));
        }
        for(Airplane plane:planes)
            plane.requestLanding(release);
    }
}

```
## OUTPUT:
<img width="982" height="531" alt="image" src="https://github.com/user-attachments/assets/262ebaee-378e-4eef-a37b-675983427768" />

## RESULT:
The program successfully demonstrates how the Mediator Pattern works by coordinating landing requests between multiple airplanes and a single Air Traffic Control mediator.
