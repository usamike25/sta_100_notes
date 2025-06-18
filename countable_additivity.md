# Cheat Sheet: Set Functions Failing Countable Additivity

Set functions that violate countable additivity (σ-additivity) despite satisfying other measure properties.

## Table of Examples

| Set Function | Defined On | Definition | Counterexample | Failure Reason |
|-------------|------------|------------|----------------|----------------|
| **Point-Lebesgue Product** | (ℝ, B(ℝ)) | `μ(A) = λ(A)·δ₀(A)` <br>where λ = Lebesgue measure, <br>δ₀(A) = 1_{0}(A) | A₁ = {0}, A₂ = (1,2) <br>μ(A₁) = 0, μ(A₂) = 0 <br>μ(A₁∪A₂) = μ([0,2)) = 1 ≠ 0 | Dirac mass dominates Lebesgue null sets when 0 ∈ A |
| **Finite/Infinite Dichotomy** | (ℕ, 𝒫(ℕ)) | `μ(A) = {0 if A finite, ∞ if A infinite}` | Aₙ = {n} (disjoint) <br>μ(Aₙ) = 0 ∀n <br>μ(∪Aₙ) = μ(ℕ) = ∞ ≠ 0 | Finitely additive but not σ-additive |
| **Binary Jump** | ([0,1], B([0,1])) | `μ(A) = {0 if λ(A)=0, 1 if λ(A)>0}` | Aₙ = (1/(n+1), 1/n] <br>μ(Aₙ) = 1 ∀n <br>μ(∪Aₙ) = μ((0,1]) = 1 ≠ Σ1 = ∞ | Measures only presence of positive Lebesgue measure |
| **Asymptotic Density** | (ℕ, 𝒫(ℕ)) | `μ(A) = lim_{n→∞} |A∩{1,...,n}|/n` (if exists) | Aₙ = {n} (singletons) <br>μ(Aₙ) = 0 ∀n <br>μ(∪Aₙ) = μ(ℕ) = 1 ≠ 0 | Limit operation prevents countable additivity |

## Additional Examples

| **Logarithmic Density** | (ℕ, 𝒫(ℕ)) | `μ(A) = lim_{n→∞} 1/log(n) Σ_{k∈A∩[1,n]} 1/k` | Aₙ = {n} <br>μ(Aₙ) = 0 ∀n <br>μ(ℕ) = ∞ | Harmonic series behavior breaks additivity |
| **Ultrafilter Measure** | (ℕ, 𝒫(ℕ)) | `μ(A) = {1 if A ∈ 𝓤, 0 otherwise}` <br>(𝓤 = free ultrafilter) | Aₙ = {2ⁿ} <br>μ(Aₙ) = 0 ∀n <br>μ(∪Aₙ) = μ(ℕ) = 1 | Non-measurability under ultrafilter |

## Failure Patterns

1. **Point Mass Interference**: Dirac measures can override Lebesgue null sets
2. **Finite vs. Infinite**: Infinite unions of finite/null sets may have non-zero measure
3. **Discontinuous Measures**: Threshold-based measures ignore set granularity
4. **Asymptotic Limits**: Limits may not commute with infinite sums
5. **Non-σ Structures**: Ultrafilters and similar constructs violate countable additivity
