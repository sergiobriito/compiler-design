# Syntax Analysis

## Purpose

Syntax Analysis, often referred to as parsing, plays a critical role in the compilation process, following Lexical Analysis. Its primary objective is to analyze the syntactical structure of the source code and construct a structured representation known as an abstract syntax tree (AST). This phase ensures that the code adheres to the syntax rules of the programming language, facilitating subsequent stages such as semantic analysis and code generation.

## Key Concepts

### Parsing

Parsing is the process of analyzing the syntactical structure of the source code, following the rules defined by the programming language's grammar. It involves breaking down the code into a sequence of language constructs, ensuring that they are correctly structured and adhere to the language's syntax rules. Common parsing techniques include top-down parsing (e.g., LL(k)) and bottom-up parsing (e.g., LR(k)), each with its own advantages and use cases.

### Context-Free Grammar (CFG)

Context-Free Grammar is a formal notation used to specify the syntax rules of a programming language. It defines the valid combinations of language elements, such as keywords, identifiers, operators, and expressions. CFG serves as the foundation for creating parsers that can validate the syntax of source code and generate the AST.

![CFG Example](https://binaryterms.com/wp-content/uploads/2021/12/Ambiguous-sentence-of-context-free-grammar-1-2.jpg)

#### Components of CFG

1. **Terminals**: These are the fundamental symbols or tokens in the language, such as keywords, identifiers, operators, and literals. Terminals are the basic building blocks used in the language's syntax.

2. **Non-terminals**: Non-terminals are variables or placeholders representing groups of symbols in the language. They serve as placeholders for constructing valid sentences or expressions. Non-terminals are often represented in uppercase, like `EXPR` or `STATEMENT`.

3. **Start Symbol**: CFG has a designated start symbol, often denoted as `S`, representing the top-level structure of the language. The goal of parsing is to derive the input source code into this start symbol.

4. **Production Rules**: Production rules define how non-terminals can be replaced by sequences of terminals and non-terminals. These rules determine the valid syntactical structures of the language.

### Ambiguity

Ambiguity in the context of parsing refers to situations where the grammar allows multiple valid interpretations for a given piece of code. Resolving ambiguity is a crucial aspect of syntax analysis, ensuring that the parser can consistently and accurately determine the code's intended meaning. Techniques like precedence and associativity rules are often used to resolve ambiguity.

### Error Handling

Syntax analysis includes robust error handling mechanisms. When the parser encounters syntax errors in the source code, it must provide informative error messages to aid developers in identifying and fixing issues. Error recovery strategies, such as panic mode recovery and error reporting, are essential for making the compiler user-friendly.

### Abstract Syntax Tree (AST)

The Abstract Syntax Tree is a hierarchical representation of the syntactic structure of the source code. It captures the relationships between different language constructs, including statements, expressions, and declarations. Each node in the tree corresponds to a specific language element, and the tree's structure mirrors the code's nested structure. The AST serves as a crucial data structure for subsequent compilation phases, including semantic analysis and code generation.

### Example AST Node Types

Here are some common types of nodes found in an AST:

- **Program Node**: Represents the entire program.
- **Function Declaration Node**: Captures information about functions and their parameters.
- **Statement Nodes**: Represent different types of statements, such as assignments, conditionals, loops, etc.
- **Expression Nodes**: Capture expressions, including binary operations, function calls, and literals.
- **Identifier Nodes**: Store information about variables and identifiers.

For example, the AST of this code sample:

```plaintext
while b ≠ 0
    if a > b
        a := a − b
    else
        b := b − a
    return a
```

Would look like this:

![Example AST](https://miro.medium.com/v2/resize:fit:828/format:webp/0*oq2dv-R02zuVRHAj.png)

[Main Page](../README.md)