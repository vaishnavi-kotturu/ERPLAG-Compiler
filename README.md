# ERPLAG-Compiler

Implemented a compiler for ERPLAG in C as a term project for CS F363 Compiler Construction.

# modules
1. Lexer (lexer.c)
2. Parser (parser.c)
3. AST Construction (ast.c) 
4. Symbol Table and Type Extraction (symbol.c) 
5. Type Checking and Semantic Analyser (semanticAnalyzer.c)
6. Code Generation (codeGen.c)

# compatibility
gcc version 5.0 or above<br/>
NASM 2.14.02 (64-bit compatible)

# execution
1. Use `make` to compile the compiler code.<br/>
2. The command line argument for execution of the driver is as follows:<br/>
`./compile testcase.txt code.asm`
<br/>
3. Select options out of 0-9 to run different modules.<br/>
<br/>
4. Producing the binary from .asm file :<br/><br/>
-Ubuntu 16.04<br/>
```
nasm -f elf64 -o output.o code.asm
gcc output.o
./a.out
```
<br/>
-Ubuntu 18.04 and higher versions<br/>
```
nasm -f elf64 -o output.o code.asm
gcc output.o -no-pie
./a.out
```
