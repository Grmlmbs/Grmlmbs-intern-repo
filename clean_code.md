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







**Poor comment:** 



int total = price + tax; // add price and tax



**Good comment:** 



int total = price + tax; // includes VAT for local compliance





**When should you add comments?**



&#x09;You should write comments in lines of codes that might cause confusion or if it can't explain for itself. You also use comments for possible future improvements limits or explaining what a big code block do and why it was there. 



**When should you avoid comments and instead improve code?**



&#x09;If it is pretty much self explanatory you don't have to put comment for it, just name your variables properly and improve the overall readability of the code block.





**Code with poor error handling:**



public class Calculator {



&#x20;   public static int divide(int a, int b) {

&#x20;       return a / b;

&#x20;   }



&#x20;   public static void main(String\[] args) {

&#x20;       int result = divide(10, 0);

&#x20;       System.out.println("Result: " + result);

&#x20;   }

}




**Code with good error handling:**



public class Calculator {



&#x20;   public static Integer divide(int a, int b) {



&#x20;       // Guard clause: handle invalid input early

&#x20;       if (b == 0) {

&#x20;           System.out.println("Error: Cannot divide by zero.");

&#x20;           return null; // or you could return 0 depending on your design

&#x20;       }



&#x20;       return a / b;

&#x20;   }



&#x20;   public static void main(String\[] args) {



&#x20;       Integer result = divide(10, 0);



&#x20;       if (result != null) {

&#x20;           System.out.println("Result: " + result);

&#x20;       } else {

&#x20;           System.out.println("Calculation failed.");

&#x20;       }

&#x20;   }

}



**What was the issue with the original code?**



&#x09;it didn't check if the input is a valid one and if you didn't do the necessary validation of inputs the program might fail and will render the code unusable.



**How does handling errors improve reliability?**



&#x09;Handling errors can improve reliability as proper error handling will make your function run properly and run without the threat of failing. handling errors also makes it more robust and ensure that if an error occurs, the code can recover on its own with minimal and predictable interventions.





**Overly complicated code:**



public class OrderSystem {



&#x20;   public static void process(String name, String email, String\[] items, double\[] prices, boolean member) {



&#x20;       if (name != null) {

&#x20;           if (email.contains("@")) {

&#x20;               if (items.length > 0) {



&#x20;                   double total = 0;



&#x20;                   for (int i = 0; i < prices.length; i++) {

&#x20;                       if (prices\[i] > 0) {

&#x20;                           total = total + prices\[i];

&#x20;                       } else {

&#x20;                           System.out.println("Invalid price detected");

&#x20;                       }

&#x20;                   }



&#x20;                   double discount = 0;



&#x20;                   if (member == true) {

&#x20;                       discount = total \* 0.1;

&#x20;                   } else {

&#x20;                       if (total > 1000) {

&#x20;                           discount = total \* 0.05;

&#x20;                       }

&#x20;                   }



&#x20;                   double finalTotal = total - discount;



&#x20;                   double tax = finalTotal \* 0.12;

&#x20;                   finalTotal = finalTotal + tax;



&#x20;                   System.out.println("Customer: " + name);

&#x20;                   System.out.println("Email: " + email);



&#x20;                   for (int i = 0; i < items.length; i++) {

&#x20;                       System.out.println(items\[i] + " - " + prices\[i]);

&#x20;                   }



&#x20;                   System.out.println("Total: " + finalTotal);



&#x20;               }

&#x20;           }

&#x20;       }

&#x20;   }

}



**Clean and refactored:**



public class OrderSystem {



&#x20;   public static void process(String name, String email, String\[] items, double\[] prices, boolean member) {



&#x20;       if (!validateInput(name, email, items, prices)) return;



&#x20;       double total = calculateTotal(prices);

&#x20;       double discount = calculateDiscount(total, member);

&#x20;       double finalTotal = applyTax(total - discount);



&#x20;       printReceipt(name, email, items, prices, total, discount, finalTotal);

&#x20;   }



&#x20;   // 1. Validation (Guard Clauses)

&#x20;   private static boolean validateInput(String name, String email, String\[] items, double\[] prices) {



&#x20;       if (name == null || name.isEmpty()) return false;



&#x20;       if (email == null || !email.contains("@")) return false;



&#x20;       if (items == null || items.length == 0) return false;



&#x20;       if (prices == null || prices.length == 0) return false;



&#x20;       return true;

&#x20;   }



&#x20;   // 2. Calculate total

&#x20;   private static double calculateTotal(double\[] prices) {

&#x20;       double total = 0;



&#x20;       for (double price : prices) {

&#x20;           if (price > 0) {

&#x20;               total += price;

&#x20;           }

&#x20;       }



&#x20;       return total;

&#x20;   }



&#x20;   // 3. Discount logic

&#x20;   private static double calculateDiscount(double total, boolean member) {

&#x20;       if (member) return total \* 0.10;

&#x20;       if (total > 1000) return total \* 0.05;

&#x20;       return 0;

&#x20;   }



&#x20;   // 4. Tax calculation

&#x20;   private static double applyTax(double amount) {

&#x20;       return amount \* 1.12;

&#x20;   }



&#x20;   // 5. Output

&#x20;   private static void printReceipt(String name, String email, String\[] items, double\[] prices,

&#x20;                                    double total, double discount, double finalTotal) {



&#x20;       System.out.println("\\n--- RECEIPT ---");

&#x20;       System.out.println("Customer: " + name);

&#x20;       System.out.println("Email: " + email);



&#x20;       for (int i = 0; i < items.length; i++) {

&#x20;           System.out.println(items\[i] + " - " + prices\[i]);

&#x20;       }



&#x20;       System.out.println("Subtotal: " + total);

&#x20;       System.out.println("Discount: " + discount);

&#x20;       System.out.println("Total: " + finalTotal);

&#x20;   }

}



**What made the original code complex?**



&#x09;The original code is structured as one singular function. The whole function does everything and there were no separation of responsibilities.



**How did refactoring improve it?**



&#x09;Refactoring it made the code cleaner, modular, and much easier to maintain as you only have to make changes in specific parts to fix issues if there was any. Unlike in the original where it is one single function and is reliant to the whole structure for it to work.



