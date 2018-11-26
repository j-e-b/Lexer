# Overview
Implementation of a lexical analyzer for the programming language PL/0. Capable of doing lexical analysis on a given source program written in PL/0, identifying errors, and giving the source program's lexeme table (LexerOut).

# Components

* [Makefile](Makefile): The makefile that helps to build, test and clean.

* [main.c](main.c): The C file that contains the main function, the code required to interpret command line arguments, and the  call to `lexicalAnalyzer()` function which you should implement.

* [data.h](data.h): Defines the enumaration and the string representations of the tokens, and constants.

* [lexical_analyzer.h](lexical_analyzer.h): Includes:
  * The declaration of the `lexicalAnalyzer()` function.
  * The definition of LexerOut struct, which is the return type of the `lexicalAnalyzer()` function.
  * The `LexErr` enumeration, which includes the types of possible lexer errors.

* [lexical_analyzer.c](lexical_analyzer.c): Declarations and definitions of the needed functions to run the lexicalAnalyzer() function,
including the function itself.

* [lexical_analyzer_deleteLexerOut.c](lexical_analyzer_deleteLexerOut.c): The implementation of `deleteLexerOut()` function.

* [source_code.h](source_code.h): The header file that contains the declarations for the source code manipulation functions.

* [source_code.c](source_code.c): The C file that implements the functions declared in [source_code.h](source_code.h).

* [token.h](token.h): The header file that contains the definitions of the structs Token, TokenList, and the declarations of the functions that manipulates those structs.

* [token.c](token.c): The C file that implements the functions declared in [token.h](token.h).

# Command Line Arguments
Usage: `./la.out (pl0_source_code_file) (tokenlist_output_file)`

* pl0_source_code_file: The path to the file containing the source code for the programming language PL/0.

* tokenlist_output_file: The path to the file to write the lexical analyzer output, which contains the lexeme table.

# Build & Run
The build is done with the help of the Makefile included in the repository. Following command is enough to build solution and obtain the executable file `la.out`:
```
$ make
```
Then, to run program, use the following command by feeding necessary command line arguments:

```
$ ./la.out (pl0_source_code_file) (tokenlist_output_file)
```
