# Getting Started — Cognitive Meta-Engine (CME)

**Author & Steward:** Harsh Khambra  
**Audience:** New contributors, researchers, developers  
**Goal:** Run the system locally and understand the mental model in under 30 minutes

---

## 1. What You Are About to Run

You are **not** running an AI model.
You are running a **cognitive research platform**.

This system:
- does not claim AGI or ASI
- does not act autonomously in the real world
- runs only in controlled simulations
- is designed to be inspected, paused, and stopped

> If you are looking for a chatbot or quick demo, this project is not for you.

---

## 2. Prerequisites

Make sure you have the following installed:

- **Python 3.10 or higher**
- **Git**
- A Unix-like shell (Linux / macOS / WSL on Windows)

Check versions:

```bash
python3 --version
git --version
```

---

## 3. Clone the Repository

```bash
git clone https://github.com/harshkhambrajr/sgi_v0_master
cd sgi_v0_master
```

---

## 4. Repository Mental Model (Important)

Before running anything, understand this:

```
.md   → documentation (what & why)
.cml  → cognition rules (thinking & constraints)
.py   → execution (how it runs)
.sh   → helper scripts (how to operate)
```

> **Never confuse CML with executable code.**

---

## 5. Environment Setup

Create a virtual environment and install dependencies:

```bash
bash scripts/setup.sh
```

What this does:
- creates a virtual environment
- installs Python dependencies
- keeps your system clean

---

## 6. Run the Minimal Example

A minimal example is provided under:

```
examples/hello_world/
```

Run it using:

```bash
bash scripts/run.sh
```

Expected behavior:
- kernel starts
- CML files are parsed
- constraints are validated
- cognition loop begins

There is **no UI**, **no chatbot**, and **no automation**.
This is intentional.

---

## 7. What Just Happened (Step-by-Step)

```
1. kernel.py starts
2. run.cml is loaded
3. all referenced .cml files are parsed
4. CML → Intermediate Representation (IR)
5. force-fields are validated
6. plugins are loaded
7. observe → think → act loop starts
```

Everything is logged and traceable.

---

## 8. Your First Safe Experiment

Open:

```
examples/hello_world/cognition.cml
```

Try:
- changing a purpose string
- adjusting an intent priority
- adding a harmless constraint

Then rerun:

```bash
bash scripts/run.sh
```

You are **editing the mind blueprint**, not code execution.

---

## 9. Common Mistakes (Read This)

❌ Trying to add logic in CML  
❌ Removing force-fields  
❌ Expecting intelligence or answers  
❌ Running without understanding constraints  

This system is **about structure**, not output.

---

## 10. Where to Go Next

After this file, read in order:

1. `ARCHITECTURE.md` — how the system is built
2. `CML_SPEC.md` — how the language works
3. `CONTRIBUTING.md` — how to safely add things

---

## 11. Getting Help

- Use GitHub Issues for questions
- Read existing discussions before asking
- Be precise and technical

---

## 12. Final Reminder

> **If you cannot explain what you changed,
> you should not change it.**

This project values clarity over speed.

---

**© Harsh Khambra — All Rights Reserved**

