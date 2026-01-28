# System Architecture & CML Integration

**Project:** Living Super-Intelligence Platform (ASI‑Direction)

**Author & Steward:** Harsh Khambra

---

## 1. Purpose of This Document

This document explains:

1. **Where CML (Cognitive Meta Language) fits** in the system
2. **Which architectural layers are written in CML** vs traditional code
3. **How the system runs (end‑to‑end)** in a simple, understandable way

This is a **bridge document** between:
- the *architecture diagram*
- the *CML language spec*
- the *actual runtime system*

---

## 2. Core Principle: Code vs CML

### 🔑 Golden Rule

> **CML defines intent, structure, constraints, and cognition.**  
> **Python / Rust execute mechanics.**

CML never replaces the kernel.
CML **configures and governs intelligence**, not execution.

---

## 3. What Is Implemented in CML (and Why)

### ✅ Implemented in CML

CML is used for **everything that describes intelligence behavior**:

| Layer | CML File | Why |
|------|---------|-----|
| Cognition | `cognition.cml` | reasoning, representations, thinking rules |
| Memory | `memory.cml` | memory types, retention rules |
| Learning | `learning.cml` | feedback & update logic |
| Force‑Fields | `constraints.cml` | safety must be declarative |
| Discovery | `discovery.cml` | math / algorithm exploration |
| Simulations | `simulations.cml` | universe rules |
| Plugin Wiring | `plugins.cml` | what is enabled |
| Intent | `run.cml` | what the system tries to do |

CML answers **“WHAT & WHY”**.

---

### ❌ NOT Implemented in CML

These layers are **always real code**:

| Layer | Language | Reason |
|-----|---------|-------|
| Kernel | Python / Rust | must be stable & trusted |
| Event Bus | Python / Rust | performance + safety |
| Plugin Manager | Python | lifecycle control |
| Force‑Field Execution | Python | enforcement |
| Sandbox | Rust / Python | isolation |

Code answers **“HOW”**.

---

## 4. Architecture → CML Mapping

### 4.1 Kernel Layer

```
KERNEL (code only)
├── kernel.py
├── loop.py
├── state.py
└── interfaces.py
```

🚫 No CML here.
This layer **reads** CML but is never modified by it.

---

### 4.2 Force‑Fields Layer

```
force_fields/
└── constraints.cml
```

Example:
```cml
constraint Safety.NoPowerSeeking {
    forbid: Action.PowerAccumulation
    severity: CRITICAL
}
```

✔ Declarative safety
✔ Human‑auditable
✔ Impossible to silently bypass

---

### 4.3 Cognition Layer

```
plugins/cognition/
└── cognition.cml
```

Defines:
- reasoning modes
- representations
- uncertainty handling
- curiosity bounds

CML defines **how thinking is structured**, not how it executes.

---

### 4.4 Memory Layer

```
plugins/memory/
└── memory.cml
```

Defines:
- working vs episodic memory
- consolidation rules
- forgetting limits

---

### 4.5 Learning Layer

```
plugins/learning/
└── learning.cml
```

Defines:
- feedback rules
- learning rate caps
- meta‑learning (sandboxed)

---

### 4.6 Discovery Layer

```
plugins/discovery/
└── discovery.cml
```

Defines:
- math exploration
- novelty criteria
- hypothesis scoring

---

### 4.7 Simulation Layer

```
simulations/
└── simulations.cml
```

Defines:
- world laws
- observables
- constraints of universes

---

## 5. How the System RUNS (Simple Flow)

### Step‑by‑Step Runtime

```
1. kernel.py starts
2. load run.cml
3. parse all *.cml files
4. build Intermediate Representation (IR)
5. validate constraints
6. load plugins
7. apply force‑fields
8. start observe → think → act loop
```

---

### Visual Flow

```
CML Files
   ↓
CML Parser
   ↓
Intermediate Representation (IR)
   ↓
Kernel + Plugin System
   ↓
Simulated Worlds
```

---

## 6. Example Minimal Project

```
project/
├── cognition.cml
├── memory.cml
├── learning.cml
├── constraints.cml
├── simulations.cml
├── plugins.cml
└── run.cml
```

Run command:
```bash
python kernel.py --run project/run.cml
```

---

## 7. Why This Design Is Future‑Proof

- CML can evolve without breaking kernel
- New plugins can be added weekly
- Safety rules remain visible
- Intelligence is inspectable
- Growth is controlled

---

## 8. Final Mental Model

> **Kernel = Body**  
> **CML = Mind Blueprint**  
> **Plugins = Organs**  
> **Force‑Fields = Immune System**

---

## 9. Final Note

CML is intentionally limited.

It cannot:
- execute raw code
- bypass safety
- create autonomy

That limitation is **the feature**, not a weakness.

---

**© Harsh Khambra — All Rights Reserved**

