
import java.util.Scanner;

public class GradeCalculator {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		double weight;
		int score;
		int totalKnownGradeWeight;
		int Exam1;
		int  Exam2;
		int finalExam;
		int labs;
		int Projects;
		int Participation;
		int Quizzes;
		int Score1 = 0;
		int Score2;
		int Score3;
		int labScore;
		int projectAverage = 0;
		int quizAverage = 0;
		int participationAverage = 0;
		Score2 = 0;
		Score3 = 0;
		labScore = 0;
		Projects = 0;
		Participation = 0;
		Quizzes = 0;
		double currentGradeScore;

		Scanner keyboard = new Scanner(System.in);
		System.out.println("Grading Scale:");
		System.out.println("A    \t90-100");
		System.out.println("B    \t80-89 ");
		System.out.println("C    \t70-70 ");
		System.out.println("D    \t60-69 ");
		System.out.println("F \tbelow 60 ");

		System.out.println("What letter grade do you want to achieve for this course?");
		String letterGrade = keyboard.nextLine();

		System.out.println("Enter percentage weights below");
		System.out.print("Exam 1:     \t");
		Exam1 = keyboard.nextInt();


		System.out.print("Exam 2:     \t");
		Exam2 = keyboard.nextInt();


		System.out.print("Final Exam: \t");
		finalExam = keyboard.nextInt();


		System.out.print("Labs        \t");
		labs = keyboard.nextInt();

		System.out.print("Projects    \t");
		Projects = keyboard.nextInt();

		System.out.print("Participation\t");
		Participation = keyboard.nextInt();

		System.out.print("Quizzes     \t");
		Quizzes = keyboard.nextInt();

		totalKnownGradeWeight = (Exam1 + Exam2 + finalExam + labs + Projects + Participation + Quizzes);
		if(totalKnownGradeWeight == (100));
		{


		}


		{

		}
		String Answer1 = "Yes";
		System.out.print("Do you know your exam 1 score?");

		Scanner scanner = new Scanner(System.in);
		String Answer = scanner.nextLine();


		if(Answer1.equalsIgnoreCase(Answer) || Answer.equalsIgnoreCase("y"))
		{
			System.out.print("Score recieved on exam 1:");
			Score1 = keyboard.nextInt();



			System.out.print("Do you know your score on exam 2?");
			Scanner scanner1 = new Scanner(System.in);
			String Answer2 = scanner1.nextLine();
			if(Answer1.equalsIgnoreCase(Answer2) || Answer.equalsIgnoreCase("y"))
			{
				System.out.print("Score recieved on exam 2:");
				Score2 = keyboard.nextInt();
			}

			System.out.print("Do you know your final exam score?");
			Scanner scanner2 = new Scanner(System.in);
			String Answer3 = scanner2.nextLine();
			if(Answer1.equalsIgnoreCase(Answer3) || Answer.equalsIgnoreCase("y"))
			{
				System.out.print("Score received on final exam:");
				Score3 = keyboard.nextInt();
			}
		}


		System.out.print("Do you know your lab average?");
		Scanner scanner3 = new Scanner(System.in);
		String Answer4 = scanner3.nextLine();
		if(Answer1.equalsIgnoreCase(Answer4) || Answer.equalsIgnoreCase("y"))
		{
			System.out.print("Average lab grade:");
			labScore = keyboard.nextInt();
		}

		System.out.print("Do you know your project average?");
		Scanner scanner4 = new Scanner(System.in);
		String Answer5 = scanner4.nextLine();
		if(Answer1.equalsIgnoreCase(Answer5) || Answer.equalsIgnoreCase("y"))
		{
			System.out.print("Average project grade:");
			projectAverage = keyboard.nextInt();
		}

		System.out.print("Do you know your participation average");
		Scanner scanner5 = new Scanner(System.in);
		String Answer6 = scanner5.nextLine();
		if(Answer1.equalsIgnoreCase(Answer6) || Answer.equalsIgnoreCase("y"))
		{
			System.out.print("Average participation grade");
			participationAverage = keyboard.nextInt();
		}

		System.out.print("Do you know your average quiz grade?");
		Scanner scanner6 = new Scanner(System.in);
		String Answer7 = scanner6.nextLine();
		if(Answer1.equalsIgnoreCase(Answer7) || Answer.equalsIgnoreCase("y"))
		{
			System.out.print("Average quiz grade:");
			quizAverage = keyboard.nextInt();
		}
		String letterGrade1="";

		double currentGradeScore2;
		double currentGradeScore3;
		currentGradeScore = (Exam1 * Score1) + (Exam2 * Score2) + ( finalExam * Score3) + (labs * labScore) + (Projects * projectAverage) + (Participation * participationAverage)+(Quizzes * quizAverage);
		currentGradeScore2 = Exam1 + Exam2 + finalExam + labs + Projects + Participation + Quizzes ;
		currentGradeScore3 = (currentGradeScore / currentGradeScore2);

		if(currentGradeScore3 >= 90) {
			letterGrade1 = "A";
		}
		else if (currentGradeScore3 >= 80) {
			letterGrade1 = "B";
		}
		else if (currentGradeScore3 >= 70) {
			letterGrade1 = "C";
		}
		else if (currentGradeScore3 >= 60) {
			letterGrade1 = "D";
		}
		else if (currentGradeScore3 < 60) {
			letterGrade1 = "F";
		}

		System.out.println("Current grade score:" + currentGradeScore3);

		System.out.println("Your current letter grade:" + letterGrade1);

		if(letterGrade.equalsIgnoreCase (letterGrade1)) 
		{
			System.out.println("Congratulations! You recieved the " + letterGrade1 +" that you wanted!");
		}
		else {
			System.out.println("Unfortunately, a grade of " + letterGrade1 + " is not possible.");
		}
	}

