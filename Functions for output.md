---
Theme: "[[C]]"
---

| **Function** | **Description**                           | **Features**                                     |
| ------------ | ----------------------------------------- | ------------------------------------------------ |
| `printf`     | Formatted output                          | Simple and versatile                             |
| `puts`       | Outputs a string with a newline           | No formatting, adds `\n`                         |
| `fputs`      | Outputs a string without adding a newline | Allows specifying the stream                     |
| `putchar`    | Outputs a single character                | Useful for character-by-character output         |
| `fprintf`    | Formatted output to an arbitrary stream   | Supports various streams (e.g., files)           |
| `vprintf`    | Formatted output with variable arguments  | Used for handling a variable number of arguments |
| `write`      | Low-level unbuffered output               | Used for low-level output                        |

---

## Format Specifiers

| **Specifier**  | **Description**                           |
| -------------- | ----------------------------------------- |
| `%c`           | For character type                        |
| `%d`           | For signed integer type                   |
| `%e`, `%E`     | For scientific notation of floats         |
| `%f`           | For float type                            |
| `%g`, `%G`     | For float type with the current precision |
| `%i`           | Signed integer                            |
| `%ld`, `%li`   | Long                                      |
| `%lf`          | Double                                    |
| `%Lf`          | Long double                               |
| `%lu`          | Unsigned int or unsigned long             |
| `%lli`, `%lld` | Long long                                 |
| `%llu`         | Unsigned long long                        |
| `%o`           | Octal representation                      |
| `%p`           | Pointer                                   |
| `%s`           | String                                    |
| `%u`           | Unsigned int                              |
| `%x`, `%X`     | Hexadecimal representation                |
| `%n`           | Prints nothing                            |
| `%%`           | Prints `%` character                      |
