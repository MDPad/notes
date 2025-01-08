---
Theme: "[[C]]"
---

| **Directive** | **Description**                                                            |
| ------------- | -------------------------------------------------------------------------- |
| `#define`     | Defines a macro. Can be used for constants or macro functions.             |
| `#undef`      | Undefines a macro.                                                         |
| `#include`    | Includes the contents of a file in the current file before compilation.    |
| `#if`         | Starts a conditional block, compiled only if the condition is true.        |
| `#ifdef`      | Compiles the following block if the macro is defined.                      |
| `#ifndef`     | Compiles the following block if the macro is not defined.                  |
| `#else`       | Creates an alternative block if the initial condition is false.            |
| `#elif`       | Adds an "else if" condition in preprocessor directives.                    |
| `#endif`      | Ends a conditional block started with `#if`, `#ifdef`, or `#ifndef`.       |
| `#error`      | Generates a compilation error with a custom message.                       |
| `#pragma`     | Issues special commands to the compiler. Specifics depend on the compiler. |
| `#line`       | Changes the current line number and filename in compiler error messages.   |
