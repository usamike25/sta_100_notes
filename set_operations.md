# Set Operations: Union and Intersection Cheat Sheet

## Definitions
- **Union**: \(A \cup B = \{ x \mid x \in A \text{ or } x \in B\}\)
- **Intersection**: \(A \cap B = \{ x \mid x \in A \text{ and } x \in B\}\)

---

## Key Properties
### General Laws
| Property          | Union                               | Intersection                         |
|-------------------|-------------------------------------|--------------------------------------|
| **Commutative**   | \(A \cup B = B \cup A\)             | \(A \cap B = B \cap A\)              |
| **Associative**   | \((A \cup B) \cup C = A \cup (B \cup C)\) | \((A \cap B) \cap C = A \cap (B \cap C)\) |
| **Idempotent**    | \(A \cup A = A\)                    | \(A \cap A = A\)                     |
| **Identity**      | \(A \cup \emptyset = A\)            | \(A \cap U = A\) (U = universal set) |
| **Domination**    | \(A \cup U = U\)                    | \(A \cap \emptyset = \emptyset\)     |

### Distributive Laws
1. \(A \cup (B \cap C) = (A \cup B) \cap (A \cup C)\)
2. \(A \cap (B \cup C) = (A \cap B) \cup (A \cap C)\)

### Absorption Laws
- \(A \cup (A \cap B) = A\)
- \(A \cap (A \cup B) = A\)

---

## Proof Strategies
### Equality Proofs
To prove \(X = Y\):
1. Show \(X \subseteq Y\)  
   (Assume \(x \in X\), prove \(x \in Y\))
2. Show \(Y \subseteq X\)  
   (Assume \(y \in Y\), prove \(y \in X\))

### Subset Relations
To prove \(A \subseteq B\):  
Assume \(a \in A\), then show \(a \in B\).

---

## Proof Examples
### 1. Distributive Law Proof: \(A \cup (B \cap C) = (A \cup B) \cap (A \cup C)\)
> **Proof**  
> **(i) Show \(A \cup (B \cap C) \subseteq (A \cup B) \cap (A \cup C)\)**  
> Let \(x \in A \cup (B \cap C)\).  
> Then \(x \in A\) **or** \(x \in B \cap C\).  
> - If \(x \in A\), then \(x \in A \cup B\) and \(x \in A \cup C\), so \(x \in (A \cup B) \cap (A \cup C)\).  
> - If \(x \in B \cap C\), then \(x \in B\) and \(x \in C\). Thus \(x \in A \cup B\) and \(x \in A \cup C\), so \(x \in (A \cup B) \cap (A \cup C)\).  
>   
> **(ii) Show \((A \cup B) \cap (A \cup C) \subseteq A \cup (B \cap C)\)**  
> Let \(x \in (A \cup B) \cap (A \cup C)\).  
> Then \(x \in A \cup B\) **and** \(x \in A \cup C\).  
> - If \(x \in A\), then \(x \in A \cup (B \cap C)\).  
> - If \(x \notin A\), then \(x \in B\) (from \(x \in A \cup B\)) and \(x \in C\) (from \(x \in A \cup C\)). Thus \(x \in B \cap C\), so \(x \in A \cup (B \cap C)\).  
>   
> ∴ Equality holds by double inclusion. ■

### 2. Absorption Law Proof: \(A \cap (A \cup B) = A\)
> **Proof**  
> **(i) Show \(A \cap (A \cup B) \subseteq A\)**  
> Let \(x \in A \cap (A \cup B)\).  
> Then \(x \in A\) **and** \(x \in A \cup B\). Thus \(x \in A\).  
>   
> **(ii) Show \(A \subseteq A \cap (A \cup B)\)**  
> Let \(x \in A\).  
> Then \(x \in A \cup B\) (since \(A \subseteq A \cup B\)), so \(x \in A \cap (A \cup B)\).  
>   
> ∴ Equality holds by double inclusion. ■

---

## De Morgan's Laws (Sets)
- \( (A \cup B)^c = A^c \cap B^c \)  
- \( (A \cap B)^c = A^c \cup B^c \)

---

## Tips for Proofs
- **Membership Tables**: Verify identities by enumerating cases.  
- **Venn Diagrams**: Visualize relationships (but not formal proofs).  
- **Logical Equivalence**: Convert \(\cup\) to \(\lor\) and \(\cap\) to \(\land\) in logic statements.  