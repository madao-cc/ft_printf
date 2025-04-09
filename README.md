# ft_printf

> **Objective:** Recreate the C standard library's `printf` function, gaining a deeper understanding of variadic functions, formatted output, and low-level data manipulation.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Supported Format Specifiers](#supported-format-specifiers)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Implementation Details](#implementation-details)
- [Learning Outcomes](#learning-outcomes)
- [Acknowledgments](#acknowledgments)

## Project Overview

The **ft_printf** project involves implementing a custom version of the standard `printf` function in C. This project enhances your understanding of handling variable arguments, parsing format specifiers, and producing formatted output. citeturn0search4

## Key Features

- **Variadic Function Handling:** Manage functions that accept a variable number of arguments using `stdarg.h`.
- **Format Specifier Parsing:** Interpret and process various format specifiers to format output accordingly.
- **Formatted Output Production:** Generate output based on specified formats, ensuring alignment with standard `printf` behavior.

## Supported Format Specifiers

Your `ft_printf` implementation handles the following specifiers:

- `%c`: Prints a single character.
- `%s`: Prints a string of characters.
- `%p`: Prints a pointer address in hexadecimal format.
- `%d`/`%i`: Prints a signed decimal integer.
- `%u`: Prints an unsigned decimal integer.
- `%x`: Prints a number in hexadecimal (lowercase) format.
- `%X`: Prints a number in hexadecimal (uppercase) format.
- `%%`: Prints a percent sign.

## Project Structure

The repository is organized as follows:

- `ft_printf.c`: Contains the main `ft_printf` function, handling the parsing of the format string and delegation to appropriate handlers.
- `ft_printf.h`: Header file with function prototypes and necessary includes.
- `ft_printchar.c`, `ft_printstr.c`, `ft_printnbr.c`, etc.: Individual files handling specific format specifiers.
- `Makefile`: Automates the compilation process, generating the `libftprintf.a` library.

## Installation

To incorporate `ft_printf` into your project:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/madao-cc/ft_printf.git
   ```


2. **Navigate to the Project Directory:**
   ```bash
   cd ft_printf
   ```


3. **Compile the Project:**
   ```bash
   make
   ```

   This generates the `libftprintf.a` library.

## Usage

To use `ft_printf` in your project:

1. **Include the Header:**
   ```c
   #include "ft_printf.h"
   ```


2. **Link the Library During Compilation:**
   ```bash
   gcc your_program.c -L. -lftprintf -o your_program
   ```


3. **Call `ft_printf` as You Would with Standard `printf`:**
   ```c
   ft_printf("Hello, %s! You have %d new messages.\n", username, message_count);
   ```


## Implementation Details

- **Variadic Functions:** Utilizes `stdarg.h` to handle functions with a variable number of arguments.
- **Format String Parsing:** Iterates through the format string, identifying and processing valid specifiers.
- **Output Functions:** Each specifier has a dedicated function to handle its specific output requirements.
- **Error Handling:** Ensures that invalid specifiers are handled gracefully, maintaining program stability.

## Learning Outcomes

Through this project, you will:

- **Deepen Understanding of Variadic Functions:** Gain practical experience with functions that accept a variable number of arguments.
- **Enhance String Parsing Skills:** Develop techniques for parsing and interpreting complex format strings.
- **Improve Low-Level Data Manipulation:** Learn to manage different data types and memory representations effectively.
- **Strengthen Debugging Abilities:** Refine skills in testing and debugging functions that interact closely with system-level features.

## Acknowledgments

This project is part of the curriculum at 42 School, designed to deepen understanding of standard library functions and their underlying implementations.
