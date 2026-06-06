clean\_code



**Messy code:**



public class Main {



&#x09;public static void main(String\[] args) {

&#x09;	int a=10, b=5;

&#x09;	int r=a+b;

&#x09;	System.out.println("sum is "+r);

&#x09;}

}





**Clean code:**



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



**What makes a good variable or function name?** 



&#x09;A good function and variable name are concise and descriptive of what that variable and class is for and what does it do in the entire codebase.



**What issues can arise from poorly named variables?** 



&#x09;Poorly named variables can cause confusion and ambiguity. Instead of helping other developers understand your code, it might make it hard for them to figure out and understand what you've done.



**How did refactoring improve code readability?**



&#x09;Refactoring can make the code simpler and a lot more manageable. it can also optimize the certain code blocks to help it run smoother and prevent unnecessary confusions.

