# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
finalPrice = purchaseWeight * (goldRatePerGram - discount)
For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).
## AIM:
To write a Java program using inheritance to calculate the final gold purchase price for Regular and Premium customers by applying their respective discounts, and to compute cashback for Premium customers.

## ALGORITHM :
1. Start
2. Input:
   - customerType (Regular / Premium / Other)
   - customerId
   - name
   - purchaseWeight
   - goldRatePerGram
3. Create an object based on customerType:
   - If Regular → create RegularCustomer
   - If Premium → create PremiumCustomer
   - Else → create normal Customer
4. For each customer calculate discount rate:
   - General = 0%
   - Regular = 2%
   - Premium = 5%
5. Compute discount amount
   - discountAmount = goldRatePerGram * (discountRate / 100)

6. Compute effective rate
   - effectiveRate = goldRatePerGram - discountAmount

7. Compute final price
   - finalPrice = purchaseWeight * effectiveRate

8. For Premium customer compute cashback
   - cashback = finalPrice * 0.01
  
9. Display customer details and final price.

10. End

## PROGRAM:
 ```
Program to implement a Inheritance and Aggregation using Java
Developed by: Sowmya V
RegisterNumber: 212222110045 
```
## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer 
{
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() 
    {
        return 0;
    }

    double calculateFinalPrice() 
    {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer 
{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() 
    {
        return 2;
    }

    @Override
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer 
{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() 
    {
        return 5;
    }

    double getCashback() 
    {
        return calculateFinalPrice() * 0.01;
    }

    @Override
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        String customerType = sc.next(); 
        String id = sc.next();
        String name = sc.next();
        double weight = sc.nextDouble();
        double goldRate = sc.nextDouble();

        Customer c;

        if (customerType.equals("Regular")) 
            c = new RegularCustomer(id, name, weight, goldRate);
        else if (customerType.equals("Premium")) 
            c = new PremiumCustomer(id, name, weight, goldRate);
        else 
            c = new Customer(id, name, weight, goldRate);

        c.display();
    }
}

```
## OUTPUT:
<img width="808" height="694" alt="image" src="https://github.com/user-attachments/assets/7e99564a-202b-46c1-ac2a-6a74413442a8" />

## RESULT:
The program successfully calculates the final price for Regular and Premium customers by applying the appropriate discounts. It also computes and displays the cashback amount for Premium customers, demonstrating the use of inheritance and method overriding in Java.
