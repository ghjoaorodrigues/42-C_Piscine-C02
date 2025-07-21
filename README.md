# C Piscine - C 02

![42 Badge](https://img.shields.io/badge/42-C_Piscine-brightgreen)
![C Badge](https://img.shields.io/badge/Language-C-blue)
![Status Badge](https://img.shields.io/badge/Status-Completed-success)

## What I Learned

Through this second C module of the 42 Piscine, I developed fundamental string manipulation and memory handling skills:

- **String manipulation fundamentals** - Mastered basic string operations like copying, comparison, and transformation
- **Memory safety practices** - Learned to handle buffer boundaries and prevent overflow vulnerabilities
- **Character classification** - Implemented functions to validate and categorize character types
- **ASCII and hexadecimal understanding** - Gained deep knowledge of character encoding and representation
- **Pointer arithmetic basics** - Applied pointer operations for efficient string traversal
- **Input validation techniques** - Developed robust checking for edge cases and invalid inputs
- **Low-level output formatting** - Created custom display functions for non-printable characters
- **Memory visualization** - Implemented hexdump-like functionality for debugging purposes
- **Function prototyping** - Followed strict function signatures and return value conventions
- **Norminette compliance** - Maintained 42's coding standards throughout all implementations

This module strengthened my understanding of C strings, memory layout, and low-level programming concepts essential for systems programming.

## About the Project

C 02 is the second module of the C Piscine at 42 School, focusing on string manipulation and character handling. The project consists of 13 exercises that progressively build complexity from basic string operations to advanced memory visualization tools.

## Implementation Details

The module consists of 13 exercises divided into four main categories:

### String Copying Functions

Basic string manipulation operations with size control:

| Function | Purpose | Key Learning |
|----------|---------|--------------|
| ft_strcpy | Copy entire string | Basic pointer manipulation |
| ft_strncpy | Copy n characters | Buffer size awareness |
| ft_strlcpy | Size-bounded copy | Safe string handling |

### Character Classification Functions

Boolean functions that validate string content:

| Function | Validation | Return Value |
|----------|------------|--------------|
| ft_str_is_alpha | Alphabetical only | 1 if valid, 0 otherwise |
| ft_str_is_numeric | Digits only | 1 if valid, 0 otherwise |
| ft_str_is_lowercase | Lowercase letters only | 1 if valid, 0 otherwise |
| ft_str_is_uppercase | Uppercase letters only | 1 if valid, 0 otherwise |
| ft_str_is_printable | Printable characters only | 1 if valid, 0 otherwise |

*Note: All classification functions return 1 for empty strings*

### String Transformation Functions

Functions that modify string content in place:

| Function | Transformation | Behavior |
|----------|----------------|----------|
| ft_strupcase | Convert to uppercase | Modifies original string |
| ft_strlowcase | Convert to lowercase | Modifies original string |
| ft_strcapitalize | Capitalize words | First letter of each word uppercase |

### Advanced Display Functions

Complex functions for debugging and memory visualization:

| Function | Purpose | Output Format |
|----------|---------|---------------|
| ft_putstr_non_printable | Display with hex escapes | Non-printable as \xx |
| ft_print_memory | Hexdump-style display | Address: hex bytes + ASCII |

## Usage Examples

### Basic String Operations
```c
#include <stdio.h>

// String copying
char dest[20];
ft_strcpy(dest, "Hello World");
printf("%s\n", dest); // Output: Hello World

// Limited copying
char buffer[10];
ft_strncpy(buffer, "Very long string", 5);
// buffer contains "Very " (note: may not be null-terminated)
```

### Character Validation
```c
// Check if string contains only letters
int result = ft_str_is_alpha("HelloWorld");    // Returns 1
int result2 = ft_str_is_alpha("Hello123");     // Returns 0
int result3 = ft_str_is_alpha("");             // Returns 1 (empty string)

// Validate numeric strings
int is_num = ft_str_is_numeric("12345");       // Returns 1
int is_num2 = ft_str_is_numeric("123a5");      // Returns 0
```

### String Transformation
```c
char text[] = "hello world";
ft_strupcase(text);
printf("%s\n", text); // Output: HELLO WORLD

char mixed[] = "hELLo WoRLd";
ft_strlowcase(mixed);
printf("%s\n", mixed); // Output: hello world

char sentence[] = "salut, comment tu vas ? 42mots quarante-deux";
ft_strcapitalize(sentence);
printf("%s\n", sentence); // Output: Salut, Comment Tu Vas ? 42mots Quarante-Deux
```

### Advanced Display
```c
// Display string with non-printable characters
char str[] = "Coucou\ntu vas bien ?";
ft_putstr_non_printable(str);
// Output: Coucou\0atu vas bien ?

// Memory visualization
char data[] = "Bonjour les amins";
ft_print_memory(data, strlen(data));
// Output: hexdump-style display with address, hex, and ASCII
```

## Technical Challenges Overcome

- **Buffer overflow prevention** - Ensuring bounded operations never write beyond allocated memory
- **Null termination handling** - Managing string termination in size-limited operations
- **Character encoding mastery** - Working with ASCII values for case conversion and validation
- **Hexadecimal formatting** - Converting bytes to hexadecimal representation for display
- **Memory address calculation** - Implementing proper address arithmetic for memory dumps
- **Edge case handling** - Managing empty strings, null pointers, and boundary conditions
- **Performance optimization** - Implementing efficient single-pass algorithms where possible

## Key Concepts Reinforced

- **Pointer vs Array notation** - Understanding when to use each approach
- **Memory layout visualization** - Learning how data is stored and accessed
- **Character sets and encoding** - ASCII table manipulation and validation
- **String immutability concepts** - When to modify in-place vs create new strings
- **Debugging techniques** - Using memory visualization tools for troubleshooting

---

*This project was completed as part of the 42 Piscine curriculum, demonstrating proficiency in C string manipulation, character handling, and low-level programming fundamentals.*

---

## License

This project is licensed under the [MIT License](./LICENSE).
