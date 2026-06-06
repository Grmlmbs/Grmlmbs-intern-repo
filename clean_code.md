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

