# Reading Plan: Mean-Variance Hedging to Rough Volatility

> **Goal:** Understand mean-variance hedging theory and extend the Černý-Kallsen framework (R3) from Heston to rough volatility models.

---

## Overview

```
Phase 1: Foundations ──────► Phase 2: General Theory ──────► Phase 3: Heston ──────► Phase 4: Rough Volatility
   (R16, R18)                      (R17)                        (R3)                   (R4, R6, R14)
```

**Estimated Total Time:** 4-5 weeks

---

## Phase 1: Foundations

> **Goal:** Understand what mean-variance hedging is and the key objects involved.

### Reading 1: Schweizer's Guided Tour (R16)

📄 **Paper:** *A Guided Tour through Quadratic Hedging Approaches*
👤 **Author:** Martin Schweizer
📅 **Time Estimate:** 2 days

- [ ] Read Section 1 — Introduction and motivation
- [ ] Read Section 2 — Setup and notation
- [ ] Read Section 3 — Local risk-minimization
- [ ] Read Section 4 — Mean-variance hedging
- [ ] Write summary notes

**Focus:** Big picture understanding of quadratic hedging approaches and how they compare.

---

### Reading 2: Pham, Rheinländer & Schweizer (R18) — Part 1

📄 **Paper:** *Mean-Variance Hedging for Continuous Processes: New Proofs and Examples*
👤 **Authors:** Pham, Rheinländer, Schweizer
📅 **Time Estimate:** 2 days

- [ ] Read Section 0 — Introduction
- [ ] Read Section 1 — Preliminaries and motivation
- [ ] Read Section 2 — Closedness of $G_T(\Theta)$ and Föllmer-Schweizer decomposition
- [ ] Understand Proposition 1 (exponential weighting technique)
- [ ] Understand Corollary 4 (closedness) and Corollary 5 (FS decomposition)
- [ ] Write summary notes

**Focus:** Concrete setup, why closedness matters, the Föllmer-Schweizer decomposition.

---

### Reading 3: Pham, Rheinländer & Schweizer (R18) — Part 2

📅 **Time Estimate:** 2 days

- [ ] Read Section 3 — Description of optimal strategy
- [ ] Understand the special assumption $\hat{L}_T = 0$
- [ ] Understand Theorem 7 (feedback formula)
- [ ] Understand Corollary 9 (minimal quadratic risk)
- [ ] Read Section 4 — Examples
- [ ] Work through Example 2 (diffusion model)
- [ ] Work through Examples 5-6 (stochastic volatility)
- [ ] Understand Theorem 11 and 12 (when special assumption fails)
- [ ] Write summary notes

**Focus:** The feedback formula, when minimal = variance-optimal martingale measure, and importantly, when this fails.

---

### Phase 1 Checkpoint

- [ ] **I can explain:** What is the Föllmer-Schweizer decomposition?
- [ ] **I can explain:** What is the mean-variance tradeoff process $\hat{K}$?
- [ ] **I can explain:** What is the minimal martingale measure $\hat{P}$?
- [ ] **I can explain:** When does $\hat{P}$ = variance-optimal measure (and when does it fail)?

---

## Phase 2: General Theory

> **Goal:** Understand the Černý-Kallsen framework that R3 uses.

### Reading 4: Černý & Kallsen General Theory (R17) — Setup

📄 **Paper:** *On the Structure of General Mean-Variance Hedging Strategies*
👤 **Authors:** Aleš Černý, Jan Kallsen
📅 **Time Estimate:** 2 days

- [ ] Read Section 1.1 — Overview
- [ ] Read Section 1.2 — Semimartingale characteristics and notation
- [ ] Read Section 2.1 — Admissible strategies
- [ ] Read Section 2.2 — Mean-variance hedging problem definition
- [ ] Create notation reference sheet
- [ ] Write summary notes

**Focus:** Setting up the general semimartingale framework and understanding the notation.

---

### Reading 5: Černý & Kallsen (R17) — Core Theory

📅 **Time Estimate:** 4 days

- [ ] Read Section 3.1 — Opportunity process $L$
- [ ] Understand Lemma 3.1 and 3.2
- [ ] Understand Definition 3.3 (opportunity process)
- [ ] Understand Proposition 3.6 (link to Sharpe ratio)
- [ ] Read Section 3.2 — Adjustment process $\tilde{a}$
- [ ] Understand Lemma 3.7 and Definition 3.8
- [ ] Read Section 3.3 — Variance-optimal signed martingale measure
- [ ] Understand Definition 3.12 and Proposition 3.13
- [ ] Read Section 3.4 — Opportunity-neutral measure $P^\star$
- [ ] Understand Definition 3.16 and Lemma 3.17
- [ ] Read Section 3.5 — Characterization of $L$ and $\tilde{a}$
- [ ] Understand Theorem 3.25 (main characterization)
- [ ] Write summary notes

**Key equations to understand:**

| Object | Definition | Interpretation |
|--------|------------|----------------|
| $L$ | Opportunity process | $L_t^{-1} - 1 = \varrho_t^2$ (max Sharpe ratio squared) |
| $\tilde{a}$ | Adjustment process | Optimal shares per unit wealth |
| $K$ | $\mathcal{L}(L)$ | Modified mean-variance tradeoff |
| $P^\star$ | Opportunity-neutral measure | Makes dynamic problem myopic |
| $Q^\star$ | Variance-optimal measure | Minimal martingale measure relative to $P^\star$ |

---

### Reading 6: Černý & Kallsen (R17) — When $P^\star = P$ and Computation

📅 **Time Estimate:** 2 days

- [ ] Read Section 3.6 — When does $P^\star = P$ hold?
- [ ] Understand Proposition 3.28
- [ ] Understand Corollaries 3.30 and 3.31
- [ ] Read Section 3.7 — Determination of opportunity process
- [ ] Work through Example 3.32 (discrete time recursion)
- [ ] Write summary notes

**Focus:** Understanding when the problem simplifies (deterministic MVT) and how to compute $L$ in practice.

---

### Reading 7: Černý & Kallsen (R17) — Hedging Formulas

📅 **Time Estimate:** 2 days

- [ ] Read Section 4.1 — Mean value process and pure hedge coefficient
- [ ] Understand Definition 4.2 (mean value process $V$)
- [ ] Understand Definition 4.6 (pure hedge coefficient $\xi$)
- [ ] Understand Proposition 4.7
- [ ] Read Section 4.2 — Main results
- [ ] **Understand Theorem 4.10** (optimal hedge in feedback form)
- [ ] Understand Corollary 4.11 (gains process)
- [ ] **Understand Theorem 4.12** (hedging error formula)
- [ ] Read Section 4.3 — Connections to literature
- [ ] Write summary notes

**The key formula (Theorem 4.10):**
$$\varphi_t = \xi_t - (v_0 + \varphi \bullet S_{t-} - V_{t-})\tilde{a}_t$$

---

### Phase 2 Checkpoint

- [ ] **I can explain:** What is the opportunity process $L$ and what does it represent?
- [ ] **I can explain:** What is the adjustment process $\tilde{a}$?
- [ ] **I can explain:** What is the opportunity-neutral measure $P^\star$ and why is it useful?
- [ ] **I can explain:** How does the feedback hedging formula work?
- [ ] **I can derive:** The hedging error formula from Theorem 4.12

---

## Phase 3: Heston Application

> **Goal:** See how the abstract theory becomes concrete in an affine model.

### Reading 8: Černý & Kallsen Heston Paper (R3) — Setup

📄 **Paper:** *Mean-Variance Hedging and Optimal Investment in Heston's Model with Correlation*
👤 **Authors:** Aleš Černý, Jan Kallsen
📅 **Time Estimate:** 2 days

- [ ] Read Section 1 — Introduction
- [ ] Understand the model equations (1.1) and (1.2)
- [ ] Read Section 1.1 — Computation and verification strategy
- [ ] Read Section 1.2 — Interpretation
- [ ] Read Section 2 — Preliminaries
- [ ] Understand the semimartingale characteristics for Heston (equations 2.2, 2.3)
- [ ] Write summary notes

**The Heston model:**
$$\mathcal{L}(S) = \mu Y^2 \cdot I + Y \cdot W$$
$$Y^2 = Y_0^2 + (\zeta_0 + \zeta_1 Y^2) \cdot I + \sigma Y \cdot (\rho W + \sqrt{1-\rho^2} U)$$

---

### Reading 9: Černý & Kallsen (R3) — Computing $L$ and $\tilde{a}$

📅 **Time Estimate:** 3 days

- [ ] Read Section 3 — The Merton Problem
- [ ] Understand Definition 3.1 (candidate opportunity process)
- [ ] **Work through Proposition 3.1** — derivation of $\kappa_0$, $\kappa_1$
- [ ] Understand the Riccati equation for $\kappa_1$
- [ ] Understand equations (3.7)-(3.11) for the $\tilde{P}$-dynamics
- [ ] Read and understand Lemma 3.1 (properties of candidate $\tilde{Q}$)
- [ ] **Work through Proposition 3.2** — verification of true VOMM
- [ ] Understand Proposition 3.3 — admissibility conditions
- [ ] Read Appendix A — Riccati equation solutions
- [ ] Write summary notes

**Key result — exponential affine form:**
$$L = \exp(\kappa_0(t) + \kappa_1(t) Y_t^2)$$
$$\tilde{a} = (\mu + \rho\sigma\kappa_1)/S$$

---

### Reading 10: Černý & Kallsen (R3) — Hedging and Error

📅 **Time Estimate:** 2 days

- [ ] Read Section 4 — Optimal Hedging
- [ ] Understand Proposition 4.1 (PDE for mean value process)
- [ ] Understand equation (4.1) for pure hedge $\xi$
- [ ] Read Remark 4.1 (Fourier representation)
- [ ] Read Section 5 — Hedging Error
- [ ] Understand the formula for $\varepsilon_0^2$
- [ ] Understand Lemma 5.1 (maximal Sharpe ratio with options)
- [ ] Write summary notes

---

### Phase 3 Checkpoint

- [ ] **I can explain:** Why does Heston admit an exponential-affine opportunity process?
- [ ] **I can derive:** The Riccati equations for $\kappa_0$ and $\kappa_1$
- [ ] **I can explain:** How correlation $\rho$ affects the adjustment process
- [ ] **I can explain:** The verification argument for admissibility
- [ ] **I understand:** What breaks when moving to rough volatility

---

## Phase 4: Rough Volatility

> **Goal:** Understand rough models and existing work on mean-variance hedging there.

### Reading 11: Background — Volatility is Rough

📄 **Paper:** *Volatility is Rough* (external paper)
👤 **Authors:** Gatheral, Jaisson, Rosenbaum
📅 **Time Estimate:** 1 day

- [ ] Read introduction and motivation
- [ ] Understand empirical evidence for roughness
- [ ] Understand the Hurst parameter $H < 1/2$
- [ ] Understand the rough Bergomi and rough Heston models
- [ ] Write summary notes

---

### Reading 12: Affine Volterra Processes (R4) — Part 1

📄 **Paper:** *Affine Volterra Processes*
👤 **Author:** Eduardo Abi Jaber (et al.)
📅 **Time Estimate:** 2 days

- [ ] Read Section 1 — Introduction
- [ ] Read Section 2 — Setup and definitions
- [ ] Understand Volterra processes
- [ ] Understand the affine structure in the Volterra setting
- [ ] Write summary notes

---

### Reading 13: Affine Volterra Processes (R4) — Part 2

📅 **Time Estimate:** 2 days

- [ ] Read Section 3 — Riccati-Volterra equations
- [ ] Understand existence and uniqueness results
- [ ] Compare to classical Riccati equations from R3
- [ ] Understand the characteristic function formula
- [ ] Write summary notes

**Key insight:** Riccati ODEs become fractional Riccati equations:
$$\psi(t) = \int_0^t K(t-s) F(\psi(s)) ds + f(t)$$

---

### Reading 14: Rough Heston Characteristic Function (R6)

📄 **Paper:** *The Characteristic Function of Rough Heston Models*
👤 **Author:** Omar El Euch (et al.)
📅 **Time Estimate:** 2 days

- [ ] Read main results on characteristic function
- [ ] Understand how this relates to R4
- [ ] Understand numerical methods for the fractional Riccati equation
- [ ] Write summary notes

---

### Reading 15: Mean-Variance Hedging in Rough Volatility (R14)

📄 **Paper:** *Mean-Variance Hedging in Rough Volatility Models*
👤 **Author:** Martins (et al.)
📅 **Time Estimate:** 3 days

- [ ] Read entire paper carefully
- [ ] Identify what framework they use
- [ ] Identify what they achieve vs. what remains open
- [ ] Compare their approach to R3
- [ ] Identify potential extensions or gaps
- [ ] Write detailed summary notes

---

### Phase 4 Checkpoint

- [ ] **I can explain:** What makes volatility "rough" (Hurst parameter $H < 1/2$)?
- [ ] **I can explain:** What is an affine Volterra process?
- [ ] **I can explain:** How do Riccati-Volterra equations differ from standard Riccati?
- [ ] **I can identify:** What has been done on MV hedging in rough volatility
- [ ] **I can identify:** What gaps remain for my research

---

## Supplementary Materials

### Optional Readings

- [ ] **R5:** Perfect Hedging in Rough Heston Models (El Euch) — if interested in complete hedging
- [ ] **R13:** Multifactor Approximation of Rough Volatility (Abi Jaber) — for numerical methods
- [ ] **R15:** Deep Quadratic Hedging (Gnoatto) — for ML approaches

### Background References

- [ ] Shreve Vol 2, Chapters 4-5 — if stochastic calculus is rusty
- [ ] Filipović "Term Structure Models" Chapter 10 — for affine processes
- [ ] Heston (1993) original paper — for model background

---

## Notation Reference Sheet

Fill this in as you read to keep track of notation across papers:

| Symbol | R17 | R3 | R18 | Meaning |
|--------|-----|-----|-----|---------|
| $L$ | | | | Opportunity process |
| $\tilde{a}$ | | | | Adjustment process |
| $K$ | | | | Modified MVT process |
| $\hat{K}$ | | | | Mean-variance tradeoff |
| $P^\star$ | | | | Opportunity-neutral measure |
| $Q^\star$ | | | | Variance-optimal measure |
| $\hat{P}$ | | | | Minimal martingale measure |
| $V$ | | | | Mean value process |
| $\xi$ | | | | Pure hedge coefficient |
| $\varphi$ | | | | Optimal hedging strategy |

---

## Progress Tracker

| Phase | Status | Completion Date |
|-------|--------|-----------------|
| Phase 1: Foundations | ⬜ Not Started | |
| Phase 2: General Theory | ⬜ Not Started | |
| Phase 3: Heston Application | ⬜ Not Started | |
| Phase 4: Rough Volatility | ⬜ Not Started | |

**Status Legend:** ⬜ Not Started | 🟨 In Progress | ✅ Complete

---

## Research Ideas Log

Use this section to jot down ideas as you read:

### Questions
1.

### Potential Extensions
1.

### Gaps in Literature
1.

### Technical Challenges
1.

---

*Last updated: <!-- Add date -->*
