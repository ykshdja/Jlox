# JLox an Interpreter using Abstract Syntax Trees.

JLOX is a based Lox Programming language. Implemented using recursive descent parsing and runs on the Java Virtual Machine (JVM).Details the grammar, evaluation model, and execution workflow of JLOX.

# Introduction

# Features
**Dynamic Typing**: Variables can hold any type at runtime.

**Garbage Collection**: Managed by the JVM.

**Lexical Scoping**: Variables are scoped within blocks.

**Functions as First-Class Citizens**: Functions can be assigned to variables, passed as arguments, and returned.

## Lox Programming language

### **Lexical Analysis**

The Scanner converts source code into tokens.

var x = 10;

**Produces tokens** -

VAR IDENTIFIER( x ) EQUAL NUMBER( 10 ) SEMICOLON


### **Parsing (Abstract Syntax Tree)**

The Parser constructs an AST from tokens.

Example AST for var x = 10;:
```
VarDecl(
  name = "x",
  initializer = Literal(10)
)
```
### **Semantic Analysis**

Resolves variable scope

Validates function calls

### **Interpretation (Execution)**

The Interpreter walks the AST and executes code.
```
print x;
Would produce output:
10
```

## **Syntax**

**Variables**
```
var x = 10;
var name = "Alice";
```
**Control Flow**
```
If-Else
if (x > 5) {
    print "Greater than 5";
} else {
    print "Not greater than 5";
}
```
**Loops**
```
while (x < 20) {
    print x;
    x = x + 1;
}
```
**Functions**
```
fun greet(name) {
    print "Hello, " + name;
}
greet("Alice");
```

## Contributing
Fork this repository.
## Acknowledgement 
Book - **Crafting Interpreters** by Robert Nystrom
## License

[MIT](https://choosealicense.com/licenses/mit/)
