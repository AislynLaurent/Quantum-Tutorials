---
description: >-
  A summary of important parts of a qiskit program, which users may not be
  familiar with already
---

# Parts of a Qiskit Program

## Classical Registers

On a classical system, a register is a storage unit which holds multiple bits. Registers are not used to preform any instructions or math, though instructions may be stored on them. We use classical registers in our quantum program to hold the result when we measure out qubit.

You create a new classical register in qiskit like this:

```text
cr = ClassicalRegister(2)
```

This piece of code creates two classical registers and stores them in the variable `cr`.



