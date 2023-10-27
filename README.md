## ft_printf
ft_printf is reproduced C's printf function. Just like real printf, it allows the following functionality:

```
%[flags][width][.precision][length]type 
```

Result is a formated string. Each of these parts is explained below.
To produce ft_printf() function, only UNIX write, malloc, free, exit, stdarg functions have been used. Rest of the functionality is custom built.

# Getting Started

Run **make**, which results in library called libftprintf.a. In your source file, use ft_printf() function just as you would use printf(). Furthermore, compile your source code with libftprintf.a to use ft_printf() function. So libftprint.a includes the ft_printf() function.

```
gcc main.c libftprintf.a
```

# Type

A partial reimplementation of the printf in C. Handles only the following conversions.

| Conversion | Short Description                                                                             |
|------------|-----------------------------------------------------------------------------------------------|
| %c         | Print a single character.                                                                     |
| %s         | Print a string of characters.                                                                 |
| %p         | The void * pointer argument is printed in hexadecimal.                                        |
| %d         | Print a decimal (base 10) number.                                                             |
| %i         | Print an integer in base 10.                                                                  |
| %u         | Print an unsigned decimal (base 10) number.                                                   |
| %x         | Print a number in hexadecimal (base 16), with lowercase.                                      |
| %X         | Print a number in hexadecimal (base 16), with uppercase.                                      |
| %%         | Print a percent sign.                                                                         |

# Return value

Function returns bytes written to standard output. Thus, if multibyte character is printed, ft_printf() would return the amount of bytes it consists of not how many characters were printed.
