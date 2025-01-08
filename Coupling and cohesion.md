---
Theme: "[[Software design]]"
---
## Coupling
**Definition**: The degree of dependency between modules.

- **Ideal**: Loose Coupling (minimal dependency between modules).
- **Problems with Tight Coupling**:
  - Difficult maintenance and testing.
  - Changes in one module affect others.
- **Recommendation**: Minimize dependencies between modules.

---

## Cohesion
**Definition**: The degree to which elements within a module belong together.

- **Ideal**: High Cohesion (module focuses on a single task).
- **Problems with Low Cohesion**:
  - Poor readability and maintainability.
  - Scattered and unrelated logic.
- **Recommendation**: Ensure modules perform one well-defined task.

---

## Comparative Table

| **Aspect**                  | **Coupling**                              | **Cohesion**                                         |
| --------------------------- | ----------------------------------------- | ---------------------------------------------------- |
| **Focus**                   | Dependency between modules.               | Connection between functions within a single module. |
| **Ideal**                   | Loose Coupling (minimal interdependence). | High Cohesion (focus on a single task).              |
| **Problems with low level** | Tight coupling hinders modularity.        | Blurred logic and poor maintainability.              |
| **Recommendations**         | Minimize dependencies between modules.    | Ensure each module performs one specific task.       |

---

**Key Goal**: Achieve **Loose Coupling** and **High Cohesion** for better modularity and maintainability.
