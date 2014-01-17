# Dafny: a Programming System for Functional Correctness


state of programming verification

- Costly (building/maintaining)
- expense is making sure the software fits reqs
- cycle: design - dev - test - ship - support
- focused on dev

- helping the dev
- capture more of the design in text
- redundancy
- description
 - ux
 - perf
 - information flow
 - functional behavior <- focus
 - can be enforced by docs
  - doesn't really work

- tools are where it's at
- verification is an ideal
- we can focus on certain portions of the application for verification

- focus on accessible program verification

- hand proof
 - very hard
 - very effective
 - only works for small programs
- interactive proof assistants
 - mechanically ensure the proof is valid
 - tools require expertise
- extended static checking
 - basic properties like array bounds
 - easy automate
 - SMT solvers
- Dafny
 - move the SMT to the functional correctness level

- Dafny PL
 - designed from the beginning with verification in mind
 - small areas that highlight this approach
 - verifier designed WITH the language

- Lang Demo
 - dafny in browser
 - datatype tree
 - generics
 - methods and function distinction
 - functions are pure
 - methods are everything else
 - attempts to prove termination of functions
  - eg, recursing on same node in a tree
 - methods have sets? of return param
 - postcondition with `ensures`?
 - ensures are formulae
  - eg, array index bounds
 - precondition `requires`
  - eg, not null
 - effects (?) with `modifies`
 - specification used to augment reasoning

- Proof Demo
 - mirrored tree
 - lemmas
  - postconditions are the proved thing
  - recursion is IH
  - induction supported automatically

- Verification arch
 - pl
 - IR lang "Boogie"
 - decision using Z3

- Boogie is used for many verifiers
 - many front ends
 - many back ends
 - shared infra for front ends

- At MS
 - VCC verify hyper visor
 - Corral/Poirot/HAVOC, static driver verific
 - SymDiff, semantic diff
  - Boogie IR can be used to verify semantics in different langs
 - Dafny, ironclad, cloudmake
 -

- Teaching
 - reasoning about programs/discrete math
