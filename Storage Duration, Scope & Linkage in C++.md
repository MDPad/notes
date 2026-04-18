---
Theme:
  - C++
---

Defined by three properties:

1. **Lifetime** — duration for which data lives in memory.
2. **Scope** — regions of code that can access the data.
3. **Linkage** — if data can be referred to from another translation unit, linkage is _external_; otherwise _internal_.

#### Automatic / Register Storage

| Lifetime          | Scope | Linkage |
| ----------------- | ----- | ------- |
| Automatic (block) | Block | None    |
```cpp
{
    int i = 5;
}

if (true) {
    register int j = 3; // register is deprecated
}

for (int k = 0; k < 7; ++k) {}
```

#### Static without Linkage

| Lifetime | Scope | Linkage |
| -------- | ----- | ------- |
| Static   | Block | None    |
```cpp
void foo()
{
    static int j = 3; // initialised on first call
}
```

#### Static with External Linkage

| Lifetime | Scope | Linkage  |
| -------- | ----- | -------- |
| Static   | File  | External |
```cpp
static int i = 5; // initialised before main()
```

#### Static with External Linkage

| Lifetime | Scope | Linkage  |
| -------- | ----- | -------- |
| Static   | File  | External |
```cpp
// .cpp
int i = 0;

// .h
extern int i;
```