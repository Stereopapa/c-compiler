# C Compiler Frontend

## Overview

This project implements the frontend of a C programming language compiler, targeting early C standards (C89/C99). It currently performs lexical and syntax analysis. Semantic analysis and code generation are not implemented in this phase. The project utilizes Flex for lexical scanning and Bison for parser generation.



## Features

* **Lexical Analysis:** Tokenizes input source code. Recognizes identifiers, numerical constants (integers, floating-point numbers), character constants, string literals, and standard C operators. It also handles single-line and multi-line comments.
* **Syntax Analysis:** Parses token streams to validate the grammatical structure of the program. Supports basic control flow structures (`if`, `while`, `do-while`), blocks, and conditional expressions.

## Prerequisites

The provided build script automatically installs the required dependencies on Debian-based systems. The core dependencies are:

* `cmake` (version 3.10 or higher)
* `build-essential` (compiler toolchain)
* `flex` and `libfl-dev`
* `bison` and `liby-dev`

## Build Instructions

An automated setup script is provided to install dependencies, generate the build system files, and compile the project.

1.  Make the setup script executable:
    ```bash
    chmod +x setup.sh
    ```
2.  Execute the build script:
    ```bash
    ./setup.sh
    ```

The compiled executable (`c_compiler`) will be generated in the `bin` directory located in the project root.

## Usage

To run the compiler, use standard stream redirection to supply the input file and save the output. 

```bash
./bin/c_compiler < in_file_path > out_file_path