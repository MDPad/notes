---
Theme:
  - "[[Go]]"
---
- Go source code is always UTF-8
- A strings hold arbitrary bytes
- - A string literal, absent byte-level escapes, always holds valid UTF-8 sequences
- This sequence represent Unicode "code points", called runes
- No guarantee is made in Go that characters in strings are normalised 