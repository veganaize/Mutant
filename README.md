# Mutant
SQL mutation testing majigger

* [Mutation Testing Advances: An Analysis and Survey](https://mutationtesting.uni.lu/survey.pdf)
* [Wikipedia: Mutation Testing](https://en.wikipedia.org/wiki/Mutation_testing):
    - Goals of mutation testing:
      - Identify weakly tested pieces of code (for which mutants aren't killed).
      - Identify weak tests (that never kill mutants).
      - Compute the mutation score (number of mutants killed / total number of mutants).
      - Learn about error propagation and state infection in the program.
    - Conditions for killing mutant:
      1. Test must reach mutated statement.
      2. Test input data should infect program state, causing different program states for the mutant and the original program.
      3. Incorrect program state must propagate to program's output and be checked by the test. ("Strong" mutation testing requires this.)
    - Mutation operators for imperative languages:
      - Statement deletion.
      - Statement duplication or insertion, e.g. `goto fail;`
      - Replacement of boolean subexpressions with _true_ and _false_.
      - Replacement of some arithmetic operations with others, e.g. `+` with `*`, `-` with `/`.
      - Replacement of some boolean relations with others, e.g. `>` with `>=`, `==` and `<=`.
      - Replacement of variables with others from the same scope (variable types must be compatible).
      - Remove method body.
