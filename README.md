# Implement-NFA-with-epsilon-move-to-DFA-Conversion
"Implementation of Nondeterministic Finite Automaton (NFA) with epsilon transitions converted to Deterministic Finite Automaton (DFA), facilitating efficient pattern recognition and language processing in computational models."

1. Create a graph GD with vertex {q0}. Identify this vertex as the initial
vertex.
2. Repeat the following steps until no more edges are missing.
Take any vertex {qi, qj , ..., qk} of GD that has no outgoing edge for some
a ∈ Σ. Compute δ∗N (qi, a), δ∗N (qj , a), ..., δ∗N (qk, a).
If δ∗N (qi, a) ∪ δ∗N (qj , a) ∪ ... ∪ δ∗N (qk, a) = {ql, qm, ..., qn},
create a vertex for GD labeled {ql, qm, ..., qn} if it does not already exist.
Add to GD an edge from {qi, qj , ..., qk} to {ql, qm, ..., qn} and label it
with a.
4. Every state of GD whose label contains any qf ∈ FN is identified as a
final vertex.
5. If MN accepts λ, the vertex {q0} in GD is also made a final vertex.
