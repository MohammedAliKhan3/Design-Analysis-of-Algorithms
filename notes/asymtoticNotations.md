# Asymptotic Notations

Mathematical tools to describe algorithm growth rates (time/space) as input size `n` approaches infinity. Focuses on growth patterns rather than exact values.

## Core Notations

### 1. Big-O (O) - Upper Bound
**Definition**:  
`f(n) = O(g(n))` if ∃ constants `C > 0`, `n₀ ≥ 0` such that:  
`f(n) ≤ C * g(n)` for all `n ≥ n₀`  

**Interpretation**:  
"Worst-case growth rate - won't exceed this"

**Example**:  
`2n + 3 = O(n)` with `C=3`, `n₀=3`

---

### 2. Omega (Ω) - Lower Bound
**Definition**:  
`f(n) = Ω(g(n))` if ∃ constants `C > 0`, `n₀ ≥ 0` such that:  
`f(n) ≥ C * g(n)` for all `n ≥ n₀`  

**Interpretation**:  
"Best-case growth rate - won't be better than this"

**Example**:  
`5n² + n = Ω(n²)` with `C=1`, `n₀=0`

---

### 3. Theta (Θ) - Tight Bound
**Definition**:  
`f(n) = Θ(g(n))` if ∃ constants `C₁,C₂ > 0`, `n₀ ≥ 0` such that:  
`C₁ * g(n) ≤ f(n) ≤ C₂ * g(n)` for all `n ≥ n₀`  

**Interpretation**:  
"Exact growth rate - bounded above and below"

**Example**:  
`3n + 5 = Θ(n)` with `C₁=3`, `C₂=4`, `n₀=5`

---

### 4. Little-o (o) - Strict Upper Bound
**Definition**:  
`f(n) = o(g(n))` if:  
`lim (n→∞) f(n)/g(n) = 0`  

**Interpretation**:  
"Grows strictly slower than"

**Example**:  
`n = o(n²)`

---

### 5. Little-omega (ω) - Strict Lower Bound
**Definition**:  
`f(n) = ω(g(n))` if:  
`lim (n→∞) g(n)/f(n) = 0`  

**Interpretation**:  
"Grows strictly faster than"

**Example**:  
`n² = ω(n)`

---

## Key Concepts

### Choosing g(n)
1. Identify the **dominant term** in f(n) (fastest-growing term)
2. Drop constants and lower-order terms
3. Match to standard growth classes:


### About n₀
- The threshold beyond which the inequality holds
- Small values may violate the bound (irrelevant for asymptotic analysis)

### Cheat Sheet
Notation | Relation | Analogy
--- | --- | ---
O | ≤ | "At worst"
Ω | ≥ | "At best"
Θ | = | "Exactly"
o | < | "Strictly less"
ω | > | "Strictly more"