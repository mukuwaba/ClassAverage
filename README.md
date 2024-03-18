import java.util.Scanner;

//This is a sample using the WHILE loop
public class ClassAverage {
    public static void main(String[] args) { // shortcut --> m + TAB

        Scanner input = new Scanner(System.in); //Create a Scanner Object to collect user input

        //Init's
        int total= 0;
        int gradeCounter = 0;

        System.out.print("Enter grade or -1 to quit: ");
        //printf only for when there is text and a format string defined
        int grade =input.nextInt();

        //Loop through and process the grades

        while(grade != -1) { //Loop counter compared to another value
            //while stay true as long as the value of less than or equal to 10
            //allows the while loop to end
            total = total + grade; //keeps adding the grades to the running total
            gradeCounter = gradeCounter + 1;
            //can do gradeCounter++

            System.out.print("Enter grade or -1 to quit: ");
            grade =input.nextInt();

        }//END: while
        //Only print the grade report if the user has entered grades
        if(gradeCounter != 0){
            //double average = total / 10
            double average = (double) total / gradeCounter;
            System.out.printf("%nTotal of all 10 grades is %d%n", gradeCounter, total);// souf + TAB
            System.out.printf("Class average is %.2f%n," , average); //float with 2 decimal statements
        }

        else {
            System.out.println("No grades were entered.");
        }
        //Calculate the average
       // int average = total / 10;

    }// END: main
}//END: class classAverage
