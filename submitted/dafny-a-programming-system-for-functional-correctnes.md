# Professor Rustan Leino, Dafny: a Programming System for Functional Correctness

Professor Rustan Leino presented on the programming language Dafny and how it can be used to prove properties about sensitive portions of code for which it is important to establish proven invariants.

He began by discussing the state of program verification. In particular he talked about the time intensive and expensive nature of verifying code. Additionally he described his work as being focused on the development stage of the software life cycle. In general assisting the developer in capturing more of the design and specification semantics in the code is best done by automatic tooling but often requires help from the developer. His solution for heavier weight verification with is to focus on important and relatively static portions of code and libraries.

He also described the continuum of verification techniques from extended static checkers to hand written proofs. On the side of static checkers are simple properties and large over approximations with minimal effort from the developer. Obviously on the other end with hand written proofs much more effort is required but the properties of code can be shown very exactly.

Dafny is an attempt to leverage the power of SMT constraint solvers to allow programmers to specify properties of their code for themselves and let the compiler verify that the code satisfies those properties. During the demo he showed how inductive proofs on data structures can be shown in the property specification portion of the language. He also demonstrated the difficulty of showing complex inductive properties even for a basic tree traversal algorithms which suggested that being able to prove only some of the properties was of great value.

He concluded by siting other possible uses for Dafny such as standing in as an intermediate verification language for higher level abstract languages and also for pedagogical purposes.
