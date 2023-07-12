# Printf #
_printf is a custom implementation of the C programming function printf.

Prototype: int _printf(const char *, ...);

Examples
#### String ####

Input: _printf("%s\n", 'This is a string.');
Output: This is a string.
#### Character ####

Input: _printf("The first letter in the alphabet is %c\n", 'A');
Output: The first letter in the alphabet is A
#### Integer ####

Input: _printf("There are %i dozens in a gross\n", 12);
Output: There are 12 dozens in a gross
#### Decimal ####

Input: _printf("%d\n", 1000);
Output: 1000
# Project Requirements #
***All files will be compiled on Ubuntu 14.04 LTS***
Programs and functions will be compiled with gcc 4.8.4 using flags -Wall -Werror -Wextra and -pedantic
Code must follow the Betty style
Global variables are not allowed
Authorized functions and macros:
write (man 2 write)
malloc (man 3 malloc)
free (man 3 free)
va_start (man 3 va_start)
va_end (man 3 va_end)
va_copy (man 3 va_copy)
va_arg (man 3 va_arg)
## Mandatory Tasks ##
 Write function that produces output with conversion specifiers c, s, and %.
 Handle conversion specifiers d, i.
 Create a man page for your function.
## Advanced Tasks ##
 Handle conversion specifier b.
 Handle conversion specifiers u, o, x, X.
 Use a local buffer of 1024 chars in order to call write as little as possible.
 Handle conversion specifier S.
 Handle conversion specifier p.
 Handle flag characters +, space, and # for non-custom conversion specifiers.
 Handle length modifiers l and h for non-custom conversion specifiers.
 Handle the field width for non-custom conversion specifiers.
 Handle the precision for non-custom conversion specifiers.
 Handle the 0 flag character for non-custom conversion specifiers.
 Handle the custom conversion specifier r that prints the reversed string.
 Handle the custom conversion specifier R that prints the rot13'ed string.
 All above options should work well together.
# File Descriptions #
main.h: - contains all function prototypes used for _printf.
Flags (In development...)

## Flag Description ##

Left-justify the output within the field width that was given; Right justification is the default (see width sub-specifier).
Preceeds the result with a plus or minus sign (+ or -) even for positive numbers. By default, only negative numbers are preceded with a - sign.
(space) If no sign is going to be written, a blank space is inserted before the value.

Used with o, x or X specifiers the value is preceeded with 0, 0x or 0X respectively for values different than zero.
0 Left-pads the number with zeroes (0) instead of spaces when padding is specified (see width sub-specifier).

Width (In development...)

## Width Description ##

(number) Minimum number of characters to be printed. If the value to be printed is shorter than this number, the result is padded with blank spaces. The value is not truncated even if the result is larger.

The width is not specified in the format string, but as an additional integer value argument preceding the argument that has to be formatted.

## Precision Description ##

.(number) For integer specifiers (d, i, o, u, x, X): precision specifies the minimum number of digits to be written. If the value to be written is shorter than this number, the result is padded with leading zeros. The value is not truncated even if the result is longer. A precision of 0 means that no character is written for the value 0. For s: this is the maximum number of characters to be printed. By default all characters are printed until the ending null character is encountered. If the period is specified without an explicit value for precision, 0 is assumed.

Length modifiers (In development...)

Modifier/Specifier d & i u, o, x, X c s p

none int unsigned int int char pointer void pointer

h short int unsigned short int

l long int unsigned long int

Files contained in this repository

man_3_printf Man page of the _printf() function.

main.h Header file with the data type struct, standard libraries and custom prototypes

funcs.c

funcs1.c

get_flags.c

get_precision.c

get_size.c

handle_print.c

utils.c

write_handlers.c



# Authors #
Sebastian K. John | @seb-art
