# The Axiomatic Basis for Computer Programming 
> By C.A.R Hoare. Link [here](https://www.cs.cmu.edu/~crary/819-f09/Hoare69.pdf). 

- Axioms: the set of facts we have to work with (true or false)
- Theorems are build from axioms based on _deduction rules_ 
  - Detachment: $$P \to Q \\ P \vdash Q$$
  - Syllogism: $$P \to Q \\ Q \to R \\ P \vdash R$$
  - Contrapositive: $$P \to Q \\ \neg Q \vdash \neg P$$
- These are rules of reasoning; Hoare's contributions were 1) how to reason about programs, and 2) a way to prove characterization (schemas, a way to go from axioms to theorems)
- Hoare Triple (contract about what it means for program to be correct): $$P\{Q\}R$$
  - \\( P\\) is precondition (needs to be satisfied for everything else to be true)
  - \\( Q\\) is program 
  - \\( R\\) is postcondition (what is true if precondition is satisfied and program ran)
    - Assumes program terminates. 
- Has assignment axiom schema (tells you how to make axioms): \\( P_0 \{x := f\}P\\)
  - \\( x\\) is variable identifier
  - \\( f\\) is an expression
  - \\( P_0\\) is obtained from P by substituting f for all occurences of x
- Can chain Hoare Triples together
- Iteration \\(  P \land B\{S\}P \\)
  - Invarient: true no matter state changes
  - Whole body of work on strongest / weakest invarients and preconditions
- Undecidable: can't assign algorithm for figuring out what it means (or no guarentee that algorithm will ever finish)
- OS's are holy grail of verified programming (type safe and memory safe)