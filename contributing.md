# Contributing to Cognitive Meta-Engine (CME)

**Author & Steward:** Harsh Khambra  
**Audience:** Contributors, researchers, engineers  
**Status:** Mandatory reading before any contribution

---

## 1. Contribution Philosophy

CME is a **research-grade cognitive platform**, not a product repository.

Contributions are evaluated on:
- safety
- clarity
- modularity
- auditability

> **Power is easy to add. Discipline is not.**

This document exists to protect the system, the research intent, and contributors.

---

## 2. What You Are Allowed to Contribute

You are welcome to contribute:

### ✅ Allowed
- New **plugins** (cognition, memory, learning, discovery)
- **CML files** (rules, constraints, simulations)
- **Observers & metrics**
- **Documentation**
- **Examples & tests**

All contributions must be:
- modular
- reversible
- documented

---

## 3. What You Are NOT Allowed to Contribute

### ❌ Prohibited
- Modifications to **kernel invariants**
- Removal or bypassing of **force-fields**
- Hard-coded power into the kernel
- Autonomous real-world execution
- Claims of AGI, ASI, sentience, or consciousness
- Obfuscated or non-auditable logic

PRs violating these rules will be rejected without exception.

---

## 4. Contribution Boundaries (Very Important)

### Kernel Layer

- Treated as **read-only**
- Changes require explicit maintainer approval

### Plugins

- Must follow interface contracts
- Must declare resources and limits
- Must be sandbox-safe

### CML

- Must be declarative
- Must not encode execution logic
- Must respect constraint precedence

---

## 5. How to Contribute (Step-by-Step)

1. **Fork** the repository
2. Create a **feature branch**
3. Add your change (plugin / CML / docs)
4. Add at least one:
   - test
   - simulation
   - example
5. Document assumptions
6. Submit a **Pull Request**

---

## 6. Pull Request Requirements

Every PR must include:

- Clear description of *what* and *why*
- Scope of change (which layers affected)
- Safety considerations
- Rollback plan

PRs without explanation will not be reviewed.

---

## 7. Review Process

- PRs are reviewed by the maintainer
- High-risk changes require additional discussion
- Maintainer decision is final

This is not a voting-based project.

---

## 8. Versioning Rules

- One major capability per PR
- No sweeping refactors
- Experimental features must be flagged

Small, controlled changes are preferred.

---

## 9. Communication Guidelines

- Be precise
- Be technical
- Avoid hype or speculative claims
- Assume good intent

This project values **signal over noise**.

---

## 10. Enforcement

Contributions that:
- remove safety
- increase opacity
- misrepresent scope

may result in PR closure or contributor removal.

---

## 11. Final Note

> **If you cannot explain the impact of your contribution,
> you should not submit it.**

CME grows through careful, deliberate work.

---

**© Harsh Khambra — All Rights Reserved**
