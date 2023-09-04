# Lexical Analysis

## Purpose

Lexical Analysis, also known as scanning or tokenization, is the fundamental first phase of the compiler process. Its primary purpose is to break down the source code into a sequence of tokens, which are the smallest meaningful units in a programming language. This process simplifies the subsequent parsing and analysis phases of compilation.

<div align="center">
<img src="https://github.com/sergiobriito/compiler-design/assets/64617586/3747b83a-cdb8-4333-9e6b-185888889ad5" alt="drawing" width="500"/>
</div>


## Key Concepts

### Tokenization

Tokenization is the process of dividing the source code into tokens. Tokens are the building blocks of a programming language and can represent keywords, identifiers, literals, symbols, and more. For example, in the code `int x = 42;`, the tokens are `int`, `x`, `=`, and `42`. Tokenization is crucial for understanding the structure and meaning of the code.

### Regular Expressions

Regular expressions play a vital role in Lexical Analysis. They are used to define patterns for identifying tokens in the source code. Regular expressions provide a powerful and flexible way to specify the structure of tokens. For instance, you can define a regular expression to match all valid variable names or numeric literals in a programming language. This allows Lexical Analysis to recognize tokens efficiently.

### Finite Automata

Finite Automata are mathematical models used to implement Lexical Analysis efficiently. There are two main types of Finite Automata used in Lexical Analysis: Nondeterministic Finite Automaton (NFA) and Deterministic Finite Automaton (DFA). Let's explore both:

#### Nondeterministic Finite Automaton (NFA)

- **Overview**: NFA is a computational model that allows multiple transitions from a single state on the same input symbol. This non-deterministic behavior gives it flexibility in recognizing patterns.

- **Use in Lexical Analysis**: NFAs are used to model regular expressions efficiently. They are capable of recognizing complex token patterns with fewer states compared to DFAs, making them valuable in lexical analysis.

#### Deterministic Finite Automaton (DFA)

- **Overview**: DFA is a computational model where each input symbol leads to a unique state transition. It operates deterministically and is known for its simplicity.

- **Use in Lexical Analysis**: DFAs are employed to optimize the recognition of tokens once NFAs define the token patterns. DFAs convert regular expressions into minimal state machines that efficiently identify tokens in the source code.

#### Efficiency

- **NFA vs. DFA**: NFAs are expressive but may require backtracking, making them potentially less efficient than DFAs. DFAs, on the other hand, excel in terms of performance due to their deterministic nature and minimal state count.

