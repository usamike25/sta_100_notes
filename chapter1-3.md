# Mathematical Foundations Cheat Sheet

## 1. Sets and Set Operations

### Basic Definitions
- **Set**: A collection of distinct elements (e.g., `A = {1, 2, 3}`)
- **Element**: 
  - `ω ∈ A` (element is in set)
  - `ω ∉ A` (element is not in set)

### Important Sets
| Symbol | Name                  | Description                          |
|--------|-----------------------|--------------------------------------|
| ℕ      | Natural Numbers       | Positive integers (1, 2, 3, ...)    |
| ℤ      | Integers              | (..., -2, -1, 0, 1, 2, ...)         |
| ℚ      | Rational Numbers      | Fractions p/q where p,q ∈ ℤ, q ≠ 0  |
| ℝ      | Real Numbers          | Includes √2, π, e, etc.             |
| ℂ      | Complex Numbers       | Numbers of form a + bi, i² = -1     |

### Set Operations
- **Union**: A ∪ B = {x | x ∈ A or x ∈ B}
- **Intersection**: A ∩ B = {x | x ∈ A and x ∈ B}
- **Difference**: A \ B = {x ∈ A | x ∉ B}
- **Complement**: If A ⊆ Ω, then Aᶜ = Ω \ A
- **Subset**: A ⊆ B if all elements of A are in B

### Special Cases
- **Empty Set (∅)**: The set containing no elements
  - Property: ∅ ⊆ A for any set A
- **Disjoint Sets**: A ∩ B = ∅ (no common elements)

### Key Properties
- **Density of ℚ in ℝ**: Between any two real numbers, there exists a rational number
- **Completeness of ℝ**: Every bounded subset has both a supremum (least upper bound) and infimum (greatest lower bound) in ℝ

---

## 2. Functions

### Basic Definition
A **function** f: A → B is a rule that assigns each element a ∈ A to exactly one element f(a) ∈ B.

### Important Concepts
- **Image**: f(E) = {f(a) | a ∈ E} for E ⊆ A
- **Preimage**: f⁻¹(D) = {a ∈ A | f(a) ∈ D} for D ⊆ B

### Function Types
| Type        | Condition                                  | Example                  |
|-------------|--------------------------------------------|--------------------------|
| Injective   | a₁ ≠ a₂ ⇒ f(a₁) ≠ f(a₂) (one-to-one)      | f(x) = 2x                |
| Surjective  | f(A) = B (onto)                            | f: ℝ → [0,∞), f(x)=x²    |
| Bijective   | Both injective and surjective (invertible) | f: ℝ → ℝ, f(x)=x³        |

### Monotonicity
- **Increasing**: x₁ < x₂ ⇒ f(x₁) ≤ f(x₂)
- **Strictly Increasing**: x₁ < x₂ ⇒ f(x₁) < f(x₂)

### Continuity
- **Topological Definition**: f: ℝᵐ → ℝᵏ is continuous if f⁻¹(U) is open for every open U ⊆ ℝᵏ
- **Sequence Criterion**: f is continuous at x iff for all sequences xₙ → x, we have f(xₙ) → f(x)

### Important Properties
- Preimage respects:
  - Unions: f⁻¹(⋃ⱼ Dⱼ) = ⋃ⱼ f⁻¹(Dⱼ)
  - Intersections: f⁻¹(⋂ⱼ Dⱼ) = ⋂ⱼ f⁻¹(Dⱼ)
- Bijective functions have unique inverses

---

## 3. Sequences

### Basic Definition
A **real sequence** (aₙ)ₙ∈ℕ is a function from ℕ to ℝ.

### Convergence
We say lim aₙ = a if:
∀ε > 0, ∃N ∈ ℕ such that ∀n ≥ N, |aₙ - a| < ε

### Divergence
- aₙ → +∞ if ∀M > 0, ∃N, ∀n ≥ N, aₙ > M
- aₙ → -∞ if ∀M < 0, ∃N, ∀n ≥ N, aₙ < M

### Key Properties
- **Boundedness**: Sequence is bounded if ∃M > 0 st |aₙ| ≤ M ∀n
- **Monotonic Sequences**:
  - Increasing: aₙ₊₁ ≥ aₙ
  - Decreasing: aₙ₊₁ ≤ aₙ
  - **Theorem**: Monotonic + Bounded ⇒ Convergent

### Subsequences
- A subsequence (aₖₙ) is obtained by selecting terms with increasing indices
- **Bolzano-Weierstrass Theorem**: Every bounded sequence has a convergent