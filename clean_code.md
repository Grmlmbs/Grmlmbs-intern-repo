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







**Complex and long function:**



public class OrderProcessor {



&#x20;   public static void processOrder(String customerName, String email, String\[] items, double\[] prices, boolean isMember) {



&#x20;       System.out.println("Starting order processing...");



&#x20;       // 1. Validate inputs

&#x20;       if (customerName == null || customerName.equals("")) {

&#x20;           System.out.println("Invalid customer name");

&#x20;           return;

&#x20;       }



&#x20;       if (email == null || !email.contains("@")) {

&#x20;           System.out.println("Invalid email");

&#x20;           return;

&#x20;       }



&#x20;       if (items == null || prices == null || items.length == 0 || prices.length == 0) {

&#x20;           System.out.println("No items in order");

&#x20;           return;

&#x20;       }



&#x20;       if (items.length != prices.length) {

&#x20;           System.out.println("Items and prices mismatch");

&#x20;           return;

&#x20;       }



&#x20;       // 2. Calculate total

&#x20;       double total = 0;

&#x20;       for (int i = 0; i < prices.length; i++) {

&#x20;           if (prices\[i] < 0) {

&#x20;               System.out.println("Invalid price detected at item: " + items\[i]);

&#x20;               return;

&#x20;           }

&#x20;           total += prices\[i];

&#x20;       }



&#x20;       // 3. Apply discount

&#x20;       double discount = 0;

&#x20;       if (isMember) {

&#x20;           discount = total \* 0.10;

&#x20;       } else if (total > 1000) {

&#x20;           discount = total \* 0.05;

&#x20;       }



&#x20;       double finalTotal = total - discount;



&#x20;       // 4. Tax calculation

&#x20;       double tax = finalTotal \* 0.12;

&#x20;       finalTotal += tax;



&#x20;       // 5. Generate receipt

&#x20;       System.out.println("\\n===== RECEIPT =====");

&#x20;       System.out.println("Customer: " + customerName);

&#x20;       System.out.println("Email: " + email);



&#x20;       System.out.println("\\nItems:");

&#x20;       for (int i = 0; i < items.length; i++) {

&#x20;           System.out.println("- " + items\[i] + " : $" + prices\[i]);

&#x20;       }



&#x20;       System.out.println("\\nSubtotal: $" + total);

&#x20;       System.out.println("Discount: $" + discount);

&#x20;       System.out.println("Tax: $" + tax);

&#x20;       System.out.println("Total: $" + finalTotal);



&#x20;       // 6. Simulate saving to database

&#x20;       System.out.println("\\nSaving order to database...");

&#x20;       try {

&#x20;           Thread.sleep(500); // fake delay

&#x20;       } catch (InterruptedException e) {

&#x20;           System.out.println("Database error");

&#x20;       }



&#x20;       // 7. Send email confirmation

&#x20;       System.out.println("Sending confirmation email to " + email);



&#x20;       if (finalTotal > 5000) {

&#x20;           System.out.println("Flagging order for manual review (high value order)");

&#x20;       }



&#x20;       System.out.println("Order processing completed.");

&#x20;   }

}



**Cleaned code:** 



public class OrderProcessor {



&#x20;   public static void processOrder(String customerName, String email, String\[] items, double\[] prices, boolean isMember) {



&#x20;       if (!validateOrder(customerName, email, items, prices)) {

&#x20;           return;

&#x20;       }



&#x20;       double total = calculateTotal(items, prices);

&#x20;       double discount = calculateDiscount(total, isMember);

&#x20;       double finalTotal = applyTax(total - discount);

&#x20;       

&#x20;       printReceipt(customerName, email, items, prices, total, discount, finalTotal);

&#x20;       saveOrder(customerName, email, finalTotal);

&#x20;       sendEmail(email, finalTotal);



&#x20;       if (finalTotal > 5000) {

&#x20;           flagHighValueOrder();

&#x20;       }



&#x20;       System.out.println("Order processing completed.");

&#x20;   }



&#x20;   // 1. Validation

&#x20;   private static boolean validateOrder(String customerName, String email, String\[] items, double\[] prices) {



&#x20;       if (customerName == null || customerName.isEmpty()) {

&#x20;           System.out.println("Invalid customer name");

&#x20;           return false;

&#x20;       }



&#x20;       if (email == null || !email.contains("@")) {

&#x20;           System.out.println("Invalid email");

&#x20;           return false;

&#x20;       }



&#x20;       if (items == null || prices == null || items.length == 0 || prices.length == 0) {

&#x20;           System.out.println("No items in order");

&#x20;           return false;

&#x20;       }



&#x20;       if (items.length != prices.length) {

&#x20;           System.out.println("Items and prices mismatch");

&#x20;           return false;

&#x20;       }



&#x20;       return true;

&#x20;   }



&#x20;   // 2. Calculate total

&#x20;   private static double calculateTotal(String\[] items, double\[] prices) {

&#x20;       double total = 0;



&#x20;       for (int i = 0; i < prices.length; i++) {

&#x20;           if (prices\[i] < 0) {

&#x20;               System.out.println("Invalid price for item: " + items\[i]);

&#x20;               return 0;

&#x20;           }

&#x20;           total += prices\[i];

&#x20;       }



&#x20;       return total;

&#x20;   }



&#x20;   // 3. Discount logic

&#x20;   private static double calculateDiscount(double total, boolean isMember) {

&#x20;       if (isMember) {

&#x20;           return total \* 0.10;

&#x20;       } else if (total > 1000) {

&#x20;           return total \* 0.05;

&#x20;       }

&#x20;       return 0;

&#x20;   }



&#x20;   // 4. Tax calculation

&#x20;   private static double applyTax(double amount) {

&#x20;       double tax = amount \* 0.12;

&#x20;       return amount + tax;

&#x20;   }



&#x20;   // 5. Print receipt

&#x20;   private static void printReceipt(String customerName, String email, String\[] items, double\[] prices,

&#x20;                                    double total, double discount, double finalTotal) {



&#x20;       System.out.println("\\n===== RECEIPT =====");

&#x20;       System.out.println("Customer: " + customerName);

&#x20;       System.out.println("Email: " + email);



&#x20;       System.out.println("\\nItems:");

&#x20;       for (int i = 0; i < items.length; i++) {

&#x20;           System.out.println("- " + items\[i] + " : $" + prices\[i]);

&#x20;       }



&#x20;       System.out.println("\\nSubtotal: $" + total);

&#x20;       System.out.println("Discount: $" + discount);

&#x20;       System.out.println("Total: $" + finalTotal);

&#x20;   }



&#x20;   // 6. Save order (simulation)

&#x20;   private static void saveOrder(String customerName, String email, double finalTotal) {

&#x20;       System.out.println("\\nSaving order to database...");

&#x20;       try {

&#x20;           Thread.sleep(500);

&#x20;       } catch (InterruptedException e) {

&#x20;           System.out.println("Database error");

&#x20;       }

&#x20;   }



&#x20;   // 7. Send email (simulation)

&#x20;   private static void sendEmail(String email, double finalTotal) {

&#x20;       System.out.println("Sending confirmation email to " + email);

&#x20;   }



&#x20;   // 8. High value flag

&#x20;   private static void flagHighValueOrder() {

&#x20;       System.out.println("Flagging order for manual review (high value order)");

&#x20;   }

}

**Why is breaking down function beneficial?** 



&#x09;breaking down functions makes the function modular, easier to read, and easier to debug.



**How did refactoring improve the structure of the code?**



&#x09;Refactoring makes a code block or function look cleaner. It lets other developers spend less time understanding what you wrote and gives them more time thinking solutions.



**What were the issues with duplicated code?**



&#x09;Duplicated makes your code take up unnecessary storage space and it make the code run slower unnecessarily as it have to read those inputs still before processing. 



**How did refactoring improve maintainability?**



&#x09;Refactoring makes code much more readable and simpler. It also makes it so that we only need to change a specific section rather than the whole codebase. 










