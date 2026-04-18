---
Theme:
  - "[[C++]]"
---
The C++ Standard does **NOT** mandate exact sizes for these types.

https://en.cppreference.com/w/cpp/language/types.html

| Signed  | Unsigned                     |
| ------- | ---------------------------- |
| `char`  | `unsigned char`              |
| `short` | `unsigned short`             |
| `int`   | `unsigned` or `unsigned int` |
| `long`  | `unsigned long`              |

https://en.cppreference.com/w/cpp/types/integer.html

| Width (bits) | Type                                       |
| ------------ | ------------------------------------------ |
| 8            | `int8_t`, `int_fast8_t`, `int_least8_t`    |
| 16           | `int16_t`, `int_fast16_t`, `int_least16_t` |
| 32           | `int32_t`, `int_fast32_t`, `int_least32_t` |
| 64           | `int64_t`, `int_fast64_t`, `int_least64_t` |
The unsigned variant is obtained by adding the prefix `u`, e.g. `uint32_t`.