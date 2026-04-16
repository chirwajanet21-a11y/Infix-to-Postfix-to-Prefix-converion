 # Infix to Postfix & Prefix Converter

Ever wondered how a calculator actually reads your math? 
This Java program does exactly that  it takes a normal 
math expression like `A+B*C` and converts it into formats 
that computers can easily evaluate.



## What This Program Does

It converts an **infix expression** (the way humans write math)
into two computer-friendly formats:

- **Postfix** → operators come *after* operands `A B C * +`
- **Prefix** → operators come *before* operands `+ A * B C`



## Files in This Project

 `InfixConverter.java` (The main Java program )
`PSEUDO CODES FOR THE INFIX` (Step by step logic breakdown )
 `workflowforinfixtopostfix.jpg` 
 'workflowforinfixtoprefix.jpg'(Workflow diagram )


## How It Works

### Converting to Postfix
The program reads your expression from left to right.
Every time it sees an operator like `+` or `*`, it checks
if there's a higher priority operator waiting — if yes,
that one goes first. It uses a **stack** to keep track
of everything.

### Converting to Prefix
This one's clever:
1. Flip the entire expression backwards
2. Swap every `(` with `)` and vice versa
3. Run the same Postfix conversion
4. Flip the result again that's your Prefix!

#Code Structure
​getPrecedence(char ch): Assigns weight to operators.  
​infixToPostfix(String exp): The core Shunting-Yard logic.  
​infixToPrefix(String exp): String manipulation logic for prefix output.  


## Operator Priority

 `^` | Highest (3) 
`*` `/` | Medium (2) 
 `+` `-` Lowest (1) 

So `A+B*C` means multiply first, then add — just like
normal math rules.


## How to Run It

Make sure Java is installed on your computer, then:


# Step 1 — Compile
javac InfixConverter.java

# Step 2 — Run
java InfixConverter
Example Results
Expression
Postfix
Prefix
A+B*C
A B C * +
+ A * B C
(A+B)*(C-D)
A B + C D - *
* + A B - C D
A^B^C
A B C ^ ^
^ A ^ B C
The Algorithm Behind It
This program uses the Shunting-Yard Algorithm, invented
by the famous computer scientist Edsger Dijkstra. It's the
same logic used inside real calculators and compilers.


