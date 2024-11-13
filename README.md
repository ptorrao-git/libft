# LIBFT

LIBFT is a custom implementation of a standard C library. The project involves recreating a set of commonly used functions that are part of the C standard library, as well as creating some new functions from scratch. The purpose of this project is to familiarize students with low-level programming and memory management.

## Table of Contents

- [Introduction](#introduction)
- [Project Requirements](#project-requirements)
- [Implemented Functions](#implemented-functions)
  - [Memory Functions](#memory-functions)
  - [String Functions](#string-functions)
  - [Character Functions](#character-functions)
  - [Conversion Functions](#conversion-functions)
  - [Additional Functions](#additional-functions)
- [Compiling the Library](#compiling-the-library)
- [Usage Example](#usage-example)
  
---

## Introduction

LIBFT is a personal implementation of the standard C library functions and additional utilities. It includes memory management functions, string manipulation tools, and various other utilities that can be used in other projects at the 42 school. The goal is to practice writing clean, efficient C code, and to gain a deeper understanding of how standard library functions are implemented.

---

## Project Requirements

The project consists of several basic tasks that each involve the creation of a C function to replicate an existing standard library function. The functions need to be written from scratch without using any of the standard library functions themselves (except for `write`, `malloc`, and `free`).

Here are the main components of the project:

- **Memory management functions**
- **String manipulation functions**
- **Character handling functions**
- **Conversion functions**
- **Other utility functions**

---

## Implemented Functions

LIBFT contains the following functions, which are grouped by their category:

### Memory Functions

- `ft_memset()`: Fills the first `n` bytes of the memory area with the constant byte `c`.
- `ft_bzero()`: Sets the first `n` bytes of the memory area to zero.
- `ft_memcpy()`: Copies `n` bytes from source to destination.
- `ft_memccpy()`: Copies `n` bytes from source to destination, stopping when `c` is found.
- `ft_memmove()`: Moves `n` bytes from source to destination, handles overlapping memory regions.
- `ft_memchr()`: Searches for the first occurrence of `c` in `n` bytes.
- `ft_memcmp()`: Compares `n` bytes between two memory areas.
- `ft_calloc()`: Allocates memory for an array of `nmemb` elements, each of size `size`, and initializes all bytes to zero.

### String Functions

- `ft_strlen()`: Returns the length of a string.
- `ft_strdup()`: Returns a pointer to a newly allocated string, which is a duplicate of the input string.
- `ft_strcpy()`: Copies a string from source to destination.
- `ft_strncpy()`: Copies up to `n` characters from the source to the destination string.
- `ft_strcat()`: Concatenates two strings.
- `ft_strncat()`: Concatenates up to `n` characters from the source string.
- `ft_strlcpy()`: Safely copies a string and ensures null-termination.
- `ft_strlcat()`: Safely concatenates two strings with size limit.
- `ft_strchr()`: Searches for the first occurrence of a character in a string.
- `ft_strrchr()`: Searches for the last occurrence of a character in a string.
- `ft_strstr()`: Locates the first occurrence of a substring in a string.
- `ft_strnstr()`: Locates the first occurrence of a substring in a string up to `len` characters.
- `ft_strcmp()`: Compares two strings.
- `ft_strncmp()`: Compares two strings up to `n` characters.
- `ft_atoi()`: Converts a string to an integer.
- `ft_itoa()`: Converts an integer to a string.

### Character Functions

- `ft_isalpha()`: Checks if a character is an alphabetic letter.
- `ft_isdigit()`: Checks if a character is a digit.
- `ft_isalnum()`: Checks if a character is alphanumeric.
- `ft_isascii()`: Checks if a character is an ASCII character.
- `ft_isprint()`: Checks if a character is printable.
- `ft_toupper()`: Converts a character to uppercase.
- `ft_tolower()`: Converts a character to lowercase.

### Conversion Functions

- `ft_atoi()`: Converts a string to an integer.
- `ft_itoa()`: Converts an integer to a string.

### Additional Functions

- `ft_putchar_fd()`: Writes a character to a file descriptor.
- `ft_putstr_fd()`: Writes a string to a file descriptor.
- `ft_putendl_fd()`: Writes a string followed by a newline to a file descriptor.
- `ft_putnbr_fd()`: Writes an integer to a file descriptor.

---

## Compiling the Library

To compile the library, simply run the following commands in your terminal:

1. Clone the repository:

   ```bash
   git clone git@github.com:ptorrao-git/libft.git

2. Navigate to the project directory:

   ```bash
   cd libft

3. Compile the library using `make`:

   ```bash
   make

This will generate a static library file `libft.a`.

3. (Optional) To clean up the object files after compiling:

   ```bash
   make clean

3. (Optional) To remove all compiled files and the library:

   ```bash
    make fclean

3. To recompile the library after cleaning:

   ```bash
   make re

---

## Usage Example

Once you've compiled the library, you can link it to your other projects. For example, to use LIBFT in another C program:

1. Make sure libft.a is in the same directory as your project.

2. Compile your project with LIBFT linked:

   ```bash
   cc -o libft.a my_program.c -L. -lft

3. You can then use the functions from LIBFT in your code. For example:

   ```my_program.c
   #include "libft.h"
   #include <stdio.h>

   int main() {
     char *str = "Hello, world!";
     printf("Length of string: %zu\n", ft_strlen(str));
     return 0;
   }
