---
Theme: "[[Database]]"
---
- **Atomic** — each transaction is either completed or reverted entirely. The transaction can’t modify only some records and fail for others.
- **Consistent** — modified entities must still meet all the consistency requirements. Foreign keys must point to existing entities, values must meet the data type specifications, and other checks must still pass.
- **Isolated** — transactions must interact with each other following the isolation levels they specified.
- **Durable** — when the transaction is confirmed to be committed, the changes must be persistent even in the face of software issues and hardware failures.