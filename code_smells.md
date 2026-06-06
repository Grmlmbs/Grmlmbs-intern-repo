code\_smells



**original code:**



public class Main {



&#x09;//public static void main(String\[] args) {

&#x09;	//int a=10, b=5;

&#x09;	//int r=a+b;

&#x09;	//System.out.println("sum is "+r);

&#x09;//}

//}

&#x09;public static int add(int num1, int num2) {

&#x09;	return num1 + num2;

&#x09;}



&#x09;public static void main(String\[] args) {

&#x09;

&#x09;	int sum = add(10, 5);

&#x09;	System.out.println("Sum is " + sum);

&#x09;}

}



**cleaned code:**



public class Main {



&#x09;public static int add(int num1, int num2) {

&#x09;	return num1 + num2;

&#x09;}



&#x09;public static void main(String\[] args) {

&#x09;

&#x09;	int sum = add(10, 5);

&#x09;	System.out.println("Sum is " + sum);

&#x09;}

}



**What code smells did you find in your code?**



&#x09;I found some commented-out code, inconsistent Naming and a long function.



**How did refactoring improve the readability and maintainability of the code?**



&#x09;Refactoring made the code more readable and organized. It also removed unnecessary parts specifically the commented-out code block.



**How can avoiding code smells make future debugging easier?**



&#x09;Avoiding code smells make future debugging easier by making the code simpler. It removes unnecessary details and makes the overall code readable for other developers to handle.

