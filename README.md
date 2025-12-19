# Libft

A custom implementation of essential C standard library functions, created as part of the curriculum at Codam (42 Amsterdam).

## About

Libft is the first project at 42, where students recreate their own library of standard C functions. This library serves as a foundation for future projects throughout the 42 curriculum, providing essential tools for string manipulation, memory management, and more.

This extended version of Libft includes:
- **Standard C Library Functions** - Core functions for string, memory, and character operations
- **Additional Utility Functions** - Enhanced string manipulation and output functions
- **ft_printf** - Custom implementation of formatted output functions
- **get_next_line** - Line reading functionality for file descriptors

## Project Information

- **Author**: rmengelb
- **School**: Codam (42 Amsterdam)
- **Cohort**: 2024
- **Project**: Libft

## Functions

### Part 1 - Libc Functions

These functions replicate the behavior of standard C library functions:

**Character Checks & Conversions:**
- `ft_isalpha` - checks for alphabetic character
- `ft_isdigit` - checks for digit character
- `ft_isalnum` - checks for alphanumeric character
- `ft_isascii` - checks for ASCII character
- `ft_isprint` - checks for printable character
- `ft_toupper` - converts character to uppercase
- `ft_tolower` - converts character to lowercase

**String Functions:**
- `ft_strlen` - calculates string length
- `ft_strlcpy` - size-bounded string copying
- `ft_strlcat` - size-bounded string concatenation
- `ft_strchr` - locates first occurrence of character in string
- `ft_strrchr` - locates last occurrence of character in string
- `ft_strncmp` - compares two strings up to n characters
- `ft_strnstr` - locates substring in string
- `ft_strdup` - duplicates a string

**Memory Functions:**
- `ft_memset` - fills memory with a constant byte
- `ft_bzero` - zeros a byte string
- `ft_memcpy` - copies memory area
- `ft_memmove` - copies memory area (handles overlap)
- `ft_memchr` - scans memory for a character
- `ft_memcmp` - compares memory areas

**Conversion:**
- `ft_atoi` - converts string to integer (returns long int)

**Memory Allocation:**
- `ft_calloc` - allocates and zeros memory

### Part 2 - Additional Functions

Additional useful functions not in the standard library:

- `ft_substr` - extracts substring from string
- `ft_strjoin` - concatenates two strings
- `ft_strjoin_array` - joins array of strings with separator
- `ft_strtrim` - trims characters from beginning and end of string
- `ft_split` - splits string into array of strings by delimiter
- `ft_itoa` - converts integer to string
- `ft_strmapi` - applies function to each character of string
- `ft_striteri` - applies function to each character of string with index
- `ft_putchar_fd` - outputs character to file descriptor
- `ft_putstr_fd` - outputs string to file descriptor
- `ft_putendl_fd` - outputs string to file descriptor with newline
- `ft_putnbr_fd` - outputs integer to file descriptor

### ft_printf

Custom implementation of printf with formatted output:

- `ft_printf` - outputs formatted string to stdout
- `ft_dprintf` - outputs formatted string to specified file descriptor

**Supported format specifiers:**
- `%c` - character
- `%s` - string
- `%p` - pointer address
- `%d` - decimal integer
- `%i` - integer
- `%u` - unsigned integer
- `%x` - hexadecimal (lowercase)
- `%X` - hexadecimal (uppercase)
- `%%` - percent sign
- `%r` - reverse string (custom specifier)

### get_next_line

Reads a line from a file descriptor:

- `get_next_line` - reads and returns the next line from a file descriptor, including the newline character

## Compilation

The library includes a Makefile with the following rules:

```bash
make        # Compiles the library (libft.a)
make clean  # Removes object files
make fclean # Removes object files and library
make re     # Recompiles the library
```

The compiled library (`libft.a`) includes all standard libft functions, ft_printf, and get_next_line.

## Usage

1. Clone the repository:
```bash
git clone <repository-url> libft
cd libft
```

2. Compile the library:
```bash
make
```

3. Include in your project:
```c
#include "libft.h"
```

4. Compile your project with the library:
```bash
gcc -Wall -Wextra -Werror your_file.c -L. -lft -o your_program
```

## Project Structure

```
libft/
├── Makefile
├── README.md
├── libft.h
├── ft_*.c              # Standard libft functions
├── printf/
│   ├── ft_printf.c
│   └── ft_print_*.c    # Format specifier implementations
└── gnl/
    ├── ft_gnl.c
    └── ft_gnl_helpers.c
```

## Norms

This project adheres to the 42 Norm, which includes:

- Maximum 25 lines per function
- Maximum 5 functions per file
- Forbidden: for, do-while, switch, case, goto
- All variables must be declared at the beginning of the function
- No more than 4 parameters per function

## Testing

It's recommended to test your library with various testers available in the 42 community:

- [Libft Unit Tests](https://github.com/alelievr/libft-unit-test)
- [Libftest](https://github.com/jtoty/Libftest)
- [war-machine](https://github.com/0x050f/libft-war-machine)

## Resources

- [42 Norm Documentation](https://github.com/42School/norminette)
- [C Library Reference](https://www.cplusplus.com/reference/clibrary/)

## License

This project is part of the 42 curriculum and is intended for educational purposes.

---

*Made with ☕ at Codam (42 Amsterdam) - 2024*