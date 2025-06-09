## 📘 **Predicate Logic**

---

### 1. **Basic Understanding of the Topic Name**

* **Predicate**: A statement or function that becomes **true or false** depending on the value of its variable(s). Example: “x is greater than 5” → becomes true/false depending on x.

* **Logic**: The study of reasoning, involves using **rules and principles** to draw conclusions.

* Together, **Predicate Logic** (also called *First-Order Logic*) is an extension of **Propositional Logic** that allows reasoning about **objects** and their **properties**.

* Analogy: In **Propositional Logic**, you can say “It is raining”.
  In **Predicate Logic**, you can say “It is raining in Bangalore” — adding objects (like location).

---

### 2. **Explanation of the Topic**

**Predicate Logic = Predicates + Quantifiers + Logical Connectives**

#### a) Predicates:

* Denote properties or relations of objects.
* Written as: `P(x)` → P is a predicate, x is a variable.
* Example: `Student(x)` → “x is a student”.

#### b) Quantifiers:

* Help express statements about **some** or **all** objects.

1. **Universal Quantifier** `(∀)` — "for all"

   * Example: `∀x Student(x)` → *All x are students*.
2. **Existential Quantifier** `(∃)` — "there exists"

   * Example: `∃x Student(x)` → *There exists an x such that x is a student*.

#### c) Logical Connectives:

* AND ( ∧ ), OR ( ∨ ), NOT ( ¬ ), IMPLIES ( → ), IFF ( ↔ ).

#### d) Nested Quantifiers:

* Quantifiers can be nested:
  `∀x ∃y Loves(x, y)` → *For every x, there exists a y such that x loves y.*

#### e) Syntax and Semantics:

* Syntax: Formal structure of writing formulas.
* Semantics: Meaning — interpretation in terms of a domain of discourse.

---

### 3. **Relevance in Computer Science**

* Forms the foundation of **formal specification**, **automated reasoning**, **knowledge representation**, and **program verification**.
* Core to:

  * **Artificial Intelligence** (logic-based agents).
  * **Databases** (SQL WHERE clauses can be expressed in predicate logic).
  * **Compiler Design** (semantic analysis).
  * **Formal Verification** (proving software/hardware correctness).

---

### 4. **UGC NET CSE Relevance**

* Appears in **Unit 1: Discrete Structures and Optimization**.
* Syllabus mentions: *Predicate Logic, Predicates and Quantifiers, Nested Quantifiers, Rules of Inference*.
* Frequently asked in:

  * **Paper II (Technical)**.
  * **Moderately Expected** — about 1-2 questions in most papers.
* Typical question patterns:

  * Identify correct logical form.
  * Translate sentences into predicate logic.
  * Negate predicate logic statements.

---

### 5. **Applications in CS Projects / Research**

* **AI reasoning systems** → Prolog (logic programming language).
* **Natural Language Processing (NLP)** → translating human language into formal logic.
* **Database Query Optimizers** → use predicate logic to reason about query transformations.
* **Software Engineering** → formal specification using Z, Alloy.
* **Theorem Provers** → tools like Coq, Isabelle use predicate logic to prove correctness of algorithms.

---

### 6. **Possible UGC NET Questions**

#### MCQs

1. What does `∀x ∃y Likes(x, y)` represent? *(Easy)*
2. Which of the following is the negation of `∀x P(x)`? *(Moderate)*

#### Conceptual Short-Answer

3. Explain the difference between **Propositional Logic** and **Predicate Logic**. *(Moderate)*
4. What is meant by **nested quantifiers**? Give an example. *(Moderate)*

#### Application-based

5. Translate the sentence: “Every student loves some subject” into **Predicate Logic**. *(Tough — seen in past NET questions)*

---

Here is a **List of Important Equivalences for Predicate Logic** — these are very helpful for UGC NET and for reasoning clearly:

---

### 1️⃣ **Quantifier Negation (De Morgan for Quantifiers)**

| Original Statement | Equivalent Negation |
| ------------------ | ------------------- |
| ¬(∀x P(x))         | ∃x ¬P(x)            |
| ¬(∃x P(x))         | ∀x ¬P(x)            |

👉 **Tip**: Negation *flips* the quantifier and pushes inside.

---

### 2️⃣ **Distributive Laws with Quantifiers**

#### a) Distributivity of ∀ over ∧:

* ∀x (P(x) ∧ Q(x)) ≡ (∀x P(x)) ∧ (∀x Q(x))

#### b) Distributivity of ∃ over ∨:

* ∃x (P(x) ∨ Q(x)) ≡ (∃x P(x)) ∨ (∃x Q(x))

👉 **Tip**: Universal (∀) distributes over AND; Existential (∃) distributes over OR.

---

### 3️⃣ **Quantifier and Logical Connectives (Restrictions)**

#### a) For ∀ over OR:

* ∀x (P(x) ∨ Q(x)) **NOT** ≡ (∀x P(x)) ∨ (∀x Q(x)) → This equivalence is NOT valid!

#### b) For ∃ over AND:

* ∃x (P(x) ∧ Q(x)) **NOT** ≡ (∃x P(x)) ∧ (∃x Q(x)) → This equivalence is NOT valid!

👉 **Tip**: Be careful — these *don’t* distribute like in the earlier case.

---

### 4️⃣ **Implication Equivalence**

* P → Q ≡ ¬P ∨ Q

In Predicate Logic:

* ∀x (P(x) → Q(x)) ≡ ∀x (¬P(x) ∨ Q(x))
* ∃x (P(x) → Q(x)) ≡ ∃x (¬P(x) ∨ Q(x))

---

### 5️⃣ **Moving Quantifiers (Scope Manipulation)**

If variable **x** is not free in **Q**:

* ∀x P(x) ∧ Q ≡ (∀x P(x)) ∧ Q
* ∃x P(x) ∨ Q ≡ (∃x P(x)) ∨ Q

👉 You can pull quantifiers outside or push them in, if variable independence holds.

---

### 6️⃣ **Double Negation**

* ¬¬P(x) ≡ P(x)
* ¬¬∀x P(x) ≡ ∀x P(x)
* ¬¬∃x P(x) ≡ ∃x P(x)

---

### 7️⃣ **Contrapositive in Predicate Logic**

* ∀x (P(x) → Q(x)) ≡ ∀x (¬Q(x) → ¬P(x))

👉 Contrapositive holds in predicate logic too!

---

### Summary Table for Quick Revision:

| Rule                | Key Idea                          |
| ------------------- | --------------------------------- |
| Quantifier Negation | Flip quantifier and negate inside |
| Distribute ∀ over ∧ | Yes                               |
| Distribute ∃ over ∨ | Yes                               |
| Distribute ∀ over ∨ | No                                |
| Distribute ∃ over ∧ | No                                |
| Implication         | P → Q ≡ ¬P ∨ Q                    |
| Contrapositive      | Holds for ∀ (P → Q ≡ ¬Q → ¬P)     |
| Double Negation     | Always valid                      |

---

