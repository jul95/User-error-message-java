# User-error-message-java
if a person were to type anything other than a number it would send out a message "Not a number "and tell you to put in your age and would not let you pass until you do put in a number for your age.

import java.util.Scanner;

public class Methodonist {
    public static void main(String[] args) {
      sayHello();

    }

    public static void sayHello() {
        Scanner agescann = new Scanner(System.in);
        int number = 0;
        boolean isNumber;
        // int age = agescann.nextInt();
       do {
           System.out.println("What is your age? ");

           if (agescann.hasNextInt()) {
               number = agescann.nextInt();
               isNumber = true;
           } else {
               System.out.println("Did not push number");
               isNumber = false;
               agescann.next();
           }
        } while (!(isNumber));

       System.out.println(number);

        Scanner namescann = new Scanner(System.in);
        System.out.println("whats your name? ");
        String name = namescann.nextLine();
        System.out.println("Your name: " + name + " Has been verified " + "And so is your age: " + number );




    }
}

