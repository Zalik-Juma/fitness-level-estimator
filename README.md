[fitnesslevel.java](https://github.com/user-attachments/files/24345364/fitnesslevel.java)
/*
*Name:Zalik Barasa Juma
*Reg No: J77-10594-2024
*Description: Program to determine fitness level based on daily steps
*/
import java.util.Scanner;

public class FitnessLevel {

    // Method to determine fitness level based on daily steps
    public static String getFitnessLevel(int steps) {
        if (steps >= 10000) {
            return "Excellent";
        } else if (steps >= 7000) {  // steps >= 7000 and < 10000
            return "Good";
        } else if (steps >= 4000) {  // steps >= 4000 and < 7000
            return "Average";
        } else {
            return "Poor";
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your steps for today: ");
        int steps = scanner.nextInt();

        String level = getFitnessLevel(steps);
        System.out.println("Your fitness level: " + level);

        scanner.close();
    }
}
