## ASCII

7-bit encoding (0–127)

**Pros:**
- Compact  
**Cons:**
- Covers only Latin letters, numbers, punctuation marks, and control characters

---
## UTF-8

Variable-length encoding, ranging from 1 to 4 bytes.  
Designed for backward compatibility with **ASCII**:  
The first 128 characters in UTF-8 correspond one-to-one with ASCII.

| First Code Point | Last Code Point | Byte 1   | Byte 2   | Byte 3   | Byte 4   |
| ---------------- | --------------- | -------- | -------- | -------- | -------- |
| U+0000           | U+007F          | 0yyyzzzz |          |          |          |
| U+0080           | U+07FF          | 110xxxyy | 10yyzzzz |          |          |
| U+0800           | U+FFFF          | 1110wwww | 10xxxxyy | 10yyzzzz |          |
| U+010000         | U+10FFFF        | 11110uvv | 10vvwwww | 10xxxxyy | 10yyzzzz |

**Pros:**
- Memory-efficient for ASCII
- Compatibility with ASCII
- Uses a hexadecimal (16-based) representation, for compactness and readability of encoded bytes
**Cons:**
- Variable length complicates processing

---
## UTF-16

Variable-length encoding, ranging from 2 to 4 bytes.  
Often used for Asian languages, as it is more efficient for these character sets.

**Pros:**
- More efficient for languages with large character sets (e.g., Chinese, Japanese, Korean)  
- Uses a hexadecimal (16-based) representation, for compactness and readability of encoded bytes
**Cons:**
- Variable length can complicate processing

---
## UTF-32

Fixed-length encoding, always 4 bytes per character.  
Space-inefficient but allows constant-time access to any code point.

**Pros:**
- Simple and predictable due to fixed length  
- Constant-time access to code points  
- Uses a hexadecimal (16-based) representation, for compactness and readability of encoded bytes
**Cons:**
- Space-inefficient compared to other encodings

---
## Legacy and Extended Encodings

Several other encodings have been used historically or as extensions of ASCII:

- **Extended ASCII (ANSI)**: 8-bit encodings that added support for regional characters (e.g., Windows-1252 for Western Europe, Windows-1251 for Cyrillic). Common before the adoption of Unicode.  
- **ISO/IEC 8859 (Latin Series)**: A family of 8-bit encodings for regional use:
  - **ISO-8859-1 (Latin-1)**: Western European languages.  
  - **ISO-8859-5**: Cyrillic script.  
  - **ISO-8859-15**: Adds the euro (€) symbol to Latin-1.  
- **KOI8-R**: A Russian encoding popular in Soviet-era systems.  
- **Shift JIS**: Japanese encoding, widely used in older applications.  
- **Big5**: Traditional Chinese encoding used in Taiwan and Hong Kong.  
- **EBCDIC**: Developed by IBM for mainframes, incompatible with ASCII.

These legacy encodings are mostly obsolete, having been replaced by Unicode (primarily UTF-8) due to its universal support for all characters and global standardization.
