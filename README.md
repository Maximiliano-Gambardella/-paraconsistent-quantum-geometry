# Geometry of Paraconsistent Quantum Channel Optimisation: Formal Verification

This repository provides the **formal verification in Lean 4** of the geometric and stability theorems presented in the research paper:

> **"Geometry of Paraconsistent Quantum Channel Optimisation: Morse–Bott Landscape, Diamond-Norm Stability, and Jacobi Scaling on the Stiefel Manifold"**  
> *Maximiliano Gambardella (2026)*

## 🔬 Overview
This project resolves the "open problem" of formalising paraconsistent quantum channel optimisation as identified in the original manuscript [1-3]. Using the **Lean 4** interactive theorem prover and the **Mathlib** library, we certify the entire logical chain from paraconsistent logical foundations to global topological convergence on the Stiefel manifold $St(d, rd)$.

## 🛠️ Certified Levels
The formal proof is structured into 5 hierarchical levels of certification:

1. **Level 1: Foundation (Assumption 2.2)**  
   Formal verification of the paraconsistent evidence weights (Belnap weights $\mu_T, \mu_F$) and the certification of the critical spectral value $\kappa > 1$ [1, 4, 5].
   
2. **Level 2: Spectral Obstruction (Proposition 4.1)**  
   Mechanized proof that the trace-preservation (TP) fibre $\pi^{-1}(Id_d)$ is empty on the Stiefel manifold, establishing the fundamental geometric impossibility of perfect reconstruction under paraconsistent weights [6-8].

3. **Level 3: Minimum Residual (Theorem 4.2)**  
   Verification of the tight lower bound for the spectral residual: $R_{min} = \mu_F\sqrt{d}$ [6, 9, 10].

4. **Level 4: Diamond-Norm Stability (Theorem 6.2)**  
   Certification of the corrected stability bound: $\| \Phi_V - I \|_\diamond \leq \varepsilon + \mu_F + \sqrt{r}\delta$. This proof specifically validates the correction of previous literature by using the **diamond norm** $\mu_F$ instead of the Frobenius norm $\mu_F\sqrt{d}$, ensuring physical consistency [11-13].

5. **Level 5: Morse–Bott Topology (Theorem 5.2)**  
   Formal classification of critical points as **strict saddles**. The proof certifies that every non-optimal critical point has a negative curvature coefficient of $-2\mu_T(\mu_T - \mu_F) < 0$ [10, 11, 14]. This guarantees the absence of spurious local minima and ensures global convergence for Riemannian gradient descent.
