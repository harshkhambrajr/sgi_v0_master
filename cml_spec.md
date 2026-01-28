# Cognitive Meta Language (CML)

**Author & Steward:** Harsh Khambra  
**Status:** Experimental / Research (v0.1)  
**License:** MIT (see LICENSE)  

---

## 1. What is CML?

**Cognitive Meta Language (CML)** is a **declarative meta-language** used to describe *how an intelligence system is structured, constrained, and allowed to learn*.

CML does **not** execute logic.
CML **describes cognition**.

> Think of CML as a **blueprint of the mind**, not the muscles.

---

## 2. Why CML Exists

Traditional languages answer:
> *How do I compute this?*

CML answers:
> *What is the system allowed to think, learn, and attempt — and under what constraints?*

CML exists to make:
- cognition explicit
- safety visible
- uncertainty first-class
- intelligence auditable

---

## 3. What CML IS / IS NOT

### CML IS
- A meta-language for cognition
- A specification language for intelligent behavior
- A coordination layer for plugins and simulations
- Human-readable and reviewable

### CML IS NOT
- A general-purpose programming language
- A replacement for Python / Rust / C++
- A self-aware or autonomous system
- A runtime execution engine

---

## 4. Design Principles

1. **Declarative over Imperative**  
   Describe *what*, not *how*.

2. **Constraint-First**  
   Safety rules exist before actions.

3. **Uncertainty Native**  
   Confidence must be explicit.

4. **Composable Intelligence**  
   Cognition is modular.

5. **Human-Auditable**  
   Every rule should be readable by humans.

---

## 5. CML Project Structure

```
project/
├── cognition.cml        # reasoning & representation rules
├── memory.cml           # memory policies
├── learning.cml         # learning constraints
├── discovery.cml        # exploration & novelty
├── constraints.cml      # force-fields
├── simulations.cml      # sandboxed worlds
├── plugins.cml          # enabled plugins
└── run.cml              # execution intent
```

---

## 6. Core Language Constructs

### 6.1 module

Defines a logical capability.

```cml
module Cognition.BasicReasoning {
    purpose: "Deductive and probabilistic reasoning"
}
```

---

### 6.2 state

Defines internal state with uncertainty.

```cml
state Belief {
    value: Symbol
    confidence: Float in [0,1]
}
```

---

### 6.3 constraint (Force-Field)

Defines a rule that cannot be bypassed.

```cml
constraint Safety.NoPowerSeeking {
    forbid: Action.PowerAccumulation
    severity: CRITICAL
}
```

---

### 6.4 intent

Defines what the system is allowed to attempt.

```cml
intent DiscoverMath {
    domain: AbstractStructures
    priority: MEDIUM
}
```

---

### 6.5 uncertainty

Explicit representation of doubt.

```cml
uncertainty {
    hypotheses:
        H1: "Structure is consistent"
        H2: "Structure collapses"
    confidence:
        H1: 0.61
        H2: 0.39
}
```

---

### 6.6 learning_rule

Defines bounded learning behavior.

```cml
learning_rule UpdateBelief {
    when: Feedback.Received
    adjust: Belief.confidence by gradient
    limit: 0.1 per cycle
}
```

---

### 6.7 simulation

Defines a sandboxed universe.

```cml
simulation ToyUniverse {
    laws:
        - Conservation
        - Locality
    observables:
        - Symmetry
        - Entropy
}
```

---

### 6.8 plugin

Declares plugin usage and limits.

```cml
plugin MathExplorer {
    interface: Discovery
    sandbox: true
    resources:
        cpu: LOW
}
```

---

### 6.9 run

Entry point describing execution intent.

```cml
run {
    load constraints.cml
    load cognition.cml
    load simulations.cml
    start loop
}
```

---

## 7. Type System (Minimal)

- Symbol
- Quantity
- Relation
- Structure
- Probability
- Constraint
- Intent

No raw memory access.
No unchecked mutation.

---

## 8. Compilation Model

```
CML Source
   ↓
CML Parser
   ↓
Intermediate Representation (IR)
   ↓
Kernel + Plugin System
```

CML never runs directly on hardware.

---

## 9. Safety Guarantees (By Design)

- Constraints are evaluated before actions
- Uncertainty cannot be silently removed
- No hidden side effects
- All decisions are traceable

---

## 10. Versioning & Evolution

- v0.x → experimental
- Grammar may evolve
- Backward compatibility is attempted but not guaranteed

---

## 11. Roadmap

### v0.1
- Core grammar
- Parser skeleton
- IR generation

### v0.2
- Constraint solver
- Static validation

### v1.0
- Stable grammar
- Formal verification hooks

---

## 12. Final Note

> **CML is intentionally limited.**
> Those limits are what make the system safe, inspectable, and stoppable.

Designed to evolve slowly.
Designed to be audited.
Designed to be stopped.

---

**© Harsh Khambra — All Rights Reserved**

