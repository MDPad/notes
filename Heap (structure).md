---
Theme:
  - "[[Computer science]]"
---
always extract the minimal/maximal element quickly

## Core Operations

#### 1. `Push(item)` — Insert

1. **Append** `item` at end of `items`.
2. **Sift-Up**:
    - Let `i` = index of the new element.
    - While `i > 0` and `cmp(items[i], items[parent(i)])` is true:
        - Swap `items[i]` with its parent.
        - Set `i = parent(i)`.
    - Stops when the heap property is restored or the element reaches the root.

**Time Complexity:** O(log n)

#### 2. `Pop()` — Remove Top

1. Swap root `items[0]` with last element.
2. Remove (slice-truncate) the last element (old root).
3. **Sift-Down** from index 0:
    - Let `i = 0`.
    - Repeatedly compare `items[i]` with its children:
        - Choose the “better” child (smaller for min-heap, larger for max-heap).
        - If `cmp(child, items[i])`, swap and set `i` to that child’s index.
        - Otherwise, stop.

**Time Complexity:** O(log n)

#### 3. `Peek()` & `Len()`

- **`Peek()`** returns `items[0]` without removal (O(1)).
- **`Len()`** returns `len(items)` (O(1)).


## Complexity Summary

| Operation | Time     |
| --------- | -------- |
| Build     | O(n)     |
| Push      | O(log n) |
| Pop       | O(log n) |
| Peek/Min  | O(1)     |

```js
Index:  0   1   2   3   4   5   6    7    8    9    10
Item:  [p0, l0, r0, l1, r1, l2, r2,  l3,  r3,  l4,  r4]
```

```js
              p0 (i=0)
       ┌───────┴───────┐
     l0 (1)         r0 (2)
    ┌──┴──┐         ┌──┴──┐
 l1(3) r1(4)     l2(5) r2(6)
  ┌─┴─┐ ┌─┴─┐
l3(7) r3(8) l4(9) r4(10)

```