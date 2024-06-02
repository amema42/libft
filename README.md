# libft

## Overview

`libft` (a 42 School Project) is a custom implementation of standard C library functions and additional utility functions often used in C programming. It serves as a foundation for developing more complex projects (for example: 42's common core projects) and helps in understanding how basic C functions work internally.

## Purpose

The primary goal of `libft` is to provide a comprehensive set of reusable functions that mimic the standard C library, as well as additional functions for common tasks. This library is typically used in educational settings, such as the 42 school, to teach students about low-level programming, memory management, and algorithm implementation.

## Features

The `libft` library includes a variety of functions categorized into the following groups:

1. **Memory Management Functions**
2. **String Manipulation Functions**
3. **Character Check Functions**
4. **List Manipulation Functions**
5. **Output Functions**
6. **Conversion Functions**

## Usage Instructions

To use `libft` in your project, follow these steps:

1. **Clone the Repository**: Clone or download the `libft` repository.
2. **Compile the Library**: Navigate to the `libft` directory and run `make` to compile the library.
3. **Include the Header**: Include `libft.h` in your project files.
4. **Link the Library**: Link the compiled library `libft.a` with your project during compilation.

Example:
```sh
git clone https://github.com/amema42/libft.git
cd libft
make
gcc -o your_program your_program.c -L. -lft
```

## Functions and Implementation

Below is an overview of the key functions in `libft`, along with insights into their logic and guidance on how to implement them.

### Memory Management Functions

- **ft_memset**: Fills a block of memory with a specified value.
- **ft_bzero**: Sets a block of memory to zero.
- **ft_memcpy**: Copies a block of memory from one location to another.
- **ft_memmove**: Copies a block of memory from one location to another, handling overlapping areas correctly.
- **ft_memchr**: Locates a byte in a block of memory.
- **ft_memcmp**: Compares two blocks of memory.
- **ft_calloc**: Allocates memory for an array, initializes it to zero.

### String Manipulation Functions

- **ft_strlen**: Returns the length of a string.
- **ft_strdup**: Duplicates a string.
- **ft_strcpy**: Copies a string to another location.
- **ft_strncpy**: Copies up to a specified number of characters of a string to another location.
- **ft_strcat**: Concatenates two strings.
- **ft_strncat**: Concatenates up to a specified number of characters from one string to another.
- **ft_strlcpy**: Copies a string to another location, ensuring null-termination.
- **ft_strlcat**: Concatenates two strings, ensuring null-termination.
- **ft_strchr**: Locates a character in a string.
- **ft_strrchr**: Locates the last occurrence of a character in a string.
- **ft_strstr**: Locates a substring in a string.
- **ft_strnstr**: Locates a substring in a string, up to a specified number of characters.
- **ft_strcmp**: Compares two strings.
- **ft_strncmp**: Compares up to a specified number of characters of two strings.
- **ft_strjoin**: Concatenates two strings into a new string.
- **ft_strtrim**: Trims leading and trailing whitespace from a string.
- **ft_split**: Splits a string into an array of substrings based on a delimiter.
- **ft_substr**: Extracts a substring from a string.
- **ft_strmapi**: Applies a function to each character of a string to create a new string.
- **ft_striteri**: Applies a function to each character of a string, modifying the string in place.

### Character Check Functions

- **ft_isalpha**: Checks if a character is an alphabetic letter.
- **ft_isdigit**: Checks if a character is a digit.
- **ft_isalnum**: Checks if a character is alphanumeric.
- **ft_isascii**: Checks if a character is an ASCII character.
- **ft_isprint**: Checks if a character is printable.
- **ft_toupper**: Converts a character to uppercase.
- **ft_tolower**: Converts a character to lowercase.

### List Manipulation Functions

- **ft_lstnew**: Creates a new list element.
- **ft_lstadd_front**: Adds an element to the front of a list.
- **ft_lstadd_back**: Adds an element to the back of a list.
- **ft_lstsize**: Returns the number of elements in a list.
- **ft_lstlast**: Returns the last element of a list.
- **ft_lstdelone**: Deletes a list element.
- **ft_lstclear**: Deletes all elements of a list.
- **ft_lstiter**: Iterates over a list, applying a function to each element.
- **ft_lstmap**: Iterates over a list, applying a function to each element to create a new list.

### Output Functions

- **ft_putchar_fd**: Outputs a character to a file descriptor.
- **ft_putstr_fd**: Outputs a string to a file descriptor.
- **ft_putendl_fd**: Outputs a string followed by a newline to a file descriptor.
- **ft_putnbr_fd**: Outputs an integer to a file descriptor.

### Conversion Functions

- **ft_atoi**: Converts a string to an integer.
- **ft_itoa**: Converts an integer to a string.

## Detailed Implementation Guidance

To implement these functions independently, consider the following steps:

1. **Understand the Function Requirements**: Clearly define what each function is supposed to do. Refer to the standard C library documentation for detailed descriptions and edge cases.
2. **man**: Often, your only tool to describe the behavior of a function is the `man` - try to use it and to understand how it's written.
  - example : `man strlen`
  ```bash
  bash-3.2$ man strlen
  STRLEN(3)                               Library Functions Manual                               STRLEN(3)

  NAME
       strlen, strnlen – find length of string

  LIBRARY
       Standard C Library (libc, -lc)

  SYNOPSIS
       #include <string.h>

       size_t
       strlen(const char *s);

       size_t
       strnlen(const char *s, size_t maxlen);

  DESCRIPTION
       The strlen() function computes the length of the string s.  The strnlen() function attempts to
       compute the length of s, but never scans beyond the first maxlen bytes of s.

  RETURN VALUES
       The strlen() function returns the number of characters that precede the terminating NUL character.
       The strnlen() function returns either the same result as strlen() or maxlen, whichever is smaller.

  SEE ALSO
       string(3), wcslen(3), wcswidth(3)

  STANDARDS
       The strlen() function conforms to ISO/IEC 9899:1990 (“ISO C90”).  The strnlen() function conforms
       to IEEE Std 1003.1-2008 (“POSIX.1”).

  macOS 13.6                                  February 28, 2009                                 macOS 13.6
  ```
3. **Plan the Logic**: Outline the steps required to achieve the function's goal. Consider edge cases and input validation.
4. **Write the Code**: Implement the function in C, making sure to handle memory management and edge cases correctly.
5. **Test Thoroughly**: Write test cases to ensure your function works as expected in all scenarios. Use both typical and edge case inputs.
6. **Optimize and Refactor**: Review your code for efficiency and readability. Refactor if necessary to improve performance and maintainability.

Example: `ft_strlen`

Purpose: Calculate the length of a string.

```c
size_t i; // declare a variable i of type size_t

i = 0; // initialize i to 0

while (s[i]) // loop until the null character is reached
    i++; // increment i for each character in the string

return (i); // return the final value of i, which is the length of the string
```

## Conclusion

The `libft` library is a fundamental tool for understanding C programming at a deeper level, as a first step with this library. By implementing these functions, you gain insight into memory management, algorithm design, and efficient coding practices. Use this library as a stepping stone for more complex projects and as a resource for developing your programming skills.

## Author & License
For any questions or contributions, feel free to [contact me](mailto:ani.mema@proton.me)
by [Ani Mema](https://github.com/amema42) - This project is licensed under the MIT License.
```css
This `README.md` file consolidates all the detailed explanations, code examples, and logical flow of this Libft project.
```
