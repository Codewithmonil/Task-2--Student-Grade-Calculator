# Task-2--Student-Grade-Calculator
import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
        // Input: Number of subjects
                System.out.print("Enter the number of subjects: ");
                        int numSubjects = scanner.nextInt();
        // Initialize variables
                int totalMarks = 0;
        // Input marks for each subject and calculate total marks
                for (int i = 1; i <= numSubjects; i++) {
                            System.out.print("Enter marks obtained in subject " + i + " (out of 100): ");
                                        int subjectMarks = scanner.nextInt();
                                                    totalMarks += subjectMarks;
                                                            }
        // Calculate average percentage
                double averagePercentage = (double) totalMarks / (numSubjects * 100) * 100;
        // Calculate grade
                String grade = calculateGrade(averagePercentage);
        // Display results
                System.out.println("Total Marks: " + totalMarks);
                        System.out.println("Average Percentage: " + averagePercentage + "%");
                                System.out.println("Grade: " + grade);
        scanner.close();
            }
    // Function to calculate grades
        public static String calculateGrade(double percentage) {
                if (percentage >= 90) {
                            return "A+";
                                    } else if (percentage >= 80) {
                                                return "A";
                                                        } else if (percentage >= 70) {
                                                                    return "B";
                                                                            } else if (percentage >= 60) {
                                                                                        return "C";
                                                                                                } else if (percentage >= 50) {
                                                                                                            return "D";
                                                                                                                    } else {
                                                                                                                                return "F";
                                                                                                                                        }
                                                                                                                                            }
                                                                                                                                            }
