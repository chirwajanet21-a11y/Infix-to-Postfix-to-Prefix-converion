 Infix to Postfix & Prefix Converter

​This Java project provides a robust implementation for converting mathematical Infix expressions into Postfix (Reverse Polish Notation) and Prefix (Polish Notation) using the Shunting-Yard algorithm.  
    Features
​Converts complex infix expressions (e.g., A+B*(C-D)) to Postfix and Prefix.  
​Supports operator precedence (e.g., ^ > * > +).  
​Handles parentheses for changing evaluation order.  
​Uses a stack-based approach for efficient conversion.  

​ Logic & Workflow
​1. Infix to Postfix
​The program scans the expression from left to right. It uses a Stack to hold operators and ensures they are appended to the result based on their mathematical priority.  
​2. Infix to Prefix
​The conversion follows a four-step process:  
​Reverse the infix string.
​Swap the brackets ( ( becomes ) and vice versa).
​Perform Postfix conversion on the modified string.
​Reverse the final result to get the Prefix expression.

How to Run
1.Ensure Java is installed:
java -version
2.Compile the program:
javac InfixConverter.java
3.Run the application:
java InfixConverter

Code Structure
​getPrecedence(char ch): Assigns weight to operators.  
​infixToPostfix(String exp): The core Shunting-Yard logic.  
​infixToPrefix(String exp): String manipulation logic for prefix output. 

Example Output
Infix:   A+B*(C-D)
Postfix: ABCD-*+
Prefix:  +A*B-CD


