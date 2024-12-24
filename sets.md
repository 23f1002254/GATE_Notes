# Sets in Mathematics

## Definitions
- **Set**: A collection of distinct elements, often denoted by curly brackets `{}`.
- **Subset**: A set `A` is a subset of set `B` (written `A ⊆ B`) if all elements of `A` are also elements of `B`.

## Basic Set Operations

### 1. **Union ( ∪ )**
- The union of two sets `A` and `B` is the set of elements that are in either `A`, `B`, or both.
  \[
  A ∪ B = \{x \ | \ x \in A \ \text{or} \ x \in B\}
  \]

### 2. **Intersection ( ∩ )**
- The intersection of two sets `A` and `B` is the set of elements that are in both `A` and `B`.
  \[
  A ∩ B = \{x \ | \ x \in A \ \text{and} \ x \in B\}
  \]

### 3. **Difference ( - )**
- The difference of two sets `A` and `B` (also called the complement of `B` in `A`) is the set of elements that are in `A` but not in `B`.
  \[
  A - B = \{x \ | \ x \in A \ \text{and} \ x \notin B\}
  \]

### 4. **Complement ( Aᶜ )**
- The complement of set `A` refers to all elements that are not in `A` (relative to a universal set `U`).
  \[
  A^c = \{x \ | \ x \notin A\}
  \]

## De Morgan's Laws

De Morgan's Laws relate the complement of unions and intersections of sets:

1. **First Law:**
   \[
   (A ∪ B)^c = A^c ∩ B^c
   \]
   - The complement of the union is the intersection of the complements.

2. **Second Law:**
   \[
   (A ∩ B)^c = A^c ∪ B^c
   \]
   - The complement of the intersection is the union of the complements.

## Examples in Python

### Set Operations in Python

```python
# Defining sets
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

# Union
union = A | B  # {1, 2, 3, 4, 5, 6}

# Intersection
intersection = A & B  # {3, 4}

# Difference
difference = A - B  # {1, 2}

# Symmetric Difference (elements in A or B but not both)
symmetric_difference = A ^ B  # {1, 2, 5, 6}

# Complement (assuming a universal set U)
U = {1, 2, 3, 4, 5, 6, 7, 8}
complement_A = U - A  # {5, 6, 7, 8}

# De Morgan's Laws Verification
A_union_B_complement = U - (A | B)  # Complement of union
A_complement_intersection_B_complement = (U - A) & (U - B)
assert A_union_B_complement == A_complement_intersection_B_complement

A_intersection_B_complement = U - (A & B)  # Complement of intersection
A_complement_union_B_complement = (U - A) | (U - B)
assert A_intersection_B_complement == A_complement_union_B_complement

This markdown format is GitHub-friendly and includes both the theory and Python code examples. Let me know if you need further customization!
```
