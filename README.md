# Simple-rock-paper-scissor
This is a simple rock paper scissor game code using java

import java.util.Random;              // Generating random number 
import java.util.Scanner;             // importing Scanner class
public class advnc_rk_ppr_scr {
    public static void main(String[] args) {   // Main method

        int n = 1;
        int com = 0;
        int man = 0;

        while (n <= 5) {          // while loop to play 5 rounds
            int x = 6 - n;

            Random random = new Random();  // creating object to generate random number
            int c = random.nextInt(1, 4);   // Generating random numbers between 1 and 4

            System.out.printf(".....Winner will be diclared after %d rounds....", +x);
            System.out.println("\nEnter your choice from below");
            System.out.println(" 1.paper\n 2.rock\n 3.scissor");   
            System.out.print("Enter choice : ");
            Scanner sc = new Scanner(System.in);
            int a = sc.nextInt();

            if (c == a) {
                System.out.println("draw");
            } else if (c == 1 && a == 2) {
                System.out.println("your choice is rock");
                System.out.println("Computer choice is paper");
                System.out.println("Computer won");
                com = com+1;

            } else if (c == 1 && a == 3) {
                System.out.println("your choice is scissor");
                System.out.println("Computer choice is paper");
                System.out.println("you won");
                man = man + 1;

            } else if (c == 2 && a == 1) {
                System.out.println("your choice is paper");
                System.out.println("Computer choice is rock");
                System.out.println("you won");
                man = man + 1;

            } else if (c == 2 && a == 3) {
                System.out.println("your choice is scissor");
                System.out.println("Computer choice is rock");
                System.out.println("Computer won");
                com = com+1;

            } else if (c == 3 && a == 2) {
                System.out.println("your choice is rock");
                System.out.println("Computer choice is scissor");
                System.out.println("you won");
                man = man + 1;

            } else if (c == 3 && a == 1) {
                System.out.println("your choice is paper");
                System.out.println("Computer choice is scissor");
                System.out.println("Computer won");
                com = com+1;

            }
            else {
                System.out.println("!!!Enter correct choice!!!");
                break;
            }
	    System.out.println("________________");
            System.out.println("              ");
            n++;
        }

        System.out.format("\nComputer won %d rounds ", +com);
        System.out.format("\nyou won %d rounds \n", +man);

        if(com == man){
            System.out.println("Draw");
        }

        else if (com < man){
            System.out.println("....Congrats you are the final winner....");
        }
        else {
            System.out.println("....The final winner is computer...");
        }
    }
}
