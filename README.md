import java.util.Scanner;

public class StudentGradeCalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the Student Grade Calculator!");

        // Input for marks in 5 subjects (you can modify the number of subjects)
        System.out.print("Enter marks for Subject 1: ");
        double subject1 = scanner.nextDouble();
        
        System.out.print("Enter marks for Subject 2: ");
        double subject2 = scanner.nextDouble();
        
        System.out.print("Enter marks for Subject 3: ");
        double subject3 = scanner.nextDouble();
        
        System.out.print("Enter marks for Subject 4: ");
        double subject4 = scanner.nextDouble();
        
        System.out.print("Enter marks for Subject 5: ");
        double subject5 = scanner.nextDouble();

        // Calculate total marks and percentage
        double totalMarks = subject1 + subject2 + subject3 + subject4 + subject5;
        double percentage = (totalMarks / 500) * 100;

        // Determine grade based on percentage
        String grade = determineGrade(percentage);

        // Output the results
        System.out.println("\nResults:");
        System.out.println("Total Marks: " + totalMarks + " out of 500");
        System.out.println("Percentage: " + percentage + "%");
        System.out.println("Grade: " + grade);

        scanner.close();
    }

    // Method to determine the grade based on the percentage
    public static String determineGrade(double percentage) {
        if (percentage >= 90) {
            return "A+ (Excellent)";
        } else if (percentage >= 80) {
            return "A (Very Good)";
        } else if (percentage >= 70) {
            return "B+ (Good)";
        } else if (percentage >= 60) {
            return "B (Satisfactory)";
        } else if (percentage >= 50) {
            return "C (Average)";
        } else if (percentage >= 40) {
            return "D (Pass)";
        } else {
            return "F (Fail)";
        }
    }
}
