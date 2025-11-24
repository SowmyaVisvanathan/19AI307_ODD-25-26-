# Ex.No:3(C) ABSTRACTION

## QUESTION:
- Create abstract class GameScore with method finalScore().
- Subclasses:
  1. ArcadeGame: score = baseScore + (level × 100)
  2. PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500
 
## AIM:
To write a Java program that uses an abstract class to calculate game scores for two types of games—ArcadeGame and PuzzleGame by implementing the abstract method in each subclass.

## ALGORITHM :
1. Start the program.
2. Create an abstract class game with an abstract method score().
3. Create subclass arc for ArcadeGame:
   - Data members: base score b, level l
   - Score formula: score = b + (l × 100)
4. Create subclass puzzle for PuzzleGame:
   - Data member: attempts a
   - Score formula:
```
        If a ≤ 3:
            score = 1000 - (a × 100)
        Else:
            score = 500
```
5. In main(): Read an integer t
6. If t == 1, create an object of arc
7. Otherwise, create an object of puzzle
8. Call the score() method polymorphically.
9. Print the final score.
10. End program.
    
## PROGRAM:
 ```
Program to implement a Abstraction using Java
Developed by: Sowmya V
RegisterNumber: 212222110045 
```

## SOURCE CODE:
```
import java.util.*;
abstract class game
{
    abstract int score();
}
class arc extends game
{
    int b,l;
    arc(int x,int y)
    {
        b=x;
        l=y;
    }
    int score()
    {
        return b+(l*100);
    }
}
class puzzle extends game
{
    int a;
    puzzle(int x)
    {
        a=x;
    }
    int score()
    {
    if(a<=3)
        return 1000-(a*100);
    else
        return 500;
    }
}
public class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        game g;
        if(t==1)
        {
            int b=sc.nextInt();
            int l=sc.nextInt();
            g=new arc(b,l);
        }
        else
        {
            int a=sc.nextInt();
            g=new puzzle(a);
        }
        System.out.println(g.score());
    }
}
```
## OUTPUT:

## RESULT:
The program successfully demonstrates runtime polymorphism using an abstract class.Depending on user input, the program creates either an ArcadeGame or PuzzleGame object, invokes the overridden score() method, and displays the correct final score.
