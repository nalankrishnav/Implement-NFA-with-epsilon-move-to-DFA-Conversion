# 🔁 Epsilon-NFA to DFA Conversion using Python and Graphviz

This project implements the conversion of a **Nondeterministic Finite Automaton (NFA)** with **epsilon (ε) transitions** into an equivalent **Deterministic Finite Automaton (DFA)** using Python. It visualizes both the E-NFA and resulting DFA using the `graphviz` library for clear graphical representation.

---

## 🎯 Objective

To automate the **subset construction algorithm** for ε-NFA to DFA conversion, which is crucial in compiler design and lexical analysis for transforming ambiguous state machines into deterministic ones.

---

## 🧠 Concept Overview

1. **Epsilon Closure Calculation**:
   - For each state, compute the set of states reachable via epsilon (ε) transitions.

2. **Subset Construction**:
   - Begin with the ε-closure of the start state.
   - For each DFA state and input symbol, compute the union of ε-closures of transitions from all included NFA states.

3. **Final States**:
   - Any DFA state containing at least one NFA final state is marked as a DFA final state.

4. **Dead State (ϕ)**:
   - Transitions that result in no reachable state are routed to a universal dead state ϕ.

---

## ⚙️ How It Works

- Takes input from the user: states, alphabets, transitions (including epsilon 'e'), and final states.
- Constructs an internal transition table using dictionaries.
- Uses BFS-like logic to explore all reachable combinations (subsets of NFA states) and form DFA states.
- Renders both the E-NFA and DFA using **Graphviz** as `.pdf` or `.png` files.

---

## 📦 Requirements

- Python 3.x
- [graphviz](https://graphviz.org/download/)
- Python `graphviz` module
  ```bash
  pip install graphviz
